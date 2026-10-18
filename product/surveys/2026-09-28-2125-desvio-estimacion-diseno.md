---
opportunity: desvio-estimacion-diseno
status: ready
date: 2026-09-28
language: es
---

# Encuesta: desvío de estimación de diseño en las células

- **Objetivos de aprendizaje:**
  1. **Magnitud y absorción del desvío** (creencias 1 y 2). ¿Con qué frecuencia el diseño toma más de lo planificado, cuánto más, y cómo lo absorbe la célula? → *Decide si seguimos, descartamos o reformulamos la oportunidad.* La encuesta mide percepción. El dato duro sale de Jira, que todavía no se revisa, así que no lo reemplaza.
  2. **Proceso: cuándo y quién estima diseño** (creencia 5, causa «proceso»). ¿Diseño estima dentro del planning o después? ¿Con qué frecuencia y en cuánto se recorta su estimación? → *Decide si las ideas apuntan a integrar la estimación de diseño en el planning.*
  3. **Capacidad vs. requisitos cambiantes** (creencia 6 y la «tercera causa» del research del 2026-09-17). ¿Con qué estiman hoy los diseñadores? ¿Con qué frecuencia cambia el problema cuando diseño ya empezó? → *Decide si hace falta método o referencias históricas, o si el problema está antes del diseño (conecta con la creencia 3).*
  4. **Dónde viviría el registro** (viabilidad de medir). ¿Dónde queda hoy el esfuerzo real de diseño y dónde miran PO y TL el avance? → *Decide entre una capa sobre Jira y una app aparte.*
- **Respondentes:** diseñadores/as, Product Owners y Tech Leads de las células de producto de Continuum que trabajaron en iniciativas del roadmap con diseño en los últimos 3 meses. Queda fuera cualquier otro rol, incluidas las áreas que piden piezas sueltas (persona negativa: Patricia Vergara).
- **Largo estimado:** 2 preguntas de filtro, 11–12 sustantivas según el rol, 2 demográficas y el bloque de opt-in. Unos 6 minutos.
- **Límite conocido:** no hay trabajo cualitativo real todavía. Las opciones de respuesta salen de las personas sintéticas y del research secundario, y todas las preguntas de opción tienen «Otro» o «No sé».

---

**Texto de introducción (para el respondente):**
> Queremos entender cómo se estima y cómo avanza el trabajo de diseño en las células. Toma unos 6 minutos. Es anónima: los resultados se reportan agregados, nunca por persona ni por célula, y no se usan para evaluar a nadie. Si al final aceptas una conversación, tu contacto se usa solo para coordinarla.

## Filtro

S1. ¿Cuál es tu rol principal en tu célula? [opción única]
   - Diseñador/a
   - Product Owner
   - Tech Lead
   - Otro → fin de la encuesta
   > Objetivo: filtro y corte por rol (todos los objetivos)

S2. En los últimos 3 meses, ¿participaste en al menos una iniciativa del roadmap que incluyera trabajo de diseño? [opción única]
   - Sí
   - No → fin de la encuesta
   > Objetivo: filtro (solo responde quien tiene experiencia reciente)

## Preguntas

### A. Lo que pasó en las iniciativas recientes

Q1. Piensa en la iniciativa más reciente con trabajo de diseño que ya pasó a desarrollo. Comparado con lo que se había planificado, el diseño tomó… [opción única]
   - Menos de lo planificado
   - Más o menos lo planificado
   - Hasta un 30% más
   - Entre un 30% más y el doble
   - Más del doble
   - No había una estimación de diseño
   - No sé
   > Objetivo 1. Magnitud anclada en un caso concreto y reciente. El corte en 30% calza con el umbral de la creencia 1.

Q2. En los últimos 3 meses, de las iniciativas con diseño en las que participaste, ¿en cuántas el diseño tomó un 30% más de lo planificado, o más? [opción única]
   - Ninguna
   - Menos de la mitad
   - Alrededor de la mitad
   - Más de la mitad
   - Todas
   - No sé
   > Objetivo 1. Frecuencia: prueba directamente la parte «en al menos la mitad» de la creencia 1.

