---
opportunity: desvio-estimacion-diseno
survey: product/surveys/2026-09-28-2125-desvio-estimacion-diseno.md
mode: exploration
status: draft
date: 2026-09-28
language: es
---

# Guía de entrevista: cómo se fija y se sigue la estimación de diseño en la célula

- **Objetivos de aprendizaje:**
  1. **Cómo se fija el tiempo de diseño en el planning** (creencia 5, causa «proceso»). ¿Quién pone el número de diseño, cuándo y qué le pasa entre que se dice y que queda en el plan? → *Decide si las ideas apuntan a integrar la estimación de diseño en el planning.* La encuesta (Q5–Q7) dice cuándo y cuánto se recorta; esta guía busca **cómo** pasa.
  2. **Cómo estiman hoy los diseñadores** (creencia 6, causa «capacidad»). ¿Con qué arman su número, contra qué lo comparan y qué se les queda fuera? → *Decide si hace falta método o referencias históricas, o si el método no es la palanca.* Complementa Q9 de la encuesta.
  3. **Dónde siguen PO y TL el avance de diseño** (viabilidad de medir). ¿Por dónde se enteran PO y TL de cómo va diseño y de que su plazo cambió? → *Decide entre una capa sobre Jira y una app aparte, y si Andrea (PO) sigue como persona secundaria o pasa a terciaria.* Complementa Q12 de la encuesta.
- **Participantes:** toda la célula —diseñador/a (Camila Rojas, Matías Contreras), Product Owner (Andrea Muñoz) y Tech Lead (Felipe Soto)— de células de producto de Continuum que trabajaron en una iniciativa del roadmap con diseño que pasó a desarrollo en los últimos 3 meses. Queda fuera Patricia Vergara (áreas que piden piezas sueltas).
- **Modo:** exploración. No se muestra ninguna idea ni prototipo.
- **Duración:** 30 minutos (lo que promete el opt-in R2 de la encuesta). Introducción + tronco común + un bloque según el rol.
- **Fuera de alcance a propósito:** la magnitud del desvío y cómo lo absorbe la célula (creencias 1 y 2) las miden Jira y la encuesta; la entrevista no las reemplaza. La tercera causa (requisitos que cambian) no es objetivo de esta guía: si aparece sola, un probe y se anota (ver nota del bloque B).

## Notas para quien entrevista

- **Un solo caso, de principio a fin.** Toda la entrevista gira en torno a la iniciativa del bloque A. Las opiniones generales («siempre pasa que…») se devuelven al caso: «¿y en esta iniciativa?».
- **No uses las palabras de la hipótesis** antes de que las diga la persona: «recorte», «ancla», «te lo bajaron», «falta de método». Si la persona las dice, úsalas de vuelta. Tampoco digas en la introducción que la entrevista es sobre diseño o sobre estimaciones: un TL lo lee como diseño buscando más tiempo.
- **La encuesta ya sembró un marco.** Quien responde la encuesta ordenó causas en Q10. No menciones sus respuestas hasta el cierre; primero el caso, después (si hace falta) «en la encuesta marcaste X, ¿cómo se ve eso en esta iniciativa?».
- **Relación de poder.** Si quien entrevista es el Design Lead y el/la diseñador/a le reporta, la persona puede exagerar el problema o cuidarse al hablar de su propia estimación. Si es posible, que entreviste otra persona; si no, nómbralo en la introducción. La promesa de confidencialidad va **al inicio**, antes de cualquier pregunta sobre su propio trabajo.
- **Mismo caso, varios lados.** Cuando entrevistes a más de un rol de la misma célula, usa la variante A1b con el nombre de la iniciativa que dio el primero. Las diferencias entre versiones son el hallazgo. No le cuentes a nadie lo que dijo otro rol.
- **Relatos que se van a los stakeholders.** Si el relato de A1 se queda en la negociación con el área solicitante (típico en PO), redirige: «¿y cuándo entró diseño en eso?». Si aparece que diseño no participa en definir el problema (creencia 3), anótalo como señal y sigue; no se profundiza.
- **El desvío no siempre es atraso.** Puede aparecer como un handoff que llega a tiempo pero incompleto y se termina durante el sprint. Anótalo como desvío igual.
- **Jira como fuente de medición.** Si alguien dice que el esfuerzo real de diseño no quedó en Jira (tarea cerrada en el handoff, trabajo fuera de horario, dudas resueltas por Slack), anótalo como señal sobre la fuente que mide la creencia 1. No se pregunta más allá de eso.

