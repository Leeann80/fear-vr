# The road to F.E.A.R. VR by TheFreeMike

The first public release arrived on **September 11, 2026**, after weeks of
prototype development, headset testing, private betas, and player feedback.
The earliest retained development checkpoint is **July 21, 2026**: a working
VR prototype already existed at that point. This timeline covers the recorded
work from that checkpoint through the public launch, rather than claiming an
exact date for the project's first experiment.

This is a summary of TheFreeMike's project. It is separate from the
[DR-89/fear-vr project](https://github.com/DR-89/fear-vr); this repository's
support covers releases published by TheFreeMike here.

## From prototype to a playable campaign

**July 21–30 — Building the VR foundation.** The recorded work developed the
room-scale rig, tracked weapon aiming, dual-wield controls, throwable handling,
physical hand/prop contact, analog walking, and tactile feedback. Menus and
loading screens gained VR presentation. Stereo effects and reflections,
recentring, mission transitions, and scripted camera recovery received fixes.
Hands-only comfort, physical melee, dual-pistol aim indicators, and a wrist HUD
followed. These were repeated gameplay and presentation iterations around the
original campaign, not just a single stereo-rendering switch.

**Early August–August 13 — Making weapons and interactions physical.** Manual
reload work progressed weapon by weapon, including the shotgun, scoped rifle,
HV Penetrator, Type-7, Cannon, and Missile Launcher. Work also covered grabbing
props, two-hand steering, weapon selection, reload guides, aiming and muzzle
occlusion, controller stability, ladders, water traversal, the head-mounted
flashlight, and a dedicated VR settings screen.

## Private-beta milestones

Dates below are the recorded GitHub publication dates. Some features were
implemented and tested before the release that collected them.

| Published | Milestone | What changed for players |
| --- | --- | --- |
| August 14 | RC1 | First private release candidate for invited testers, with a packaged installer and launcher for the GOG base game. |
| August 14 | RC2 | Expanded controller mappings and handedness documentation, weapon-selection work, installer compatibility fixes, and a correction for an affected black-headset rendering case. |
| August 14 | RC3 | Fine-motion controller stability, contextual pickup/swap guidance, aiming improvements, campaign interaction fixes, and further launcher/install reliability work. |
| August 15 | RC3.1 | Seated crouch recovery after saving and pausing, frozen tracked hands while paused, cutscene input guards, and a centered desktop mirror. |
| August 28 | RC4 | A larger interaction update: body holsters, physical grenade handling, ladder and scope/reload work, prop handling, contact melee, physical pickups and weapon exchanges, contextual tutorials, audio integration, and turret fixes. |
| August 29 | RC4.1 | Crouch-aware pistol reload zones, turning around the rendered headset position, and recovery-uninstaller cleanup. |
| September 4 | RC5.1 | In-headset body/hand/weapon and sight calibration, animated hand presentation, display controls, interaction reliability, and reduced routine diagnostic work. |
| September 5 | RC5.2 | Packaged the missing main-menu calibration-room resources, preserved modified managed files during uninstall, and clarified controller guidance. |
| September 6 | RC5.3 | Replaced script-based installation with native Windows Setup, direct upgrades, an installed uninstaller, and interrupted-operation recovery. Gameplay/runtime files stayed the same as RC5.2. |
| September 9 | RC6 | Consolidated configurable controls, hand fitting, movement defaults, collision/melee and camera fixes, calibration save protection, weapon-relative racking, and administrator-startup support. |
| September 9 | RC6.1 | Applied controller hand fitting to held weapons and support grips; added optional experimental flashlight shadows. |
| September 10 | RC6.2 | Clarified physical holster versus Classic Sticky switching, prevented stowed-weapon reloads, refined tutorial resets and reload cues, improved ladder recovery, added capture safeguards, and introduced optional dual-pistol indicator colors. |
| September 11 | Public v0.1.0 | Released the accepted RC6.2 campaign baseline publicly, with corrected startup diagnostics, Alma application icons, and a comprehensive set of player guides. |

## The work between the release numbers

Much of the effort was making interactions hold up during normal campaign
play: crouching to reload, grabbing near obstacles, climbing and stepping off
ladders, resuming from a save, entering a turret, crossing water, or recovering
from a scripted camera sequence. Those cases prompted focused fixes and repeat
headset checks throughout the beta period.

Calibration and controls also grew through iteration. Players gained saved,
resettable adjustments for height, hands, holsters, weapon grips and sights,
alongside handedness and button-layout choices. The aim was to make the mod
fit the player while keeping the original game's weapon and interaction
systems authoritative.

Release work mattered too: verifying packages, preserving original backups and
saves, testing upgrade/uninstall/recovery paths, and writing guides people can
use without joining Discord. Private-tester feedback helped identify cases
that one development setup could not reveal.

## How to read this history

This page summarizes retained development commits and private-beta release
notes. The private beta archive remains private; source code is not being
published. The timeline makes those milestones visible without directing new
players to superseded downloads or installation instructions.

Historical experiments are not a current compatibility promise. Some earlier
betas investigated runtime routes that are now unsupported. Use today's
[installation guide](INSTALLATION.md) and [known limitations](KNOWN-LIMITATIONS.md).
Quest 3/Touch is the physical validation baseline; automated checks do not
establish acceptance on every headset. Public v0.1.0's packaging and icon/logging
changes were verified offline without a new headset launch.

[Download the current release](https://github.com/thefreemike31/fear-vr/releases/latest)
· [Release notes](RELEASE-NOTES.md) · [Troubleshooting](TROUBLESHOOTING.md)
