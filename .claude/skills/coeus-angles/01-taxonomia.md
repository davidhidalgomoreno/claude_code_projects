# 01 · Taxonomía de ángulos — COEUS

Diccionario del sistema. Todo lo que el motor genere se etiqueta con estos tres
ejes. Si un ángulo no encaja en ninguno, no se fuerza: se abre una propuesta de
código nuevo y se decide fuera del motor.

**Origen:** ingeniería inversa sobre 61 anuncios del *COEUS – Content Grid Paid
Media*. Los códigos `FALC`, `PUDO` y `DDIA` son originales de COEUS y se
conservan. El resto sustituye a `OBCS`, que se retira.

---

## Por qué tres ejes y no uno

La nomenclatura original mezclaba tres cosas distintas en dos campos. `OBCS`
agrupaba 26 de 61 anuncios (43 %) y dentro convivían un momento de funnel
(«Ya viste X»), dos ángulos reales (coste comparado, escepticismo) y un formato
de producción (fundador a cámara). Un código así no se puede medir: al cruzarlo
con datos de Meta, su rendimiento medio promedia cosas que no se parecen.

```
ÁNGULO          ×   FORMATO          ×   MOMENTO
qué palanca         cómo se produce      a quién le habla
mental usa          la pieza             según lo que ya sabe
```

Los tres son independientes. Un mismo ángulo se puede rodar como fundador a
cámara o como voz en off, y servirse en frío o en retargeting.

---

## EJE 1 · ÁNGULO

### Códigos originales confirmados

| Código | Palanca | Test de pertenencia |
|---|---|---|
| `FALC` | **Falsa creencia de mecanismo.** Corrige lo que el usuario cree que hace una cosa. | ¿La pieza dice *«X no hace lo que crees que hace»*? |
| `PUDO` | **Punto de dolor vivido.** Describe la escena del dolor sin corregir ninguna creencia. | ¿Podría contarlo el usuario en primera persona sin aprender nada nuevo? |
| `DDIA` | **Lo que el sistema sanitario no cubre.** El espacio entre tratar una patología y gestionar el día a día. | ¿Nombra explícitamente al médico, la consulta o la analítica como algo válido pero insuficiente? |

`FALC` y `PUDO` se confirmaron contra 29 piezas de copy sin una sola excepción.
`DDIA` se confirmó contra 1 de sus 2 piezas; la otra estaba mal etiquetada y se
ha remapeado a `VENT`.

### Códigos nuevos que sustituyen a OBCS

| Código | Palanca | Test de pertenencia |
|---|---|---|
| `ESCE` | **Escepticismo de categoría.** *«Ya lo probé —producto o hábito— y no funcionó.»* | ¿Arranca reconociendo un intento previo fallido del usuario? |
| `FRAG` | **Fragmentación de la solución.** Un bote por síntoma, o un ingrediente que no cubre todos los frentes. | ¿El argumento es que faltan piezas, no que la pieza sea mala? |
| `COST` | **Coste comparado.** Ancla el precio contra un gasto que el usuario ya acepta sin pensarlo. | ¿Aparece una cifra en euros comparada con otra cifra en euros? |
| `SILE` | **Lo que no se cuenta.** Territorio de silencio, tabú o resignación normalizada. | ¿La pieza da permiso a nombrar algo que el usuario calla? |
| `GENE` | **Contraste generacional.** Lo que la generación anterior aguantó porque no tenía opción. | ¿Compara explícitamente con una generación previa? |
| `VENT` | **Ventana de actuación.** Actuar mientras todavía hay margen, no cuando ya duele. | ¿Se dirige a alguien que *ahora mismo está bien*? |

### Códigos nuevos de la capa marca

Incorporan a paid el material que hoy solo vive en orgánico y es el que más se
guarda y se envía.

| Código | Palanca | Test de pertenencia |
|---|---|---|
| `CRIT` | **Criterio de etiqueta.** Enseña a leer y comparar antes de comprar: extracto vs. planta molida, relación de extracción, forma biodisponible, ingrediente patentado con ensayos. | ¿El usuario sale sabiendo evaluar cualquier bote, incluido uno que no sea nuestro? |
| `RETR` | **Retroaging® como protocolo.** Anti-aging describe un deseo; Retroaging® tiene entrada, proceso y salida verificable. Medir antes de suplementar. | ¿La pieza defiende el método por encima del producto? |

