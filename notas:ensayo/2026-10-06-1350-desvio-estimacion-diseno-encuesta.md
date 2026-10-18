---
opportunity: desvio-estimacion-diseno
source: synthetic
sources:
  - notas:ensayo/respuestas_encuesta.csv (set de ensayo, no son respuestas reales)
  - diseño de la encuesta: product/surveys/2026-09-28-2125-desvio-estimacion-diseno.md
date: 2026-10-06
language: es
---

# Insights (ensayo): encuesta de desvío de estimación de diseño

> **Ensayo:** estos datos no son respuestas reales. Sirven para probar el análisis de la encuesta. Los insights son hipótesis y no cambian el estado de ninguna creencia de `product/overview.md`.

**Denominador.** 30 respuestas: 25 completas, 1 parcial, 4 descalificadas en el filtro. Válidas: **26** — 12 diseñadores/as, 8 PO, 6 TL. Todo está bajo 30 por rol: **los resultados son direccionales**, se leen como patrones.

**Sesgo de canal.** Rol y canal casi coinciden: 9 de 12 diseñadores llegaron por el Slack de diseño, y los 14 PO/TL por el envío de la Head of Product. Por eso, toda diferencia entre diseño y PO/TL puede ser también del canal: deseabilidad de mostrar el problema en uno, de cuidar a la célula en el otro. Cobertura por célula: no se puede calcular, porque D2 es opcional (7 células nombradas) y el total de células sigue unknown.

**Calidad.** 3 respondentes dejaron el ranking de Q10 en el orden en que se presentó (R020, R022, R030). Las cifras de Q10 se informan con y sin ellos. R020 además se contradice (Q1 «menos de lo planificado», Q2 «todas»).

Las citas van por ID y rol, nunca por nombre ni por célula, como prometió la introducción de la encuesta.

---

## 1. El desvío nace de cambios de requisitos con el diseño ya iniciado, no de la falta de método para estimar

En los tres roles, la causa número uno es que el problema o los requisitos cambian cuando diseño ya empezó: 14 de 21 la ponen primera en Q10 (11 de 18 sin los rankings sin tocar). «Falta método o referencias» no la pone primera nadie (0 de 21) y queda en el último lugar promedio. Q8 lo respalda con conducta: 15 de 26 dicen que los requisitos cambian «frecuentemente» o «siempre» con el diseño andando, y solo 1 dice «rara vez». En 8 de las 16 respuestas abiertas, el desvío lo gatilla un cambio de alcance o de regla que pide legal, compliance, negocio, el PO o una prueba con usuarios. **Implicancia:** un método de estimación no arregla esto. Lo que necesita el producto es registrar el cambio cuando ocurre (qué cambió, quién lo pidió, cuánto diseño se rehízo) y re-estimar en el momento. Esta causa está antes del diseño y conecta con la oportunidad C (diseño fuera de la definición del problema). *Límite:* Q10 es opinión, y «requisitos» era el primer ítem de la lista. Aun así, PO y TL, que no tienen motivo para proteger a diseño, la ponen igual de arriba.

> Evidencia: «Negocio cambió la regla de copago dos veces mientras se diseñaba. Diseño no tenía cómo saberlo, nosotros tampoco.» — R009, Product Owner
> «Legal pidió cambios cuando ya tenía el 70% diseñado y hubo que rehacer casi todo, estimamos 2 semanas y fueron casi 4.» — R001, diseñador/a

## 2. Diseño absorbe el desvío sin que se vea: recorta estados y casos borde, y en Jira la iniciativa aparece a tiempo

En las iniciativas que se desviaron, 7 de 12 diseñadores dicen que se dejó fuera parte del diseño (estados, casos borde, validación) y 5 de 12 que trabajaron fuera de horario. Entre PO y TL, cada uno de esos costos lo marca solo 1 de 12. La percepción del desvío también se parte por rol: 8 de 12 diseñadores ven desvío de 30% o más en la mitad o más de sus iniciativas, contra 4 de 14 PO/TL. En 3 de las 4 células donde respondieron diseño y PO/TL, no coinciden. El costo reaparece después, en desarrollo, en QA o en producción (4 respuestas abiertas), y la herramienta no lo registra: en Jira, diseño es una sola tarjeta que se cierra en el handoff. **Implicancia para la métrica del sponsor:** el «desvío planificado vs. real», medido con la tarjeta de Jira de hoy, va a dar cerca de cero. La métrica tiene que contar el alcance de diseño que se dejó fuera y el retrabajo, no solo la fecha de cierre. El paso de la agenda «exportar de Jira el esfuerzo de diseño real» corre riesgo: 4 de 11 diseñadores dicen que su esfuerzo real no queda registrado en ninguna parte.

> Evidencia: «No sabría decir cuánto tomó de verdad. En Jira diseño es una sola tarjeta que se cierra cuando pasa a desarrollo, así que siempre se ve "a tiempo".» — R006, Product Owner
> «Rehice como 3 veces el flujo de pago y eso no lo midió nadie, en el sprint aparece como si hubiera tomado lo planificado.» — R005, diseñador/a
> «Los casos borde los terminamos definiendo los devs con QA porque no venían en el Figma.» — R013, Tech Lead

## 3. El recorte de la estimación y el plazo impuesto no son la norma: se concentran en los diseñadores con menos de 2 años

