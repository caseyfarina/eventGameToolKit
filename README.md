# Event Game Toolkit

**Version 1.2.0** | Unity 6+

An educational Unity toolkit designed for the "Animation and Interactivity" class. Provides modular, no-code components using UnityEvents to create interactive experiences without writing code.

## Overview

The Event Game Toolkit is built around an **event-driven architecture** where students visually connect components in the Unity Inspector using UnityEvents. This enables complex interactive behaviors without requiring programming knowledge.

### Core Philosophy

- **Input Components** (Event Sources) — Detect events like key presses, collisions, mouse clicks
- **Action Components** (Event Targets) — Perform actions when triggered (spawn, display, animate)
- **UnityEvents** — Visual connections in the Inspector that wire behaviors together

### What's Included

- **54 educational scripts** (100% XML-documented)
- **21 custom Inspector editors** with conditional field visibility
- **11 example scene generators** (Tools > Examples menu)
- **Comprehensive documentation** system
- **DOTween integration** for professional animations

---

## Installation

### Method 1: Git URL (Recommended)

1. Open Unity 6 Package Manager (**Window > Package Manager**)
2. Click **+ (plus icon)** in top-left
3. Select **Add package from git URL...**
4. Enter: `https://github.com/caseyfarina/eventGameToolKit.git`
5. Click **Add**

### Method 2: Local Installation

1. Clone this repository
2. In Unity Package Manager, click **+ > Add package from disk...**
3. Navigate to the cloned folder and select `package.json`

---

## Components Library

### Input Components (Event Sources)
Located in `Runtime/Input/`

- **InputTriggerZone** — 3D collision detection with tag filtering
- **InputKeyPress** — Key press and hold events
- **InputKeyCountdown** — Press a key N times to trigger an event
- **InputCheckpointZone** — Saves a checkpoint when the player enters
- **InputMouseInteraction** — Click and hover on 3D objects (free cursor)
- **InputFPMouseInteraction** — Click and hover in first-person (locked cursor)
- **InputOnStart** — Fire events at scene start (Awake or Start, with optional delay)
- **InputQuitGame** — Application quit handler
- **InputClickDrag** — Click and drag objects on a constrained plane, with optional grid snapping, limits, and damping
- **InputClickRotate** — Click and drag to rotate objects around an axis, with optional angle snapping, limits, and damping

### Action Components (Event Targets)
Located in `Runtime/Actions/`

**Object Management:**
- **ActionSpawnObject** — Spawn single objects
- **ActionAutoSpawner** — Automatic spawning with random timing
- **ActionRespawnPlayer** — Player respawn system

**Events:**
- **ActionRandomEvent** — Fires one of several UnityEvents chosen at random, with configurable per-entry weights
- **ActionShuffleEvent** — Fires UnityEvents in a shuffled order, cycling through all entries before reshuffling

**UI & Display:**
- **ActionDisplayText** — Text display with DOTween animations
- **ActionDisplayImage** — Image fading and scaling with DOTween
- **ActionDialogueSequence** — Complete dialogue / visual novel system with typewriter effect and branching decisions
- **DialogueUIController** — Dialogue UI management

**Decal Animation System:**
- **ActionDecalSequence** — Frame-by-frame URP decal animation
- **ActionDecalSequenceLibrary** — Manage multiple decal sequences
- **ActionBlinkDecal** — Automatic blinking (material-based)
- **ActionBlinkDecalOptimized** — Optimized blinking (texture-based)

**Scene & Animation:**
- **ActionRestartScene** — Scene restart with optional fade
- **ActionTeleportToTransform** — Teleport an object to a target transform
- **ActionAnimateTransform** — DOTween-based transform animation with AnimationCurve support
- **ActionEmissionAnimation** — Animate material emission for glowing effects
- **ActionPlaySound** — Audio playback with randomized volume and pitch
- **ActionTriggerAnimatorParameter** — Set Animator parameters via events
- **ActionPlayCharacterEmoteAnimation** — Play emote animations on the character controller

### Physics Systems
Located in `Runtime/Physics/` and `Runtime/CharacterControllers/`

**Player Controllers:**
- **CharacterControllerCC** — Advanced humanoid controller with moving platforms, slopes, dodge, and checkpoint spawning
- **PhysicsBallPlayerController** — Simple physics ball controller
- **PhysicsCharacterController** — Rigidbody-based character controller

**AI Controllers:**
- **PhysicsEnemyController** — AI chase behavior with configurable jump modes
- **EnemyControllerCC** — CharacterController-based AI enemy

**Physics Effects:**
- **PhysicsBumper** — Bumper with configurable force and DOTween feedback
- **PhysicsBumperTag** — Tag-filtered bumper variant
- **PhysicsPlatformStick** — Moving platform parent attachment
- **PhysicsPlatformAnimator** — Waypoint-based platform animation with easing, loop, and ping-pong modes
- **CharacterPushRigidBody** — Lets the character controller push Rigidbody objects

### Game Management
Located in `Runtime/Game/`

- **GameStateManager** — Pause and victory state management
- **GameTimerManager** — Count-up / countdown timer with self-contained UI (clock text + fill bar, both with gradient color)
- **GameHealthManager** — Health system with thresholds, events, and optional self-contained UI
- **GameCollectionManager** — Score / collection tracking with optional self-contained UI
- **GameInventoryManager** — Multi-slot inventory with per-slot capacity limits and events; optional self-contained UI row of icon + count cards
- **GameUIManager** — Centralized UI data display with DOTween animations
- **GameAudioManager** — Audio system with mixer integration
- **GameCameraManager** — Cinemachine camera switching
- **GameCheckpointManager** — Persistent checkpoint system (survives scene reloads via DontDestroyOnLoad)

