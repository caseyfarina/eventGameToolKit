# Event Game Toolkit v1.0.1 - Release Notes

**Release Date:** November 4, 2025
**Tag:** v1.0.1

---

## 📦 What's Included

- **46 educational components** (100% XML-documented)
- **11 example scene generators** (Tools > Examples menu)
- **Comprehensive documentation** (CharacterControllerCC, Decal Animation System)
- **DOTween FREE integration** for professional animations

---

## 🚀 Installation

### Method 1: Git URL (Recommended for Read-Only Use)

```
Window > Package Manager > + > Add from git URL
https://github.com/caseyfarina/eventGameToolKit.git
```

**Pros:** Easy updates via Package Manager
**Cons:** Read-only (can't edit scripts)

### Method 2: Download & Install to Assets (Recommended for Students)

1. Download **"Source code (zip)"** from this release
2. Extract the ZIP file
3. Copy the entire folder to your project's `Assets/eventGameToolKit/` folder
4. Unity will import automatically

**Pros:** Fully editable scripts
**Cons:** Manual updates (replace folder when new version released)

See [UPDATING.md](https://github.com/caseyfarina/eventGameToolKit/blob/main/UPDATING.md) for detailed update instructions.

---

## 📚 Documentation

- **[README.md](https://github.com/caseyfarina/eventGameToolKit/blob/main/README.md)** - Complete component library reference
- **[UPDATING.md](https://github.com/caseyfarina/eventGameToolKit/blob/main/UPDATING.md)** - How to safely update the toolkit (NEW!)
- **[CharacterControllerCC_Documentation.md](https://github.com/caseyfarina/eventGameToolKit/blob/main/Documentation/CharacterControllerCC_Documentation.md)** - 940-line controller setup guide
- **[DecalAnimationSystem_Documentation.md](https://github.com/caseyfarina/eventGameToolKit/blob/main/Documentation/DecalAnimationSystem_Documentation.md)** - 830-line URP decal guide
- **[CLAUDE_STUDENT.md](https://github.com/caseyfarina/eventGameToolKit/blob/main/CLAUDE_STUDENT.md)** - Claude AI assistance guide for students

---

## ✨ Component Library

### Input Components (6 scripts)
Event sources that detect user actions and triggers:
- **InputTriggerZone** - 3D collision detection with tag filtering
- **InputKeyPress** - Simple key press events
- **InputKeyCountdown** - Countdown system with UI display
- **InputCheckpointZone** - Checkpoint trigger system
- **InputMouseInteraction** - Mouse-based interactions
- **InputQuitGame** - Application quit handler

### Action Components (12 scripts)
Event targets that perform actions when triggered:

**Spawning:**
- **ActionSpawnObject** - Spawn single objects
- **ActionAutoSpawner** - Automatic spawning with random timing

**UI & Display:**
- **ActionDisplayText** - Text display with DOTween animations
- **ActionDisplayImage** - Image fading and scaling with DOTween
- **ActionDialogueSequence** - Complete dialogue/visual novel system
- **DialogueUIController** - Dialogue UI management

**Decal Animation System (URP):**
- **ActionDecalSequence** - Frame-by-frame decal animation
- **ActionDecalSequenceLibrary** - Manage multiple decal sequences
- **ActionBlinkDecal** - Automatic blinking (material-based)
- **ActionBlinkDecalOptimized** - Optimized blinking (texture-based)

**Scene & Audio:**
- **ActionRestartScene** - Scene restart functionality
- **ActionPlaySound** - Audio playback

### Physics Systems (7 scripts)

**Player Controllers:**
- **CharacterControllerCC** - Advanced humanoid controller with moving platforms, slopes, dodge mechanics (Unity TPC style)
- **PhysicsBallPlayerController** - Simple physics ball controller
- **PhysicsCharacterController** - Rigidbody-based character controller

**AI Controllers:**
- **PhysicsEnemyController** - AI chase behavior with configurable jump modes
- **EnemyControllerCC** - CharacterController-based AI enemy

**Physics Effects:**
- **PhysicsBumper** - Advanced bumper with DOTween animations
- **PhysicsPlatformStick** - Moving platform attachment

### Game Management (9 scripts)
Complete game systems with event-driven architecture:
- **GameStateManager** - Pause and victory state management
- **GameTimerManager** - Comprehensive timer system (count-up/countdown)
- **GameHealthManager** - Health system with thresholds and events
- **GameCollectionManager** - Score/collection tracking
- **GameInventorySlot** - Inventory management with capacity
- **GameUIManager** - UI data display with DOTween animations
- **GameAudioManager** - Audio system with mixer integration
- **GameCameraManager** - Cinemachine camera switching
- **GameCheckpointManager** - Persistent checkpoint system

### Puzzle System (2 scripts)
Multi-state puzzle components:
- **PuzzleSwitch** - Multi-state switch component
- **PuzzleSwitchChecker** - Verify switch state combinations

### Animation (1 script)
DOTween-based animation:
- **ActionAnimateTransform** - Transform animation with AnimationCurve support (9 properties)

### UI (1 script)
Automatic transitions:
- **FadeInFromBlackOnRestart** - Automatic scene transition fade (works during pause)

---

## 🎓 Educational Features

### No-Code Philosophy
Students create complex interactions by:
1. Adding components to GameObjects
2. Configuring settings in the Inspector
3. Connecting UnityEvents visually
4. Testing and iterating

**Example Flow:**
```
InputTriggerZone (detects player)
  → onTriggerEnterEvent
    → ActionSpawnObject.SpawnSinglePrefab() (spawns enemy)
```

### Learning Outcomes
- Event-driven programming concepts
- Component-based architecture
- Physics and animation principles
- Systems thinking for interactive design

### Auto-Generated Documentation
Access via **Tools > Script Documentation Generator** to generate an interactive Canvas showing all components organized by category with their functions and events.

### Example Scene Generators
Generate working example scenes via **Tools > Examples** menu:
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

---

## 🔧 Technical Requirements

- **Unity Version:** Unity 6 (6000.0.0f1 or later)
- **Render Pipeline:** Universal Render Pipeline (URP) 17.0.3+
- **Required Packages:**
  - Input System 1.11.2+
  - TextMeshPro 3.0.6+
  - Cinemachine 3.1.2+
- **Optional:** DOTween FREE (included in package)

---

## 🆕 What's New in v1.0.1

### New Features
- **UPDATING.md** - Comprehensive update guide for students
- Improved package.json metadata for better Package Manager display

### Documentation Improvements
- Added installation comparison (Git URL vs Assets folder)
- Update instructions for both installation methods
- Troubleshooting section for common update issues

### Bug Fixes
- Fixed ExampleMaterialHelper auto-creation
- Version bump to force Unity package cache refresh

---

## 🔄 Updating from Previous Versions

See [UPDATING.md](https://github.com/caseyfarina/eventGameToolKit/blob/main/UPDATING.md) for complete instructions.

**Quick Summary:**
- **Package Manager users:** Click "Update" button in Package Manager
- **Assets folder users:** Replace `Assets/eventGameToolKit/` folder with new version (Unity closed)

Your work is safe! GameObject components, settings, and UnityEvent connections are all preserved during updates.

---

## 🙏 Credits

**Author:** Casey Farina
**Course:** Animation and Interactivity
**Institution:** [Your Institution]
**Powered by:** DOTween FREE, Unity 6, URP

---

## 📄 License

[Add appropriate license information]

---

## 📞 Support

- **Documentation:** Check README.md and toolkit documentation files
- **Script Reference:** Use Script Documentation Generator (Tools menu)
- **Examples:** Generate via Tools > Examples menu
- **Issues:** Contact your instructor or file an issue on GitHub

---

## 🔗 Links

- **GitHub Repository:** https://github.com/caseyfarina/eventGameToolKit
- **Installation Guide:** See README.md
- **Update Guide:** See UPDATING.md
- **Full Documentation:** See Documentation/ folder
