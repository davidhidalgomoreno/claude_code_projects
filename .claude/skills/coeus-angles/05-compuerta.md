# 05 · Compuerta de cumplimiento

**Corre siempre. Corre al final. Tiene derecho de veto.**

No es una consideración a tener en cuenta al generar: es un paso posterior con
autoridad para rechazar. Meterla dentro del prompt de generación es el fallo
clásico de estos sistemas — siempre se cuela algo, porque el mismo proceso que
busca impacto no puede ser el que lo frena.

Entrada: una pieza generada (ángulo + tesis + hooks + microcopy + brief).
Salida: dictamen, y pieza corregida o rechazada.

## Los tres veredictos

| | Significado |
|---|---|
| **PASA** | Sale tal cual. |
| **REESCRIBE** | El ángulo es válido, la formulación no. Se corrige y se vuelve a pasar por la compuerta entera, no solo por el control que falló. |
| **VETO** | El ángulo no es recuperable en este territorio. No se reescribe: se descarta y se genera otro. |

Un solo VETO tumba la pieza aunque los otros cinco controles pasen.

---

## C1 · Producto excluido

¿La pieza menciona **FitRX**? → **VETO**.

Medicamento sujeto a prescripción. Su publicidad al público general está
prohibida en España. No hay reformulación posible.

## C2 · Territorio prohibido

¿La pieza entra en **DIGESTIÓN** (hinchazón, tránsito, digestiones pesadas,
acidez)? → **VETO**.

Sin declaración autorizada de magnesio para digestión, y con riesgo añadido de
clasificación como medicamento por función: el carbonato y el hidróxido de
magnesio son antiácidos, y otras sales magnésicas actúan como laxantes
osmóticos. Ver `data/territorios-retromag.csv`.

## C3 · Declaración de propiedades saludables

La pregunta operativa: **¿qué promete la pieza que le va a pasar al cuerpo?**

Se coge esa promesa y se busca en la tabla de declaraciones autorizadas de
`03-producto/<sku>.md`.

- Está en la tabla → **PASA**
- No está, pero el ángulo funciona sin ella → **REESCRIBE** (ver regla abajo)
- No está y el ángulo se sostiene solo sobre ella → **VETO**

Territorios sin declaración autorizada de magnesio, comprobados: **sueño,
digestión, salud cardiovascular**. Los tres aparecen hoy en anuncios vivos.

### La regla de reescritura

> **El dolor se nombra. La promesa se ancla.**

Describir el síntoma que vive el usuario **no es una declaración de salud**: es
su experiencia. Prometer que el producto lo resuelve, sí lo es.

| Se puede | No se puede |
|---|---|
| *«Te despiertas a las 3 y ya no vuelves a dormir»* | *«Duerme del tirón»* |
| Cerrar en sistema nervioso, función psicológica o fatiga | Cerrar en sueño, digestión o corazón |

La reescritura casi siempre consiste en **dejar intacto el hook y cambiar el
remate**. Si al cambiar el remate el ángulo se cae, no era un ángulo: era una
promesa.

## C4 · Trazabilidad de cifras y activos

Toda cifra, porcentaje, certificación, credencial y nombre propio tiene que
existir en `03-producto/<sku>.md`. Si no está ahí, no está verificado.

- Cifra sin fuente → **REESCRIBE**, se retira la cifra
- Sello o certificación sin certificado localizado → **REESCRIBE**
- Dato del §5 del calendario editorial (caída de NAD+, edad biológica del
  fundador, audiencia, «más avanzada de Europa») → **REESCRIBE**, se retira

Nunca se sustituye una cifra sin fuente por otra aproximada. Se quita.

## C5 · Política de plataforma (Meta)

Verificado contra el Centro de Transparencia de Meta. Tres controles:

1. **Autopercepción negativa.** Meta prohíbe el contenido que implique o
   intente generar una percepción negativa de uno mismo para promocionar
   productos de salud. En retroaging el riesgo es de manual: convertir
   envejecer en un defecto a corregir. → **REESCRIBE**
2. **Antes y después.** Restringido en salud, y explícitamente en tratamientos
   antienvejecimiento y de arrugas. Aplica también a primeros planos que
   señalan una parte del cuerpo como problema. → **REESCRIBE el brief visual**
3. **Lenguaje sensacionalista o promesa milagro.** → **REESCRIBE**

**Segmentación por edad:** la regla de 18+ para productos de salud tuvo una
actualización en julio de 2026 por la que vitaminas y suplementos pueden correr
sin restricción de edad salvo que reclamen pérdida o ganancia de peso. Retromag
no reclama peso. *Confirmar la configuración vigente en el centro de políticas
antes de montar la campaña — esta regla ha cambiado recientemente y puede
volver a cambiar.*

## C6 · Prohibiciones específicas de COEUS

De `03-producto/<sku>.md`. Todas son **REESCRIBE**.

| Control | Qué se busca |
|---|---|
| Función por sal | *«Cinco magnesios para cinco cosas»*. Sin respaldo documental. |
| Origen de ingredientes | Sugerir magnesio español. La ficha dice que todos son de fuera de la UE. |
| Declaración general suelta | *«Más de 300 funciones»* sin declaración autorizada al lado (art. 10.3 del Reglamento 1924/2006). |
| Velocidad de efecto | *«Desde la primera semana»*, *«en X días»*. |
| Contradicción interna | Presentar el carbonato como sal de alta absorción mientras se ataca a las formas baratas. |
| Dosis como argumento | Hasta confirmar el máximo vigente de AESAN. |

---

## Registro

Cada pieza que pasa por la compuerta deja una fila en
`data/registro-compuerta.csv`: fecha, pieza, control que falló, veredicto y
acción. Sin registro no hay forma de saber si el motor está mejorando o si
estamos corrigiendo lo mismo una y otra vez.

---

## Límite de esta compuerta

Esto es control de calidad, **no asesoría legal**. Detecta lo que sabemos que
está mal y evita que se propague a escala. No sustituye la revisión de un
profesional antes de publicar, especialmente en la redacción literal de las
declaraciones, que se toma del registro comunitario y no de estos archivos.
