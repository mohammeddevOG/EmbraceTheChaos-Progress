# 👻 ProjectChaos — Dev Progress
# سجل تطوير بروجكت كيوس

> **Game Name / اسم اللعبة:** `Embrace The Choas`
> **Inspired By / مستوحى من:** `Backrooms and FROM TV SHOW`
> **Engine:** `Unreal Engine 5.6`
> **Genre:** `Horror · Multiplayer`
> **Network:** `Online — Advanced Sessions Plugin`
> **Source Control / تحكم المصدر:** `Diversion (Game Files) · GitHub (Progress)`
> **Team:** `Mohammed — Dev 👨‍💻` · `Abdullah — Map Designer 🎨`
> **Started / البدء:** `2025`
> **Target / الهدف:** `[30/07/2026]`

---

## 📊 Overall Progress — التقدم الكلي

| Phase / المرحلة | Owner | Status | Progress |
|---|---|---|---|
| Core Programming / البرمجة | 👨‍💻 Mohammed | 🟡 In Progress | `██████░░░░ 60%` |
| Multiplayer / الشبكة | 👨‍💻 Mohammed | 🟡 In Progress | `███████░░░ 70%` |
| Monster AI / الذكاء الاصطناعي | 👨‍💻 Mohammed | ⬜ Not Started | `░░░░░░░░░░ 0%` |
| UI / الواجهة | 👨‍💻 Mohammed | 🟡 In Progress | `██████░░░░ 60%` |
| Maps & Environments / الخرائط | 🎨 Abdullah | 🟡 In Progress | `███░░░░░░░ 30%` |
| Lighting & Atmosphere / الجو | 🎨 Abdullah | 🟡 In Progress | `██░░░░░░░░ 20%` |
| Audio / الصوت | 👥 Both | ⬜ Not Started | `░░░░░░░░░░ 0%` |
| Testing & Release / الاختبار | 👥 Both | ⬜ Not Started | `░░░░░░░░░░ 0%` |

> `✅ Done` · `🟡 In Progress` · `⬜ Not Started` · `🔴 Blocked`

---

## 🏁 Milestones — المراحل

| # | Milestone / الهدف | Deadline | Status |
|---|---|---|---|
| 1 | GameInstance Complete / انتهاء الجيم انستنس | `[Date]` | 🟡 |
| 2 | First Playable Lobby / لوبي قابل للعب | `[Date]` | ⬜ |
| 3 | Multiplayer Working End-to-End / شبكة تعمل | `[Date]` | ⬜ |
| 4 | First Playable Map / أول خريطة قابلة للعب | `[Date]` | ⬜ |
| 5 | Alpha Build / ألفا | `[Date]` | ⬜ |
| 6 | Beta Playtest / بيتا | `[Date]` | ⬜ |
| 7 | Release / الإطلاق 🚀 | `[Date]` | ⬜ |

---

## 🩸 Concept — الفكرة

```
Multiplayer horror game inspired by the TV show FROM.
Players are trapped in a mysterious town with no way out.
Survivors must complete objectives while a monster hunts them.

لعبة رعب متعددة اللاعبين مستوحاة من مسلسل FROM.
اللاعبون محاصرون في بلدة غامضة لا مخرج منها.
الناجون يجب أن يكملوا المهام بينما الوحش يطاردهم.
```

**Fear Pillars / ركائز الخوف:**
1. `Isolation / العزلة — players can be separated`
2. `The Unknown / المجهول — monster not always visible`
3. `Helplessness / العجز — limited tools and resources`

---

---

## 👨‍💻 DEV — البرمجة
### *Owner: Mohammed*

### ⚙️ Core Systems

| System | Status | Notes |
|---|---|---|
| `BP_ProjectChaosGameInstance` | 🟡 In Progress | Reviewing — needs final wiring |
| `BP_GameMode_Lobby` | ✅ Done | Referenced in GameInstance |
| `BP_GameMode_Main` | 🟡 In Progress | Needs review |
| `BP_LobbyGameState` | ✅ Done | ConnectedPlayers array working |
| `BP_LobbyPlayerState` | ✅ Done | bIsTalking replicated |
| `PC_Lobby` | 🟡 In Progress | SettingUp function works — needs review |
| `BP_LobbyManager` | ✅ Done | LobbyCamera referenced in PC |

