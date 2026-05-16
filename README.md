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

## 📖 Story — القصة

```
You wake up.

No memory. No explanation. No way out — at least not yet.

Five places. Each darker than the last.
Someone — or something — put you here.
And the only way forward is through.

Alone you won't make it. Together you might.
But the longer you stay, the worse it gets.

Find the exit. Survive what's hunting you.
Embrace the chaos — because you have no choice.

استيقظت.

لا ذكريات. لا تفسير. لا مخرج — على الأقل ليس بعد.

خمسة أماكن. كل واحد أظلم من السابق.
شيء ما — أو شخص ما — وضعك هنا.
والطريق الوحيد للأمام هو المضي قدمًا.

وحدك لن تنجح. معًا ربما تنجح.
لكن كلما طال بقاؤك، ازداد الأمر سوءًا.

ابحث عن المخرج. انجُ مما يطاردك.
عانق الفوضى — لأنه لا خيار لك.
```

**The Connection Between Levels:**
- Levels 0 → 1 are physically connected via elevator
- Levels 1 → 2 → 3 → 4 share the same nightmare logic — different places, same inescapable feeling
- No lore explanation is given. The horror comes from not knowing why.

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

| # | Level Name | Concept | Monsters | Status |
|---|---|---|---|---|
| 0 | **The Meetings** | Backroom yellow aesthetic | Two NightMare Creatures | 🟡 Nearly Done |
| 1 | **Astray** | Backrooms + puzzles + multiple monsters | Joker and SCP096 | 🟡 Nearly Done |
| 2 | **FROM** | Open world trapped town (FROM inspired) | 6 slow + 2 fast per player | 🟡 Nearly Done |
| 3 | **The Cave** | Underground cave level | NightMare + Parasite | 🟡 Nearly Done |
| 4 | **Sewers** | Large sewer level | 1 Brown Maynard + 1 Black | 🟡 Nearly Done |

---

## 🧩 Puzzles — الألغاز

---

### Level 0 — The Meetings
**Puzzle: Lever Activation**
```
Scattered across the yellow rooms are levers — one per connected player.
All levers must be pulled simultaneously (or in sequence) to power the elevator.

The number of levers scales with the number of players in the session.
Solo run = 1 lever. Full lobby = 4 levers.

This forces players to split up and cover the map — separating them,
making each one vulnerable, alone in a room with whatever is watching.

The elevator only opens when all levers are active.
```
| Detail | Value |
|---|---|
| Lever count | = Connected players count |
| Trigger | All levers active → elevator unlocks |
| Risk | Players must split — no safety in numbers |
| Status | ⬜ Not Connected |

---

### Level 1 — Astray
**Puzzle: Three Gates + Run Sequence**
```
The level has three main puzzles that must be solved to unlock the run area.
Each puzzle opens one gate. All three must be open before the run begins.

Once the run area is unlocked, two final puzzles stand between
the players and the exit. These must be solved under pressure —
the monsters don't stop when the run starts.

The run area is a gauntlet. Solve both puzzles. Reach the exit. Don't die.
```
| Detail | Value |
|---|---|
| Phase 1 | 3 puzzles → unlock run area |
| Phase 2 | 2 puzzles inside the run area |
| Trigger | All 5 complete → exit opens |
| Risk | Phase 2 is under active monster pressure |
| Status | ⬜ Puzzle issue — connection pending |

---

### Level 2 — FROM
**Puzzle: Signal Towers (Proposed)**
```
Scattered across the open town are 4 signal towers — each broken, each in
a different zone (North Forest, East, West Woods, Town Center).

Players must find and repair each tower by solving a small interaction
at the base (e.g. connecting wires, entering a code found nearby).

When all 4 towers are active, a signal is sent — the escape route opens
at the town's edge. But activating a tower also alerts nearby monsters.

The open-world nature of FROM means players spread out across the map,
each isolated in their zone, repairing towers while avoiding the 6 slow
creatures and the 2 fast ones that roam unpredictably.
```
| Detail | Value |
|---|---|
| Puzzle count | 4 signal towers across the map |
| Trigger | All 4 active → escape route unlocks |
| Risk | Activating a tower draws monsters |
| Status | ⬜ TBD — proposed concept |

> 💡 **Note:** This is a proposed design. Mohammed and Abdullah to confirm or replace.

---

### Level 3 — The Cave
**Puzzle: Coal Burning (Devour-style)**
```
Deep in the cave are ritual fire pits — cold, dark, dead.
Players must find coal scattered across the cave and carry it
back to the pits, lighting them one by one.

The darkness of the cave means limited visibility.
The monsters that live here are drawn to sound and movement.
Moving fast makes noise. Moving slow wastes time.

When all pits are lit, an ancient mechanism activates —
a stone door grinds open. The way out is through.
```
| Detail | Value |
|---|---|
| Mechanic | Find coal → carry → deposit in pit → light |
| Pit count | TBD (suggested: 3–5 pits) |
| Trigger | All pits lit → stone door opens |
| Risk | Darkness + sound detection monsters |
| Status | ⬜ Concept confirmed — implementation TBD |

> 💡 **Alternative / Addition:** If coal alone feels thin, add a secondary step —
> players need a torch (found item) to actually light each pit.
> Torch is shared. Only one exists. Players coordinate who carries it.

---

