# NÚCLEOS — MAPA DEL GRAFO DE CONOCIMIENTO (ClaudeDM)
> Índice navegable de los **núcleos (nodos)** del mundo y sus **aristas (relaciones)**. Es el mapa manual que mantiene la coherencia y orienta a Graphify. El grafo "vivo" lo genera `/graphify .` en `graphify-out/graph.json` + `graphify-out/GRAPH_REPORT.md`.
>
> **Uso (CLAUDE.md §6):** consulta este mapa / el grafo ANTES de leer archivos en bruto. Localiza el núcleo implicado y abre solo su fuente.

## Tipos de núcleo
| Tipo | Qué es | Vive en |
|---|---|---|
| 🜂 **Regla** | Mecánica del sistema | `Skills/dm_engine.md`, `Skills/generador_procedural.md` |
| 🌍 **Continente** | Región mayor del mundo | `WorldSaves/world_state.md` |
| 🌊 **Mar** | Ruta marítima transicional | `WorldSaves/world_state.md`, `Base_de_Datos/Monstruos/Mares.md` |
| 🏰 **Reino/Facción** | Poder político de un continente | `WorldSaves/world_state.md` |
| 🐉 **Monstruo** | Bestia/entidad (Cría/Adulto/Alfa) | `Base_de_Datos/Monstruos/*` |
| 👤 **NPC** | Personaje no jugador con ficha | `NPCs/*` |
| 🧝 **Jugador** | Personaje jugable | `Saves/*` |
| ⚔️ **Objeto/Material** | Equipo, loot, materiales (con Tier y peso) | en fichas / loot de bestiarios |
| 📍 **Localización** | Lugar concreto (ciudad, mazmorra, palacio) | donde se cree |
| 🎯 **Misión/Evento** | Hilo narrativo o suceso global | `WorldSaves/timeline.md` |
| 🕘 **Sesión** | Registro temporal de partida | `WorldSaves/timeline.md` + log del jugador |

## Núcleos actuales (registro)
### 🜂 Reglas
- **Núcleo Mecánico** → `Skills/dm_engine.md` (tiers, combate, daño por diferencia, ventaja/desventaja, peso, materiales, monstruos, loot, economía, tiempo).
- **Generador Procedural** → `Skills/generador_procedural.md`.
- **Directrices del DM** → `CLAUDE.md` (tono, voz, notación, reloj, núcleos).
- **Plantillas** → `Saves/Plantilla_Jugador.md`, `NPCs/Plantilla_NPC.md`.

### 🌍 Continentes y 🏰 reinos → `WorldSaves/world_state.md`
- **Ventar** (Imperio de Kaelor · Kragoroth · Glint · **Veth'ira** [oculto])
- **Arbolra** (Lumeria · Silvane · Oakhaven · Altos Humanos / La Sombra del Loto [clan])
- **PartForj** (Magmador · Ferrum · Cinder)
- **Gromrack** (Kahnato de Darak · Akil · Vultur)
- **Moglar** (Círculo de Aethel · Noxus · Zephyr)

### 🗺️ Mapas → `WorldSaves/Mapas/`
- **Ventar** → `WorldSaves/Mapas/Ventar.svg` (Glacia · Puerto Escarchado · Muro Gris · Kragoroth · Glint · Veth'ira [oculto] · rutas y biomas).

### 🌊 Mares → `Base_de_Datos/Monstruos/Mares.md`
- Mar de Cristal · Océano de Vapor · Mar de Ámbar · Golfo de la Disyunción · Estrecho del Hierro Roto

### 🐉 Bestiarios → `Base_de_Datos/Monstruos/`
- `Ventar.md` · `Arbolra.md` · `PartForj.md` · `Gromrack.md` · `Moglar.md` · `Mares.md` · `Epicos_SSS.md` (SSS + Tier X) · índice en `catalogo_monstruos.md`.
- **Nuevos en Ventar (P0):** **Lobo de Escarcha** (Adulto D / Alfa C — especie de Botón) · **Halcón de Llama Glacial / "Fulgor de Escarcha"** (Adulto D / Alfa C — predador aéreo de la Cordillera Blanca; sus plumas azul-metálicas eran el "misterio del depredador aéreo").

### 🧝 Jugadores / 👤 NPCs
- **Zero (J1 · P0)** → `Saves/Zero_Log_P0.md` ✓ Tier D Sombra Alto Humano · Ventar · **Glacia** (alias **"Glor"**, criador de lobos)
- **Alyna (J2 · P0)** → `Saves/Alyna_Log_P0.md` ✓ Tier F Maga Humana · Ventar · **Glacia**
- **Botón (compañero · P0)** → `NPCs/Boton_Lobo_Companero.md` · **Lobo de Escarcha Alfa Tier C** · aliado provisional / montura del grupo
- **Maestra Syleth** → `NPCs/Syleth_Alquimista_Glacia.md` · Elfa de Hielo · alquimista de Glacia · contacto VIP de materiales naturales
- **Comerciante Volas** → `NPCs/Volas_Comerciante_Glacia.md` · Humano · artefactos/materiales arcanos en Glacia
- **Capitán Aelhir** → `NPCs/Capitan_Aelhir_Glacia.md` · Elfo de Hielo · jefe de la guardia de Glacia · *encuentro pendiente*

### 📍 Localizaciones
- **Glacia** (capital del Imperio de Kaelor) → detalle en `WorldSaves/world_state.md` §1: Elfos de Hielo, murallas de Hielo-Verdadero, comercios (Syleth, Volas, Hierro y Cuero, Colmillo Norte, posada El Ancla de Hielo), capitán Aelhir.

### 🕘 Sesiones
- **P0** — Partida activa. Inicio: Año 0 · Enero · Día 1 · 00:00 · Ventar. **Estado actual:** Día 3 · 12:04 · Glacia (grupo: Zero/"Glor" + Alyna + Botón). Próximo: comparecer ante el capitán Aelhir; reabastecer raciones; rumbo norte (Muro Gris → Veth'ira).

## Aristas principales (relaciones del grafo)
- **Regla** —gobierna→ **todo** (Tiers, daño, peso aplican a cualquier núcleo).
- **Continente** —contiene→ **Reinos/Facciones** y —limita con→ **Mar(es)**.
- **Mar** —conecta→ dos **Continentes**.
- **Monstruo** —habita→ **Continente/Mar**; —tiene estados→ Cría(G)/Adulto/Alfa; —suelta→ **Objeto/Material**.
- **NPC/Jugador** —pertenece a→ **Raza** (de un Continente); —porta→ **Objeto**; —tiene→ **Psicología** (define las 3 habilidades de subida de Tier).
- **Jugador (ausente)** —puede ser encarnado como→ **NPC por el DM**, guiándose por su **Psicología**, sin salir de `Saves/` (CLAUDE.md §12).
- **Objeto/Material** —tiene→ **Tier** (pureza de maná → mejoras) y **peso (kg)**; en **Luz de Luna Roja** sube +1 Tier.
- **Misión/Evento** —ocurre en→ **Localización/Tiempo**; —involucra→ **NPCs/Jugadores**.
- **Estación (Luz de Luna Roja)** —modifica→ **Monstruos** (intensidad) y **Objetos** (+1 Tier).

## Cómo expandir el grafo
1. Crea/edita el núcleo en su archivo (NPC nuevo → `NPCs/`, lugar → su archivo, etc.).
2. Enlázalo aquí (añádelo al registro y a las aristas que toque).
3. Regenera el grafo: `/graphify . --update`.
