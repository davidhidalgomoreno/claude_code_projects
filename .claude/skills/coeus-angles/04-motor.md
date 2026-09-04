# 04 · Motor de generación

Calibrado con 90 días reales de Meta: 113 anuncios, 25.340 € de inversión, 619
compras. Datos en `data/calibracion-meta-90d.csv`.

---

## Regla cero: dos nomenclaturas conviven

La cuenta usa **dos convenciones a la vez** y la buena no es la que documenta el
Content Grid.

| Convención | n | Gasto | ROAS |
|---|---|---|---|
| `JL/AG…` (julio 2026 en adelante) | 73 | 8.399 € | **1,38** |
| `VID–…` (Content Grid, mayo) | 15 | 3.942 € | 1,02 |
| Sin convención (`DIEGO 52`, `TOFU_ACTO2_…`) | 25 | 12.999 € | 1,10 |

La convención `JL/AG` es más rica que la del Content Grid: ya trae **awareness
y avatar**, que es exactamente lo que faltaba.

```
JL018.1/26 _ Video Ad _ RETROMAG _ TOFU _ Solution Aware _ MUJER MEDIANA EDAD
           _ VILLANO_MAGNESIO BARATO _ PROBLEM/SOLUTION _ Diego
```

**El motor genera sobre esta convención**, añadiendo el código de ángulo de
`01-taxonomia.md` en el campo de territorio. El 51 % de la inversión está en
anuncios sin ninguna convención y por tanto es ilegible: cerrar esa fuga vale
más que cualquier ángulo nuevo.

### Mapa entre el campo TERRITORIO y el eje ÁNGULO

| Territorio en la cuenta | Ángulo | Territorio de dolor |
|---|---|---|
| `VILLANO_MAGNESIO BARATO` | `CRIT` | transversal |
| `VILLANO_MELATONINA` | `FALC` | DESCANSO |
| `PROBLEMAS PARA DORMIR` | `PUDO` | DESCANSO |
| `…_CANSANCIO` · `…_RECUPERACIÓN` | `PUDO` | RENDIMIENTO |
| `…_CALAMBRES` | `PUDO` | TENSIÓN |
| `NIEBLA MENTAL` | `PUDO` | FOCO |
| `DIGESTIÓN` | — | **prohibido**, ver `05-compuerta.md` |

---

## Pesos calibrados

Lo que el motor privilegia, con el dato que lo sostiene.

| Dimensión | Preferir | ROAS | Frente a | ROAS |
|---|---|---|---|---|
| **Ángulo** | `CRIT` (villano magnesio barato) | **1,54** | `FALC` (villano melatonina) | 0,62 |
| **Avatar** | Mujer de mediana edad | **1,72** | Biohacker | 0,92 |
| **Awareness** | Solution Aware | **1,45** | Problem Aware | 1,02 |
| **Formato** | Vídeo | **1,57** | Estático | 1,11 |
| **Estructura** | Problem/Solution | **2,25** | Viral · Reddit · Us vs Them | ≤0,96 |

**Referencia de la cuenta:** ROAS 1,18 · CPA 40,94 € · AOV 48,32 €.
Para Retromag: CPA 37,88 €. Cualquier celda por debajo de 1,0 con más de 400 €
de reparto se considera refutada, no pendiente.

### Cómo se usa el peso

El motor **no genera solo ganadores**: reproduciría el inventario en lugar de
ampliarlo. Reparto por lote:

- **60 % explotación** — celdas con ROAS medido por encima de la cuenta.
- **30 % exploración dirigida** — celdas vacías en territorios de riesgo bajo
  (FOCO, TENSIÓN, RENDIMIENTO), que hoy no tienen ni un anuncio.
- **10 % refutación** — una celda que los datos dan por perdida, reformulada
  con la hipótesis explícita de por qué esta vez sería distinto. Sin hipótesis
  escrita, no entra.

---

## Lo que los datos refutaron

Tres lecturas mías que el export corrige. Quedan aquí para que el sistema no
las repita.

1. **Las 3 de la mañana no son un activo.** Escribí que lo eran por aparecer en
   dos anuncios del Content Grid. En 90 días, `DESPERTAR 3AM` acumula 10
   creatividades y 165 € de reparto. Meta dejó de servirlas. El sueño genérico
   sí funciona (1,36); la especificidad de la hora, no.
2. **El avatar no es «ambos géneros».** Mujer de mediana edad 1,72 frente a
   biohacker 0,92, ambos con gasto suficiente. La categoría sugiere biohacker;
   la caja dice otra cosa.
3. **`CRIT` no estaba sin explotar: ya era el ganador.** Dije que tenía cero
   anuncios, leyendo solo la nomenclatura antigua. Bajo el nombre
   `VILLANO_MAGNESIO BARATO` concentra el 70 % de la inversión parseada de
   Retromag y es el mejor territorio de la cuenta, con un CPA de 26,72 € frente
   a 37,88 € de media del SKU. La hipótesis era correcta; la lectura de
   cobertura, no.

---

## Cautelas de lectura

No sobreinterpretar. Escrito aquí para que el motor no invente certeza.

- **`PROBLEM/SOLUTION` con 2,25 lo sostiene un solo anuncio** (JL018.1). Es la
  estructura mejor colocada, no un hecho establecido.
- **El talento está confundido con la estructura.** Diego 2,23 y Susana 0,97,
  pero Diego rodó Problem/Solution y Susana rodó Viral. No se puede separar sin
  un test cruzado: mismo guion, dos talentos.
- **El conjunto pesa tanto como el creativo.** `JL016` marca 0,69 en un
  conjunto y 2,11 en otro **siendo el mismo anuncio**. Antes de atribuir un
  resultado a la creatividad, comprobar en qué conjunto corrió.
- **Todo por debajo de 250 € de reparto es ruido.** Se etiqueta y se acumula,
  no se concluye.
- **La cuenta está en 1,18 de ROAS.** Si el margen sobre un AOV de 48 € no
  cubre eso, el problema no es de ángulos y ningún motor lo va a arreglar.

---

## Salida

Cada pieza generada sale con: código de ángulo, avatar, awareness, territorio,
estructura, formato, hipótesis medible y celda de origen en la matriz. Formato
en `06-salida.md`. Después pasa por `05-compuerta.md`, siempre.
