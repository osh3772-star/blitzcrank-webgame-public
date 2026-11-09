# Blitzcrank web and Blender source project

웹 게임과 Blender 제작 코드를 탐색하고 수정하기 위한 공개 소스 프로젝트입니다. 압축 백업 전달물이 아닙니다. 원본 보존용 비공개 백업과 구분됩니다.

## Status and license
Project license selection is pending owner confirmation. No new license is granted by this publication. Source visibility alone does not establish an open-source reuse license. Third-party Three.js retains its MIT license. See LICENSE_STATUS.md and THIRD_PARTY_NOTICES.md.

## Structure
- web/: JavaScript/HTML/CSS client, package-lock, tests and vendored Three.js. Base package version 0.24.87 plus experimental v49 modules.
- modeling/flower-candidate/: independent Blender flower candidate generation and validation scripts.
- modeling/fungi-v49/: independently modeled mushroom generation, GLB append and geometry checks, with provenance reference.

## Install and test
Use a recent Node.js supporting node:test and ES modules. From web/, run npm ci to install lockfile-pinned dependencies. No install was performed as part of publication.

Asset-independent checks: node --test tests/combo-practice.test.js tests/duel-round-rules.test.js tests/mode-records.test.js
These three test files were executed against this source tree on 2026-11-09: 47 passed, 0 failed, 0 skipped. No other tests are claimed to pass.

## Preview and build
From web/, npm run build invokes build.mjs. To inspect the static client, run python3 -m http.server 8000 in web/ and visit http://localhost:8000. Both require omitted assets for complete functionality; loading may fail. Neither a successful build nor playable browser preview is claimed for this public tree. npm test runs broader tests, including asset-dependent ones expected to need omitted files.

## Blender
Review scripts before execution. They require Blender Python (bpy/mathutils), and some GLB checks require NumPy. model_fungi.py expects source/Summoners_Rift_Structure_Study_48.blend; the flower generator expects source/Summoners_Rift_Structure_Study_49.blend. These scenes and material/object dependencies are NOT included. The scripts show construction and validation logic but cannot regenerate the complete map standalone. No Unity installation is required.

## Missing assets and scope
Model binaries, editable .blend scenes, textures/images, audio/video, generated asset JSON/binary bundles and historical validation reports remain withheld pending public rights/provenance review. W/E/R, turret and flash audio records explicitly lack confirmed game-use licensing. No substitute audio is introduced. Missing assets affect models, sound, rendering, builds and asset tests. EXCLUSIONS.json records the original web exclusions. This is a source project in progress, not a complete runnable release.

Internal transfer tools, private service identifiers, host paths, credentials, caches and logs are not included. The private backup remains separate and unchanged.

## Contributing
Open an issue describing the change, affected module and reproduction steps. For a proposed patch, separate code from third-party assets, provide provenance/license evidence for new dependencies or media, and run relevant tests. Do not commit credentials or private files. Project licensing must be resolved before representing this as freely reusable open-source software.

## Verification limits
Selected automated logic tests passed; Python scripts were syntax-parsed. Archive-era results are not release evidence. No browser, GPU, mobile-device, audio listening, full build, or Blender scene regeneration was performed for this tree.
