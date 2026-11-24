# Build status

## Source validation

GitHub Actions runs source-only checks on pushes, pull requests, and manual dispatch:

- Python syntax validation for `tools/` and `tests/`.
- JSON configuration parsing.
- Android XML parsing.
- Launcher branding checks.

These checks do **not** build an APK.

## Full APK build requirements

The upstream build instructions in `readme.md` require a 64-bit Windows/PowerShell environment and pinned Android/JDK/Python toolchains. More importantly, packaging all three editions requires legally obtained original game inputs listed in `config/inputs.json`, plus generated native game code. Those copyrighted game executables, DLLs, and assets are intentionally not included in this repository.

Do not commit original game files, private installer files, signing keys, or credentials to this public repository. A full APK workflow should only be added after a secure, user-controlled way to provide the required licensed inputs and a compatible build runner has been established.
