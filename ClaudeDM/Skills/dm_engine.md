# NÚCLEO MECÁNICO (DM_ENGINE v3.0)
> Referencia densa. Stats inmutables. El DM NO inventa reglas fuera de aquí.

## 1. Tabla de Tiers
El Tier existe en TODO: personas, NPCs, monstruos, materiales, ingredientes y objetos. Funciona distinto en cada cosa (ver §1.2, §6 y §7). Esta es la columna de personajes (jugadores y NPCs).

| Tier | Significado (qué representa) | HP | Mín | Máx | Crít (= Máx×2) | Nº Habilidades |
|---|---|---|---|---|---|---|
| **X** | **Dios.** Capaz de recrear el mundo a voluntad; poder casi omnipotente. | ∞ / Narrativo | 100+ | 150+ | 300+ | Ilimitadas |
| **SSS** | **Héroe Maestro.** Técnica + sabiduría entrenadas **MÁS** una habilidad de nacimiento. | 500+ | 40 | 70 | 140 | 6 |
| **SS** | **Héroe.** Como el SSS pero **sin** habilidad de nacimiento. | 350 | 25 | 45 | 90 | 5 |
| **S** | **Gran Maestro.** Sabiduría y técnica en estado teórico (poder altísimo) **pero con una limitación**: edad avanzada o fragilidad física. | 220 | 18 | 30 | 60 | 5 |
| **A** | **Veterano de élite.** Asesinos secretos, Emperadores de guerra. | 150 | 12 | 22 | 44 | 4 |
| **B** | **Mano derecha del ejército / Instructor.** | 110 | 8 | 16 | 32 | 4 |
| **C** | **Soldado de alto rango.** | 75 | 6 | 12 | 24 | 3 |
| **D** | **Soldado.** | 50 | 4 | 10 | 20 | 3 |
| **E** | **Aventurero con cierta habilidad.** | 35 | 3 | 8 | 16 | 2 |
| **F** | **Adulto normal.** | 20 | 2 | 5 | 10 | 2 |
| **G** | **Niño, bebé o cosa inútil.** | 10 | 2 | 2 | 4 | 1 |

- El Tier es una **descripción de potencial** según la historia y entrenamiento del personaje: dónde encaja y cómo de fuerte es. Dos personajes del mismo Tier no son idénticos; el Tier marca el techo de poder, no la personalidad.
- En personajes, el Tier define: **nº de habilidades**, nivel de poder de la especie, HP máximo y daño.
- **HP** = Vida Actual / Vida Máxima (ej. 18/20). La Vida Máxima la fija el Tier.
- **Daño Medio = (Mín+Máx)/2** (referencia narrativa).

## 2. Combate — Choque Simultáneo
**Fase 1:** el DM declara la intención enemiga; el jugador declara su acción.
**Fase 2:** ambos lanzan **1d20**. `X = |ganador − perdedor|`.

### 2.1 Daño por Diferencia (REGLA CLAVE)
El daño **escala con la diferencia X**. Cada punto de diferencia vale un **20% del Daño Máximo**, redondeado **a la baja** (enteros, sin decimales):

`Daño = ⌊ (mín(X,5) / 5) × DañoMáx ⌋`  → con **suelo en DañoMín** (todo golpe que conecta hace al menos su Mín). Hacen falta **5 de diferencia** para el Daño Máximo.

**CRÍTICO = Máx × 2.** Cuando la diferencia es **el DOBLE o más** de la necesaria para el máximo (es decir **X ≥ 10**), el daño se duplica: el ganador hace **Daño Máximo × 2**.

| Diferencia X | Ganador | Perdedor | Orden / Efecto |
|---|---|---|---|
| **X ≥ 10** | **CRÍTICO = Máx × 2** | 0 (cancelado) | Interrupción demoledora |
| **X = 5–9** | **100% Máx** | 0 (cancelado) | Interrupción: impacto perfecto |
| **X = 4** | **80% Máx** | Mín | Ganador 1º, perdedor después |
| **X = 3** | **60% Máx** | Mín | Ganador 1º, perdedor después |
| **X = 2** | **40% Máx** | Mín | Ganador 1º, perdedor después (≈ daño mínimo) |
| **X = 1** | Mín (roce) | Mín | Casi simultáneo |
| **X = 0** | 0 | 0 | Colisión, ambos fallan |

