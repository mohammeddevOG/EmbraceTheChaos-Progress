# 👻 Embrace the Chaos — عناق الفوضى
# سجل تطوير اللعبة

> **Game Name / اسم اللعبة:** `Embrace the Chaos — عناق الفوضى`
> **Engine:** `Unreal Engine 5.6`
> **Genre:** `Horror · Multiplayer`
> **Network:** `Online — Advanced Sessions Plugin · Steam`
> **Source Control:** `Diversion (Game Files) · GitHub (Progress)`
> **Team:** `Mohammed — Dev 👨‍💻` · `Abdullah — Map Designer 🎨`
> **Steam:** `✅ Live on Steam — tested`
> **Started / البدء:** `2025`
> **Target / الهدف:** `[30/07/2025]`

---

## 📊 Overall Progress — التقدم الكلي

| Phase / المرحلة | Owner | Status | Progress |
|---|---|---|---|
| Core Programming / البرمجة | 👨‍💻 Mohammed | 🟡 In Progress | `██████░░░░ 60%` |
| Multiplayer / الشبكة | 👨‍💻 Mohammed | 🟡 In Progress | `███████░░░ 70%` |
| UI / الواجهة | 👨‍💻 Mohammed | 🟡 In Progress | `██████░░░░ 60%` |
| Level 0: The Meetings | 🎨 Abdullah | 🟡 In Progress | `████████░░ 80%` |
| Level 1: Astray | 🎨 Abdullah | 🟡 In Progress | `████████░░ 80%` |
| Level 2: FROM | 🎨 Abdullah | 🟡 In Progress | `████████░░ 80%` |
| Level 3: The Cave | 🎨 Abdullah | 🟡 In Progress | `████████░░ 80%` |
| Level 4: Sewers | 🎨 Abdullah | 🟡 In Progress | `████████░░ 80%` |
| Puzzle Connection / ربط الألغاز | 👥 Both | ⬜ Not Started | `░░░░░░░░░░ 0%` |
| Level Progression / تسلسل المراحل | 👥 Both | ⬜ Not Started | `░░░░░░░░░░ 0%` |
| Audio / الصوت | 👥 Both | ⬜ Not Started | `░░░░░░░░░░ 0%` |
| Bug Fixes / إصلاح الأخطاء | 👥 Both | 🟡 In Progress | `███░░░░░░░ 30%` |
| Testing & Release / الاختبار | 👥 Both | 🟡 In Progress | `██░░░░░░░░ 20%` |

> `✅ Done` · `🟡 In Progress` · `⬜ Not Started` · `🔴 Blocked`

---

## 🏁 Milestones — المراحل

| # | Milestone / الهدف | Deadline | Status |
|---|---|---|---|
| 1 | Code Review Complete / مراجعة الكود | `[16/05/2025]` | 🟡 |
| 2 | GameInstance Final Wiring / ربط الجيم انستنس | `[17/05/2025]` | ⬜ |
| 3 | All Puzzles Connected / ربط كل الألغاز | `[30/05/2025]` | ⬜ |
| 4 | Level Progression Working / تسلسل المراحل | `[30/05/2025]` | ⬜ |
| 5 | Animation Bug Fixed / إصلاح الأنيميشن | `[30/05/2025]` | ⬜ |
| 6 | Full Multiplayer Test / اختبار كامل | `[15/06/2025]` | ⬜ |
| 7 | Release / الإطلاق 🚀 | `[30/06/2025]` | ⬜ |

---

## 🎮 Game Levels — مراحل اللعبة

| # | Level Name | Concept | Monsters | Status | Missing |
|---|---|---|---|---|---|
| 0 | **The Meetings** | Backroom yellow aesthetic | TBD | 🟡 Nearly Done | Puzzle connection |
| 1 | **Astray** | Backrooms + puzzles + multiple monsters | Multiple | 🟡 Nearly Done | Puzzle connection |
| 2 | **FROM** | Open world trapped town (FROM inspired) | 1 | 🟡 Nearly Done | Puzzle connection |
| 3 | **The Cave** | Underground cave level | TBD | 🟡 Nearly Done | Puzzle connection |
| 4 | **Sewers** | Large sewer level — 2 monsters | 2 | 🟡 Nearly Done | Puzzle connection |