## Introducción (1 min) — todos los roles

I1. *(leer)* Estamos conversando con personas de distintas células para entender cómo se planifica el trabajo, desde que llega una iniciativa hasta que sale. No hay respuestas correctas y no evaluamos a nadie: lo que me cuentes se reporta agregado. Puede que converse con otras personas de tu célula sobre la misma iniciativa; lo que tú me digas no se les comenta.
   > Si quien entrevista es el Design Lead y la persona le reporta, dilo aquí.

## Calentamiento (3 min) — todos los roles

W1. Cuéntame qué hace tu célula y cuál es tu parte en ella.
   - Probe: ¿Cuánto tiempo llevas en esta célula?
   > Confirma el perfil (rol, ≥3 meses en la célula) y relaja. Sin objetivo propio.

## Cuerpo

### A. La iniciativa (7 min) — todos los roles

A1. Piensa en la iniciativa más reciente con trabajo de diseño que ya pasó a desarrollo. Cuéntame cómo fue, desde que llegó a la célula hasta que salió a producción —o hasta hoy, si todavía no sale.

A1b. *(segundo y tercer rol de la misma célula)* Quiero conversar de [nombre que dio el primero]. Cuéntame cómo fue para ti, desde que llegó a la célula hasta que salió a producción —o hasta hoy, si todavía no sale.
   - ¿Qué pasó después?
   - ¿En qué momento entró diseño?
   - ¿Qué tomó más o menos de lo que se esperaba? ¿Cómo se notó?
   > Objetivos 1, 2 y 3: fija el caso sobre el que se construye todo lo demás. Pide la **más reciente**, no la peor: la peor sobrerrepresenta el desvío. «Hasta que salió a producción» es a propósito: para diseño, «entregar» es el handoff, y el trabajo posterior (dudas de desarrollo, estados que faltaban) quedaría fuera del relato.

### B. Cómo se decidió el tiempo de diseño (8 min) — todos los roles

B1. Volvamos al momento en que se planificó esa iniciativa. ¿Cómo se decidió cuánto tiempo tendría diseño?
   - ¿Hubo un número para diseño? ¿Quién lo dijo primero?
   - Cuando se dijo ese número, ¿ya estaba decidido cuándo empezaba desarrollo?
   - ¿Qué pasó con ese número entre que se dijo y que quedó en el plan?
   - *(si aparece una fecha comprometida)* ¿De dónde salió esa fecha?
   - ¿Esta iniciativa fue como las demás o fue distinta? ¿En qué?
     - *(si «igual»)* ¿Te acuerdas de alguna que no haya sido así? ¿Qué pasó distinto?
   > **Objetivo 1 · creencia 5.** Creemos que la estimación de diseño se fija **después** de que PO y TL cierran la suya y se ajusta hacia abajo por un ancla o una presión (no por una conversación donde diseño decide).
   > **Nos equivocamos si:** diseño dice su número en el planning junto a PO y TL y ese número se mantiene; o el ajuste sale de un recorte de alcance que el propio diseño propuso; o PO y TL cuentan que esperan el número de diseño antes de cerrar el suyo.
   > **Ojo:** un número que se mantiene **no** falsifica si diseño ya lo había ajustado al espacio que dejaba el plan de desarrollo antes de decirlo (autorrecorte). Es la creencia 5 con otra forma; el probe «¿ya estaba decidido cuándo empezaba desarrollo?» es el que lo distingue.
   > **Origen del ancla:** si la fecha viene fijada por el área solicitante antes del planning, anota que el ancla es externa a la célula. Cambia la decisión: integrar diseño en el planning no alcanza si la fecha ya venía puesta.
   > **Si aparece la tercera causa** («el problema cambió cuando ya estaba diseñando»): un solo probe —«¿qué cambió y quién lo cambió?»— y seguir. Se anota como señal para la creencia 3, no se profundiza.

