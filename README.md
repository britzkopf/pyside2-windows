# pyside2-windows

[![Build status](https://ci.appveyor.com/api/projects/status/fhgrc83ql9w09kei/branch/master?svg=true)](https://ci.appveyor.com/project/fredrikaverpil/pyside2-windows/branch/master)

:warning: This is a (possibly temporary?) development/research repository for building standalone PySide2 wheels on Windows.

<br><br>


## Download the standalone wheels

[Releases](https://github.com/fredrikaverpil/pyside2-windows/releases) contain built PySide2 wheels.

If you wish to check the wheels produced by e.g. a PR, see the [AppVeyor build history](https://ci.appveyor.com/project/fredrikaverpil/pyside2-windows/history), navigate to a build and download the attached artifacts.

<br><br>


## Known issues

### Build issues
- libxml2/libxslt libraries are not installed/available

### Upstream issues
- [PYSIDE-356](https://bugreports.qt.io/browse/PYSIDE-356) pyside2uic of pyside-tools installs for Python 3 only
- [PYSIDE-357](https://bugreports.qt.io/browse/PYSIDE-357) Compiler module missing from pyside2uic

Note: PRs attempting to fix upstream fixes will not be accepted. Please send your PR upstream instead.

<br><br>


## Notes on releases

Tagging causes AppVeyor to generate a release and attach the built wheels to it. Use lightweight tags for simplicity:

```bash
git commit -am "Commit all of my changes..."
git push  # triggers an AppVeyor build
git tag v0.0.1
git push origin v0.0.1  # cancels previous build, starts new build and generates release
```
