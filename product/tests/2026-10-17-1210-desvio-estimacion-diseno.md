---
opportunity: desvio-estimacion-diseno
solutions: product/solutions/2026-10-06-1359-desvio-estimacion-diseno.md
status: designed
---

# Tests de solución para: Desvío de estimación de diseño en las células

## Por qué testear
Se testea A4 `problema-listo-para-diseno`, la alternativa elegida. El dolor que ataca, los cambios de requisitos con el diseño ya iniciado, tiene evidencia preliminar (`secondary` y `synthetic`). Que un criterio de entrada lo alivie no tiene evidencia: nadie ha reaccionado al criterio y ninguna PO real lo ha visto. Hay dos preguntas que pueden descartar A4 antes de construir nada: si el criterio habría detectado esos cambios (T1) y si las PO lo adoptarían (T2).

## T1. problema-listo-para-diseno: revisión retrospectiva de 10 iniciativas
- **Test status:** ready
- **Belief under test:** "[feature: problema-listo-para-diseno] [value] De las últimas 10 iniciativas con desvío de diseño, al menos el 60% de los cambios de requisitos ocurridos con el diseño iniciado se habría detectado con un criterio de entrada (reglas de negocio, legal o compliance, alcance validados)."
- **Risk:** [value]. Está registrada así, pero la señal es una tasa de detección y no una conducta: el test pregunta si el criterio habría detectado los cambios.
- **Test type:** technical-test (retrospectivo, con clave de respuesta: la clave son los cambios que de verdad ocurrieron)
- **What we do:**
  1. Antes de mirar cualquier iniciativa, se dejan por escrito tres definiciones:
     - **Ítems del criterio:** reglas de negocio validadas; requisitos de legal o compliance validados; alcance validado; diseño participó en la definición del problema.
     - **Cambio de requisitos con el diseño iniciado:** un cambio en reglas, requisitos o alcance, pedido después de que empezó el diseño, que obligó a rehacer trabajo de diseño.
     - **Detectable:** lo que cambió corresponde a un ítem del criterio, y ese ítem no estaba validado (con registro) cuando empezó el diseño. Los cambios que nacen de pruebas con usuarios, o de información que no existía al inicio, cuentan como no detectables.
  2. Se eligen las últimas 10 iniciativas cerradas con desvío de diseño: aquellas en que diseño tomó un 30% más que lo planificado o más, según Jira, o según el diseñador y la PO si Jira no lo registra. Se recorren hacia atrás en el tiempo sin saltarse ninguna, y la lista se cierra antes de revisar los cambios.
  3. Para cada iniciativa se reúnen los documentos (Jira, Confluence, actas, correos con legal o negocio) y se hace una entrevista de 20 minutos con el diseñador y la PO para listar y fechar cada cambio.
  4. Dos personas clasifican cada cambio por separado como detectable o no detectable, mirando solo cómo estaban los documentos cuando empezó el diseño. Después comparan, resuelven los desacuerdos conversando y registran el acuerdo inicial.
- **With whom:** el diseñador y la PO de cada una de las 10 iniciativas (hasta 20 entrevistas cortas). Clasifican Pancho y una segunda persona que no haya trabajado en esas iniciativas, por ejemplo un diseñador o TL de otra célula.
- **Material needed:**
  - (1) Hoja de definiciones, con los ítems del criterio y las reglas de clasificación del paso 1.
  - (2) Guía de entrevista de 20 minutos para listar y fechar los cambios: qué cambió, cuándo, quién lo pidió y cuánto se rehízo. No menciona el criterio, para no inducir respuestas.
  - (3) Planilla de captura con una fila por cambio: iniciativa, fecha del cambio, fecha de inicio del diseño, ítem del criterio, si estaba validado al inicio (con fuente), la clasificación de cada persona y la clasificación final.
  - Queda fuera a propósito: cualquier plantilla o herramienta del criterio, y la medición de esfuerzo o de días perdidos.
- **Material:** [product/tests/materials/t1-problema-listo-para-diseno/](materials/t1-problema-listo-para-diseno/) — hoja de definiciones, guía de entrevista, planilla de captura (`.xlsx`) y mensajes de invitación
- **Duration:** 2 semanas
- **Signal and threshold:** porcentaje de cambios detectables sobre el total de cambios de las 10 iniciativas. Umbral: 60% o más. El resultado vale solo si hay al menos 6 iniciativas con cambios documentados, al menos 10 cambios en total y un acuerdo inicial entre clasificadores de 70% o más. Si no, es `inconclusive`.
- **Decision rule:**
  - `continue` si se detecta el 60% o más.
  - `change` entre 40 y 59%: A4 sigue con un criterio limitado a los ítems que sí detectaron cambios, y A3 vuelve para los cambios que no se podían prever. Esa versión combinada necesita su propio test.
  - `discard` bajo 40%: pasa A3, como indica el archivo de soluciones, y T2 no se corre.
