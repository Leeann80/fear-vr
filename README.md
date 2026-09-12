# F.E.A.R. VR by TheFreeMike

<img src="assets/alma.png" alt="Alma, F.E.A.R. VR artwork" width="240">

Play the original F.E.A.R. campaign in PC VR, with tracked hands, physical
weapon handling, configurable controls, and comfort options.

**Current release: v0.1.1. Free, unofficial, and made by TheFreeMike.**
You need a legitimate copy of the supported **GOG F.E.A.R. Platinum Collection**
and a Windows PC capable of PC VR. The base game is not included.

[Download the latest release](https://github.com/thefreemike31/fear-vr/releases/latest)
· [Installation](INSTALLATION.md) · [Troubleshooting](TROUBLESHOOTING.md)

## Make sure you have the right mod

This is **TheFreeMike's F.E.A.R. VR**, distributed by **thefreemike31**.
The separate [DR-89/fear-vr project](https://github.com/DR-89/fear-vr) has its own
releases and instructions. TheFreeMike does not maintain or provide support
for that project's builds or other F.E.A.R. VR mods.

For support here, use a release downloaded from
[thefreemike31/fear-vr](https://github.com/thefreemike31/fear-vr/releases) and
include its version and download URL in your report. Do not combine installers
or files from different VR mods.

## From prototype to public release

The public launch follows weeks of development and private-beta testing, with
retained milestones from July 21 through September 11, 2026: physical reloads
and holsters, campaign interaction fixes, calibration, configurable controls,
and a native installer with recovery support.

[Read the development history and beta milestones](https://github.com/thefreemike31/fear-vr/blob/main/HISTORY.md).

## Start here

1. Confirm the unmodified GOG base game works on your PC.
2. From the release's **Assets** list, download `fear-vr-v0.1.1.zip` and its
   `.sha256` file. GitHub's automatic **Source code** downloads are not the mod.
3. Verify and extract the complete ZIP. Keep **setup-files** beside
   **F.E.A.R. VR Setup.exe**.
4. Close F.E.A.R., open Setup, select the base game's folder, then install or
   upgrade. Setup keeps saves and backs up replaced files.
5. Connect your headset and controllers through one supported route below.
6. Run **F.E.A.R. VR.exe** in the installed game folder.

Follow the [step-by-step installation guide](INSTALLATION.md) for runtime setup,
checksum verification, shortcuts, upgrading, uninstalling, and recovery.

## Supported setup

| Requirement | What to use |
| --- | --- |
| Game | Supported GOG F.E.A.R. Platinum Collection base game; Setup checks the exact executable |
| PC | Windows 10/11; this is a PC VR mod, not a standalone headset app |
| Quest connection | Virtual Desktop + VDXR, or Steam Link + SteamVR with Win32 OpenXR support |
| Other PC VR headsets | SteamVR with Win32 OpenXR support; hardware coverage remains experimental |
| Physically validated hardware | Quest 3 with Touch controllers |

Meta Quest Link and Air Link are unsupported, including through SteamVR.
Steam/retail editions, Extraction Point, Perseus Mandate, multiplayer, and
Linux/Proton are outside this release's supported scope. A controller mapping
does not mean that hardware has been physically tested.

## What is included

- Stereo VR rendering, tracked head and hands, and controller aiming.
- **Grip & Holsters** for physical body draws, or **Classic Sticky** weapon handling.
- Manual-reload options, physical interactions, ladder handling, and tutorial cards.
- Height, controller hand fit, holster/pouch, grip, and sight calibration.
- Configurable handedness, button layouts, movement, turning, and comfort settings.
- Native install, upgrade, uninstall, and interrupted-install recovery.

## Player guides

| Guide | Find out how to… |
| --- | --- |
| [Installation](INSTALLATION.md) | Install, connect the runtime, launch, update, remove, or recover the mod |
| [Controls](CONTROLS.md) | Navigate menus, choose weapon handling, reload, remap, and use comfort settings |
| [Calibration](CALIBRATION.md) | Set height, fit hands, move holsters, and reset individual adjustments |
| [Troubleshooting](TROUBLESHOOTING.md) | Work through startup, graphics, controllers, performance, audio, and save issues |
| [Known limitations](KNOWN-LIMITATIONS.md) | Check hardware coverage and experimental features |
| [Release notes](RELEASE-NOTES.md) | See the latest fixes and update instructions |
| [Security and privacy](SECURITY.md) | Understand installation, unsigned files, and diagnostic privacy |
| [Third-party notices](THIRD-PARTY-NOTICES.md) | Read component notices and licenses |

The ZIP also includes **Controller Layouts.html**, with diagrams/tables for the
supported mapping profiles. Download and open it in your browser; GitHub may
show its HTML source instead of rendering it. These guides are also installed
under **FEAR-VR-Install**, so you can read them without joining Discord.

## Help and support

Start with [Troubleshooting](TROUBLESHOOTING.md). If the problem remains, use
[GitHub Issues](https://github.com/thefreemike31/fear-vr/issues) and the report
template at the end of that guide. Search existing issues first. Review logs
before posting; keep personal paths and crash dumps private.

[Join the Discord community](https://discord.gg/NtAnbK6z9B) ·
[Support TheFreeMike on Ko-fi](https://ko-fi.com/thefreemike)

The mod is free. Donations are optional and do not purchase support, access,
or a response deadline.

## Credits and AI transparency

**F.E.A.R. VR was built through a collaboration between TheFreeMike and Codex,
OpenAI's AI coding assistant.** AI was a substantial part of the engineering
process, and we want to be transparent about that contribution.

- **TheFreeMike (Mike):** project direction, gameplay and comfort decisions,
  hands-on headset testing, feedback that guided repeated revisions, and
  community and release stewardship.
- **Codex (OpenAI):** substantial engineering assistance across code
  implementation, debugging, code review, automated checks, build and installer
  tooling, release packaging, and player documentation, working iteratively
  with Mike's direction and test results.
- **Private-beta testers:** hardware reports, reproduction steps, and gameplay
  feedback that helped uncover issues beyond the development setup.

The collaboration combined AI-assisted engineering with human judgment and
real headset testing. Mike maintains the project and makes the final release
decisions; AI-generated changes still need review and validation. This is an
independent community project, not an OpenAI product or endorsement.

## About this repository

This is the **distribution and documentation repository**. It contains player
guides and release downloads; the mod's development source is not published.
It is not an open-source release. Third-party components retain their own
licenses. F.E.A.R. belongs to its respective rights holders; this unofficial
mod is not endorsed by them and includes no standalone copy of the game.
