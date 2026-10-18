---
source: secondary
method: web
date: 2026-09-17
question: ¿Cuánto y por qué se desvían las estimaciones de diseño, cómo estiman diseño los equipos in-house, qué herramientas existen para medirlo y hacia dónde van DesignOps e IA en la planificación del diseño?
opportunity: desvio-estimacion-diseno
---

# Research: desvío de estimación de diseño en equipos de producto

Búsqueda web del 2026-09-17, con 4 agentes en paralelo (uno por carril). Tres advertencias de método:
- Las citas pasaron por un resumen automático de las páginas. Antes de usarlas en un documento formal, conviene revisar el texto original.
- Reddit, DesignOps Assembly y el informe original Figma AI 2025 bloquearon el acceso. No hay señal de foros de diseñadores.
- Casi toda la evidencia viene de software en general, de agencias o de EE.UU. y Europa. **Nada de esto verifica lo que pasa en las células de Continuum.**

**Los tres hallazgos que cambian decisiones:**

1. **Nadie mide el desvío de estimación de diseño.** No encontramos estudios ni productos que lo midan. En software el desvío está bien documentado: 30–40% de sobreesfuerzo medio, y entre 61% y 84% de los proyectos terminan sobre lo estimado. En diseño no hay ni un solo dato de estimado vs. real. Esto tiene dos consecuencias:
   - El umbral del sponsor no se puede tomar prestado del mercado. La línea base tiene que salir de Jira.
   - El espacio está libre, pero lo genérico ya existe y es barato: Jira nativo, Tempo, Float, Runn. Lo propio de diseño probablemente cabe como una capa sobre Jira y no justifica una app aparte.
2. **La disyuntiva "proceso vs. capacidad" está incompleta.** En la literatura sobre desvíos, la causa más citada es otra: información poco clara y requisitos que cambian. Además:
   - El anclaje y la presión para bajar estimaciones, que son causas de *proceso*, tienen evidencia robusta.
   - La experiencia sola no mejora la precisión. Sí la mejoran los datos históricos y las analogías con trabajos anteriores.
   - Implicancia: dar un método sin datos propios y sin un lugar en el planning probablemente no baja el desvío. Además, la tercera causa conecta con la creencia 3 (diseño fuera de la definición del problema).
3. **La IA está cambiando *qué* se estima, no *cómo* se gestiona.** En 2026 el 91% de los diseñadores usa IA cada semana, el 65% absorbe trabajo de PM o ingeniería, y los story points se vuelven inestables en flujos asistidos por LLM. Ninguna fuente muestra IA usada para planificar o estimar diseño. Si Design Owner estima con patrones históricos por entregable, heredaría esa inestabilidad.

---

## 1. Magnitud y causas del desvío

### Magnitud en software (no hay datos de diseño)

