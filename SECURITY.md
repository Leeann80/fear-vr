# Security and privacy

F.E.A.R. VR runs locally inside the 32-bit F.E.A.R. process and submits frames
to the active OpenXR runtime. It contains no telemetry, advertising, account
system, updater, downloader, background service, driver, firewall change, or
security-software exclusion.

The included native **F.E.A.R. VR Setup.exe**:

- accepts only the verified GOG `FEAR.exe` and original GOG `d3d9.dll`;
- verifies the package manifest against the identity compiled into Setup and
  checks every payload file against that manifest;
- stages and re-verifies files before installation;
- backs up every replaced file and records exact hashes;
- rolls back a failed install and retains recovery snapshots if rollback cannot
  finish; and
- preserves modified managed files under `FEAR-VR-Install/preserved-files`
  before an upgrade or uninstall, then restores original files or removes files
  created by the mod. Saves and profiles are kept.

Setup does not launch F.E.A.R. For a protected game folder, you can run Setup
as administrator. If setup is interrupted, reopen it for the same game folder
and choose **Recover interrupted setup** before retrying. Keep its recovery
backups until recovery succeeds.

## Package verification

This package is not Authenticode-signed. Compare the ZIP against the
SHA-256 published with the release before running it. The bridge, launcher, and
DxWrapper are PE32/x86 binaries with ASLR and DEP/NX enabled. GameClient and
GameServer retain the original Visual C++ 7.1 compatibility toolchain and do
not advertise those modern PE mitigations; do not mix this beta with untrusted
mods, maps, archives, or saves.

## Antivirus blocks

For a Defender block or quarantined mod file, see [the troubleshooting steps
for allowing the official download](TROUBLESHOOTING.md#download-or-antivirus-problem).
Any allow rule or exclusion is your choice in Windows Security; Setup does not
change antivirus settings. Keep protection enabled and exclusions narrowly scoped.

## Diagnostics

Normal player launches keep verbose developer diagnostics disabled. Read
**TROUBLESHOOTING.md** for the logs to provide when reporting a problem.
Logs can contain local filesystem paths. If support separately requests a crash
dump, it can also contain process memory and player names. Review diagnostic
files and share them privately only when requested.

Report suspected security problems privately and include the exact release name
and ZIP checksum. Do not attach crash dumps or private filesystem paths to a
public issue.