Q3. *(Se muestra si Q2 ≠ «Ninguna»)* En esas iniciativas, ¿qué ocurrió? Marca todas las que correspondan. [opción múltiple]
   - Diseño trabajó fuera de horario
   - Se dejó fuera parte del diseño (estados, casos borde, validación con usuarios)
   - Se recortó el alcance de la funcionalidad
   - Hubo cambios de diseño con el sprint de desarrollo en curso
   - Se movió la fecha comprometida
   - Nada de lo anterior
   - Otro: ____
   > Objetivo 1 (cómo lo absorbe la célula) y creencia 2 (fecha, cambios a mitad de sprint)

Q4. *(Solo PO y TL)* En los últimos 3 meses, ¿cuántos días de desarrollo calculas que perdió tu célula por cambios de diseño con el sprint en curso? [opción única]
   - Ninguno
   - 1 a 2 días
   - 3 a 5 días
   - 6 a 10 días
   - Más de 10 días
   - No sé
   > Objetivo 1 / creencia 2. Métrica secundaria de la oportunidad (costo evitado). La cifra sintética de Felipe es 3–5 días por iniciativa.

### B. Cómo se estima

Q5. En tu célula, ¿cuándo se define normalmente la estimación de diseño de una iniciativa? [opción única]
   - Diseño la prepara antes y se discute en el planning
   - Se estima en el planning, junto con desarrollo
   - Se define después del planning, cuando PO y TL ya cerraron la suya
   - No hay estimación de diseño explícita: el diseño se ajusta a la fecha disponible
   - Cambia mucho de una iniciativa a otra
   - No sé
   > Objetivo 2. Mide la creencia 5 (diseño como complemento, fuera del planning).

Q6. En los últimos 3 meses, ¿con qué frecuencia la estimación que propuso diseño se redujo antes de empezar el trabajo? [likert-5 de frecuencia]
   - Nunca · Rara vez · A veces · Frecuentemente · Siempre
   - (fuera de escala) Diseño no propone una estimación / No sé
   > Objetivo 2. Frecuencia del recorte (causa «proceso»).

Q7. *(Se muestra si Q6 es «Rara vez» o más)* Cuando se reduce, ¿en cuánto se reduce normalmente? [opción única]
   - Menos de un 20%
   - Entre 20% y 40%
   - Entre 40% y 60%
   - Más de un 60%
   - No sé
   > Objetivo 2. Magnitud del recorte (la cifra sintética de Camila es cerca de la mitad).

### C. Por qué se desvía

Q8. En los últimos 3 meses, ¿con qué frecuencia cambió el problema o los requisitos de una iniciativa cuando diseño ya había empezado? [likert-5 de frecuencia]
   - Nunca · Rara vez · A veces · Frecuentemente · Siempre
   - (fuera de escala) No sé
   > Objetivo 3. La tercera causa, la más citada en la literatura (Pasuksmit 2024).

Q9. *(Solo diseñadores/as)* ¿En qué te basas hoy para estimar el diseño de una iniciativa? Marca todas las que correspondan. [opción múltiple]
   - Mi intuición o experiencia
   - Comparo de memoria con iniciativas parecidas
   - Un registro de lo que tomaron iniciativas anteriores (horas o puntos reales)
   - Un método o plantilla (tallas, factores, fórmula, colchón)
   - Me ajusto a la fecha o al plazo disponible
   - Le pregunto a otro diseñador/a
   - Una herramienta de IA
   - Otro: ____
   > Objetivos 3 (capacidad: método y referencias) y 4 (uso de IA para estimar)

Q10. De estas razones, ordena de más a menos las que explican que el diseño tome más de lo planificado en tu célula. [ranking, 5 ítems, no obligatoria]
   - El problema o los requisitos no están claros o cambian
   - Diseño no decide su propia estimación (se la reducen o le fijan el plazo)
   - Falta método o referencias para estimar diseño
   - Al estimar se olvidan tareas (estados vacíos, errores, handoff)
   - Pedidos fuera del roadmap que interrumpen el sprint
   > Objetivo 3. Opinión, va después de las preguntas de conducta. Compara las causas lado a lado, que es justo lo que ninguna fuente secundaria hace.

### D. Dónde queda registrado

Q11. *(Solo diseñadores/as)* Hoy, ¿dónde queda registrado el esfuerzo real de diseño de una iniciativa? Marca todas las que correspondan. [opción múltiple]
   - Jira (horas, puntos o subtareas de diseño)
   - Una planilla
   - Notion
   - Otra herramienta: ____
   - No queda registrado
   - No sé
   > Objetivo 4. Complementa la revisión de Jira del paso 1 de la agenda.