- *Ejemplo del jugador:* tiro **20**, el rival **10** → X=10 (el doble de los 5 necesarios) → **Crítico = Máx×2**.
- *Ejemplo:* Mín 1 / Máx 10, saco **4 de diferencia** → 4×20% = 80% → **8 de daño**.
- *Tier D (Máx 10 / Mín 4):* X=2→4 · X=3→6 · X=4→8 · X=5→10 · X≥10→**20**.
- *Tier F (Máx 5 / Mín 2):* X=2→2 · X=4→4 · X=5→5 · X≥10→**10**.
- **Nat 20:** el ganador **actúa primero e interrumpe** siempre, y su golpe nunca baja de Daño Máximo (será Crítico si además X≥10).

### 2.2 Casteo / Carga (2 turnos)
- **T1:** el jugador lanza d20 Concentración vs enemigo. Si el enemigo gana con X≥5 → casteo interrumpido, recibe daño y pierde la carga. Si gana con X<5 → recibe daño pero **mantiene** concentración.
- **T2:** libera con choque normal; si gana, aplica el efecto cargado.

## 3. Tiradas Generales (dificultad por lógica)
La misma escala 1–20 resuelve acciones no-combativas. **El DM fija la dificultad por sentido común**: cuanto más improbable o arriesgada la acción, mayor el número objetivo.
- *Ejemplo:* robar SOLO la lanza que un durmiente no sostiene es fácil; robar la lanza **Y** la daga que él tiene en la mano es mucho más difícil. El DM razona la dificultad antes de pedir la tirada.

### 3.1 Modificador de Situación (Ventaja / Desventaja) — SE APLICA A TODA TIRADA
El DM ajusta **cada tirada** (combate, sigilo, persuasión, físicas…) según el estado y la posición del personaje **antes de tirar**. Cuanto mejor colocado esté (terreno, posición, magia, estado físico, preparación previa), **+1 / +2 / +3**; cuanto peor, **−1 / −2 / −3**. El DM declara el modificador en voz alta antes de pedir el d20.

| Modificador | Cuándo (ejemplos acumulables, tope ±3) |
|---|---|
| **+3** | Ventaja casi total: enemigo dormido/cegado/inmovilizado, ataque por la espalda sin ser visto, terreno y preparación a tu favor. |
| **+2** | Ventaja clara: alto terreno, flanco, buff mágico activo, enemigo desequilibrado. |
| **+1** | Ventaja leve: buena posición, herramienta adecuada, aliado distrayendo. |
| **0** | Situación neutra. |
| **−1** | Desventaja leve: cansado, mala iluminación, terreno incómodo, leve herida. |
| **−2** | Desventaja seria: herido de gravedad, una mano ocupada/atada, en desequilibrio, atacando a ciegas. |
| **−3** | Desventaja extrema: atado de pies y manos, exhausto, cegado, bajo agua sin saber nadar, casi inconsciente. |

- Los modificadores de varias fuentes **se suman pero se topan en ±3** (ni más ni menos).
- Estados que el DM debe vigilar siempre: **atado, herido, cansado/exhausto, cegado, envenenado, en mal terreno, sin el arma adecuada, sobrecargado de peso** (ver §4.1).
- En **choque de combate**, el modificador se suma al d20 de cada bando *antes* de calcular la diferencia X (§2.1).

## 4. Estadísticas de Personaje: Fuerza, PA y PP
Se **tiran 1d20 en la creación** del personaje y el jugador declara sus valores. (En NPCs el DM los fija y se revelan poco a poco.)

- **FUERZA:** cuánto peso puede cargar = `Fuerza × 10 kg`. (Fuerza 10 → 100 kg.) También modula tiradas físicas de carga/empuje.

