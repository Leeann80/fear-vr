# F.E.A.R. VR v1.3.0 - Steam memory fix and experimental languages

- **Steam 4 GB memory support:** the launcher automatically prepares the verified
  original Steam executable for up to 4 GB of address space on 64-bit Windows.
  First use performs a one-time preparation and continues into VR from the same
  Play click. GOG already has this capability and its executable stays unchanged.
- **Experimental installed-language support:** keep the official language data
  already installed with your supported game. Cyrillic menu text automatically
  uses a readable fallback font. The automatic correction was tested with Russian
  menus on GOG; other languages and full-campaign coverage remain experimental.
  This is not a translation pack; VR-specific text may remain English.
- **Continue after loading with either trigger**, even when your hands point away
  from the panel. Release the trigger, then press it at the continue prompt.
- **New slow-motion tutorial card** shows your mapped button when slow motion is
  available and remembers completion alongside the existing lessons.
- Includes the v1.2 launcher, weapon-handling polish and all earlier fixes.

Close F.E.A.R., extract **fear-vr-v1.3.0.zip** into a fresh folder, keep
**setup-files** beside **F.E.A.R. VR Setup.exe**, and choose **Upgrade**.
No uninstall is needed first. Saves and profiles are preserved. Launch with
**F.E.A.R. VR.exe > Play in VR**; Steam users must sign into the owning account.

Steam preparation backs up **FEAR.exe.fearvr-memory-original** beside FEAR.exe.
Keep that backup. The updated uninstaller restores the original when the verified
backup is present. Recovery and opt-out instructions are in
[Troubleshooting](TROUBLESHOOTING.md#steam-memory-preparation). No game executable,
decrypted game code, language archives, translation database or font is shipped.

Point of Entry was tested successfully on Steam with Virtual Desktop and SteamVR.
This is not a universal out-of-memory fix: the game is still 32-bit, and high
render resolutions can exhaust memory. Steam loading remains slow, and an
existing native cleanup crash after choosing Quit remains unresolved.
Broader affected-player and language coverage is still needed.

See [Installation](INSTALLATION.md), [Controls](CONTROLS.md),
[Known limitations](KNOWN-LIMITATIONS.md) and [Troubleshooting](TROUBLESHOOTING.md).