### 🌐 Multiplayer / الشبكة

| System | Status | Notes |
|---|---|---|
| Create Session / `StartHostSession` | ✅ Done | Password + ServerName + ExtraSettings |
| Find Sessions / `FindSessions` | ✅ Done | Max 5000 results |
| Join by Code / `JoinSessionByCode` | ✅ Done | Finds session then password checks |
| Join by Browser / `Join Session Event` | ✅ Done | Checks password via ExtraSettings |
| Password Verification / التحقق | ✅ Done | GetSessionPropertyString comparison |
| Leave Session / `LeaveSession` | ✅ Done | DestroySession → ServerTravel StartUp |
| Kick Player / `KickAPlayer` | ✅ Done | DestroySession for target PC |
| Friend Invite / `OnSessionInviteAccepted` | ✅ Done | JoinSession on accept |
| Session Code Generation | ✅ Done | Stored as ExtraSettings |
| MoveDataToGS | ✅ Done | Passes ServerName + Code to GameState |
| Network Error Handler | ✅ Done | Alt+F4 → DestroySession → OpenLevel |
| Voice Chat State / `OnPlayerTalkingStateChanged` | ✅ Done | bIsTalking set per player in GameState |
| Server Travel to Lobby | ✅ Done | `/Game/Map/Lobby/Main/Lobby_Main?listen` |

### 🟡 GameInstance — Stubs (Not Yet Implemented)

| Function | Status | Notes |
|---|---|---|
| `GetSelectedCharacter` | 🟡 Stub | Empty — needs character selection logic |
| `SetServerSettings` | 🟡 Stub | Empty — needs max players / map choice |
| `LoadSaveData` | 🟡 Stub | Empty — needs save game integration |
| `ApplyGameSettings` | 🟡 Stub | Empty — needs graphics/audio settings |

### ❌ Missing in GameInstance

| Feature | Priority | Notes |
|---|---|---|
| Player Name storage | 🔴 High | Passed in but never saved to variable |
| Selected Map storage | 🔴 High | Host picks map — where is it stored? |
| Max Players exposed | 🟡 Medium | `PublicConnectionsMax` exists but never set from UI |
| Travel to Gameplay Map | 🔴 High | Travels to Lobby ✅ but not to actual game map |

### 🖥️ UI Systems

| Widget | Status | Notes |
|---|---|---|
| `WBP_MainWrapper` | 🟡 In Progress | Navigation works — needs compile warnings fixed |
| `WBP_Start` | 🟡 In Progress | Main menu screen — buttons need GI wiring |
| `WBP_HostMenu` | 🟡 In Progress | ⚠️ Host button NOT wired to GameInstance yet |
| `WBP_JoinMenu` | 🟡 In Progress | ⚠️ Join button NOT wired to GameInstance yet |
| `WBP_Continue` | 🟡 In Progress | Purpose unclear — possibly JoinByCode screen |
| `WBP_Settings` | 🟡 In Progress | Exists — settings logic not implemented |
| `WBP_Credits` | 🟡 In Progress | Exists — content not added |
| `WBP_Loading` | ✅ Done | Loading screen with auto-remove |
| `WBP_ErrorMessage` | ✅ Done | Shows custom error text, auto-removes |
| `WBP_JoinBySessionCode` | 🟡 In Progress | Referenced — status unclear |

### ⚠️ Known Widget Issues

| Issue | Widget | Fix |
|---|---|---|
| ErrorType=1 warning | `WBP_JoinMenu` variable refs | Compile and check |
| ErrorType=1 warning | `WBP_HostMenu` CreateWidget | Compile and check |
| ErrorType=1 warning | `WBP_Continue` CreateWidget | Compile and check |
| ErrorType=1 warning | `SwitchToSettingMenu` event | Compile and check |

### 🤖 Monster AI — الذكاء الاصطناعي

