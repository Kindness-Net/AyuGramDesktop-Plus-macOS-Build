# AyuGram Desktop Plus macOS builds

This repository hosts the macOS build workflow and dependency cache for [AyuGram Desktop Plus](https://github.com/Kindness-Kismet/AyuGramDesktop-Plus). Releases are coordinated and published by the source repository.

The source repository dispatches an exact commit and Release workflow run. This repository builds one Universal 2 package for Intel and Apple silicon, keeps its own GitHub Actions cache, and returns short-lived artifacts with a provenance manifest. It does not publish releases.

Pull requests only validate workflow syntax. The signing key is scoped to the dispatched build workflow and is removed from the runner workspace after each build.

Trusted manual builds from non-main source branches remain supported. The selected source commit must include `scripts/build_provenance.py` and the Packer `ccache:disable` guard.
