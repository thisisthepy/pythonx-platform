# Intent

What `pythonx-platform` is for. Recorded from the maintainer's decisions of 2026-10-04.

## Sources

> "pythonx-platform에서 알림은 뭐 말하는거야? 그건 compose-extentended 쪽에서 구현이 되어 있어야
> 하는거 아닌가?"

> "내가 말한 알람도 화면 안의 UI 컴포넌트가 아니라 OS 알람이야. extended 안에 있어야겠지?"

> "pythonx-platform: 저장소 만들고 스펙 확정하도록 해."

## 1. What this project is for

A Python app on Kotlin Multiplatform uses the device (OS notifications, camera, sensors, file picker,
permissions, sharing) with one Python API on Android, iOS and desktop.

## 2. Where the work lives

- **Kotlin implementation:** `compose-multiplatform-core-extended`, as multiplatform `androidx.*`
  libraries (the first one is OS notifications, compose-multiplatform-core-extended#13).
- **Python access:** python-multiplatform's binder exposes those libraries under their Kotlin names,
  with snake_case aliases.
- **This package:** groups them under `pythonx.platform` and adds Python-shaped conveniences where the
  Kotlin shape is awkward. It never renames a Kotlin namespace and never reimplements a feature.

## 3. Status

The name is reserved on PyPI (0.0.1a0, no behaviour). The specification is written in the pythonx
turn of the thisisthepy order (torchnative, python-multiplatform, pypackpack and toolchain,
pythonx-compose, then the other pythonx packages).
