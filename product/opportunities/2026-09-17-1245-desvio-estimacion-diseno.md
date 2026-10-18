---
status: framed
segment: Células de producto internas de Continuum (diseñador/a, Product Owner y Tech Lead) que planifican iniciativas del roadmap con una estimación de diseño
personas: camila-rojas, matias-contreras, andrea-munoz, felipe-soto
---

# Oportunidad: Desvío de estimación de diseño en las células

En las células de producto de Continuum, el esfuerzo real de diseño por iniciativa se aleja de lo planificado. El desvío lo absorbe toda la célula: horas extra, alcance recortado, cambios a mitad de sprint y fechas que se mueven. Es urgente ahora porque el sponsor eligió el desvío de estimación de diseño como una de sus dos métricas para decidir si sigue financiando.

> Insumo preliminar: todas las señales son `synthetic` o `unverified`.

## Segmento y personas

- **Segmento: toda la célula.** Cada rol paga un costo distinto:
  - **Camila Rojas** (diseñadora senior): le recortan la estimación después de que el PO y el TL cierran la suya. Trabaja fuera de horario.
  - **Matías Contreras** (diseñador junior-intermedio): estima por intuición, se queda corto y trabaja de noche sin decirlo.
  - **Felipe Soto** (TL): pierde días de desarrollo por cambios de diseño tardíos. Estima sin saber cuánto le falta a diseño.
  - **Andrea Muñoz** (PO): las estimaciones de diseño le llegan tarde o cambian, y tiene que mover fechas ya comprometidas con gerencia.
- **Queda fuera:** Patricia Vergara (stakeholder comercial, persona negativa). Sus pedidos sueltos de piezas no son este problema.
- **Persona faltante:** ninguna identificada para este segmento.
- **Dos causas en competencia, sin resolver:** (1) *proceso*: la estimación de diseño se ajusta después y fuera del planning; (2) *capacidad*: los diseñadores no tienen método ni referencias para estimar. El problema se define por el costo observable, no por una de las dos causas.

## Señales

| Señal | Provenance | Fuente |
|---|---|---|
| Recortes de estimación de diseño y retrabajo vistos en células reales | unverified | Observación de Pancho, sin archivo todavía |
| El sponsor eligió el "desvío de estimaciones de diseño" como métrica de seguimiento | unverified | product/overview.md (Liliana Reyes, Tamara Sancy) |
| La estimación de diseño se resuelve como complemento de la del PO y el TL | unverified | product/overview.md, creencia registrada |
| A Camila le queda cerca de la mitad de los días que pide y entrega fuera de horario | synthetic | product/personas/camila-rojas.md |
| Matías se demoró cerca del doble en sus últimas iniciativas | synthetic | product/personas/matias-contreras.md |
| Los cambios de diseño a mitad de sprint cuestan 3–5 días de desarrollo por iniciativa | synthetic | product/personas/felipe-soto.md |
| Las estimaciones de diseño llegan tarde o cambian y obligan a mover fechas comprometidas | synthetic | product/personas/andrea-munoz.md |

*Jira (horas o puntos de diseño planificados y reales) todavía no es una señal: es la primera fuente de datos de la agenda.*

## Resultado de negocio

Modo interno, métrica del sponsor.

- **Principal:** % de desvío entre el esfuerzo de diseño planificado y el real, por iniciativa.
- **Secundario (costo evitado):** días de desarrollo perdidos por cambios de diseño a mitad de sprint.
- Los umbrales de la métrica los define el sponsor; siguen pendientes.

## Restricciones

- Ninguna conocida por ahora. No hay fecha, presupuesto ni compliance declarados, así que la agenda usa semanas relativas.
- Pendiente (no es restricción): los umbrales de éxito que tiene que fijar el sponsor.

## Creencias

Referencias a product/overview.md, que es el registro único de creencias:

- [opportunity: desvio-estimacion-diseno] [value] En las células, el esfuerzo real de diseño supera lo planificado en ≥30% en al menos la mitad de las iniciativas, y la célula absorbe ese desvío con horas extra, recorte de alcance o cambios a mitad de sprint.
- [opportunity: desvio-estimacion-diseno] [viability] Las iniciativas con mayor desvío de diseño son las que más se atrasan contra la fecha comprometida y las que más días de desarrollo pierden por cambios a mitad de sprint.
- [opportunity: desvio-estimacion-diseno] [value] El desvío se origina principalmente en que los diseñadores no tienen método ni referencias para estimar, y no solo en el recorte posterior de su estimación. *(compite con la creencia de producto de abajo)*
- [product] [viability] La estimación de diseño no está integrada a la estimación del roadmap: se resuelve como complemento a lo que definen el PO y el Tech Lead, sin que diseño participe directamente.

## Agenda de investigación

| Creencia                     | Instrumento (del más barato al más caro)                                                                                                                                                                                                  | Decisión que desbloquea                                                                                                   | Para cuándo |
| ---------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- | ----------- |
| Todas                        | Dejar la observación propia por escrito en `product/research/` (célula, fecha, qué pasó)                                                                                                                                                  | Pasar la señal de `unverified` a `real`                                                                                   | Semana 1    |
| Value: desvío ≥30% en ≥mitad | **Datos existentes:** exportar de Jira el esfuerzo de diseño planificado y real de los últimos 2 trimestres, por célula. Si Jira no registra diseño, pasar a encuesta                                                                     | Seguir con la oportunidad, descartarla o reformularla                                                                     | Semana 1–2  |
| Viability: desvío ↔ atraso   | **Datos existentes:** cruzar en Jira el desvío de diseño con el atraso contra la fecha comprometida y con las reaperturas a mitad de sprint                                                                                               | Presentarla al sponsor como palanca del roadmap o solo como costo interno de diseño                                       | Semana 2–3  |
| Causa proceso vs. capacidad  | **Secundaria** (`/research-market`): cómo estiman diseño otros equipos in-house → **Encuesta** a la célula (diseño, PO, TL): cuándo y cómo se estima y se ajusta diseño, con opt-in → **Entrevistas** con quienes contradigan la creencia | Hacia dónde apuntan las ideas (integrar la estimación en el planning o dar un método para estimar); acota `/clarify-idea` | Semana 3–5  |

## Ideas candidatas (no evaluadas)

- **Design Owner** como aplicación interna de gestión de diseño end-to-end (así llegó en el overview). → **parked** (A1, `design-owner-app`), ver [product/solutions/2026-10-06-1359-desvio-estimacion-diseno.md](../solutions/2026-10-06-1359-desvio-estimacion-diseno.md)
- Estimaciones de diseño visibles donde la célula ya planifica, por ejemplo Jira (sale de la postura de Felipe, sintética). → **parked** (A2, `diseno-en-jira`; su medición pasa a ser requisito de la elegida), ver [product/solutions/2026-10-06-1359-desvio-estimacion-diseno.md](../solutions/2026-10-06-1359-desvio-estimacion-diseno.md)

Exploración de soluciones (2026-10-06): elegida `problema-listo-para-diseno`, ver [product/solutions/2026-10-06-1359-desvio-estimacion-diseno.md](../solutions/2026-10-06-1359-desvio-estimacion-diseno.md)

## Cola de oportunidades

- B · Impacto de diseño sin medir: sin KPIs de UX (siguiente).
- C · Diseño fuera de la definición del problema (tercera).
- D · Contexto de diseño e IA disperso: fuera por ahora.