### 4.1 Peso y Carga (TODO tiene peso, en kg)
Cada objeto del mundo tiene un **peso real en kg**. Reglas:
- **Equipado o en uso = 0 kg de carga.** El arma empuñada, la armadura puesta y la ropa no cuentan para el límite (se asume que el cuerpo los sostiene de forma natural).
- **Guardado en la Mochila = pesa de verdad.** Todo lo del apartado *Mochila* de la ficha suma su peso en kg. El DM anota el peso de cada material/objeto al adquirirlo.
- **El DINERO no pesa.** Oro, Plata y Cobre van encima del personaje / en la mochila pero **NO cuentan para el límite de carga** (excepción por convención).
- **Límite de carga = Fuerza × 10 kg** (solo cuenta la mochila, sin contar el dinero).
- **Sobrecarga:** si el peso de la mochila supera el límite, el personaje sufre **Desventaja** en tiradas físicas y de movimiento (§3.1): −1 hasta 110% del límite, −2 hasta 130%, −3 por encima; superar el 150% impide moverse hasta soltar peso.
- Referencias de peso (orientativas): daga ~1 kg · espada ~2 kg · armadura ligera ~8 kg · armadura pesada ~20 kg · poción ~0,3 kg · lingote de metal ~3 kg · pieza grande de bestia ~5–15 kg.
- **PERCEPCIÓN ACTIVA (PA):** modificador a tiradas en las que el jugador **busca activamente** algo (interrogar, detectar mentiras, registrar). El valor 1–20 da este modificador:

| Valor de PA | Modificador |
|---|---|
| 1 | −3 |
| 2–3 | −2 |
| 4–7 | −1 |
| 8–12 | 0 |
| 13–15 | +1 |
| 16–19 | +2 |
| 20 | +3 |

- **PERCEPCIÓN PASIVA (PP):** lo que el personaje capta **sin buscarlo**. No se tira: es pasiva. Si la **media de PP del grupo** es alta, el DM ofrece **más** información sensorial/contextual de forma espontánea; si es baja, ofrece **menos** y deja pistas escondidas. La PP también orienta la lectura de las marcas de rol del jugador (ver CLAUDE.md §Notación).

## 5. Progresión (sin XP — por hazañas)
Se asciende de Tier al vencer a un enemigo de Tier superior o cumplir un hito narrativo. Al ascender:
1. Detén la narrativa y notifica el ascenso.
2. Sube la Vida Máxima al nuevo Tier.
3. Genera **3 habilidades** coherentes con **Clase + Raza + Psicología** del personaje (ver §8 y la ficha).
4. El jugador **elige 1**. Actualiza la ficha (nueva habilidad + nuevo nº de habilidades del Tier).

## 6. Materiales, Ingredientes y Objetos (Tier ≠ que en personajes)
El Tier de un material indica su **pureza de maná**: a más Tier, mejor material y mejores mejoras que otorga al equiparse/craftearse.
- Un objeto/material puede conceder **entre 0 y 2 tipos de mejora** (p. ej. +Defensa y +Vida, o una **habilidad**).
- La **magnitud entera** (nunca porcentaje) de cada mejora la fija el Tier:

| Tier material | Magnitud por mejora | Umbral |
|---|---|---|
| G | 0 | Sin bono estadístico |
| F | 0 | Sin bono estadístico |
| E | 2 | **1.er umbral** — primer tier con stats (débiles) |
| D | 2 | = E |
| C | 2 | = E |
| B | 5 | **2.º umbral** — primera mejora real |
| A | 5 | = B |
| S | 10 | **3.er umbral** |
| SS | 15 | **4.º umbral** |
| SSS | 20 | Máximo |
| X | Único / narrativo | — |

*Ejemplo de la mecánica (NO valores fijos): un casco Tier SSS podría dar +20 Defensa y +20 Vida; su versión Tier C daría +2 y +2.*

### 6.2 Reglas de Equipo (cómo aplican los bonos en partida)
> Consolidación de las reglas de objetos. El DM las aplica SIEMPRE igual.
- **Umbrales reales:** los stats no suben tier a tier, suben por **umbrales**. G/F = **0** (utilidad pura, calor o protección narrativa, pero **no suman al d20**). El primer bono mecánico aparece en **Tier E (+2)**, se mantiene hasta C, y da el siguiente salto en **B (+5)**, luego **S (+10)**, **SS (+15)**, **SSS (+20)**.
- **No acumulación de mismo slot/tipo:** dos objetos que dan el mismo tipo de bono NO se suman — solo cuenta el de mayor Tier; el otro es respaldo narrativo (ej.: dos capas de lana abrigan más, pero el bono mecánico no se duplica).
- **Bonos condicionales:** un objeto puede otorgar su bono **solo bajo una condición física concreta**, declarada en su ficha. Si la condición no se cumple, el bono es 0. Ejemplos en juego:
  - *Capa de Piel de Oso Blanco (Tier E):* +1 **solo mientras el portador está inmóvil/quieto** (la piel es voluminosa; al moverse deja de aislar). Además ahuyenta bestias menores.
  - *Conjunto ninja de infiltración (Tier F):* +1 **solo estando en sombras/penumbra** (excepción narrativa: un Tier F que sí da bono, pero atado a una condición estricta).