Q12. *(Solo PO y TL)* ¿Dónde revisas el avance y los plazos de las iniciativas de tu célula? Marca todas las que correspondan. [opción múltiple]
   - Jira
   - Una planilla
   - Un dashboard (por ejemplo, Power BI)
   - En las ceremonias o reuniones de la célula
   - Otro: ____
   > Objetivo 4. Dónde tendría que aparecer la estimación de diseño para que PO y TL la vean (creencia de Felipe: «en Jira o nada»).

### E. Abierta

Q13. Piensa en la última vez que el diseño de una iniciativa tomó más de lo planificado. ¿Qué pasó? [abierta, opcional]
   > Objetivos 1 y 3. Se codifica por causa y por forma de absorción. Da citas para el sponsor y candidatos para entrevistar.

### F. Sobre ti

D1. ¿Cuántos años de experiencia tienes en tu rol actual (en Continuum o antes)? [opción única]
   - Menos de 2 · 2 a 5 · 6 a 10 · Más de 10
   > Objetivo 3. Corte junior/senior: ¿los diseñadores con menos experiencia se desvían más? El research dice que la experiencia sola no mejora la precisión.

D2. ¿En qué célula trabajas? [lista de células, opcional]
   > Meta de cobertura por célula y cruce de roles dentro de una misma célula. Es opcional porque con un diseñador por célula identifica a la persona. Si pocos la responden, la meta se mide sobre el total por rol.

## Filtro + opt-in (reclutamiento para entrevistas)

R1. ¿Llevas al menos 3 meses en tu célula actual y participaste en su planning en ese período? [sí / no]
   → No es candidato si responde «No»

R2. ¿Aceptarías una conversación de 30 minutos sobre cómo se estima y se planifica el diseño en tu célula? [sí / no]

R3. *(Solo si R2 = sí)* ¿Cómo te contactamos? [abierta, opcional: nombre y correo o Slack]
   > Prioridad para entrevistar: quienes contradicen las creencias (por ejemplo, Q2 = «Ninguna», Q6 = «Nunca» o Q10 con otra causa en primer lugar) y quienes, dentro de una misma célula, ven distinto el mismo desvío.

## Distribución

| Canal | A quién llega y su sesgo | Alcance aprox. | Link |
|---|---|---|---|
| Canal Slack de diseño de Continuum (lo publica Pancho) | Diseñadores/as de célula (Camila, Matías). **Sobrerrepresenta** a quienes están activos en el canal y a quienes tienen el dolor fresco. Como lo convoca el Design Lead, puede haber deseabilidad social: más ganas de mostrar el problema o de no quedar mal estimando. **Subrepresenta** a quienes no siguen el canal. No llega a PO ni a TL. | unknown | `…?canal=slack-diseno` |
| Correo o Teams de Tamara Sancy (Head of Product) a PO y TL | Product Owners (Andrea) y Tech Leads (Felipe). El respaldo de la Head of Product sube la tasa de respuesta. **Sesgo:** al ser el sponsor, PO y TL pueden informar menos desvío para cuidar a su célula, y los TL escépticos pueden no responder. Si la lista incluye diseñadores, S1 los separa y el link dice por dónde llegaron. | unknown | `…?canal=head-product` |

- **Meta de n:** por rol (diseño, PO, TL), respuestas de al menos el 70% de las células. Con 10 a 30 células son entre 7 y 21 respuestas por rol. Todo queda **por debajo de 30 por rol, así que los resultados son direccionales**: se reportan como patrones, no como porcentajes con precisión.
- **Chequeo de alcance:** el alcance de los dos canales es unknown. Si hay más o menos una persona por rol en cada célula, la meta exige una tasa de respuesta cercana al 70%, alta para una encuesta voluntaria. **Antes de publicar:** completar el alcance real de cada canal. En la primera revisión, si falta cobertura, mandar un recordatorio en Slack, pedir a Tamara un segundo envío y, como último recurso, abrir 6 minutos en la ceremonia de diseño (con un link aparte: `…?canal=ceremonia`).
- **Primera revisión:** lunes 2026-10-05
- **Cierre:** viernes 2026-10-16, o antes si se llega a la meta en los tres roles.