| Feature | Status | Notes |
|---|---|---|
| Behavior Tree | ⬜ Not Started | — |
| Patrol System | ⬜ Not Started | — |
| Detection (Sight/Sound) | ⬜ Not Started | — |
| Chase Logic | ⬜ Not Started | — |
| Attack Logic | ⬜ Not Started | — |
| Difficulty Scaling | ⬜ Not Started | — |

### 🐛 Known Bugs / الأخطاء

| # | Bug | Severity | Fixed? |
|---|---|---|---|
| 1 | `ProjectCleaner` plugin incompatible with UE5.6 | 🟡 Medium | ⬜ Disable it |
| 2 | `bodyShapeG_CombinedSkelMesh` material index errors LOD 0-3 | 🟡 Medium | ⬜ Reset material slots |
| 3 | Road_1 folder has broken redirectors | 🔴 High | 🟡 In Progress |
| 4 | Character BPs missing GeneratedClass tags (BP_Male01-04, BP_Female01-04) | 🟡 Medium | ⬜ |
| 5 | `CheckSession` function has compile warning | 🟡 Medium | ⬜ |
| 6 | `GetSelectedCharacter` event has ErrorType=1 | 🟡 Medium | ⬜ Implement logic |

---

---

## 🎨 DESIGNER — تصميم الخرائط
### *Owner: Abdullah*

### 🗺️ Maps / الخرائط

| Map | Inspired By | Blockout | Art Pass | Lighting | Optimized | Done |
|---|---|---|---|---|---|---|
| `L_From` | FROM TV Show town | 🟡 | ⬜ | ⬜ | ⬜ | ⬜ |
| `Lobby_Main` | — | ✅ | 🟡 | 🟡 | ⬜ | ⬜ |
| `StartUp` | — | ✅ | ⬜ | ⬜ | ⬜ | ⬜ |

### 📐 L_From Map — Technical Specs

```
Landscape Size:     2017 x 2017
Section Size:       63 x 63 quads
Sections/Component: 2 x 2
Components:         16 x 16 (256 total)
Scale:              X:100, Y:100, Z:100
Real World Size:    ~2km x 2km
Player Cross Time:  ~5.6 min (at 600 cm/s)
Streaming:          Level Streaming + HLOD
```

### 🗺️ L_From Zone Plan

```
┌─────────────────────────────────┐
│      🌲 DARK FOREST (North)     │
│         Monster Territory       │
├──────────┬──────────┬───────────┤
│ 🌲 West  │ 🏘️ TOWN  │ 🌲 East  │
│  Woods   │  CENTER  │  Forest  │
│          │  (Open)  │  + Cave  │
├──────────┴──────────┴───────────┤
│       🏘️ MAIN TOWN STREET       │
│      Buildings / Spawn Area     │
├─────────────────────────────────┤
│    🌾 SOUTH FIELDS (Danger)     │
└─────────────────────────────────┘
```

### 💡 Lighting & Atmosphere / الإضاءة

- [ ] Lumen GI configured / إعداد لومن
- [ ] Volumetric fog / الضباب الحجمي
- [ ] Dynamic shadows / الظلال الديناميكية
- [ ] Candles / lanterns / الشموع والفوانيس
- [ ] Jump scare lighting / إضاءة المفزعات
- [ ] Post-process color grade / معالجة الألوان
- [ ] Landscape material fixed (sRGB issue on roughness maps) ⬜

### 🧟 Characters & Assets

| Asset | Concept | Modeled | Textured | Rigged | In-Engine |
|---|---|---|---|---|---|
| Survivor 1 | ⬜ | ⬜ | ⬜ | ⬜ | ⬜ |
| Survivor 2 | ⬜ | ⬜ | ⬜ | ⬜ | ⬜ |
| Monster / الوحش | ⬜ | ⬜ | ⬜ | ⬜ | ⬜ |
| techwearOutfit (existing) | ✅ | ✅ | 🟡 | ✅ | 🟡 |

---

---

## 👥 SHARED — مشترك

### 🔊 Audio / الصوت