- Revisión de encuestas internacionales: 30–40% de sobreesfuerzo medio. Entre 61% y 84% de los proyectos terminan sobre presupuesto, y entre 65% y 80% se atrasan (desvío de 20–25%). Moløkken-Østvold, Simula, 2004; software general, varios países. [verificado: https://cms.simula.no/sites/default/files/publications/SE.3.Moloekken-Oestvold.2004.pdf — 2026-09-17]
- Encuesta noruega de 2003 (52 proyectos): 76% con sobreesfuerzo, de 41% en promedio. En el sector público el problema es mucho más frecuente que en el privado (67% vs. 21%). [verificado: misma URL]
- Flyvbjerg & Budzier (1.471 proyectos de TI, mayormente grandes o públicos): sobrecosto medio de 27%. Uno de cada seis proyectos es un "Black Swan", con ~200% de sobrecosto. La distribución tiene cola larga, así que el promedio esconde los casos extremos. [verificado: https://arxiv.org/abs/1304.0265 — 2026-09-17]
- Sprints ágiles (7 proyectos open source, 19.349 ítems): al 10% de los ítems les cambian los story points. En el 57% de esos casos la estimación sube entre 58% y 100%, normalmente porque cambió el alcance. Pasuksmit et al., 2022. [verificado: https://link.springer.com/article/10.1007/s10664-022-10192-9 — 2026-09-17]
- Standish CHAOS reporta 89% de sobreesfuerzo, cifra criticada como poco fiable. Eveleens & Verhoef, IEEE Software 2010. [verificado: https://www.cs.vu.nl/~x/the_rise_and_fall_of_the_chaos_report_figures.pdf — 2026-09-17]

### Datos específicos de diseño

- **Esfuerzo de diseño estimado vs. real: desconocido.** No aparece en ningún estudio, encuesta ni informe.
- NN/g, encuesta de 2020 (n=557 profesionales UX, sin separar in-house de agencia): *"Less than a third of practitioners reported operating within a comfortable capacity… and on projects that are reasonably estimated in terms of budget and timeline."* Solo el 17% documenta su proceso de diseño. [verificado: https://www.nngroup.com/articles/designops-maturity-low/ — 2026-09-17]
- NN/g, encuesta de 2019 (n=436): para el 35%, la presión por entregar es la razón principal para saltarse el discovery. [verificado: https://www.nngroup.com/articles/discoveries-in-industry-revealed/ — 2026-09-17]
- Figma, State of the Designer 2025 (n=943, sin LatAm): el 92% de los diseñadores ve espacio de mejora en el handoff. Entre las fricciones, el 63% menciona prioridades distintas. No trae datos de horas extra ni de plazos. [verificado: https://static.figma.com/uploads/1b5e45f9a06ce51faceaae0a8669ced7b3e465dc — 2026-09-17]
- **Horas extra o crunch de diseñadores: desconocido.**

### Causas documentadas

- **Información poco clara o inestable es la causa más frecuente.** Le siguen los temas del equipo: la falta de experiencia explica el 31% de los errores de estimación en un estudio. La presión del negocio queda al final del ranking. Revisión sistemática de 82 estudios ágiles, Pasuksmit et al., 2024. [verificado: https://ar5iv.labs.arxiv.org/html/2405.01569 — 2026-09-17]
- Cambiar requisitos existentes o agregar nuevos está entre las principales causas de sobreesfuerzo. Usman et al., 2015, citado en la revisión anterior. [verificado: misma URL]
- **Anclaje:** la expectativa de otro actor tiene *"a very large impact"* en la estimación, aunque se advierta que ese número no es válido. Jørgensen & Sjøberg, 2004. [verificado: https://www.sciencedirect.com/science/article/abs/pii/S0263786303000851 — 2026-09-17] Incluso anclas poco creíbles sesgan la estimación (381 profesionales, 2015). [verificado: https://www.sciencedirect.com/science/article/abs/pii/S0164121215000618 — 2026-09-17]
- **Distorsión intencional:** en empresas grandes se suben y se bajan estimaciones a propósito (Magazinius et al., 2012). [verificado: https://www.sciencedirect.com/science/article/abs/pii/S0164121212000763 — 2026-09-17] En Glass et al. (2008), el 66% admitió haber mentido en sus predicciones. En Magazinius & Feldt (2011), era común que la gerencia pidiera estimaciones más bajas sin dar argumentos. Ambos citados en Halkjelsvik & Jørgensen, 2018. [verificado: https://link.springer.com/chapter/10.1007/978-3-319-74953-2_4 — 2026-09-17]
- **Optimismo y tareas olvidadas.** Del lado del proveedor, las causas más citadas son estimaciones sobreoptimistas (51% en una encuesta) y tareas olvidadas. Moløkken, 2004. [verificado: URL de Simula] En diseño se olvidan los estados vacíos, los errores y el handoff; fuente de agencia, Netguru. [verificado: https://medium.com/design-bootcamp/the-art-of-estimating-product-design-work-a-crash-course-8b77fca11d9a — 2026-09-17]
- **La experiencia sola no mejora la precisión.** Lo que ayuda es la práctica deliberada y usar datos documentados. Jørgensen, 2004. [verificado: https://web-backend.simula.no/sites/default/files/publications/SE.4.Joergensen.2004.c.pdf — 2026-09-17] Usar tareas similares anteriores reduce el optimismo (Halkjelsvik & Jørgensen, 2018). [verificado: https://link.springer.com/chapter/10.1007/978-3-319-74953-2_7 — 2026-09-17] En contra: no hay evidencia concluyente de que las bases de experiencia resuelvan el problema (Moløkken). [verificado: URL de Simula]

### Costo del cambio tardío

- **El "costo 100x" de Boehm tiene poco sustento.** La tabla por fases atribuida a IBM no tiene fuente rastreable. Boehm & Basili (2001) hablan de ~5:1 en proyectos pequeños. [verificado: https://budgetoverrun.com/cost-of-change-curve — 2026-09-17; fuente secundaria]
- 171 proyectos entre 2006 y 2014: *"no evidence for the delayed issue effect"*. Menzies et al., 2016. [verificado: https://arxiv.org/abs/1609.04886 — 2026-09-17]
- **Retrabajo de desarrollo por diseño incompleto o cambiado:** hay fricción reconocida, pero sin cifras (estudio de UX debt, 2023). [verificado: https://link.springer.com/article/10.1007/s11219-023-09652-2 — 2026-09-17]
- **Cómo se propaga el desvío de una fase al atraso total: desconocido.**

## 2. Cómo se estima diseño en equipos in-house

### Métodos documentados

- **Tallas de camiseta (t-shirt sizing) para UX, story points para desarrollo en el mismo equipo.** Es la práctica más común según NN/g, 2017–2019. [verificado: https://www.nngroup.com/articles/ux-user-stories/ ; https://www.nngroup.com/articles/ux-scrum/ — 2026-09-17]
- **Twitch (in-house, EE.UU., 2020):** story points solo para diseño y cuatro fases (Discover / Explore / Refine / Build), en sprints sincronizados con ingeniería. *"It takes about three sprints to get to a stable velocity."* [verificado: https://blog.twitch.tv/en/2020/07/08/design-operations-how-to-improve-visibility-and-predictability-of-design-work/ — 2026-09-17]
- **Tallas definidas por factores explícitos** (blogs individuales, así que es señal):
  - McGinn: tecnología, usuarios, pantallas y complejidad. [verificado: https://uxdesign.cc/why-some-designs-take-longer-than-others-8817e94b93e0 — 2026-09-17]
  - Walker: investigación, alcance, conocimiento previo de la solución, design system y riesgo técnico. [verificado: https://samcjwalker.substack.com/p/ux-design-effort-estimator — 2026-09-17]
  - Salam: fórmula con un colchón (buffer) de 20–25%. [verificado: https://abdussalam.substack.com/p/product-design-effort-estimation — 2026-09-17]
- **Rangos y colchón mínimo de 15%.** Friedman, orientado a proyectos con cliente. [verificado: https://smart-interface-design-patterns.com/articles/estimates/ — 2026-09-17]
- **Appetite, Shape Up.** Se fija primero el tiempo disponible y el diseño se ajusta a él. *"Estimates start with a design and end with a number. Appetites start with a number and end with a design."* [verificado: https://basecamp.com/shapeup/1.2-chapter-03 — 2026-09-17]
- **Casi no hay métodos para estimar UX antes del desarrollo.** Las barreras son organizacionales y de conocimiento. Revisión sistemática de 49 estudios, Hinderks et al., 2022. [verificado: https://www.sciencedirect.com/science/article/pii/S095058492200101X — 2026-09-17]

### Quién participa y cuándo

- **A favor de estimar con todo el equipo.** Atlassian: *"Involving everyone (developers, designers, testers…) is key"*; excluir a alguien empeora la estimación y la moral. [verificado: https://www.atlassian.com/agile/project-management/estimation — 2026-09-17] Cohn: *"The people doing the work should estimate."* [verificado: https://www.mountaingoatsoftware.com/agile/story-points/planning-poker — 2026-09-17]
- **NN/g, postura intermedia.** Muchos profesionales UX *"preferred estimating their effort separately"*. Eso *"can negatively impact team cohesion… akin to Waterfall"*, así que NN/g recomienda integrar la estimación de UX a la del equipo con el tiempo. [verificado: https://www.nngroup.com/articles/ux-user-stories/ — 2026-09-17]
- **"A single estimate for user stories does not represent UX effort well"**: estimar diseño aparte de desarrollo tiene sentido, pero hay que comparar lo estimado con lo real. Loranger, NN/g, 2018. [verificado: https://www.nngroup.com/articles/tracking-ux-capacity/ — 2026-09-17]
- **Los no diseñadores estiman mal el diseño.** *"It's clearly challenging for non-designers to create accurate design estimates."* La autora recomienda que diseño participe en los plazos desde el inicio. Shedd, blog. [verificado: https://medium.com/iq-design/demanding-design-deadlines-a-survival-guide-515eaebf3919 — 2026-09-17]
- **Caso danés (software a medida, no in-house):** los diseñadores estaban en el sprint planning, pero en dos años el modelo derivó a separar diseño *"due to market pressures"*. [verificado: https://www.sciencedirect.com/science/article/pii/S0950584922001690 — 2026-09-17]
- **Cuántos equipos estiman diseño dentro del planning: desconocido.**

### Proceso vs. capacidad

- **Apoya proceso.** Los casos in-house documentados (Twitch, McGinn) se resolvieron con visibilidad, ritos y un modelo compartido con PM e ingeniería. En el caso de McGinn, ingeniería terminó usando los tiempos de UX en sus propias estimaciones.
- **Apoya capacidad.** Hay optimismo, se olvidan estados, cuesta varios intentos llegar a precisión, y no existe un método estándar. Ojo: varias de estas fuentes vienen de agencias.
- **Ninguna fuente compara las dos causas lado a lado.** Los casos exitosos combinan método y proceso.

## 3. Herramientas y alternativas

**No encontramos ningún producto que mida el desvío de estimación de diseño por iniciativa.** Que no aparezca en búsquedas no prueba que no exista.

Precios en USD, consultados el 2026-09-17 en la página oficial salvo que se indique otra fuente.

| Producto | Para quién | Estimado vs. real | Integración Jira / Figma | Precio público | Etiqueta |
|---|---|---|---|---|---|
| Jira (base) | Equipos ágiles | Sí: estimación original / tiempo registrado / restante | Nativo; Figma vía app gratis | Free ≤10 usuarios; Standard ~$9; Premium ~$18/usuario/mes | [verificado: https://support.atlassian.com/jira-software-cloud/docs/log-time-on-an-issue/ ; precio de fuente secundaria: https://community.atlassian.com/forums/App-Central-articles/Jira-Pricing-How-Much-Does-Jira-Cost-in-2026/ba-p/3284604] |
| Tempo Timesheets / Capacity Planner | Equipos que ya usan Jira | Sí, estimación original vs. horas registradas | Nativo en Jira | Timesheets $10 (1–10 usuarios) / $5,99 (11–100); Capacity Planner: desconocido | [verificado: https://www.tempo.io/pricing] |
| Jira Product Discovery | PMs, roadmap | Solo avance por issues o story points, no esfuerzo | Nativo | Free ≤3 creadores; $10 / $25 por creador | [verificado: https://www.atlassian.com/software/jira/product-discovery/pricing] |
| Figma for Jira | Diseño y desarrollo | No (embebe diseños, JQL, automatizaciones) | Jira: sí | App gratis; Figma Professional $16 por asiento completo | [verificado: https://www.figma.com/pricing/ ; https://support.atlassian.com/jira-software-cloud/docs/integrate-figma-with-jira/] |
| Zeplin | Handoff diseño → desarrollo | No se menciona | Jira: sí | Advanced $12/asiento | [verificado: https://zeplin.io/pricing] |
| Float | Agencias, recursos | Horas planificadas vs. reales (Pro) | No aparecen | $7 / $12 por persona | [verificado: https://www.float.com/pricing] |
| Runn | Capacidad y proyectos | Planificado vs. real | Jira: no aparece | $7 / $11 por recurso, mínimo 20 | [verificado: https://www.runn.io/pricing] |
| Resource Guru | Agenda de recursos | Forecast vs. real (Blackbelt) | Jira: no aparece | $5 / $8 / $12 por persona | [verificado: https://resourceguruapp.com/pricing] |
| Asana | Gestión de trabajo general | Tiempo estimado vs. real (Advanced) | Sincronización con Jira (Advanced) | $10,99 / $24,99 | [verificado: https://asana.com/pricing] |
| ClickUp | Gestión de trabajo general | Estimaciones + registro de tiempo | desconocido | $7 / $12 (anual) | [verificado: https://clickup.com/pricing] |
| Productboard | PMs | No se menciona | Jira: sí | $19 / $59 por maker | [verificado: https://www.productboard.com/pricing/] |
| Linear | Producto e ingeniería | desconocido | desconocido | $10 / $16 | [verificado: https://linear.app/pricing] |
| Forecast.app | Servicios profesionales | desconocido | Jira: sí | desconocido (lo compró Accelo en 2025) | [verificado: https://www.accelo.com/forecast] |
| Abstract | Versionado de archivos Sketch | No | desconocido | Estado en 2026: desconocido | [verificado: https://www.goabstract.com/pricing] |

**Qué prueba y qué no:**
- **Figma for Jira y Zeplin** prueban que hay demanda por conectar diseño con Jira, no por medir esfuerzo. Una solicitud en el foro de Figma pide ver story points de Jira en FigJam (142 vistas, sin respuesta oficial). Es señal, no demanda. [verificado: https://forum.figma.com/suggest-a-feature-11/jira-issue-widget-story-points-36938 — 2026-09-17]
- **Tempo** (más de 26.909 organizaciones) prueba que se paga por comparar estimación con horas reales dentro de Jira. [verificado: https://marketplace.atlassian.com/apps/6572/timesheets-by-tempo-jira-time-tracking — 2026-09-17] No prueba que los diseñadores acepten registrar horas.
- **Float, Runn y Resource Guru** muestran que el planificado vs. real es un problema resuelto y barato. Pero están pensados para agencias y facturación, no para células de producto, y suman otra herramienta. Esa es justo la objeción de Felipe (sintético).

**Alternativas y no consumo:**
- **Tickets de diseño en Jira** con estados, spikes y links a Figma. *"For designers, Jira is rarely a choice—it's a reality."* Hay quejas de que Jira no calza con la exploración de diseño. Señal. [verificado: https://www.hackdesign.org/toolkit/jira/ — 2026-09-17]
- **Épicas de diseño con story points**, estimadas por analogía con épicas pasadas. Caso individual. [verificado: https://medium.com/@danafus/making-jira-work-for-designers-2cc7d0225a49 — 2026-09-17]
- **Correr sprints de diseño y de desarrollo en paralelo en Jira es incómodo.** Hilo con 3.142 vistas y sin respuesta. Señal. [verificado: https://community.atlassian.com/forums/DevOps-discussions/How-to-run-development-sprint-and-design-sprints-in-parallel/td-p/1448057 — 2026-09-17]
- **Planillas o nada** sería lo más común. [conocimiento del modelo — verificar]
- **Las guías de DesignOps de 2026 no nombran métricas de precisión de estimación.** Miden cosas como el tiempo desde el concepto hasta un diseño listo para desarrollo. [verificado: https://lollypop.design/blog/2026/april/what-is-design-ops-the-complete-guide-to-scaling-design-without-chaos/ — 2026-09-17]

## 4. Posicionamiento

- **El espacio lleno:** la gestión de recursos para agencias (horas, utilización, facturación) y la conexión diseño → Jira (handoff).
- **El espacio vacío:** la estimación de diseño *por iniciativa* integrada al planning de una célula de producto, con aprendizaje de estimaciones pasadas. Vacío no significa demanda: puede estar vacío porque los equipos no quieren registrar esfuerzo de diseño.

## 5. Tendencias: DesignOps, planning e IA

### DesignOps y planning

- **La madurez de DesignOps es baja, pero el dato es viejo.** NN/g 2020 (n=557): 20% con roles de DesignOps y 90% de las organizaciones en niveles 1–3. [verificado: https://www.nngroup.com/articles/designops-maturity-low/ — 2026-09-17] **Cifras 2024–2026: desconocido.**
- **Product trio estable, no creciendo.** El 62,8% trabaja en un trío en 2024 (2.º año medido), igual que en 2022. La muestra es de la audiencia de Product Talk, con sesgo reconocido por los autores. Mide participación en discovery, no en planning. [verificado: https://www.producttalk.org/2025/02/impact-of-product-trios/ — 2026-09-17]
- **Qué pedirán las empresas a diseño:** *"breadth and judgment, not just artifacts."* NN/g, State of UX 2026. [verificado: https://www.nngroup.com/articles/state-of-ux-2026/ — 2026-09-17]
- **Figma, State of the Designer 2026** (n=906, incluye LatAm): el 87% dice que tener poder de decisión mejora su desempeño. [verificado: https://www.figma.com/blog/state-of-the-designer-2026/ — 2026-09-17]

### IA en el trabajo de diseño

- **AI in Design Report 2026** (Designer Fund y Foundation Capital; más de 900 diseñadores; Q1 2026; sesgo hacia empresas tech):
  - 91% usa IA cada semana (54% en 2025) y usa 7 herramientas en promedio.
  - Las alzas por tarea están en código, wireframes y design systems. **No hay categoría de planificación ni de estimación.** [verificado: https://stateofaidesign.com/chapters/tools — 2026-09-17]
  - 65% hace más trabajo de PM o ingeniería, y 34% dice que la colaboración está *"messier"*. [verificado: https://stateofaidesign.com/chapters/teams — 2026-09-17]
- **UX Tools 2024** (n=2.220): *"75.2% of AI usage focuses on writing, documentation, and content—not visuals."* [verificado: https://www.uxtools.co/survey/ai-adoption/trends — 2026-09-17]
- **Figma AI Report 2026:** 41% dice que la IA cambió cómo colabora su equipo (7% dos años antes). Los diseñadores que hacen desarrollo pasaron de 21% a 41%. [verificado: https://www.figma.com/blog/2026-ai-report/ — 2026-09-17]

### IA para estimar

- **Jira (Rovo / Atlassian Intelligence)** no estima story points ni capacidad. "AI Work Breakdown" sugiere sub-issues sin estimarlos. [verificado: https://support.atlassian.com/organization-administration/docs/atlassian-intelligence-features-in-jira-software/ — 2026-09-17]
- **Los LLM ya predicen story points sin entrenamiento previo** (zero-shot), mejor que modelos supervisados (arXiv, marzo 2026; 16 proyectos de software). [verificado: https://arxiv.org/abs/2603.06276 — 2026-09-17]
- **Pero los story points se vuelven *"unstable in LLM-assisted workflows"*:** el esfuerzo se desplaza a validar, corregir e integrar (Frontiers in AI, 2026). No habla de diseño. [verificado: https://www.frontiersin.org/journals/artificial-intelligence/articles/10.3389/frai.2026.1772418/full — 2026-09-17]
- **IA para estimar diseño: desconocido.** No encontramos herramientas ni estudios.

### Chile y LatAm

- **Diseño en Chile 2025** (Ministerio de las Culturas; n=353; no representativo): menciona la IA, sin cifras sobre equipos in-house. [verificado: https://ec.cultura.gob.cl/mes-del-diseno-2025-presentan-estudio-que-configura-al-sector-del-diseno-en-chile/ — 2026-09-17]
- **Fuera de eso, la evidencia regional es escasa.**

---

## Impacto en creencias

Nada de esto confirma ni contradice lo que pasa en Continuum. Muestra qué tan plausible es cada creencia a la luz del mercado y cambia su prioridad para research primario. Ninguna anotación de esta tabla va a `overview.md`.

| Creencia (de overview.md)                                                                                                                                                                                  | Veredicto                                                      | Evidencia                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **1.** [opportunity] [value] El esfuerzo real de diseño supera lo planificado en ≥30% en al menos la mitad de las iniciativas, y la célula lo absorbe con horas extra, recorte o cambios a mitad de sprint | **Apoya, de forma indirecta y en otro segmento**               | En software, 61–84% de los proyectos se desvían, con 30–40% en promedio (Moløkken 2004) [verificado]. Menos de un tercio de los profesionales UX dice trabajar con plazos razonables (NN/g 2020) [verificado]. Estimado vs. real en diseño: desconocido. Horas extra: sin datos. El recorte de alcance o de discovery por presión sí aparece (NN/g 2019) [verificado].                                                                                                                                                                         |
| **2.** [opportunity] [viability] Las iniciativas con mayor desvío de diseño son las que más se atrasan y más días de desarrollo pierden                                                                    | **No dice nada, con una tensión**                              | No hay estudios sobre cómo se propaga el desvío de una fase al atraso total. Menzies 2016 no encuentra que un problema tardío cueste más, y el "100x" no tiene sustento [verificado]. Esto debilita el mecanismo supuesto, pero no lo refuta en células con sprints. Cambiar el alcance sube la reestimación entre 58% y 100% (Pasuksmit 2022) [verificado].                                                                                                                                                                                   |
| **5.** [product] [viability] La estimación de diseño se resuelve como complemento de la del PO y el TL, sin que diseño participe                                                                           | **Apoya como patrón frecuente** (no dice nada sobre Continuum) | NN/g documenta que la práctica común es estimar UX por separado y advierte de un efecto "waterfall" [verificado]. Atlassian y Cohn dicen que excluir a quien hace el trabajo empeora la estimación [verificado]. Shedd: los no diseñadores estiman mal el diseño [verificado, blog].                                                                                                                                                                                                                                                           |
| **6.** [opportunity] [value] El desvío se origina *principalmente* en que los diseñadores no tienen método ni referencias, y no solo en el recorte posterior                                               | **Mixto; contradice el "principalmente"**                      | A favor: el optimismo y las tareas olvidadas están documentados, no hay método estándar para UX (Hinderks 2022), y los datos históricos reducen el sesgo (Halkjelsvik & Jørgensen 2018) [verificado]. En contra: el anclaje y la presión para bajar estimaciones son robustos (Jørgensen 2004; Magazinius 2012; Glass 2008), y la experiencia sola no mejora la precisión [verificado]. **Hay una tercera causa, la más citada, que ninguna de las dos hipótesis incluye:** requisitos poco claros o cambiantes (Pasuksmit 2024) [verificado]. |
| **4.** [product] [value] Los diseñadores usan IA para tareas puntuales, no para gestionar el diseño end-to-end                                                                                             | **Apoya parcialmente; matiza la primera mitad**                | Ninguna encuesta registra IA para planificar o estimar diseño (AI in Design 2026; Figma 2025; UX Tools 2024) [verificado], lo que apoya el "no para gestionar". Pero "tareas puntuales" se queda corto: 91% la usa cada semana, con 7 herramientas, y 65% absorbe trabajo de PM o ingeniería [verificado].                                                                                                                                                                                                                                     |
| **3.** [product] [value] Diseño no participa en la definición del problema                                                                                                                                 | **No dice nada directamente**                                  | El 62,8% de la audiencia de Product Talk trabaja en tríos, un segmento que no se puede transferir [verificado]. Conexión indirecta: si los requisitos poco claros son la principal causa de desvío, la creencia 3 podría ser una causa de la oportunidad y no solo otra oportunidad.                                                                                                                                                                                                                                                           |
| **7.** [product] [viability] Los equipos no generan KPIs de UX                                                                                                                                             | **No dice nada** (fuera del alcance de esta corrida)           | Las guías de DesignOps de 2026 miden tiempos de flujo, no la precisión de las estimaciones [verificado]. Sobre KPIs de UX no se buscó.                                                                                                                                                                                                                                                                                                                                                                                                         |

## Qué sigue necesitando research primario

**Datos existentes (Jira), primero y más barato:**
- **Creencia 1:** % de desvío por iniciativa en los últimos 2 trimestres, más la forma de la distribución. Por Flyvbjerg, mirar la cola larga y no solo el promedio.
- **Creencia 2:** cruzar el desvío con el atraso y con las reaperturas a mitad de sprint.
- **Viabilidad del producto:** verificar si Jira registra diseño. Si no lo registra, es en sí un hallazgo sobre la viabilidad de medir.

**Encuesta a la célula (cuántos, con qué frecuencia, cuánto):**
- Cuándo y quién estima diseño: dentro del planning o después.
- Con qué frecuencia se recorta la estimación de diseño y en qué magnitud.
- Con qué frecuencia cambian los requisitos después de que diseño empezó (la tercera causa).
- Cómo se absorbe el desvío: horas extra, recorte o cambio a mitad de sprint.
- Qué referencias o método usan hoy para estimar.
- Disposición a registrar esfuerzo real, y dónde (Jira u otra herramienta).
- Uso de IA en planificación o estimación.

**Entrevistas (por qué, qué hacen hoy):**
- Cómo ocurre el recorte: si hay un ancla del PO o del TL, o una presión explícita. Distinguirlo de la falta de método.
- Cómo estiman hoy los diseñadores y qué usarían como referencia.
- Si los cambios de requisitos o del problema explican el desvío mejor que las otras dos causas.
- Qué haría que un TL y una PO aceptaran la estimación de diseño dentro de Jira y no en una herramienta aparte.
- Cómo la IA está cambiando el tipo de esfuerzo de diseño que habría que estimar.