- **Mejoras de habilidad:** materiales de alto Tier (o ítems especiales) pueden conceder una **habilidad o un efecto único** en vez de stats (ej.: el Libro del Antepasado de Alyna → +1 opción al subir de Tier). No cuentan como bono de stat y por tanto no chocan con la regla de no-acumulación.
- **El DM declara el bono activo ANTES de pedir el d20** (igual que ventaja/desventaja, §3.1) y comprueba si la condición del objeto se cumple en ese momento.
- **Estación Luz de Luna Roja (mes 13, Carmesí):** el maná se satura y **todo material/objeto obtenido durante esa estación sube +1 Tier** (loot, drops y crafteo). Ver `WorldSaves/timeline.md`.

### 6.1 Crafteo
`3 materiales del mismo Tier + instalación adecuada = 1 objeto de ese Tier`. Con Tiers mixtos, el resultado hereda el **Tier más bajo** usado.

## 7. Monstruos (sistema de SOLO 3 estados)
Los monstruos **NO suben de Tier con el tiempo**. Se mantienen. Reglas:

- **Cría → Tier G:** solo las crías (o "forma cría") son Tier G. Tienen **1 habilidad**.
  - Si una especie **no tiene cría** (p. ej. elementales, constructos), **nunca** existe en Tier G.
- **Adulto → salta de golpe a su Tier:** al crecer, la cría salta **directamente** al Tier adulto de su especie (no pasa por los intermedios). Ej.: huevo/cría de dragón = G → al crecer salta de golpe a **S**.
  - **Adulto de Tier inferior a S:** **3 habilidades** (su habilidad de cría + 2 nuevas).
  - **Adulto de Tier S o superior:** **4 habilidades**.
- **Alfa → sube UN rango:** un monstruo que sobrevive **más de 10 años** se vuelve Alfa y pasa al rango inmediatamente superior. Ej.: dragón adulto S → **Alfa SS**. Un Alfa de SSS alcanza **Tier X**.
  - **Alfa de adulto inferior a S:** **4 habilidades** (las del adulto + 1).
  - **Alfa de adulto S o superior:** **5 habilidades**.

**Loot de monstruos:** las bestias **no** sueltan dinero; solo **partes extraíbles** con herramienta (vendibles en asentamientos). Solo los humanoides sueltan monedas lógicas.

## 8. Psicología del Personaje (jugadores y NPCs)
Cada ficha tiene un análisis psicológico **profesional** (amable, psicópata, controlador, narcisista, cobarde, sádico, leal…), elaborado a partir de cómo **actúa** el personaje en partida.
- En **NPCs** se define desde su creación y **dicta cómo actúan**.
- En **jugadores** se va rellenando con su comportamiento real y **determina las 3 habilidades** ofrecidas al subir de Tier (Clase + Raza + Psicología).

## 9. Botín al Matar (1d100)
| Tirada | Resultado |
|---|---|
| 1–50 | Material/parte del **MISMO** Tier |
| 51–85 | Material **−1** Tier (restos dañados) |
| 86–100 | Material **+1** Tier (anomalía) |

## 10. Economía (cerrada y realista)
- Cambio: **100 Cobre = 1 Plata · 100 Plata = 1 Oro**.
- Precios base (ajusta por región/oferta): pan malo 50 Cobre · pan bueno 2 Plata · posada+descanso 5–15 Plata · poción +10HP 10 Plata · arma/armadura Tier F 50 Plata–2 Oro · objetos Tier C+ decenas/cientos de Oro (solo capitales).

## 11. Tiempo y Descanso
- **Descanso:** recuperar HP requiere **8 h in-game**.
- El DM **lleva el reloj**: indica hora y minuto y los avanza según lo que cada acción tarda de forma lógica (ver CLAUDE.md §Tiempo).
