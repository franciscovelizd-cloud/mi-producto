---
opportunity: desvio-estimacion-diseno
status: chosen
chosen: problema-listo-para-diseno
tests: product/tests/2026-10-17-1210-desvio-estimacion-diseno.md
---

# Soluciones para: Desvío de estimación de diseño en las células

## Qué dice hoy la evidencia
- Toda la evidencia es `synthetic`, `secondary` o `unverified`. La encuesta analizada en `notas:ensayo/2026-10-06-1350-desvio-estimacion-diseno-encuesta.md` es de práctica (`synthetic`) y no cambia el estado de ninguna creencia. Todavía no existen el export de Jira ni la observación propia por escrito.
- Creencia 6 (falta de método): es la que más se movió, en contra. La literatura pone primero los requisitos que cambian (Pasuksmit 2024, `secondary`). En la encuesta de práctica, 14 de 21 ponen primero el cambio de requisitos y nadie pone primero la falta de método (`synthetic`).
- Causa "proceso" (recorte de la estimación): aparece solo en diseñadores con menos de 2 años (3 de 3, `synthetic`).
- Creencia 1 (magnitud): abierta. Diseño percibe desvío (8 de 12) y PO/TL no (4 de 14). Con la tarjeta única de Jira, la métrica del sponsor puede marcar cerca de cero (`synthetic`).
- Creencia 2 (desvío ↔ atraso): señal débil a favor. Se confirma solo con un cruce en Jira.

## Línea base: qué hace la célula hoy
Todo `synthetic` (encuesta de práctica y personas):
- Diseño absorbe el desvío sin que se vea: deja fuera estados y casos borde (7 de 12) y trabaja fuera de horario (5 de 12).
- En Jira diseño es una sola tarjeta que se cierra en el handoff y queda "a tiempo" (R006).
- El esfuerzo real no queda registrado o queda disperso (4 de 11: en ninguna parte).
- Se estima por intuición, comparando de memoria o ajustándose a la fecha. Algunos usan colchón fijo (R029).
- Los casos borde los terminan definiendo desarrollo y QA (R013; persona Felipe Soto).

## Alternativas
### A1. Design Owner, app de gestión de diseño end-to-end (`design-owner-app`)
Idea candidata de la oportunidad. Aplicación interna donde diseño planifica, estima, registra el esfuerzo real y documenta cada iniciativa; la PO consulta. Ataca la capacidad de estimar, la visibilidad y la medición. Para Camila Rojas y Matías Contreras (primarias) y Andrea Muñoz (secundaria). Reemplaza los registros dispersos y la tarjeta única.
### A2. Diseño desglosado en Jira (`diseno-en-jira`)
Idea candidata de la oportunidad. Diseño tiene estimación propia y subtareas por entregable, incluidos estados y casos borde, abiertas hasta quedar cubiertas, en el mismo tablero de PO y TL. Ataca la absorción invisible. Para Felipe Soto (terciaria), Andrea y Camila. Reemplaza la tarjeta única. Es un cambio en una herramienta actual.
### A3. Control de cambios con re-estimación (`control-cambios-diseno`)
Regla con plantilla: cada cambio de requisitos con el diseño iniciado se registra (qué cambió, quién lo pidió, cuánto se rehace). Diseño re-estima y la PO decide entre mover la fecha o recortar alcance. Ataca la causa principal haciendo visible su costo. Andrea decide; Camila y Matías re-estiman. No es software.
### A4. Problema listo antes de diseñar (`problema-listo-para-diseno`)
Criterio de entrada: las reglas de negocio y lo que pidan legal o compliance están validados, y diseño participa en la definición del problema antes de comprometer una estimación. Mientras no se cumpla, diseño solo explora, sin estimación comprometida. Ataca la causa principal antes de que ocurra. Andrea es dueña del criterio; Camila lo quiere. Es una política, no software. Conecta con la oportunidad C.
### A5. Referencias y colchón (`referencias-estimacion`)
Lo más pequeño que podría funcionar: planilla con 10 a 15 iniciativas pasadas (lo estimado contra lo real, qué se olvidó), checklist de tareas que suelen olvidarse y colchón fijo de 20 a 25%. Ataca la causa "método" y el poco peso de los juniors en el planning. Para Matías.