### C. Cómo armó su número (7 min) — solo diseñadores/as

C1. Cuéntame cómo llegaste a ese número.
   - ¿Qué tenías a la vista cuando lo pensaste?
   - Si tuvieras que mostrarme de dónde salió ese número, ¿qué me mostrarías?
     - *(si nombra una iniciativa anterior)* ¿Cuánto tomó esa en realidad? ¿Dónde lo viste?
   - Aparte de [lo que ya contó en A], ¿qué más tomó tiempo y no estaba en tu número?
   - Cuando notaste eso [lo que contó en A], ¿qué hiciste? ¿Quién lo supo, y cuándo?
   - ¿Dónde quedó registrado lo que realmente tomó?
   > **Objetivo 2 · creencia 6.** Creemos que los diseñadores estiman por intuición, sin referencias de iniciativas anteriores, y que esa es la causa **principal** del desvío.
   > **Nos equivocamos si:** el/la diseñador/a usó referencias concretas (iniciativas anteriores, un registro, un método) y aun así se desvió mucho —entonces el método no es la palanca—; o su número original habría alcanzado si no lo hubieran cambiado —apunta a «proceso», no a «capacidad»—.
   > **Referencia = dato, no recuerdo.** «Más o menos con la anterior» sin saber cuánto tomó esa no cuenta como referencia concreta.
   > Los dos últimos probes sirven al objetivo 3: el lado de diseño de «cuándo se sabe» (para cruzar con D) y si existe hoy un registro del esfuerzo real. Si falta tiempo, prioriza estos dos.

### D. Cómo sigue el avance de diseño (7 min) — solo PO y TL

D1. Durante esa iniciativa, ¿cuándo supiste por primera vez cómo iba diseño? ¿Cómo te enteraste?
   - *(si lo seguía)* ¿Dónde lo mirabas? ¿Cada cuánto?
   - En esa iniciativa, ¿el trabajo de diseño estaba en Jira? ¿Qué mostraba?
   - En esta iniciativa, ¿cambió en algún momento lo que esperabas de diseño, en fecha o en lo que llegó? ¿Cómo y cuándo te enteraste?
     - *(si no cambió)* Se puede preguntar por la última vez que sí cambió, pero anótalo como **otro caso**.
   - ¿Qué hiciste con esa información?
     - *(si menciona algo propio: un Excel, una planilla, un PPT)* Cuéntame de eso: ¿qué tiene, cada cuánto lo actualizas, quién más lo ve?
   - *(PO)* Cuando reportas a gerencia el avance de esa iniciativa, ¿de dónde sacas lo de diseño?
   - ¿Y las estimaciones de desarrollo, dónde las miras?
   > **Objetivo 3 · viabilidad.** Creemos que PO y TL siguen el avance en Jira y que la estimación de diseño solo existe para ellos si está ahí (hipótesis de las personas sintéticas, sin evidencia).
   > **Nos equivocamos si:** se enteran de diseño por ceremonias, Slack o conversación directa, y no por Jira; o Jira ya tiene las tareas de diseño y aun así los cambios los toman por sorpresa (el problema no es dónde se ve, sino cuándo se sabe). Un handoff que llega a tiempo pero incompleto cuenta como cambio que se supo tarde.
   > **Reclasificación de Andrea (criterio observable):** si el PO no mantiene nada fuera de Jira para seguir o reportar diseño, y recibe esos datos en Jira o en el planning, Andrea pasa de secundaria a terciaria. Si ya mantiene algo propio (Excel, planilla, PPT para gerencia), **no** se reclasifica.
   > Si falta tiempo, prioriza: cuándo supo → qué cambió → qué había en Jira → lo propio y el reporte a gerencia. La pregunta por las estimaciones de desarrollo es la primera en caer.

## Cierre (4 min) — todos los roles

