# GENERADOR PROCEDURAL (Skill de apoyo — ahorro de tokens)

Esta skill permite al DM improvisar contenido menor SIN leer archivos pesados. Úsala para NPCs sin ficha, encuentros aleatorios, botín y nombres. Todo lo generado hereda las reglas de `dm_engine.md`.

## 1. Tirada de Encuentro Aleatorio (por bioma)
Lanza 1d20 al viajar o explorar:
- **1-10:** Sin encuentro (ambiente, clima, rastros).
- **11-16:** Encuentro de fauna acorde al Tier de la zona (consulta archivo regional).
- **17-19:** Encuentro humanoide (bandidos, patrulla, mercader, viajero).
- **20:** Evento especial (mini-jefe regional, anomalía, hallazgo de loot raro 1 Tier superior).

## 2. Tier de la Zona (peligro escalado por distancia a capitales)
- **Cerca de capital/ciudad (radio seguro):** Enemigos Tier G-F.
- **Caminos y aldeas:** Tier F-E.
- **Naturaleza salvaje / frontera:** Tier E-D.
- **Mazmorras, ruinas, territorio hostil:** Tier D-C.
- **Guaridas de leyenda / zonas selladas:** Tier B-S (y SSS si es un Épico del catálogo).

## 3. Generación de NPC Genérico (sin ficha guardada)
Define al vuelo: Tier (según contexto), Oficio, Habilidades (según nº del Tier, `dm_engine.md §1`), un **rasgo psicológico** dominante (define cómo actúa, §8), y Actitud (Hostil/Neutral/Aliado). Stats SIEMPRE desde la tabla de `dm_engine.md`. Si es un **monstruo**, aplica el sistema Cría/Adulto/Alfa (§7). Solo guarda ficha en `NPCs/` si el NPC es recurrente o relevante para la trama.

## 4. Botín Procedural (resumen de dm_engine.md §5)
Al matar una entidad lanza 1d100:
- **1-50:** Material/parte del MISMO Tier.
- **51-85:** Material 1 Tier INFERIOR (restos dañados).
- **86-100:** Material 1 Tier SUPERIOR (anomalía biológica).
Bestias NO sueltan dinero; solo partes extraíbles con herramienta. Solo humanoides sueltan monedas lógicas.

## 5. Generadores de Nombres (semillas por región)
- **Ventar (Elfos de Hielo):** Kael-, Vry-, -ion, -eth, -lyr (ej: Vryeth, Kaelion).
- **Arbolra (Humanos/Elfos):** Al-, Ros-, -wen, -ander, -mir (ej: Roswen, Almander).
- **PartForj (Enanos):** Dur-, Bron-, Throk-, -grim, -din (ej: Durgrim, Throkdin).
- **Gromrack (Orcos/Leoninos):** Gor-, Kraa-, Zul-, -tusk, -mane (ej: Gortusk, Zulmane).
- **Moglar (Hadas/Tieflings):** Ae-, Xil-, Noc-, -ys, -thra (ej: Aethra, Xilys).

## 6. Generador de Mazmorra Rápida
1d4 salas: cada sala → 1d20 de la tabla §1 (encuentro/trampa/tesoro/vacío). Sala final = mini-jefe 1 Tier por encima de la zona. Botín final = objeto crafteable o material raro.

## 7. Clima y Tiempo (1d6 al amanecer)
1-2 Despejado · 3-4 Nublado/Templado · 5 Adverso (lluvia/nieve/calor: -1 efectividad en exteriores) · 6 Extremo (tormenta/ventisca/ola de calor: viajes peligrosos, posible daño ambiental Tier G).