En general, la estimación de diseño se hace dentro del planning o antes: así lo dicen 17 de 26 (7 de 12 diseñadores, 6 de 8 PO, 4 de 6 TL). Solo 3 de 26 dicen que se la reducen «frecuentemente» o «siempre». Pero los 3 diseñadores con menos de 2 años describen el patrón completo: la estimación se define después del planning o no existe, a 2 de ellos se la recortan entre un 40% y un 60%, los 3 se ajustan a la fecha disponible y los 3 ven desvío en la mitad o más de sus iniciativas. Los 8 diseñadores con 2 años o más no reportan recortes frecuentes, y 7 estiman dentro del planning o antes. **Implicancia:** la causa «proceso» existe, pero en un segmento, no en toda la célula. Una funcionalidad para defender la estimación en el planning (referencias de iniciativas parecidas que respalden el número) sirve sobre todo a quien todavía no tiene peso para negociarla. Quien estima con un colchón fijo cuenta que le funcionó, y eso sugiere que alcanza con una referencia simple. *Límite:* son 3 personas.

> Evidencia: «Me recortaron a la mitad lo que propuse, el TL dijo que era una pantalla nomás.» — R028, diseñador/a (menos de 2 años)
> «Nadie me pregunta cuánto me demoro, me dicen para cuándo lo necesitan.» — R003, diseñador/a (menos de 2 años)
> «Desde que le pongo colchón fijo ya casi no me pasa.» — R029, diseñador/a

## 4. Si la estimación de diseño no está en Jira, para PO y TL no existe

13 de 14 PO/TL revisan avance y plazos en Jira, y 6 de 14 lo complementan en ceremonias. Los diseñadores, en cambio, registran su esfuerzo real en lugares dispersos: Jira (4 de 11), ninguna parte (4), planilla (2), Notion (1) o un Toggl personal (1). **Implicancia (objetivo 4 de la encuesta):** esto inclina la decisión hacia una capa sobre Jira y no hacia una app aparte. Una app separada de Design Owner quedaría donde PO y TL no miran. Lo mínimo es que diseño deje de ser una sola tarjeta: subtareas o estimación propia que sigan abiertas hasta cubrir estados y casos borde.

> Evidencia: «Llegaron cambios de UI con el sprint andando y botamos casi una semana de front. Si no está en Jira para nosotros no existe.» — R007, Tech Lead

---

## Lectura por objetivo de aprendizaje

| Objetivo | Qué creíamos | Qué mostró la encuesta | Decisión |
|---|---|---|---|
| 1. Magnitud y absorción | Desvío ≥30% en ≥ la mitad, absorbido por la célula | Diseño dice que sí (8/12). PO/TL dicen que no (4/14). La absorción sí ocurre: solo 3 de 24 marcan «nada de lo anterior» | La percepción no zanja la magnitud. Seguir con la oportunidad, pero medir con un registro compartido (ver insight 2) |
| 2. Proceso | Diseño estima después y fuera del planning | Solo en juniors (3/3). En general, dentro del planning (17/26) | Integrar la estimación al planning no es la idea principal. Sirve como apoyo para un segmento |
| 3. Capacidad vs. requisitos | Falta método | Requisitos cambiantes, primera causa en los 3 roles. Método, 0 votos como primera | Apuntar las ideas a registrar y re-estimar cambios, no a enseñar a estimar |
| 4. Dónde vive el registro | Jira o nada (Felipe, sintético) | PO/TL en Jira (13/14). El registro de diseño está disperso | Capa sobre Jira |

**Días de desarrollo perdidos (Q4, PO/TL, n=14):** la mediana es 1–2 días en 3 meses, por debajo de la cifra sintética de 3–5 días por iniciativa. Los TL reportan más que los PO. Entre los PO/TL que ven desvío en la mitad o más, 3 de 4 reportan 3 días o más; entre los demás, 2 de 9. Es una señal débil a favor de la creencia 2, que confirma recién un cruce con Jira.

## «Por qué» para las entrevistas

- ¿Quién trae el cambio de requisitos con el diseño andando, en qué momento, y por qué no apareció antes del diseño?
- ¿Quién decide qué estados o casos borde quedan fuera, y si eso se dice o pasa en silencio?
- ¿Por qué diseño y PO/TL de una misma célula ven distinto el mismo desvío?
- ¿Qué tienen los diseñadores con más años que los juniors no tienen para defender su estimación?

## Pool de reclutamiento (opt-in con R1 = sí y contacto)

Los contactos están en el CSV. Aquí van solo los IDs. Primero los que contradicen las creencias:

1. **R011** (diseño, más de 10 años): «el diseño casi siempre calza», dice que no es un problema de estimar. Contradice la creencia 1.
2. **R016** (PO): la causa son los pedidos fuera del roadmap, «eso es lo que hay que ordenar, no la estimación». Contradice la creencia 6 y la causa dominante.
3. **R019** (PO, «ninguna») junto con **R005** (diseño, «más de la mitad»): en la misma célula ven distinto el mismo desvío. Es el par que pedía el diseño de la encuesta.
4. **R029** (diseño): con colchón fijo ya casi no se desvía. Prueba si una referencia simple alcanza.
5. Confirman y aportan detalle: R001, R003 (junior), R006, R007, R009, R012, R013, R022.

R028 (diseño junior, el caso más claro de recorte) aceptó la conversación pero no dejó contacto. R004 tiene un caso igual de fuerte, pero no califica por R1.
