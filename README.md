# Blitzcrank web game: source-only partial backup

공개 검토용 소스 중심 부분 백업입니다. 완전한 게임 배포본이나 모델 원본 전체 백업이 아닙니다. 기존 비공개 백업은 별도로 유지합니다.

## Included
- Web game JavaScript, CSS, HTML, package/lock files and source tests from version 0.24.87 with subsequent v49 experimental modules.
- Independent flower-candidate Blender generation, append, render and validation scripts. These depend on an existing map scene that is NOT included.
- Vendored Three.js code with its original MIT notice in web/vendor/THREE-LICENSE.txt. No new license is granted for third-party game characters or media.

## Excluded and functional impact
- All WAV/MP3/MP4 audio/video, all model binaries/Blender scenes, textures/images, asset JSON/binary bundles and historical validation artifacts are excluded. Public redistribution rights or provenance were not fully established. They are not replaced with different media.
- W/E/R, turret and flash sound manifests explicitly state unverified game-use licensing. Voice, hook and attack audio also lack verified public redistribution evidence.
- Internal transfer utilities, workspace paths, recovery details, logs, caches, dependency installations and private service identifiers are omitted. See EXCLUSIONS.json for source-relative paths; no private host paths or service IDs are retained.
- The web client will have missing assets and may fail to load. Asset-dependent builds/tests cannot be expected to pass. Modeling scripts cannot reproduce the full scene without the omitted source scene. This is not a playable release or a complete restore set.

## Use and verification
Unzip while preserving folders. Review web/package.json; dependencies are pinned by package-lock.json. On an authorized development system, npm ci installs dependencies, npm test runs tests, and npm run build invokes the build. These operations were NOT executed for this public partial package. Never interpret inclusion of a test as proof it passes here.

Packaging checks: included text inspected for known private-reference and credential patterns; archive CRC and manifest SHA256 checked. No browser/GPU/mobile/audio verification is claimed. This limited scan is not a complete security audit.

Modeling reference: modeling/flower-candidate/REFERENCE.md describes independently modeled environmental motifs, not extracted game geometry. Original editable character models are not included.
