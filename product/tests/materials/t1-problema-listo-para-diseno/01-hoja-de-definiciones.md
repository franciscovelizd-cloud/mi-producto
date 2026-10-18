# T1 · Hoja de definiciones

**Test:** T1 de `product/tests/2026-10-17-1210-desvio-estimacion-diseno.md`, revisión retrospectiva de 10 iniciativas.
**Fijada el:** ____ / ____ / 2026. Se fija **antes de abrir cualquier iniciativa** y no se cambia durante el test. Si algo resulta ambiguo a mitad de camino, se anota en "Casos dudosos" al final y se resuelve con la regla tal como está escrita. Si una definición cambia, se registra en `product/corrections.md` con la razón.

Esta hoja la usan los dos clasificadores. **No se muestra a los diseñadores ni a las PO entrevistadas.**

---

## 1. Ítems del criterio de entrada

| # | Ítem | Qué cubre |
|---|---|---|
| 1 | **Reglas de negocio validadas** | Las reglas que el producto tiene que aplicar: cálculos, condiciones, montos, quién puede hacer qué, estados. |
| 2 | **Requisitos de legal o compliance validados** | Lo que piden legal, compliance, privacidad o la normativa: textos obligatorios, consentimientos, datos que se pueden o no mostrar o pedir. |
| 3 | **Alcance validado** | Qué entra y qué no entra en la iniciativa: flujos, casos, canales, segmentos de usuario. |
| 4 | **Diseño participó en la definición del problema** | Si diseño estuvo en la definición del problema antes de comprometer la estimación. |

**Validado (con registro):** existe un registro fechado **antes del inicio del diseño** (ticket de Jira, página de Confluence, acta, correo) en el que quien responde por esa definición la da por buena: negocio para las reglas, legal o compliance para sus requisitos, la PO o el sponsor para el alcance. Un acuerdo verbal sin registro, o un registro que no se encuentra, cuenta como **no validado**.

> Sobre el ítem 4: por la definición de la sección 2, lo que cambia siempre es una regla, un requisito o el alcance. Por eso cada cambio se asigna a uno de los ítems 1 a 3, o a "Ninguno".

## 2. Cambio de requisitos con el diseño iniciado

Cuenta como cambio solo si cumple **las tres** condiciones:

1. Cambió una **regla, un requisito o el alcance** de la iniciativa.
2. Se pidió **después de que empezó el diseño**.
3. **Obligó a rehacer trabajo de diseño** que ya estaba hecho.

No cuentan como cambio:
- un ajuste que no tocó trabajo de diseño ya hecho, por ejemplo algo que se agregó antes de diseñar esa parte;
- una corrección de diseño que no viene de un cambio de regla, requisito o alcance, como un error de diseño o un ajuste visual;
- algo pedido antes del inicio del diseño.

**Inicio del diseño:** la fecha en que empezó el trabajo de diseño de la iniciativa. Se toma de Jira (el primer ticket de diseño que pasa a "en curso"). Si Jira no lo registra, se usa la fecha que den el diseñador y la PO, y se anota esa fuente.

## 3. Detectable o no detectable

Un cambio es **detectable** si se cumplen **las dos** condiciones:

- **(a)** lo que cambió corresponde a un ítem del criterio (1, 2 o 3), **y**
- **(b)** ese ítem **no estaba validado con registro** cuando empezó el diseño.

Es **no detectable** en todos los demás casos, en particular:
- el ítem sí estaba validado con registro y aun así cambió;
- lo que cambió no corresponde a ningún ítem;
- el cambio **nace de pruebas con usuarios**;
- el cambio nace de **información que no existía al inicio del diseño**, por ejemplo una norma publicada después o una decisión de negocio tomada por un hecho posterior.

Las exclusiones mandan: un cambio que nace de pruebas con usuarios es no detectable aunque el ítem no estuviera validado.

### Ejemplos (ficticios, solo para ilustrar la regla)

| Cambio | Ítem | ¿Validado al inicio? | Origen | Clasificación |
|---|---|---|---|---|
| Negocio cambia la condición para acceder a un descuento; no había registro de la regla antes de diseñar | 1 Reglas | No | Negocio lo redefine | **Detectable** |
| Legal pide un texto de consentimiento nuevo; el requisito de legal estaba aprobado por correo antes del inicio | 2 Legal | Sí | Legal lo revisa de nuevo | No detectable |
| En una prueba con usuarios nadie encuentra un paso y se rehace el flujo | 3 Alcance | No | Prueba con usuarios | No detectable |
| Se agrega un canal nuevo que no estaba en ningún documento de alcance | 3 Alcance | No | La PO lo pide | **Detectable** |
| Sale una circular regulatoria después del inicio y obliga a cambiar un campo | 2 Legal | No | Información que no existía | No detectable |
| Tech avisa que una integración no entrega un dato y se rehace el formulario | Ninguno | — | Pedido o redefinición | No detectable |

## 4. Cómo se eligen las 10 iniciativas

1. Solo iniciativas **cerradas**.
2. Con **desvío de diseño**: el esfuerzo real de diseño fue un 30% mayor que lo planificado, o más. La fuente es Jira; si Jira no lo registra, se usa lo que digan el diseñador y la PO, y se anota esa fuente.
3. Se recorren **hacia atrás en el tiempo**, desde la más reciente, **sin saltarse ninguna** que cumpla 1 y 2, hasta llegar a 10.
4. La lista se **cierra y se fecha antes de revisar cualquier cambio**. Después no entra ni sale ninguna iniciativa.

## 5. Cómo se clasifica

1. Pancho reúne los hechos de cada cambio a partir de los documentos y las entrevistas: qué cambió, cuándo, quién lo pidió, de dónde salió y qué se rehízo. Los anota en la planilla.
2. Cada clasificador, **por separado y sin ver la clasificación del otro**, decide para cada cambio: el ítem, si estaba validado al inicio (con la fuente) y si es detectable o no detectable. Para el ítem y la validación mira **solo cómo estaban los documentos cuando empezó el diseño**, no lo que se supo después.
3. Se juntan las dos clasificaciones en la planilla. El **acuerdo inicial** se calcula en ese momento, antes de conversar.
4. Los desacuerdos se resuelven conversando, con esta hoja como referencia. El resultado queda como clasificación final, con una nota de cómo se resolvió.

## Casos dudosos

Anotar aquí cada caso que esta hoja no resolvió con claridad, cómo se aplicó la regla y quién lo decidió.

| Fecha | Cambio (ID) | Duda | Cómo se aplicó la regla |
|---|---|---|---|
| | | | |