`CRIT` es el ángulo de mayor alcance orgánico de COEUS y tenía **cero presencia
en paid** antes de esta taxonomía. Es la principal vía de entrada en frío del
sistema. Su regla de oro: si la pieza deja de ser útil cuando quitas la marca,
no es `CRIT`.

### Códigos retirados

| Retirado | Motivo | Destino |
|---|---|---|
| `OBCS` | 43 % del inventario sin definición común. Mezclaba momento, ángulo y formato. | Repartido entre `ESCE`, `FRAG`, `COST`, `FALC`, `CRIT`, `SILE`, `RETR` y el eje MOMENTO. |
| `PRIN` | n=3 sin patrón interno común. | 2 piezas → `SILE`. 1 pieza → `FRAG`. |
| `EXPA` | n=1. Un solo anuncio no es una categoría. | → `GENE`, que generaliza la palanca. |

---

## EJE 2 · FORMATO

**Estado: pendiente de racionalizar. No inventar códigos aquí.**

Los códigos originales (`EDUC`, `TEST`, `FUND`, `UVTH`, `ESTA`, `PASO`, `EBAD`)
se conservan **literalmente** para no romper el histórico. Mezclan estructura
narrativa, formato de producción y mecanismo persuasivo, pero racionalizarlos
exige ver los creativos montados, no solo el copy. `EBAD` ya no aporta señal
propia: su contenido se ha absorbido en el ángulo `COST`.

Único código con lectura firme desde el copy:

- `FUND` — pieza en primera persona de una figura identificada con credencial.
  Confirmado en 4 de 4 piezas.

---

## EJE 3 · MOMENTO

Sustituye al uso implícito de TOFU/MOFU/BOFU como si fueran ángulos.

| Código | A quién le habla |
|---|---|
| `FRIO` | No conoce el problema, o no lo ha nombrado todavía. |
| `CONS` | Conoce el problema y está evaluando soluciones. |
| `RETG` | Ya ha visto la marca y no ha comprado. |

`RETG` no es un ángulo. Una pieza de retargeting **siempre lleva además un
ángulo del eje 1**: la razón por la que no compró.

---

## Nomenclatura de archivo

```
VID – MOMENTO – FORMATO – ÁNGULO – MesAA – slug
```

Ejemplo: `VID–RETG–TEST–ESCE–Sep26–Ya viste MePausa`

El campo funnel desaparece: lo absorbe MOMENTO. El orden de los campos se
mantiene para que los exports de Meta sigan siendo parseables por posición.

---

## Distribución tras el remapeo

Sobre los 60 anuncios clasificables (1 excluido por ser FitRX):

| Ángulo | n | % |
|---|---|---|
| `FALC` | 24 | 40 % |
| `ESCE` | 6 | 10 % |
| `PUDO` | 12 | 20 % |
| `FRAG` | 5 | 8 % |
| `COST` | 4 | 7 % |
| `CRIT` | 2 | 3 % |
| `SILE` | 3 | 5 % |
| `RETR` | 1 | 2 % |
| `VENT` | 1 | 2 % |
| `DDIA` | 1 | 2 % |
| `GENE` | 1 | 2 % |

**Lectura para el motor.** `FALC` + `PUDO` concentran el 60 % del inventario.
Es un territorio validado y no hay que abandonarlo, pero cualquier lote que
genere el sistema con más del 50 % en esos dos códigos está reproduciendo la
concentración existente en lugar de ampliarla. `CRIT` y `RETR` están
infrarrepresentados respecto a su rendimiento orgánico conocido.

---

## Reglas duras

1. **Un ángulo por pieza.** Si hay dos, la pieza está sin decidir. Se admite un
   ángulo secundario anotado, nunca dos primarios.
2. **`RETG` nunca va solo.** Siempre acompañado de un ángulo del eje 1.
3. **Ningún código con n<5 entra en el cálculo de rendimiento.** Se etiqueta,
   se acumula y se deja fuera de las medias hasta llegar a 5 piezas.
4. **FitRX queda fuera del sistema.** Medicamento sujeto a prescripción: su
   publicidad al público general está prohibida en España. No se etiqueta, no
   se genera, no entra en las medias.
5. **Los códigos no se renombran.** Añadir sí, renombrar rompe el histórico.