## Comparación
| Alternativa | Deseable | Factible | Viable | Creencia más riesgosa |
|---|---|---|---|---|
| A1 | mixed: diseño la quiere (creencia 4 `weakened`, personas Camila y Matías, `synthetic`); PO/TL miran Jira (13 de 14, `synthetic`); Felipe ignoraría otra plataforma (`synthetic`); no ataca el cambio de requisitos | to check with tech | mixed: podría generar la medición, pero lo genérico existe y es barato (Tempo, Float, Runn) y "no justifica una app aparte" (research 09-17, `secondary`) | En un piloto de 6 semanas, PO y TL abren Design Owner en al menos 2 de cada 3 plannings para usar la estimación de diseño |
| A2 | mixed: deja ver el desvío absorbido y está donde PO/TL miran (13 de 14, `synthetic`); es la condición de Felipe (`synthetic`); no ataca la causa | to check with tech | mixed: permite medir la métrica del sponsor, incluido el alcance dejado fuera (insight 2 de práctica, `synthetic`) | En 2 células durante 6 semanas, el desglose refleja el esfuerzo real (menos de 20% de diferencia con lo que reporta diseño) en al menos 4 de 5 iniciativas |
| A3 | mixed: ataca la causa principal (`secondary` + 14 de 21 `synthetic`; 8 de 16 respuestas abiertas la mencionan como gatillo); reacciona después del cambio | mixed: no requiere software; reabrir le cuesta capital político a la PO (persona Andrea, `synthetic`) | mixed: genera el registro de retrabajo que la métrica necesita (`assumption`) | Con el cambio registrado y re-estimado, la PO elige mover la fecha o recortar alcance en al menos 2 de 3 casos, en vez de pedir que diseño lo absorba |
| A4 | mixed (la más respaldada; pain evidenced, relief not tested): ataca la causa principal antes de que ocurra (`secondary` + `synthetic`); no cubre los cambios que nacen de pruebas con usuarios ni el recorte de los juniors | mixed: depende de que la PO y legal o negocio acepten el criterio; Andrea teme perder control (`synthetic`); pedidos fuera del roadmap (R016, `synthetic`) | mixed: debería bajar el desvío y los días de desarrollo perdidos, pero sola no mide (`assumption`) | En las últimas 10 iniciativas que se desviaron, al menos el 60% de los cambios de requisitos se habría detectado con la checklist de entrada |
| A5 | weak para la célula: la causa "método" no la pone primera nadie (0 de 21, `synthetic`); sirve a juniors (n=3) y el colchón le funcionó a R029 (`synthetic`); comparar con trabajos anteriores reduce el optimismo (`secondary`) | mixed: hacer la planilla es trivial, pero falta el dato histórico (4 de 11 sin registro, `synthetic`) | weak: el colchón baja el % inflando lo planificado, no el costo (`assumption`) | Cuando un diseñador con menos de 2 años lleva referencias al planning, su estimación se recorta menos de 20% en al menos 2 de cada 3 iniciativas |

## Decisión
Elegida: **A4, problema listo antes de diseñar**. La eligió Pancho, siguiendo la recomendación de la IA. Razones: es la única alternativa preventiva que ataca la causa respaldada por dos fuentes independientes, cuesta poco ponerla en marcha, y su creencia más riesgosa se revisa con datos existentes (las últimas 10 iniciativas desviadas) sin construir nada.

**Requisito heredado de A2:** cualquier implementación de A4 tiene que dejar medible el desvío, incluido el retrabajo y el alcance dejado fuera, donde planifican PO y TL. Sin eso no hay métrica del sponsor.

**Qué cambiaría la decisión:** si la revisión muestra que la mayoría de los cambios no se podía prever, pasa A3. Si el sponsor exige ver la métrica antes de cambiar el proceso, sube A1, siempre que tech confirme la integración con Jira.

Durante la exploración, Pancho sacó A2 y A3 por ser reactivas o depender de herramientas actuales, y después las repuso. Quedan en espera con su razón.