> **Self-contained UI:** GameHealthManager, GameCollectionManager, GameTimerManager, and GameInventoryManager all support an optional built-in Canvas — no GameUIManager required. Enable `showUI` in the Inspector.

### Puzzle System
Located in `Runtime/Puzzle/`

- **PuzzleSwitch** — Multi-state switch component (cycles through N states)
- **PuzzleSwitchChecker** — Validates switch combinations with automatic or manual checking modes

### Animation
Located in `Runtime/Animation/`

- **ActionAnimateTransform** — DOTween-based position, rotation, and scale animation with AnimationCurve support

### UI Components
Located in `Runtime/UI/`

- **FadeInFromBlackOnRestart** — Automatic fade-from-black on scene load

---

## Documentation

### Auto-Generated Documentation
The package includes a **Script Documentation Generator** accessible via **Tools > Script Documentation Generator**. This creates an interactive Canvas-based UI showing all components organized by category with their functions and events.

### Example Scene Generators
Generate example scenes demonstrating each system via **Tools > Examples** menu:

- Physics Bumper Example
- Character Controller Example
- Enemy Controller Example
- Collection System Example
- Health System Example
- Timer System Example
- Inventory System Example
- Checkpoint System Example
- Trigger Zone Example
- Auto Spawner Example
- Puzzle System Example

### External Documentation
- **CharacterControllerCC_Documentation.md** — Complete setup guide with Quick Start
- **DecalAnimationSystem_Documentation.md** — Complete URP decal guide
- **GameUI_QuickStart.md** — Guide to self-contained UI vs. GameUIManager

---

## Educational Use

### Learning Outcomes

Students will understand:
- Event-driven programming concepts
- Component-based architecture
- Physics and animation principles
- Systems thinking for interactive design

### No-Code Approach

Students create complex interactions by:
1. Adding components to GameObjects
2. Configuring settings in the Inspector
3. Connecting UnityEvents visually
4. Testing and iterating

**Example Flow:**
```
InputTriggerZone (detects player)
  → onTriggerEnter
    → ActionSpawnObject.SpawnSinglePrefab() (spawns enemy)

InputClickDrag (drag a puzzle piece)
  → onDragEnd
    → PuzzleSwitchChecker.CheckPuzzle()
```

---

## Technical Requirements

- **Unity Version:** Unity 6 (6000.0.0f1 or later)
- **Render Pipeline:** Universal Render Pipeline (URP) 17.0.3+
- **Required Packages:**
  - Input System 1.11.2+
  - TextMeshPro 3.0.6+
  - Cinemachine 3.1.2+
  - DOTween FREE

---

## Code Conventions

### Naming Pattern
Scripts follow educational naming:
- **Input**[Purpose] — Event sources (e.g., `InputKeyPress`, `InputClickDrag`)
- **Action**[Purpose] — Event targets (e.g., `ActionSpawnObject`, `ActionRandomEvent`)
- **Physics**[Purpose] — Movement systems (e.g., `PhysicsBumper`)
- **Game**[Purpose] — Game managers (e.g., `GameHealthManager`, `GameInventoryManager`)

### XML Documentation
All 54 educational scripts include XML documentation comments:
```csharp
/// <summary>
/// Detects when objects with specific tags enter a trigger zone and fires events
/// </summary>
public class InputTriggerZone : MonoBehaviour
```

---

## Updates

Students can update the package to get new features and bug fixes:

1. Open Package Manager
2. Find "Event Game Toolkit" in the list
3. Click **Update** button when available

---

## Version History

### 1.2.0
- **New:** `InputClickDrag` — click-and-drag with plane constraints, grid snapping, limits, and damping
- **New:** `InputClickRotate` — click-and-drag rotation with axis constraints, angle snapping, limits, and damping
- **New:** `GameInventoryManager` — multi-slot inventory replacing `GameInventorySlot`; optional self-contained card UI
- **New:** `ActionRandomEvent` — weighted random event selection
- **New:** `ActionShuffleEvent` — shuffled event queue with cycle tracking
- **New:** `InputFPMouseInteraction` — first-person mouse interaction (locked cursor)
- **New:** `InputOnStart` — fire events at scene initialization (Awake / Start)
- **Fixed:** `PuzzleSwitchChecker` — RemoveListener with lambdas was always a no-op; replaced with named method
- **Fixed:** `ActionDialogueSequence` — skipping a typewriter tween via direct TMP property was overwritten by DOTween each frame
- **Fixed:** `GameCheckpointManager` — RestoreAll double-fired restore events
- **Fixed:** `PhysicsPlatformAnimator` — division by zero when totalAnimationTime was 0
- **Fixed:** `CharacterControllerCC` — dead ISpawnPointProvider array cast always returned null

### 1.0.0
- Initial release with 46 educational components

---

## Credits

**Author:** Casey Farina
**Course:** Animation and Interactivity
**Powered by:** DOTween FREE, Unity 6, URP

---

## Support

- **Component Reference:** Use the Script Documentation Generator (Tools menu)
- **Example Scenes:** Generate examples via Tools > Examples menu
- **Instructor Help:** Contact Casey Farina
