---
project: eventGameToolKit
category: unity
status: active
updated: 2026-09-11
---

## Now

Shipping package. Contents are **not edited here** — they are mirrored from the
`gameToolKit` dev harness by robocopy, so anything changed directly in this repo is
overwritten on the next sync. Work in `gameToolKit/Assets/eventGameToolKit/` instead.

`STATE.md` is the one exception: the sync excludes it (`//XF STATE.md`) so this file
survives.

## Next

- Keep receiving syncs from the harness as example-scene coverage is completed
- Fix the packaging bug below before anyone installs by git URL again

## Recently finished

- **Input System migration.** No `UnityEngine.Input`, no `KeyCode`, no `OnMouseXXX` remain.
  This mattered: Unity 6.3 creates projects with Active Input Handling set to Input System
  only, where the legacy class does not work — `InputKeyPress` did nothing at all in a
  student's project.
- **Key components now use inline Input Actions.** `InputKeyPress` and `InputKeyCountdown`
  expose a binding UI (press +, then Listen) instead of a key dropdown, so the same binding
  also accepts a gamepad button. Existing scenes need their keys set again.
- **2D support.** `CharacterController2D`, 2D trigger zones and mouse picking,
  `PhysicsBumper2D`, `PhysicsForceZone2D`, `PhysicsPlatformStick2D`. `PhysicsBumperTag`
  merged into `PhysicsBumper` as an optional tag filter and removed.
- **Six new example scenes**, including one labelled station per input component and a
  demo of which moving-platform animator pairs with which character controller.

## Blocked

- none

## Known issues

- **The package depends on four assets it does not ship.** `alwaysOnTop.mat` references a
  texture from Unity's StarterAssets, and `storeExample` / `checkPointExample` reference
  sprites and a material from the Cinemachine samples. A Package Manager install therefore
  has a missing texture and two example scenes with missing assets. Students who receive
  the whole project are unaffected. Fix by replacing those four references with assets the
  package owns — copying Unity's sample assets into a public repo is a licensing grey area.
