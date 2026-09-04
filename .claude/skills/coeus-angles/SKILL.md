---
name: coeus-angles
description: Genera ángulos de anuncio para suplementación de longevidad y retroaging de COEUS, con hooks y brief de rodaje. Úsala cuando alguien pida ángulos, hooks, ideas de creativos, briefs o guiones para anuncios de pago de COEUS (Retromag, Mepausa, NadTime, Renergy, Rescanso, Noestres, Renegen, Performan), o cuando pida analizar el rendimiento de creativos existentes por ángulo. NO cubre FitRX.
---

# COEUS · Motor de ángulos

Sistema de generación de ángulos de anuncio para el catálogo de suplementación
de COEUS Retroaging. Produce, por cada ángulo: tesis, avatar, mecanismo, tres
hooks alternativos y brief de rodaje.

## Orden de ejecución — no alterar

```
1. Leer 01-taxonomia.md          → el diccionario. Siempre.
2. Leer 02-avatares.md           → a quién le habla.
3. Leer 03-producto/<sku>.md     → qué se puede afirmar de este producto.
4. Ejecutar 04-motor.md          → generar.
5. Ejecutar 05-compuerta.md      → OBLIGATORIO. Con derecho de veto.
6. Formatear con 06-salida.md    → entregable.
```

**El paso 5 no es opcional y no se adelanta.** La compuerta de cumplimiento
corre después de generar y antes de entregar. Meterla como consideración dentro
del prompt de generación es el fallo clásico: siempre se cuela algo.

## Estado de los módulos

| Módulo | Estado |
|---|---|
| `01-taxonomia.md` | **Listo.** 11 ángulos, 3 ejes. Derivado de 61 anuncios reales. |
| `data/remapeo-obcs.csv` | **Listo.** 31 anuncios históricos reetiquetados. |
| `02-avatares.md` | **Listo.** Avatar de Retromag, con restricción de claim verificada. |
| `03-producto/retromag.md` | **Listo.** Composición, declaraciones verificadas y prohibiciones. |
| `04-motor.md` | Pendiente. Requiere calibración con export de Meta. |
| `05-compuerta.md` | Pendiente. Bloqueante para uso en producción. |
| `06-salida.md` | Pendiente. |

**Hasta que exista `05-compuerta.md`, nada que salga de este sistema se publica
sin revisión humana de cumplimiento normativo.**

## Fuera de alcance

- **FitRX.** Medicamento sujeto a prescripción. Su publicidad dirigida al
  público general está prohibida en España. No se generan ángulos, no se
  etiqueta, no entra en ninguna media de rendimiento.
- **Capa marca `@coeus.time` pilar TIEMPO.** Decisión de septiembre de 2026:
  de los tres pilares orgánicos huérfanos solo `RETROAGING®` (con el material
  de `CRITERIO` dentro) baja a paid.

## Deuda técnica conocida

Registrada para que el sistema no la herede en silencio:

1. **Ficha técnica de Retromag** — el carbonato de magnesio declara 80,42 mg por
   cápsula y 106,84 mg por dos. Debería ser 160,84. El Mg elemental
   (20,90 → 41,80) sí duplica bien. Parece errata de materia prima. Confirmar
   con Marnac Twins Pharma antes de que el módulo 03 la use como fuente.
2. **Contradicción en anuncio vivo** — `COEUS Ad 1` presenta el carbonato como
   sal de alta absorción junto al bisglicinato, dos frases antes de atacar las
   formas baratas. Verificar contra fuente primaria de biodisponibilidad
   comparada y corregir el copy si se confirma.
3. **Declaración de sueño en anuncio vivo** — la microcopy de `COEUS Ad 1`
   («Duerme del tirón desde la primera semana») es una declaración de
   propiedades saludables sobre el sueño. Verificado contra el Reglamento (UE)
   432/2012: el magnesio **no tiene declaración autorizada de sueño** en la UE;
   sus territorios autorizados son sistema nervioso, función psicológica,
   cansancio y fatiga, metabolismo energético, función muscular, equilibrio
   electrolítico, huesos, dientes, división celular y síntesis proteica. La
   única sustancia con declaración de sueño autorizada es la melatonina.
   Añade además una atribución de velocidad de efecto. Elevar a asesoría legal.
4. **«Más de 300 funciones»** en `COEUS Ad 6` — declaración general no
   específica. Solo admisible acompañada de una declaración autorizada concreta
   (art. 10.3 del Reglamento 1924/2006). Hoy va sola.
5. **Dosis diaria de magnesio** — Retromag declara 279,6 mg de magnesio
   elemental por toma de 2 cápsulas (74,57 % VRN). El nivel máximo de ingesta
   tolerable de la UE para magnesio **suplementario** de sales fácilmente
   disociables se sitúa habitualmente en 250 mg/día, y los máximos nacionales
   varían. No he podido confirmar el límite vigente que aplica AESAN en España.
   Verificar antes de que ningún creativo use la dosis como argumento de venta
   («a la dosis que de verdad necesitas», COEUS Ad 1).
6. **Bloque §5 del calendario editorial** — diez datos de marca sin fuente
   primaria localizada, entre ellos la caída de NAD+ del 65 %, la edad biológica
   del fundador y quién firma la dirección científica. Ninguno puede entrar en
   un creativo hasta resolverse.