### Level 4 — Sewers
**Puzzle: Power Restoration**
```
The sewer system is dead — flooded, dark, and alive with something worse.
Four electrical boxes are spread across different sections of the sewer network.
Each one needs to be manually switched on.

But the sewer isn't just one path. It's a maze.
Players need to navigate the network, find each box, flip it —
then locate the four keys hidden across the level and bring them
to the central generator to complete the circuit and open the exit gate.

The two monsters in the sewers patrol specific sections.
Learning their routes is the difference between surviving and not.
```
| Detail | Value |
|---|---|
| Step 1 | Find and activate 4 electrical boxes |
| Step 2 | Find 4 keys scattered across the level |
| Step 3 | Bring all keys to central generator → exit opens |
| Risk | Maze layout — easy to get lost or cornered |
| Status | ⬜ Designed — connection pending |

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

## 👨‍💻 DEV — البرمجة
### *Owner: Mohammed*

### ⚙️ Core Systems

| System | Status | Notes |
|---|---|---|
| `GI_EmbraceTheChoas` | 🟡 In Progress | Rebuilt — final wiring pending |
| `GM_ProjectChaos` | 🟡 In Progress | SpawnPlayerCharacter, PostLogin, OnPlayerDied, CheckWinCondition done |
| `GS_ProjectChaos` | ✅ Done | Replicated variables set |
| `PS_ProjectChaos` | 🟡 In Progress | Rebuilt from scratch — wiring pending |
| `BP_GameMode_Lobby` | ✅ Done | Referenced and working |
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
| ServerTravel (level progression) | ✅ Done | Via AdvancedSessions plugin |

### 🟡 GameInstance — Stubs (Not Yet Implemented)

| Function | Priority | Notes |
|---|---|---|
| `GetSelectedCharacter` | 🟡 Medium | Empty stub |
| `SetServerSettings` | 🟡 Medium | Empty stub |
| `LoadSaveData` | 🟡 Medium | Empty stub |
| `ApplyGameSettings` | 🟡 Medium | Empty stub |

### ❌ Missing / Pending

| Feature | Priority | Notes |
|---|---|---|
| Player Name storage | 🔴 High | Passed in but never saved |
| Selected Map storage | 🔴 High | Host needs to pick level |
| Max Players from UI | 🟡 Medium | Variable exists, not set from UI |
| PS_ProjectChaos Begin Play wiring | 🔴 High | PCRef, PlayerRef, Player_ID setup |
| Hunt/Help UI (PC_Main) | 🔴 High | Client_ShowHuntOrHelpUI RPC pending |
| OnPlayerDied → CheckWinCondition link | 🔴 High | Final connection needed |
| GS variables connected to GM | 🔴 High | PlayersAlive/Escaped not yet driven from GM |

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

## 🎨 DESIGNER — تصميم الخرائط
### *Owner: Abdullah*

### 🗺️ Level Details

**Level 0 — The Meetings**
```
Aesthetic:   Backroom yellow rooms — wrong exits, familiar geometry, wrong
Monsters:    Two NightMare Creatures
Puzzle:      Lever activation (scales with player count)
Status:      Nearly complete — puzzle connection pending
```

**Level 1 — Astray**
```
Aesthetic:   Backrooms style — darker, deeper, narrower
Monsters:    Joker + SCP096
Puzzle:      3 gate puzzles → run area → 2 final puzzles
Status:      Nearly complete — puzzle issue pending
```

**Level 2 — FROM**
```
Aesthetic:   Open world trapped town (FROM TV show inspired)
Map Size:    12 x 12
Monsters:    6 Slow Creature per Player + 2 Main Creatures (player speed)
Streaming:   Level Streaming + HLOD
Puzzle:      Signal towers (proposed) — TBD
Status:      Nearly complete — puzzle TBD
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
Aesthetic:   Underground cave — dark, tight, disorienting
Monsters:    NightMare Creature + Parasite
Puzzle:      Coal burning (Devour-style) — find coal, light pits
Status:      Nearly complete — puzzle implementation TBD
```

**Level 4 — Sewers**
```
Aesthetic:   Large sewer maze — flooded sections, low visibility
Monsters:    1 Brown Maynard + 1 Black creature
Puzzle:      4 electric boxes + 4 keys → central generator
Status:      Nearly complete — connection pending
```

### 🧟 Characters & Assets

| Asset | Status | Notes |
|---|---|---|
| Survivor Characters | 🟡 In Progress | techwearOutfit exists |
| Monster Lvl 0-1 (NightMare) | ⬜ | — |
| Monster Lvl 1 (Joker + SCP096) | ⬜ | — |
| Monster Lvl 2 (FROM creatures) | ⬜ | — |
| Monster Lvl 3 (NightMare + Parasite) | ⬜ | — |
| Monster Lvl 4 (Maynard x2) | ⬜ | — |

---

## 👥 SHARED — مشترك

### 🔗 Level Progression — تسلسل المراحل

```
Lobby → Level 0 → Level 1 → Level 2 → Level 3 → Level 4
         Meetings   Astray     FROM      Cave      Sewers
```

- [ ] Travel from Lobby → Level 0
- [ ] Travel Level 0 → Level 1 (elevator — lever puzzle complete)
- [ ] Travel Level 1 → Level 2 (all 5 puzzles complete)
- [ ] Travel Level 2 → Level 3 (signal towers complete)
- [ ] Travel Level 3 → Level 4 (all coal pits lit)
- [ ] Win condition on Level 4 complete (generator + keys)

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
| `2026-05-15` | `v0.1` | Mohammed | Full code review day — comments only, no coding |
| `2026-05-16` | `v0.1` | Mohammed | Rebuilt core architecture — GI, GM, GS, PS from scratch. SpawnPlayerCharacter, PostLogin, OnPlayerDied, CheckWinCondition complete. ServerTravel via AdvancedSessions. E_GamePhase and E_PlayerMode enums created. |

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