---

## 🩸 Concept — الفكرة

```
Embrace the Chaos / عناق الفوضى is a multiplayer horror game
where players progress through 5 unique levels, each with its
own atmosphere, puzzles, and monsters.

From the unsettling yellow rooms of The Meetings to the vast
open town of FROM and the dark depths of the Sewers —
no level feels the same.

عناق الفوضى لعبة رعب متعددة اللاعبين تمر عبر 5 مراحل فريدة،
كل مرحلة لها جوها وألغازها ووحوشها الخاصة.
```

**Fear Pillars / ركائز الخوف:**
1. `Isolation / العزلة — players can be separated`
2. `The Unknown / المجهول — each level feels different`
3. `Helplessness / العجز — limited tools, multiple threats`
4. `Escalation / التصاعد — each level gets harder`

---

---

## 👨‍💻 DEV — البرمجة
### *Owner: Mohammed*

### ⚙️ Core Systems

| System | Status | Notes |
|---|---|---|
| `BP_ProjectChaosGameInstance` | 🟡 In Progress | Reviewing — needs final wiring |
| `BP_GameMode_Lobby` | ✅ Done | Referenced and working |
| `BP_GameMode_Main` | 🟡 In Progress | Needs review |
| `BP_LobbyGameState` | ✅ Done | ConnectedPlayers array working |
| `BP_LobbyPlayerState` | ✅ Done | bIsTalking replicated |
| `PC_Lobby` | 🟡 In Progress | SettingUp works — full review pending |
| `BP_LobbyManager` | ✅ Done | LobbyCamera working |

### 🌐 Multiplayer / الشبكة

| System | Status | Notes |
|---|---|---|
| Create Session / `StartHostSession` | ✅ Done | Password + ServerName + ExtraSettings |
| Find Sessions / `FindSessions` | ✅ Done | Working |
| Join by Code / `JoinSessionByCode` | ✅ Done | Password verified via ExtraSettings |
| Join by Browser / `Join Session Event` | ✅ Done | Working |
| Password Verification | ✅ Done | GetSessionPropertyString |
| Leave Session | ✅ Done | DestroySession → ServerTravel |
| Kick Player | ✅ Done | Working |
| Friend Invite | ✅ Done | OnSessionInviteAccepted |
| Voice Chat State | ✅ Done | bIsTalking per player |
| Network Error Handler | ✅ Done | Alt+F4 handled |
| Steam Integration | ✅ Done | Live on Steam — tested |
| Loading Screen | ✅ Done | Auto-removes after travel |
| Error Message UI | ✅ Done | Custom text, auto-removes |

### 🟡 GameInstance — Stubs (Not Yet Implemented)

| Function | Priority | Notes |
|---|---|---|
| `GetSelectedCharacter` | 🟡 Medium | Empty stub |
| `SetServerSettings` | 🟡 Medium | Empty stub |
| `LoadSaveData` | 🟡 Medium | Empty stub |
| `ApplyGameSettings` | 🟡 Medium | Empty stub |

### ❌ Missing in GameInstance

| Feature | Priority | Notes |
|---|---|---|
| Player Name storage | 🔴 High | Passed in but never saved |
| Selected Map storage | 🔴 High | Host needs to pick level |
| Max Players from UI | 🟡 Medium | Variable exists, not set from UI |
| Travel to Gameplay Map | 🔴 High | Travels to Lobby ✅ not game levels yet |
| Level Progression Logic | 🔴 High | 0 → 1 → 2 → 3 → 4 flow needed |

### 🖥️ UI Systems