X1. ¿Qué debí haberte preguntado y no te pregunté?
X2. ¿Quién más de tu célula vivió esta misma iniciativa? ¿Y conoces a alguien, en otra célula, que lo vea distinto a ti?
   > X2 recluta a los otros roles de la misma célula (para cruzar versiones del mismo caso) y a quien contradiga.

Gracias. Repite la promesa de la introducción: lo que dijo se reporta agregado, no se usa para evaluar a nadie y no se le comenta a su célula (lo mismo que prometió la encuesta).

## Plan de reclutamiento

- **Fuente principal: los opt-ins de la encuesta** [product/surveys/2026-09-28-2125-desvio-estimacion-diseno.md](../surveys/2026-09-28-2125-desvio-estimacion-diseno.md) (R2 = sí, R3 con contacto). Llegan por los canales de su sección **Distribución** (Slack de diseño para diseñadores/as; correo o Teams de Tamara Sancy para PO y TL); esta guía no agrega canales para lo que esa encuesta ya cubre.
- **Cómo elegir entre los opt-ins** (quienes contradicen primero, porque los que confirman enseñan menos):
  - Objetivo 1: Q6 = «Nunca» o «Rara vez», o Q5 = «Se estima en el planning, junto con desarrollo».
  - Objetivo 2: diseñadores/as que en Q9 marcan «Un registro de lo que tomaron iniciativas anteriores» o «Un método o plantilla», **y** en Q2 reportan desvío (usan referencias y aun así se desvían).
  - Objetivo 3: PO y TL que en Q12 **no** marcan Jira.
  - Contradicción general: Q2 = «Ninguna» o Q10 con «El problema o los requisitos…» o «Pedidos fuera del roadmap» en primer lugar.
  - Dentro de una misma célula (D2), quienes ven distinto el mismo desvío: priorizar tríos completos.
- **Canal propio, solo para lo que la encuesta no alcanza:** los TL escépticos que no respondan la encuesta (su sesgo de no respuesta está anotado en Distribución). Si en la primera revisión (2026-10-05) hay menos de 3 TL con opt-in, pedir a Tamara Sancy una presentación directa, uno a uno, a TL de células sin respuesta; y usar X2 (referidos de la misma célula).
- **Filtro** (R1 de la encuesta + uno propio; se repite en la coordinación si la persona llega por referido):
  1. ¿Cuál es tu rol principal en tu célula? → **Fuera** si no es diseñador/a, PO ni TL (incluye áreas que piden piezas sueltas).
  2. ¿Llevas al menos 3 meses en tu célula y participaste en su planning en ese período? → **Fuera** si «no».
  3. ¿Puedes nombrar una iniciativa con trabajo de diseño que haya pasado a desarrollo en los últimos 3 meses? → **Fuera** si no puede nombrar una concreta (sin caso no hay entrevista).
- **Cuántas:** 5 a 6 por rol (15 a 18 en total), idealmente con 2 o 3 tríos de la misma célula. Se para un rol cuando las historias empiezan a repetirse (saturación), no al llegar a la cuota.
- **Cuándo:** desde la primera revisión de la encuesta (lunes 2026-10-05) con los opt-ins que haya, hasta una o dos semanas después del cierre (2026-10-16). Semanas 3–5 de la agenda de la oportunidad.

## Pretest notes

### 2026-09-28 · Matías Contreras (diseñador), Andrea Muñoz (PO), Felipe Soto (TL)

Corrida en seco de la guía original con tres personas **sintéticas**, cada una por el recorrido de su rol, suponiendo que eran de la misma célula. Es control de calidad del instrumento, no evidencia: nada de esto va a `product/insights/`. Todos los cambios fueron aprobados por Pancho.

**Qué cambió**

