# RuneMasters

RuneMasters è un gioco strategico a turni su griglia esagonale, sviluppato con Unity. Il progetto include contenuti di gioco, unità e nemici, rune e abilità, mappe, interfaccia utente, animazioni ed effetti.

## Stato del progetto

Progetto Unity in fase di sviluppo/prototipazione. Il repository contiene scene di gameplay e strumenti per la modifica delle mappe; non sono documentati qui build o piattaforme di rilascio.

## Requisiti

- **Unity Editor:** `2020.3.13f1` (vedi `ProjectSettings/ProjectVersion.txt`)
- **Pacchetti Unity:** vedere `Packages/manifest.json`
- **Codice:** C#

Apri la cartella del repository con la versione Unity indicata. Unity installerà i pacchetti dichiarati nel manifest. Per evitare modifiche involontarie ai riferimenti, non spostare o rinominare asset e cartelle direttamente fuori dall'Editor.

## Scene principali

Le scene si trovano in `Assets/Scenes/`:

- `MainMenu.unity` — scena del menu principale;
- `Andrea_GameplayScene.unity` — scena di gameplay;
- `MapEditorScene.unity` — scena dell'editor mappe;
- `SampleScene.unity` — scena di esempio/prototipo.

Verifica le scene di avvio in **File → Build Settings** dentro Unity: il README non presume quale scena sia configurata come iniziale.

## Catalogo dei contenuti

La gerarchia di Unity `Assets/` è mantenuta perché prefab, scene, materiali e script fanno riferimento agli asset tramite GUID. Le cartelle già esistenti sono raggruppate per funzione:

| Percorso | Contenuto |
|---|---|
| `Assets/Scenes/` | Scene del menu, gameplay, editor mappe e prototipo |
| `Assets/Prefabs/` | Prefab di unità, nemici, tile, editor mappe, UI, audio, timeline ed effetti |
| `Assets/ScriptableObjects/` | Dati configurabili: abilità, aree, effetti, rune, audio e configurazioni di board/livelli |
| `Assets/Materials/` | Materiali del gioco per personaggi, tile e ambienti |
| `Assets/Animations/` | Clip e controller di animazione |
| `Assets/Art/` | Risorse grafiche, font, rune e mesh |
| `Assets/Hexlands_LowPolyStyle/` | Risorse di ambientazione esagonale: scene, materiali, mesh, prefab e texture |
| `Assets/Low Poly Hexagons/` | Modelli, prefab, materiali, texture e composizioni di terreno esagonale |
| `Assets/Mini Legion Grunt PBR HP Polyart/` | Modello Grunt, animazioni, prefab, scene e texture |
| `Assets/Mini Legion Lich PBR HP Polyart/` | Modello Lich, animazioni, prefab, scene e texture |
| `Assets/Magic VFX/` | Effetto magico di ghiaccio, prefab, scena demo e audio |
| `Assets/JMO Assets/Cartoon FX/` | Effetti particellari, prefab, shader, materiali e risorse demo |
| `Assets/Plugins/FMOD/` | Integrazione FMOD e librerie per le piattaforme supportate dal plugin |
| `Assets/Plugins/` | Plugin e integrazioni Unity |

### Dati di gioco (`ScriptableObjects`)

- `Abilities/` — abilità di Mage, Tank, Thief e nemici, aree d'effetto, gittate ed effetti (danno, cura, buff, debuff, danno nel tempo e interazione con la mappa).
- `Runes/` — rune generiche e set specifici per Mage, Tank e Thief.
- `Audio/` — configurazioni audio per musica, attacchi, danni, vittoria/sconfitta e interfaccia.
- `Board/` e asset `Board*` — collezioni di tile e configurazioni di board/livelli.

### Prefab

- `Prefabs/Units/` — prefab delle unità giocabili.
- `Prefabs/Tiles/` — tile della griglia e terreni.
- `Prefabs/MapEditor/` — pennelli dell'editor per unità e tile.
- `Prefabs/UI/` — HUD, menu e pannelli.
- `Prefabs/Audio/` — controller, manager, emitter e mixer.
- `Prefabs/Timeline/` — risorse Timeline.
- `Prefabs/effects/` — effetti usati dal gioco.

## Struttura di alto livello

```text
.
├── Assets/                 # Scene, codice/risorse del gioco, prefab e contenuti Unity
├── Packages/               # Manifest e lockfile dei pacchetti Unity
├── ProjectSettings/        # Impostazioni del progetto Unity
├── CONTRIBUTIONS.md        # Indicazioni per i contributi
├── .gitignore              # File esclusi dal controllo versione
└── README.md
```

## Contributi

Prima di proporre modifiche, consulta [CONTRIBUTIONS.md](./CONTRIBUTIONS.md). Per le risorse Unity, conserva insieme ogni asset e il relativo file `.meta`; preferisci spostamenti effettuati dall'Editor Unity per mantenere validi i riferimenti.

## Licenze delle risorse

Il progetto include asset e plugin di terze parti (tra cui Cartoon FX, FMOD, font e pacchetti di modelli). Le licenze possono variare: consulta i file di licenza/readme inclusi nelle rispettive cartelle e verifica i termini prima di ridistribuire o pubblicare una build. La presenza dei file nel repository non implica che tutte le risorse siano rilasciate con la stessa licenza.