| Widget | Status | Notes |
|---|---|---|
| `WBP_MainWrapper` | 🟡 In Progress | Navigation works — compile warnings pending |
| `WBP_Start` | 🟡 In Progress | Buttons not wired to GameInstance yet |
| `WBP_HostMenu` | 🟡 In Progress | ⚠️ Host button NOT wired to GI |
| `WBP_JoinMenu` | 🟡 In Progress | ⚠️ Join button NOT wired to GI |
| `WBP_Continue` | 🟡 In Progress | Purpose needs clarifying |
| `WBP_Settings` | 🟡 In Progress | Exists — logic not implemented |
| `WBP_Credits` | 🟡 In Progress | Exists — content not added |
| `WBP_Loading` | ✅ Done | Working |
| `WBP_ErrorMessage` | ✅ Done | Working |

### 🐛 Known Bugs / الأخطاء

| # | Bug | Severity | Status |
|---|---|---|---|
| 1 | Character shivering animation on join (client + host side) | 🔴 High | ⬜ Deferred — fix after code review |
| 2 | Road_1 folder broken redirectors | 🔴 High | 🟡 In Progress |
| 3 | `ProjectCleaner` incompatible with UE5.6 | 🟡 Medium | ⬜ Disable it |
| 4 | `bodyShapeG_CombinedSkelMesh` material index errors | 🟡 Medium | ⬜ |
| 5 | Character BPs missing GeneratedClass tags | 🟡 Medium | ⬜ |
| 6 | `CheckSession` compile warning | 🟡 Medium | ⬜ |
| 7 | Multiple compile warnings in WBP widgets | 🟡 Medium | ⬜ Fix during review |

---

---

## 🎨 DESIGNER — تصميم الخرائط
### *Owner: Abdullah*

### 🗺️ Level Details

**Level 0 — The Meetings**
```
Aesthetic:   Backroom yellow rooms
Monsters:    TBD
Status:      Nearly complete — puzzles need connecting
```

**Level 1 — Astray**
```
Aesthetic:   Backrooms style — darker, deeper
Monsters:    Multiple
Puzzles:     Multiple — need connecting
Status:      Nearly complete
```

**Level 2 — FROM**
```
Aesthetic:   Open world trapped town (FROM TV show inspired)
Map Size:    12 x 12
Monsters:    6 Slow Creature per Player + 2 Main Creatures are player speed
Streaming:   Level Streaming + HLOD
Status:      Nearly complete — puzzles need connecting
```

```
Zone Layout:
┌─────────────────────────────────┐
│      🌲 DARK FOREST (North)     │
├──────────┬──────────┬───────────┤
│ 🌲 West  │ 🏘️ TOWN  │ 🌲 East  │
│  Woods   │  CENTER  │  + Cave  │
├──────────┴──────────┴───────────┤
│       🏘️ MAIN TOWN STREET       │
├─────────────────────────────────┤
│       🌾 SOUTH FIELDS           │
└─────────────────────────────────┘
```

**Level 3 — The Cave**
```
Aesthetic:   Underground cave
Monsters:    TBD
Status:      Nearly complete — puzzles need connecting
```

**Level 4 — Sewers**
```
Aesthetic:   Large sewer system
Monsters:    2 monsters
Status:      Nearly complete — puzzles need connecting
```

### 🧟 Characters & Assets

| Asset | Status | Notes |
|---|---|---|
| Survivor Characters | 🟡 In Progress | techwearOutfit exists |
| Monster Lvl 0-1 | ⬜ | — |
| Monster Lvl 2 (FROM) | ⬜ | — |
| Monster Lvl 3 (Cave) | ⬜ | — |
| Monster Lvl 4-A (Sewers) | ⬜ | — |
| Monster Lvl 4-B (Sewers) | ⬜ | — |

---

---

## 👥 SHARED — مشترك

### 🔗 Level Progression — تسلسل المراحل

```
Lobby → Level 0 → Level 1 → Level 2 → Level 3 → Level 4
         Meetings   Astray     FROM      Cave      Sewers
```

