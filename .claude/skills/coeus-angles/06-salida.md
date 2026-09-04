# 06 · Formato de salida

Unidad mínima del sistema: **un ángulo que un editor o un creador puede
ejecutar sin volver a preguntar**. Ni una idea suelta ni un guion cerrado.

Toda pieza sale con estos once campos. Si falta uno, no está terminada.

```
1  ID                  nomenclatura JL/AG completa
2  CELDA               ángulo × territorio de dolor
3  AVATAR + AWARENESS   de 02-avatares.md
4  TESIS               una frase. Qué cree hoy y qué debería creer
5  HOOKS               tres alternativas, no una
6  CUERPO              estructura narrativa en bloques
7  CIERRE AUTORIZADO   la declaración concreta con la que remata
8  MICROCOPY           texto en pantalla
9  BRIEF DE RODAJE     plano, talento, duración, tono
10 HIPÓTESIS MEDIBLE   qué esperamos y contra qué se compara
11 VEREDICTO           dictamen de 05-compuerta.md
```

**Campo 10, la regla que evita el vertedero de creatividades.** Cada pieza dice
por adelantado qué espera batir y con qué métrica. Sin hipótesis previa siempre
se encuentra un número que subió.

**Campo 7, el que no se negocia.** Si el cierre no sale de la tabla de
declaraciones autorizadas de `03-producto/<sku>.md`, la pieza no sale.

---

## Ejemplo completo — celda prioritaria `CRIT × TENSIÓN`

Generado por el sistema y pasado por la compuerta. Sirve de patrón.

**1 · ID**
`CX001/26_Video Ad_RETROMAG_TOFU_Solution Aware_MUJER MEDIANA EDAD_CRIT_TENSION_PROBLEM/SOLUTION_Diego`

**2 · CELDA** — `CRIT` × TENSIÓN. Ángulo ganador (1,54) aplicado al territorio
de riesgo bajo con cero cobertura. Explotación de ángulo, exploración de
territorio.

**3 · AVATAR + AWARENESS** — Mujer de mediana edad (1,72) · Solution Aware
(1,45). Ya toma magnesio o lo ha tomado. No sabe que hay formas distintas.

**4 · TESIS** — Cree que la mandíbula apretada es estrés y que no tiene
solución. Debería creer que lleva meses tomando una forma de magnesio que su
cuerpo apenas aprovecha, y que eso se lee en la etiqueta antes de pagar.

**5 · HOOKS**
- A · *«Si en tu bote de magnesio pone óxido, tu cuerpo apenas lo aprovecha.»*
- B · *«Te levantas con la mandíbula cargada y llevas dos años pensando que es solo estrés.»*
- C · *«Hay una palabra en la etiqueta que decide si ese bote sirve o no. Y no es magnesio.»*

**6 · CUERPO** — Problem/Solution, la estructura mejor colocada de la cuenta.
1. La escena: despertarse con la mandíbula tensa, la cara cargada.
2. La invalidación: probaste magnesio y no notaste nada.
3. El mecanismo: no todas las sales se absorben igual; el óxido es la barata.
4. El criterio: qué mirar en la etiqueta — la sal, no el nombre del mineral.
5. El producto: cinco sales, entre ellas bisglicinato. Cantidad declarada y
   comparable, 279,60 mg por toma, 74,57 % del VRN.

**7 · CIERRE AUTORIZADO** — *«El magnesio contribuye al funcionamiento normal
del sistema nervioso y al funcionamiento normal de los músculos.»* Ambas
autorizadas por el Reglamento (UE) 432/2012 y disponibles porque el producto es
alto contenido en magnesio.

**8 · MICROCOPY** — *«Mira la sal, no el nombre.»*

**9 · BRIEF DE RODAJE** — Vídeo (1,57 frente a 1,11 del estático). Talking head
vertical, Diego. 30–40 s. Bote real en mano con la etiqueta legible en el bloque
4. Sin primeros planos de la mandíbula ni de la cara: eso entra en el control de
autopercepción negativa. Tono explicativo, no alarmista.

**10 · HIPÓTESIS MEDIBLE** — El ángulo `CRIT` mantiene su rendimiento fuera del
sueño. Se compara contra el CPA de `VILLANO_MAGNESIO BARATO` (26,72 €) con al
menos 250 € de reparto. Por encima de 40 € se refuta y se cierra el territorio.

**11 · VEREDICTO DE COMPUERTA** — **PASA.**
C1 sin FitRX · C2 territorio TENSIÓN permitido · C3 cierre en tabla autorizada ·
C4 las dos cifras salen de la ficha técnica · C5 sin promesa milagro, sin
antes/después, sin primeros planos del cuerpo · C6 no atribuye función a una
sal concreta, no menciona origen, no promete plazos.

---

## Nomenclatura para piezas nuevas

Se mantiene la convención `JL/AG` de la cuenta, insertando el código de ángulo
en el campo de territorio:

```
<ID>_<Formato>_<SKU>_<Funnel>_<Awareness>_<Avatar>_<ANGULO>_<TERRITORIO>_<Estructura>_<Talento>
```

Un código de ángulo por pieza. `RETG` nunca va solo. Ver `01-taxonomia.md`.

---

## Antes de entregar el lote

- ¿Menos del 50 % en `FALC` + `PUDO`? Si no, el lote reproduce el inventario.
- ¿Hay 30 % en territorios sin cobertura (FOCO, TENSIÓN, RENDIMIENTO)?
- ¿Cada pieza tiene hipótesis y umbral de refutación escritos?
- ¿Todas pasaron la compuerta, y las que no están registradas en
  `data/registro-compuerta.csv`?