- **Introducción nueva (I1, 1 min):** propósito neutro, sin mencionar diseño ni estimaciones; confidencialidad al inicio; aviso de que se entrevistará a otros roles de la célula. Motivo: la promesa estaba al final, después de las preguntas sensibles («¿les vas a preguntar por lo mismo?», Matías), y un TL leyó la entrevista como diseño buscando más tiempo («¿Esto es para que diseño pida más tiempo?», Felipe). El calentamiento baja de 4 a 3 min para hacerle espacio.
- **A1:** «hasta que se entregó» → «hasta que salió a producción —o hasta hoy—». Para diseño, «entregar» era el handoff y el relato se cortaba ahí. Se agrega la variante **A1b** para el segundo y tercer rol de la misma célula: con A1 al pie de la letra, la PO eligió otra iniciativa y se perdía el cruce entre roles.
- **B1:** probe nuevo, para todos los roles: «¿ya estaba decidido cuándo empezaba desarrollo?». Reemplaza el probe de PO/TL «¿cómo sabías cuánto necesitaba diseño?», que salió flojo y redundante («Por lo que dijo él» / «No sabía»). Se agrega el probe «¿De dónde salió esa fecha?», porque las corridas ubican el ancla en el área solicitante. Se corta «¿Qué se dijo en ese momento? ¿Quién estaba?», que no llevó a ninguna parte en los tres roles. Se agrega una pregunta de contraste tras «¿fue como las demás?», que siempre recibió «igual». Se agregan a la nota de falsación el **autorrecorte** (el número «se mantuvo» porque diseño ya lo había ajustado al espacio disponible) y el **ancla externa**.
- **C1:** «paso a paso» fuera, porque invitaba a armar un método en el momento. «¿Lo comparaste con algo…?», que era de sí o no y traía la práctica «correcta», pasa a ser «¿qué me mostrarías?» más un control de si la referencia era un dato. «¿Qué tomó tiempo y no estaba en tu número?» se ancla a lo ya dicho en A, porque era redundante. Probe nuevo sobre quién supo del desvío y cuándo: es el lado de diseño del objetivo 3. Nota: una referencia que es recuerdo no cuenta.
- **D1:** la apertura pasa a «¿cuándo supiste por primera vez…?», porque las preguntas suponían que PO y TL seguían el avance («No me entero… En ningún lado», Felipe). Se ancla al caso: «la última vez que…» llevaba a otra iniciativa. Se amplía a «en fecha o en lo que llegó» («llegó a tiempo, pero incompleto», Felipe). Probe sobre qué mostraba Jira, porque la señal de falsación lo necesitaba y nadie lo preguntaba. Probe sobre herramientas propias (el Excel de la PO) y sobre el reporte a gerencia. El criterio de reclasificación de Andrea pasa de predicción («nunca irían») a algo observable. Se quita la cita «postura de Felipe», que atribuía un dato a una persona sintética.
- **Notas para quien entrevista:** redirigir los relatos que se van a los stakeholders y anotar la creencia 3 como señal; el desvío como handoff incompleto; Jira como fuente de medición incompleta para la creencia 1; nada de lo que dijo un rol se le cuenta a otro.
- **Prioridades por tiempo** en C y D, para que la guía siga cabiendo en 30 min con los probes nuevos.

**Qué se dejó igual a propósito**

- La apertura de B1 («¿Cómo se decidió cuánto tiempo tendría diseño?»): en los tres roles sacó que el tiempo de diseño se calcula hacia atrás desde el plan de desarrollo.
- «¿Qué pasó con ese número…?»: desarmó la respuesta de la PO que sonaba a lo esperable («bien colaborativo» → «le pregunté si podía ser una semana»).
- El probe de A1 «¿Qué tomó más o menos…?», aunque PO y TL lo respondan sobre desarrollo: la diferencia entre versiones es el hallazgo (mismo episodio de los estados, contado distinto por diseño y por el TL).
- X1: respuestas pobres de perfiles junior y TL son esperables; no es defecto de la pregunta.
- «¿Y las estimaciones de desarrollo, dónde las miras?»: se mantiene, al final de D, como la primera en caer si falta tiempo.
- Magnitud y absorción del desvío siguen fuera de alcance; solo se agrega la nota sobre Jira como fuente.

**Límite:** este pretest valida estructura (inducción, redundancia, orden, cobertura), no recepción. Las personas sintéticas son más articuladas y colaboradoras que un participante real. Pendiente: una segunda corrida sobre esta versión y, antes de las entrevistas reales, una prueba con una persona real (un/a diseñador/a junior idealmente).