- [ ] Travel from Lobby → Level 0
- [ ] Travel Level 0 → Level 1 (on puzzle complete)
- [ ] Travel Level 1 → Level 2 (on puzzle complete)
- [ ] Travel Level 2 → Level 3 (on puzzle complete)
- [ ] Travel Level 3 → Level 4 (on puzzle complete)
- [ ] Win condition on Level 4 complete

### 🔊 Audio / الصوت

| Track / Sound | Status |
|---|---|
| UI Button Sound | ✅ `SW_Button` wired |
| Proximity Voice Chat | ✅ Enabled |
| All other audio | ⬜ Not Started |

### 🧪 Testing / الاختبار

| Test | Status | Notes |
|---|---|---|
| Steam — 2 PCs | ✅ Tested | Some issues found (animation) |
| Animation shiver bug | ⬜ Deferred | Fix after code review |
| Level 0 MP test | ⬜ | — |
| Level 1 MP test | ⬜ | — |
| Level 2 MP test | ⬜ | — |
| Level 3 MP test | ⬜ | — |
| Level 4 MP test | ⬜ | — |
| Full run-through all levels | ⬜ | — |

---

## 📓 Dev Log — يوميات التطوير

| Date | Version | Who | Update |
|---|---|---|---|
| `2026-05-14` | `v0.1` | Mohammed | Crash from BulkData corruption — 327 assets loaded at once |
| `2026-05-14` | `v0.1` | Mohammed | Identified Road_1 folder as broken redirectors source |
| `2026-05-14` | `v0.1` | Mohammed | Full GameInstance review — session logic ~70% wired |
| `2026-05-14` | `v0.1` | Mohammed | WBP_MainWrapper review — navigation done, buttons not wired |
| `2026-05-15` | `v0.1` | Mohammed | Full code review day — comments only, no coding - 🟡 In Progress |
| '2026-05-16' | 'v0.1' | Mohammed | Rebuidng the core logic GI,GM and PS

---

## ⚙️ Project Setup

```
Game Name:      Embrace the Chaos / عناق الفوضى
Engine:         UE 5.6.1
Epic Username:  W.O.L.F.Labs
Project:        E:/Creating_Games/Unreal/ProjectChaos/
Game Instance:  GI_EmbraceTheChoas
Default Map:    StartUp
Lobby Map:      /Game/DESIGN_Abdullah/Map/Lobby/Main/Lobby_Main.Lobby_Main
Level 0:        /Game/DESIGN_Abdullah/Map/Main_Mpas/Level_0_TheMeeting/Level_01.Level_01
Level 1:        /Game/DESIGN_Abdullah/Map/Main_Mpas/Level_1_Backrooms/L_Backrooms.L_Backrooms
Level 2:        /Game/DESIGN_Abdullah/Map/Main_Mpas/Level_2_From/L_From
Level 3:        /Game/DESIGN_Abdullah/Map/Main_Mpas/Level_3_Cave/L_Cave_Main.L_Cave_Main
Level 4:        /Game/DESIGN_Abdullah/Map/Main_Mpas/Level_4_Sewers/L_Sewres.L_Sewres

Plugins:
  ✅ Advanced Sessions
  ✅ EOS / Steam
```

---

## 🔗 Links

| | Link |
|---|---|
| 📁 Game Source (Diversion) | Not Public |
| 📊 Progress (GitHub) | `https://github.com/mohammeddevOG/ProjectChaos-Progress/` |
| 🎮 Steam Page | `https://store.steampowered.com/app/3918400/Embrace_the_Chaos/` |
| 💬 Discord | 🟡 In Progress |

---

<div align="center">

```
█████████████████████████████████████
█   FIVE LEVELS. ONE WAY IN.        █
█   NO WAY OUT.                     █
█   EMBRACE THE CHAOS.  👁️          █
█████████████████████████████████████
```

*Embrace the Chaos / عناق الفوضى*
*Built by W.O.L.F.Labs — UE 5.6*

</div>
