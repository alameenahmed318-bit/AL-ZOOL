# AZ-ZOL Windows App build branch

This branch is isolated from the ERP project's main branch.

## Build
GitHub Actions workflow: **Build AZ-ZOL Windows App**.

The workflow runs on Windows 2022 via GitHub-hosted runners, builds the desktop app with Python 3.12 + PyInstaller, and uploads `AZ-ZOL-Windows-App.zip` as an Actions artifact.

## Required source file
Place the verified application source at:

`AZ-ZOL-WINDOWS-APP/AL_ZOOL_GOLD_SNIPER_AZ_MASTER_BRAIN.py`

The source file is intentionally not fabricated or replaced with a demo. The available local copy has a starter-scaffold header and must be verified against the complete legacy trading engine before calling the result a complete trading terminal.

## Important
The current workflow creates a portable Windows application folder ZIP, not a signed Setup.exe installer. A separate Inno Setup step can create Setup.exe after the application source and runtime behavior are verified. Test only with a Deriv demo account.
