---
project: eventGameToolKit
category: unity
status: active
updated: 2026-10-13
---

## Now

Shipping package. Contents are **not edited here** — they are mirrored from the
`gameToolKit` dev harness by robocopy, so anything changed directly in this repo is
overwritten on the next sync. Work in `gameToolKit/Assets/eventGameToolKit/` instead.

`STATE.md` is the one exception: the sync excludes it (`//XF STATE.md`) so this file
survives.

## Next

- Keep receiving syncs from the harness as example-scene coverage is completed
- One scene remains in the harness: `StopMotionPostProcess` using the Mixamo robots
- Fix the packaging bug below before anyone installs by git URL again

## Recently finished

- **Do not push feature work to this repo.** A cloud session committed
  `CharacterController2D` changes to branch `claude/2d-controller-animator-params` here;
  they were ported to the harness on 2026-10-13 and arrive on `main` by sync. That branch is
  now redundant.
- **`PuzzleSequenceChecker` added to `puzzleExample`**; coverage 72 of 73.

- **Two new example scenes.** `Example3D_DecalAnimation` covers all four DecalAnimation
  components with procedurally generated RGBA decal textures the package owns.
  `Example3D_Physics` covers `PhysicsForceZone`, `PhysicsBallPlayerController`,
  `PhysicsEnemyController` and `CharacterPushRigidBody`.
- **Label legibility pass across every generated scene** — labels are larger, re-spaced to
  remove collisions, and coloured to contrast with what is behind them.
- Component coverage was 71 of 73 (75 scripts; `applicationFPSLimiting` and
  `lockMouseCursorToDisplay` are excluded by decision and will never get example scenes).
- **Input System migration.** No `UnityEngine.Input`, no `KeyCode`, no `OnMouseXXX` remain.
  This mattered: Unity 6.3 creates projects with Active Input Handling set to Input System
  only, where the legacy class does not work.
- **Key components now use inline Input Actions.** `InputKeyPress` and `InputKeyCountdown`
  expose a binding UI instead of a key dropdown. Existing scenes need their keys set again.
- **2D support.** `CharacterController2D`, 2D trigger zones and mouse picking,
  `PhysicsBumper2D`, `PhysicsForceZone2D`, `PhysicsPlatformStick2D`.

## Blocked

- none

## Known issues

- **The package depends on four assets it does not ship.** `alwaysOnTop.mat` references a
  texture from Unity's StarterAssets, and `storeExample` / `checkPointExample` reference
  sprites and a material from the Cinemachine samples. A Package Manager install therefore
  has a missing texture and two example scenes with missing assets. Students who receive
  the whole project are unaffected. Fix by replacing those four references with assets the
  package owns — copying Unity's sample assets into a public repo is a licensing grey area.
