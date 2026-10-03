# pythonx-platform

Device features for Python apps on Kotlin Multiplatform: OS notifications, camera, sensors, file
picker and permissions, as one Python API on Android, iOS and desktop.

The Kotlin implementations live in `compose-multiplatform-core-extended` as multiplatform `androidx.*`
libraries, and Python reaches them through python-multiplatform's binder. This package is a thin
Pythonic layer on top.

Status: the name is reserved; there is no behaviour yet. Read [`docs/INTENT.md`](docs/INTENT.md) and
the ecosystem overview at https://thisisthepy.github.io/projects/pythonx-platform/.

```bash
uv add --prerelease allow pythonx-platform
```

Licensed under Apache-2.0.