| Track / Sound | Status | Notes |
|---|---|---|
| Main Menu Theme | ⬜ | — |
| Lobby Music | ⬜ | — |
| Explore Phase (calm dread) | ⬜ | — |
| Chase Music | ⬜ | — |
| Monster Sounds | ⬜ | — |
| Footsteps | ⬜ | — |
| Heartbeat (near monster) | ⬜ | — |
| Ambient / Environment | ⬜ | — |
| Jump Scare Stingers | ⬜ | — |
| UI Button Sound | ✅ | `SW_Button` — wired to back button |
| 3D Spatial Audio | ⬜ | — |
| Proximity Voice Chat | ✅ | `bUseLobbiesVoiceChatIfAvailable = true` |

### 🧪 Testing / الاختبار

| Test | Status | Notes |
|---|---|---|
| NULL subsystem — 2 windows local | ⬜ | Next step after GameInstance complete |
| NULL subsystem — LAN | ⬜ | — |
| Steam — 2 PCs | ⬜ | Use SpaceWar AppID 480 for testing |
| High latency test (200ms+) | ⬜ | — |
| Disconnect / Alt+F4 handling | ✅ | Handled in GameInstance |

**Playtest Log:**

| Date | Version | Fun /5 | Scary /5 | Notes |
|---|---|---|---|---|
| — | — | — | — | — |

### 🚀 Release / الإطلاق

- [ ] Final UE5 shipping build
- [ ] Dedicated server build
- [ ] Steam / EOS configured
- [ ] Store page + trailer
- [ ] Age rating
- [ ] Post-launch patch plan

---

## 📓 Dev Log — يوميات التطوير

| Date | Version | Who | Update |
|---|---|---|---|
| `2026-05-14` | `v0.1` | Mohammed | Investigated crash from BulkData corruption — cause: loading 327 assets at once after redirector fix |
| `2026-05-14` | `v0.1` | Mohammed | Identified Road_1 folder as broken redirector source |
| `2026-05-14` | `v0.1` | Mohammed | Reviewed full GameInstance — session logic ~90% complete |
| `2026-05-14` | `v0.1` | Mohammed | Reviewed WBP_MainWrapper — navigation system complete, buttons not wired to GI yet |
| `2026-05-15` | `v0.1` | Mohammed | Full code review day — writing comments, no coding |

---

## 💡 Ideas — أفكار

| Idea | Owner | Priority |
|---|---|---|
| Proximity voice chat (players hear each other spatially) | Both | 🔴 High |
| Monster can hear player voice chat | Mohammed | 🟡 Medium |
| Session code shown in lobby so friends can join | Mohammed | 🔴 High |
| Town name never revealed (like FROM) — adds mystery | Both | 🟡 Medium |
| Jump scare lighting rig per zone | Abdullah | 🟡 Medium |

---

## ⚙️ Project Setup Notes

```
Engine Version:     UE 5.6.1
Epic Username:      W.O.L.F.Labs
Project Path:       E:/Creating_Games/Unreal/ProjectChaos/
Game Instance:      BP_ProjectChaosGameInstance
Default Map:        StartUp
Lobby Map:          /Game/Map/Lobby/Main/Lobby_Main
Gameplay Map:       /Game/Map/StartUp (placeholder)
Designer Map:       /Game/DESIGN_Abdullah/Map/Main_Mpas/Level_2_From/L_From

Plugins:
  ✅ Advanced Sessions
  ✅ EOS (Epic Online Services)
  ⚠️ ProjectCleaner — INCOMPATIBLE with 5.6 — DISABLE IT
```

---

## 🔗 Links — الروابط

| | Link |
|---|---|
| 📁 Game Source (Diversion) | `[Diversion URL]` |
| 📊 Progress (GitHub) | `[GitHub URL]` |
| 💬 Discord | `[Invite URL]` |

---

<div align="center">

```
█████████████████████████████████████
█  THE TOWN HAS NO NAME.            █
█  NO ONE KNOWS HOW THEY GOT HERE.  █
█  NO ONE HAS EVER LEFT.  👁️        █
█████████████████████████████████████
```

*Built with fear & Unreal Engine 5.6 — W.O.L.F.Labs*
*صُنع بالخوف وأنريل إنجن 5.6 — ولف لابز*

</div>