T1 cerrado inconclusive (2026-10-18), ver [tests](../tests/2026-10-17-1210-desvio-estimacion-diseno.md): la creencia más riesgosa de A4 sigue sin probar.

## Propuesta de valor: problema-listo-para-diseno
Escrita para Camila Rojas (primaria); el efecto también llega a Felipe Soto (terciaria).
- **Dolor que alivia:** rehacer el diseño cuando cambian reglas o requisitos con el trabajo avanzado. Ejemplos: «Legal pidió cambios cuando ya tenía el 70% diseñado… estimamos 2 semanas y fueron casi 4» (R001); «Negocio cambió la regla de copago dos veces mientras se diseñaba» (R009); Camila pierde 2 a 3 días por iniciativa discutiendo supuestos sin validar. Todo `synthetic`.
- **Ganancia:** diseño estima sobre un problema estable, así que su número vale en el planning. Diseño participa en la definición del problema, que es el objetivo de Camila. A desarrollo le llegan menos cambios a mitad de sprint.
- **Qué reemplaza:** empezar a diseñar sobre definiciones que todavía se mueven y absorber el desvío en silencio. Ese modo cuesta horas fuera de horario y estados incompletos que reaparecen en desarrollo, QA o producción (`synthetic`).
- **Deliberadamente no hace:** no es una app nueva; no enseña a estimar (eso es A5); no gestiona los cambios que ocurran después de empezar (eso es A3); no ordena los pedidos fuera del roadmap ni los de Patricia Vergara; no congela el problema: la exploración sin estimación comprometida está permitida.

## Creencias
Referenciadas, tal como están registradas en product/overview.md:
- [opportunity: desvio-estimacion-diseno] [value] En las células, el esfuerzo real de diseño supera lo planificado en ≥30% en al menos la mitad de las iniciativas, y la célula absorbe ese desvío con horas extra, recorte de alcance o cambios a mitad de sprint.
- [opportunity: desvio-estimacion-diseno] [viability] Las iniciativas con mayor desvío de diseño son las que más se atrasan contra la fecha comprometida y las que más días de desarrollo pierden por cambios a mitad de sprint.
- [opportunity: desvio-estimacion-diseno] [value] El desvío se origina principalmente en que los diseñadores no tienen método ni referencias para estimar, y no solo en el recorte posterior de su estimación. *(A4 apuesta en contra de esta creencia.)*

Registradas en product/overview.md (2026-10-06):
- [feature: problema-listo-para-diseno] [value] De las últimas 10 iniciativas con desvío de diseño, al menos el 60% de los cambios de requisitos ocurridos con el diseño iniciado se habría detectado con un criterio de entrada (reglas de negocio, legal o compliance, alcance validados).
- [feature: problema-listo-para-diseno] [feasibility] En un piloto de un trimestre en 2 células, la PO y las áreas solicitantes aceptan no comprometer una estimación de diseño hasta pasar el criterio en al menos 4 de 5 iniciativas, sin alargar el plazo total de la iniciativa en más de una semana.
- [feature: problema-listo-para-diseno] [viability] En las células del piloto, el desvío de diseño (con retrabajo y alcance dejado fuera) y los días de desarrollo perdidos por cambios a mitad de sprint bajan al menos 25% frente al trimestre anterior. El umbral es provisional hasta que el sponsor fije el suyo.

## Descartadas o en espera
- A1 `design-owner-app`: en espera. PO y TL no miran fuera de Jira y lo genérico ya existe. Vuelve si tech confirma la integración con Jira y el sponsor necesita un producto para ver la métrica.
- A2 `diseno-en-jira`: en espera. Su mecanismo de medición pasa a ser requisito de A4. Vuelve como implementación de esa medición.
- A3 `control-cambios-diseno`: en espera. Reacciona después del cambio. Vuelve si la revisión de las 10 iniciativas muestra que la mayoría de los cambios no se podía prever.
- A5 `referencias-estimacion`: en espera para el segmento junior. Ataca una causa que la evidencia no muestra como principal (n=3). Vuelve si las entrevistas confirman el patrón de recorte en juniors.
