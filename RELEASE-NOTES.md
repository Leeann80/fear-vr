# F.E.A.R. VR v1.1.0 - unified GOG and Steam release

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

Quit F.E.A.R., extract the complete **fear-vr-v1.1.0.zip** into a fresh folder,
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