- **Expected provenance:** real
- **Next step if it passes:** T2

## T2. problema-listo-para-diseno: conversación con 3 PO con compromiso
- **Test status:** designed
- **Belief under test:** "[feature: problema-listo-para-diseno] [feasibility] En un piloto de un trimestre en 2 células, la PO y las áreas solicitantes aceptan no comprometer una estimación de diseño hasta pasar el criterio en al menos 4 de 5 iniciativas, sin alargar el plazo total de la iniciativa en más de una semana."
- **Risk:** [feasibility]
- **Test type:** buyer-conversation
- **What we do:**
  1. Pancho le muestra a cada PO una página con el criterio.
  2. En una conversación de 30 minutos se explica qué cambia para ella: mientras la iniciativa no pase el criterio, diseño explora pero no compromete estimación.
  3. Al final se pide un compromiso concreto, distinto según la célula:
     - **PO-A**, de la célula comprometida: aplicar el criterio a la próxima iniciativa de su célula que entre a diseño, nombrándola y fijando la fecha en que se revisa el criterio.
     - **PO-B y PO-C**, de otras células: agendar, con fecha, una revisión de 30 minutos en la que traen su próxima iniciativa para revisarla contra el criterio.
  4. Cualquier condición o excepción que ponga se anota textual.
  - Este paso prueba solo la parte de la creencia que toca a la PO. Las áreas solicitantes y el límite de "no más de una semana" se prueban en el paso siguiente.
- **With whom:** 3 PO reales: la PO de la célula comprometida y 2 PO de otras células. Pancho invita a las otras dos solo para la conversación; sus células no entran al piloto.
- **Material needed:**
  - (1) Una página con el criterio: qué pide, quién valida cada ítem, qué pasa mientras no se cumple y qué no hace (no congela el problema, no gestiona los cambios posteriores). Si T1 pasó, su resultado va en una sola línea, igual para las tres.
  - (2) Guion de 30 minutos, igual para las tres hasta el pedido de compromiso. El pedido tiene dos versiones: la de PO-A y la de PO-B y PO-C.
  - (3) Planilla de captura por PO: célula, tipo de compromiso pedido, si se comprometió, la iniciativa nombrada o la revisión agendada con su fecha, las condiciones textuales y si alguna condición vacía el criterio. Una condición lo vacía si excluye los pedidos de stakeholders o de legal, o si deja la decisión a la PO caso a caso.
  - Queda fuera a propósito: cualquier herramienta, la plantilla en Jira y los argumentos de venta.
- **Material:** pendiente (`/build-solution-test`)
- **Duration:** 1 semana
- **Signal and threshold:** número de PO que se comprometen, sin condiciones que vacíen el criterio. Para PO-A cuenta la iniciativa nombrada con fecha; para PO-B y PO-C, la revisión agendada con fecha. Umbral: 2 de 3 o más, y PO-A tiene que estar entre ellas.
- **Decision rule:**
  - `continue` si se comprometen 2 de 3 o más, incluida PO-A.
  - `change` en cualquiera de estos tres casos:
    - (a) PO-A se compromete solo si se modifica el criterio. La versión modificada se testea de nuevo.
    - (b) Se compromete PO-A y ninguna otra. El concierge sigue en su célula, pero el resultado no se generaliza a otras células.
    - (c) PO-A no se compromete, pero PO-B y PO-C sí. Se busca el piloto en una de esas dos células, pidiéndole el compromiso completo.
  - `discard` si no se compromete ninguna, o solo una entre PO-B y PO-C. A4 queda sin dueña y se vuelve a la comparación (A3 o A2).
- **Expected provenance:** real. Si se ensaya antes con colegas en el rol de PO, ese ensayo es `synthetic` y no cuenta.
- **Next step if it passes:** un concierge en la célula comprometida. El criterio se aplica a mano, junto con las áreas solicitantes, a la iniciativa que nombró PO-A, y se mide si la estimación espera al criterio y si el plazo total se alarga más de una semana. Después viene el piloto de un trimestre. Antes de diseñarlo, la creencia 9 (hoy dice "2 células") se re-registra para 1 célula, con tu aprobación. Ese piloto es también donde se mide la creencia 10.

## Results

## Decision
