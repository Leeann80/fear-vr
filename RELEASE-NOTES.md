# F.E.A.R. VR v1.1.1 - GOG installer hotfix

- Fixes Setup and the VR launcher incorrectly identifying GOG's original
  `dinput8.dll` Input wrapper as another mod loader.
- The verified original GOG wrapper is kept unchanged through installation,
  upgrade, recovery and uninstall. Unknown or modified loaders remain blocked.
- Gameplay, rendering and the Steam input fix are unchanged from v1.1.0.

If you moved your original GOG `dinput8.dll` to get past the v1.1.0 warning,
close the game, put that same original file back, then install v1.1.1. If you
no longer have it, repair the game through GOG and then reinstall the VR mod.
Do not download a replacement DLL from an unrelated site or copy the Steam proxy.
The reported worsening frame times still need affected-player confirmation;
this hotfix corrects wrapper compatibility, not a verified performance regression.

Extract the complete **fear-vr-v1.1.1.zip** into a fresh folder and run Setup.
Keep **setup-files** beside it. Existing saves and profiles are preserved.

## Included v1.1.0 changes - unified GOG and Steam release

- One installer and VR launcher now support verified GOG and original Steam
  base-game copies, including upgrade, uninstall and interrupted-setup recovery.
- Steam startup passes VR settings through Steam automatically and handles its
  quoted launch arguments. The original game executable stays unchanged.
- Underwater swimming uses a shorter collision cylinder with a stable camera
  reference and collision-checked restoration to standing height.
- Steam includes the accepted input polling fix for smoother gameplay. It does
  not shorten Steam level loads; results can vary with hardware.
- Aiming is steadier with one or two hands, and firearm transfers between hands
  blend smoothly into the receiving grip.
- Nearby pickups take priority over hip holsters. Chest grenade grabs are less
  likely during weapon transfers, and small props sit closer to the hand.
- Jump requires a more deliberate upward stick push. After stick-crouching,
  return the stick to center before jumping; no double tap is required.
- Remote-charge detonators yield when either hand draws a firearm and return
  to the dominant hand after release while a charge remains active, including
  repeated grab/release cycles.
- Improved ladder completion at safe landings and GPU capture polling. Some
  reported performance stalls still need affected-player confirmation.
- Menus gain a dark floor with teal-green glow and the pink cat credit,
  **Made by thefreemike**. The floor and credit hide during level loading to
  prevent flicker.
- Includes all v0.1.2 gameplay, subtitles, calibration and comfort improvements.

Version 1.0.0 was a tester release. This update brings its unified setup and the
subsequent accepted fixes together for GOG and Steam players.

Quit F.E.A.R., extract the complete **fear-vr-v1.1.1.zip** into a fresh folder,
keep **setup-files** beside **F.E.A.R. VR Setup.exe**, and select your game folder.
Then start **F.E.A.R. VR.exe** in that installation. Steam users must be signed
into the owning account; leave the VR launcher open during startup.

GOG remains recommended because Steam level loads can take several minutes.
Use a clean game installation without other loaders. Expansions, multiplayer,
Meta Quest Link/Air Link and Linux/Proton remain unsupported. The specific
reported Blindside tunnel still lacks headset verification.

See [Installation](INSTALLATION.md), [Controls](CONTROLS.md),
[Calibration](CALIBRATION.md), [Troubleshooting](TROUBLESHOOTING.md) and
[Known limitations](KNOWN-LIMITATIONS.md).
