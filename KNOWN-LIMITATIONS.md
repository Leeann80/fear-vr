# Known limitations

[Main guide](README.md) · [Troubleshooting](TROUBLESHOOTING.md)

- This release targets verified GOG and original Steam base-game single-player
  campaigns. Other executable variants, expansions, multiplayer and Linux/Proton
  are outside its supported scope.
- Steam level loading can take several minutes. GOG remains recommended.
  Other mod loaders and hook suites are not validated together with this mod.
- Steam's included input fix filters legacy gamepad/joystick enumeration;
  keyboard, mouse and OpenXR controllers remain available. This also applies
  to flat launches from that installation while the fix is enabled. See
  [Troubleshooting](TROUBLESHOOTING.md#steam-input-fix) for the optional off switch.
- Some small props still sit slightly away from the hand. Ladder completion
  improved in repeated owner testing; broader affected-player coverage remains.
- Compact underwater collision is included, but the reported Blindside tunnel
  has not yet been reproduced and verified in a headset.
- Quest 3 with Touch controllers is the physical validation baseline. Other
  headsets, controller profiles, and wide/canted-headset display adjustments
  remain experimental. A listed mapping is not a guarantee of hardware coverage.
- Meta Quest Link and Air Link are unsupported, even through SteamVR.
- Optional **Flashlight Shadows** is experimental and off by default. Detached
  hands do not cast those flashlight shadows. Other optional visual/body
  features may have imperfect alignment or scene-dependent artifacts.
- The game remains a 32-bit application. High per-eye resolutions can create
  memory/GPU pressure even on a PC with plentiful system RAM. Start with the
  supported display defaults and adjust one setting at a time.
- Capture safeguards improve handling of a delayed GPU, but recurring stalls
  reported on some systems have not been conclusively diagnosed or universally
  resolved. Driver calls, runtime waits, loading, and streaming can still stall.
- A runtime shutdown or lost OpenXR session may require quitting and relaunching
  the game after restoring the headset connection.
- Existing save/profile data and native game behavior still matter. Keep save
  backups and report specific levels/actions for repeatable campaign problems.
- Releases are unsigned. Local download verification is not a guarantee that
  every antivirus or reputation service will accept the same archive.

- The new launcher was owner-tested on GOG in windowed 720p with VirtualDesktopXR.
  Separate Steam, fullscreen, 1080p and OBS/minimized capture coverage was not
  reported. Do not assume recording continues while the mirror is minimized.
- Small held props can still sit farther from the hand than ideal.

Read the latest release notes and open issues before assuming an old workaround
still applies. Development tools and the local Level Select menu are not shipped.
