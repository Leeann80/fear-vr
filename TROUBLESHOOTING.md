# Troubleshooting F.E.A.R. VR v0.1.1

Support here covers **F.E.A.R. VR by TheFreeMike**, downloaded from
[thefreemike31/fear-vr](https://github.com/thefreemike31/fear-vr/releases).
For builds from another author or repository, use that project's support
channels. Include your mod version and original download URL when reporting a
problem here, and do not mix files from different VR mods.

[Main guide](README.md) · [Installation](INSTALLATION.md) · [Known limitations](KNOWN-LIMITATIONS.md)

This guide is for the public native-installer package. You can troubleshoot and
report problems through GitHub; joining Discord is optional. Change one thing
at a time, and save logs from the failing attempt before relaunching.

## Start with these checks

1. Use the supported GOG base game on Windows 10/11. Confirm it works without
   the VR mod. Expansions and other executable versions are unsupported.
2. Verify the official ZIP's SHA-256 and extract the entire archive into a new
   folder. Keep **setup-files** beside Setup. See [the download steps](INSTALLATION.md#download-and-verify).
3. Use **F.E.A.R. VR.exe** in the installed game folder. A GOG shortcut or
   **FEAR.exe** can start the flat game instead.
4. Connect and wake the headset and both controllers before launching. Choose
   either VDXR or SteamVR using [the connection instructions](INSTALLATION.md#connect-the-headset).
5. For a clean baseline, remove independently added overlays/wrappers using
   their own uninstall instructions. Do not delete DLLs from the official mod
   package. Keep optional Flashlight Shadows off while isolating a problem.

| Symptom | Start here |
| --- | --- |
| Defender blocks the mod, or Setup says a file is missing | [Allow the official mod](#download-or-antivirus-problem) |
| Install/upgrade/recovery error | [Setup](#setup-stops-or-recovery-fails) |
| Launcher error or monitor-only game | [Startup](#launcher-error-or-game-only-on-the-monitor) |
| Always starts flat despite correct VR setup | [ReShade OpenXR conflict](#always-starts-flat-reshade-openxr-conflict) |
| Black, frozen, boxed, or distorted image | [Headset image](#black-frozen-boxed-or-distorted-headset-view) |
| Missing controller input or pause | [Controllers](#controllers-menus-or-pause) |
| Bad fit or missing calibration room | [Calibration](#calibration-or-player-height) |
| Reload, draw, ladder, or interaction failure | [Interactions](#weapon-reload-holster-or-interaction-problem) |
| Stutter or low frame rate | [Performance](#performance-and-recurring-stalls) |
| Game exits unexpectedly | [Crashes](#crash-or-repeatable-campaign-failure) |
| Missing/wrong audio | [Audio](#audio) |
| Still stuck | [Logs and report template](#collect-logs-without-discord) |

## Download or antivirus problem

**Some players have had Windows Defender block or remove mod files. Allowing
the mod resolved one reported installation failure.** This does not happen on
every PC; a detection still needs to be checked against the official download.

Typical symptoms include a disappearing ZIP or launcher, or Setup reporting
**Cannot verify file** / **Expected a regular file** for **F.E.A.R. VR.exe**.
Antivirus can interfere with both the extracted package and the temporary copy
Setup creates inside the game folder. These errors alone do not prove antivirus
is responsible.

### Allow the official mod in Windows Defender

1. Use only [the official GitHub release](https://github.com/thefreemike31/fear-vr/releases/latest).
   [Compare the ZIP's SHA-256](INSTALLATION.md#download-and-verify) with the
   published checksum. A match verifies the download's identity, not an
   antivirus verdict. Do not allow a mismatched or unofficial download.
2. Open **Windows Security > Virus & threat protection > Protection history**.
   Expand the event and check that **Affected items** names the official mod
   ZIP or a file in its extracted package or your F.E.A.R. game folder.
3. If you trust that verified download and choose to allow it, use **Actions >
   Allow on device**, when offered. If it is quarantined, choose **Restore**;
   Defender may detect it again, in which case review that event and choose
   **Allow on device**. Button names depend on the event's current status.
4. Close Setup and **extract the entire ZIP again into a fresh folder**, keeping
   **setup-files** beside **F.E.A.R. VR Setup.exe**. If the ZIP itself was removed,
   download it again and verify it first. Rerun Setup. Allowing a detection does
   not automatically repair an already incomplete extraction.

If Defender keeps removing verified mod files during extraction or installation,
you can use a **targeted folder exclusion**: **Virus & threat protection > Manage
settings > Exclusions > Add or remove exclusions > Add an exclusion > Folder**.
Choose the dedicated folder where you will extract this mod; if the blocked
path is inside the installed game, also choose that specific F.E.A.R. game
folder. Then extract again and retry Setup. Excluded folders are not scanned
by Defender's real-time protection, so use them only for trusted files. Never
exclude an entire drive, all Downloads, or every EXE/DLL, and leave protection
enabled. Remove the temporary extraction-folder exclusion after installation;
you can remove any exclusion from the same screen when it is no longer needed.

The `.sha256` file and `Get-FileHash` only verify the ZIP; they do not restore
missing files. An unsigned-publisher/SmartScreen warning is a separate issue.
If you are still stuck, the threat name and affected path are useful in a
GitHub issue, but no extra report is needed once your problem is solved.

Microsoft help: [Protection history and restoring files](https://learn.microsoft.com/en-us/defender-endpoint/restore-quarantined-files-microsoft-defender-antivirus)
and [antivirus exclusions](https://support.microsoft.com/en-us/defender/antivirus-and-antimalware-software-faq).

## Setup stops or recovery fails

Read the complete error. Close F.E.A.R., check the selected folder contains the
base game's **FEAR.exe**, verify the archive, and extract it again into a new
folder if its contents are incomplete. Use the new Setup's **Upgrade** action
for an existing beta. Unsupported executable errors require the supported GOG
copy, not bypassing the check.

For access-denied errors in a protected folder, close Setup and run that same
Setup as administrator. For a locked-file error, close the game and any tool
using the named file before retrying. Do not repeatedly overwrite it by hand.

If Setup reports an interrupted operation, select **Recover interrupted setup**
for the same game folder, then retry. If recovery says a file changed afterward
or a backup is damaged, preserve the error and **FEAR-VR-Install** folder and
open a GitHub issue. Do not delete state/receipt files or recovery snapshots.

## Launcher error or game only on the monitor

1. Confirm you launched **F.E.A.R. VR.exe** beside the installed game.
2. Check that the headset and controllers track in your connection software.
3. With **Virtual Desktop + VDXR**, select VDXR in Streamer and close SteamVR.
   With **Steam Link/SteamVR**, start SteamVR first and use a build with Win32
   OpenXR support. If discovery fails, set SteamVR as OpenXR runtime and restart it.
4. Preserve **FEARVR-Launcher.log** and **FEARVR-Startup.log**, if present, from
   the game folder. Read the last error and selected runtime. A flat view can
   mean module/bridge initialization failed; it does not prove a wrong runtime.
5. If it mentions a missing/invalid JSON manifest or runtime DLL, repair/update
   the selected runtime and reselect it in the runtime's own settings. Do not
   edit the JSON or point the game at an arbitrary DLL.
6. Remove any custom launch shortcut/environment override that you knowingly
   added for an old beta, then retry the normal executable. Do not change
   machine environment variables or registry keys you do not recognize.

Normal and administrator launcher startup are supported with the matching
bridge. An error requesting a matching bridge means reinstall/upgrade the
complete package; mixing older DLLs will not repair it. Meta Link and Air Link
remain unsupported even if SteamVR is running.

### Always starts flat: ReShade OpenXR conflict

**If you launch F.E.A.R. VR.exe and the game always stays on the monitor despite
a working headset/runtime setup, check for a ReShade OpenXR layer left by another
game or tool.** A player reported that disabling its 32-bit registration fixed
this problem. It is one possible cause, not a fix for every flat launch.

1. Close F.E.A.R. and any other running VR games.
2. Press **Windows + R**, type **regedit**, and press Enter. Approve the Windows
   administrator prompt.
3. Paste this exact path into Registry Editor's address bar and press Enter:

   ```text
   HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Khronos\OpenXR\1\ApiLayers\Implicit
   ```

4. In the right pane, look for a **REG_DWORD** entry named:

   ```text
   C:\ProgramData\ReShade\ReShade32_XR.json
   ```

   The installation path can differ; identify the **ReShade32_XR.json** entry.
   If the key or that entry is absent, stop here and return to the startup
   checks above. Do not create it or change other layers.
5. Right-click the **Implicit** key in the left pane and choose **Export** to
   save a backup. Note the ReShade entry's original value. Double-click that
   entry in the right pane and set **Value data** to **1**, then click **OK**.
   **0 enables the layer; 1 disables it.** If it is already 1, it is already
   disabled and this particular workaround adds nothing.
6. Close Registry Editor. Fully exit **Virtual Desktop Streamer** from its PC
   system-tray icon, reopen it, and reconnect the headset. If using SteamVR,
   restart SteamVR instead. Launch **F.E.A.R. VR.exe** again.

This disables that ReShade OpenXR layer for **other 32-bit OpenXR applications
on this PC too**. To undo it, restore the entry's original value (normally
**0**) and restart your VR connection software. If it does not help, undo the
change before trying another fix. Change the registry value only; do not delete
the JSON file or the whole registry key, and do not change **ActiveRuntime**.

The enable/disable values follow the [Khronos OpenXR loader specification](https://registry.khronos.org/OpenXR/specs/1.1/loader.html#windows-manifest-registry-usage).

## Black, frozen, boxed, or distorted headset view

First note whether audio and the game process continue and whether the runtime
dashboard still works. If the dashboard also fails, restore the headset/runtime
connection before relaunching the game. A lost runtime session may require a
full game restart.

Restore **Options > VR Settings > Headset Display** to **Centered (Recommended)**
projection and **100% View Width**, or use **Restore Display Defaults**. Turn
off optional Flashlight Shadows while isolating the issue. If it began after
a resolution change, quit and relaunch; render-resolution settings apply next launch.

If opening a SteamVR dashboard caused it, close the dashboard and allow focus
to return. Persistent black imagery after focus returns needs a report with
the runtime version, transition, and logs. Do not repeatedly change unrelated
calibration settings. Wider/canted headset modes remain experimental.

## Controllers, menus, or pause

Wake both controllers before launching. Check tracking in the runtime first,
then open **Controller Layouts.html** from the ZIP or **FEAR-VR-Install**. The
runtime can emulate a different mapping profile from the controller's name.

Use **Controls & Layout > Button Layout / Remap > Restore This Layout** to undo
an accidental remap. Check **Weapon Hand** and **Movement Stick** separately.
Runtime/system buttons may never reach the game. For SteamVR Touch pause,
press **Right A + Left X together**. The suggested Index equivalent is
**Right A + Left A together**.

If tracking works but the game reports no usable controller profile, provide
the exact headset, controller, runtime, and detected profile. Non-Touch profiles
have not all been tested on physical hardware.

## Calibration or player height

Follow [Calibration](CALIBRATION.md). Choose the correct **Play Position**, check
the runtime floor, and adjust one feature at a time. Hand fitting, weapon grip,
and sight direction are separate settings. Use their individual resets before
discarding all calibration.

The main-menu calibration room, required material, and references are included.
If the room fails to load, reinstall/upgrade using the complete official ZIP;
do not use an old developer shortcut. Calibration during a campaign stays in
that level. If Continue or a campaign save behaves incorrectly afterward,
preserve the saves and report the exact steps rather than repeatedly saving over them.

## Weapon, reload, holster, or interaction problem

**Grip & Holsters** intentionally disables weapon-button cycling and the wheel.
Draw from the body slots, or select **Classic Sticky** if you want tap/wheel
selection. A stowed gun does not respond to Reload in Grip & Holsters.

For invisible body weapons, set **Immersion & Interaction > Visible Holstered
Weapons** to Yes. No hides the models; slots and reload interactions still exist.
If a draw/pouch is uncomfortable, adjust its location in calibration.

Check reserve ammo and whether the current weapon is waiting for a chamber,
bolt, or rack action. Keep the support grip held while completing a physical
pull, and move relative to the gun. Follow the weapon's tutorial card. A full,
stowed, or reserve-empty gun may correctly have no reload card. Enable tutorial
hints if needed; starting New Game resets lesson progress, but loading does not.

For ladders or pickups, clear occupied hands and try a fresh Grip close to the
interaction. Sustained tracking loss can release a ladder anchor; brief recovery
does not guarantee every headset avoids the original issue. Decorative props
are not all interactive. If a particular grate, enemy, door, ladder endpoint,
or weapon fails consistently, report that exact object/location and whether
save/reload or a turret/cutscene transition changes it.

## Performance and recurring stalls

1. Turn off optional Flashlight Shadows and separately added capture/injection overlays.
2. Use a comfortable refresh rate your PC can sustain; 90 Hz is a useful baseline
   where supported. In SteamVR, begin with per-application resolution at 100%.
3. Check **Headset Display** for the mod's render resolution and actual per-eye
   target. Runtime scaling and mod scaling compound. Lower mod resolution if
   GPU/memory pressure is high, then restart the game to apply it.
4. On a laptop, connect power and verify that the game uses the discrete GPU.
5. Note whether the stall coincides with saving/loading, happens at regular
   intervals, or worsens over time. Compare one changed setting per run.

Desktop mirror resolution is not the per-eye render size. The game is 32-bit;
more system RAM does not remove its process address-space limit. Capture guards
bound some application polling, but do not establish that every periodic stall
is fixed. Report CPU, GPU/VRAM, RAM, resolutions, refresh rate, and timing.

## Crash or repeatable campaign failure

A crash means **FEAR.exe** exits unexpectedly. Before restarting, copy the
same-run logs. On Windows, search Start for **View reliability history**, select
the F.E.A.R. failure, then open its technical details. Record the faulting module,
exception code, and offset when shown. Do not assume the GPU brand identifies
the cause.

For a repeatable save/cutscene/gameplay problem, retain a backup of the affected
save and give the shortest reproduction: level/checkpoint, action, and result.
Say whether it also occurs without VR on the same supported game copy. Do not
upload original game files or a whole game installation.

## Audio

Select the intended Windows playback device before starting the runtime and
game. Check volume/mute in Windows and the headset software. Confirm whether
the base game has audio. The package includes its audio runtime; do not add an
extra DSOAL/OpenAL/EAX replacement on top. If you changed audio DLLs/configuration,
preserve your files and reinstall the official package for a clean comparison.

## Collect logs without Discord

Open the installed game folder and copy these files into a separate folder
before another launch. Not every log exists in every failure:

| File | What it helps identify |
| --- | --- |
| FEARVR-Launcher.log | Launch arguments, runtime selection, and launcher errors |
| FEARVR-Startup.log | Bridge initialization and the runtime failure detail |
| dxwrapper-fear.log, if present | Wrapper/device initialization details |

For a launcher preflight that does **not** start the game, open PowerShell in
the installed game folder and run:

```powershell
& '.\F.E.A.R. VR.exe' --diagnose
```

Preserve the failing launch logs first; preflight can replace the launcher log.
This checks launcher setup only, not headset rendering or every installed file.
When specifically needed for a reproducible issue, the launcher also supports:

```powershell
& '.\F.E.A.R. VR.exe' --debug
```

**That command starts the game** with extra diagnostic logging/crash capture
and may automatically continue your existing campaign save.
Quit normally after the short reproduction, copy the resulting diagnostic
files, and return to the normal launcher for everyday play. No separate debug
EXE, CMD wrapper, compatibility collector, or developer Level Select is required.
The old `--compatibility` mode is not available in this release.

Logs may include personal folder paths; review/redact them before public posting.
Crash dumps contain process memory and should be shared only through an agreed
private channel. A GitHub issue with the sanitized error and template below is
enough to start; Discord membership is not required.

## Report template

Search [existing GitHub Issues](https://github.com/thefreemike31/fear-vr/issues),
then open one issue per distinct problem:

```text
F.E.A.R. VR version and ZIP checksum verified:
Fresh install or upgrade (from which version):
Supported GOG base game works without VR: yes / no / not checked
Headset and controllers:
Connection route and OpenXR runtime/version:
Windows, CPU, GPU/VRAM, driver version, RAM:
Refresh rate, mod render resolution, runtime scale, actual per-eye size:
Exact level/checkpoint and shortest steps:
Expected result and actual result:
Repeat rate; FEAR.exe exits or remains running:
Launcher error / faulting module / exception code, if any:
Logs present or missing (redact private paths):
Other mods/overlays and changes already tried:
```

[Discord](https://discord.gg/NtAnbK6z9B) is also available for community discussion.
Responses depend on availability; neither a report nor a donation guarantees
individual troubleshooting or a response deadline.
