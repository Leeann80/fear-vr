# Controls and weapon handling

[Main guide](README.md) · [Calibration](CALIBRATION.md) · [Troubleshooting](TROUBLESHOOTING.md)

Open **Controller Layouts.html** from the downloaded ZIP or the installed
**FEAR-VR-Install** folder for the default buttons for your controller profile.
The runtime may report an emulated profile; use the detected profile rather
than relying solely on the controller's product name. Non-Touch profiles remain
experimental.

## Menus and pause

Use the controller pointer and trigger to select menu items. Runtime/system
dashboard buttons are owned by the headset software and may never reach the game.
For SteamVR Touch, press **Right A + Left X together** to pause. The suggested
Index mapping uses **Right A + Left A together**. Press simultaneously; holding
one button first can perform its normal action.

## Handedness and remapping

Open **Options > VR Settings > Controls & Layout**:

- **Weapon Hand** selects your weapon hand.
- **Movement Stick** selects the locomotion stick.
- **Tap to Walk** controls the optional utility-button run/walk toggle.
- **Weapon Button Tap** selects the tap behavior used in Classic Sticky.
- **Button Layout / Remap** reassigns gameplay button roles. Assigning an
  occupied button exchanges the two roles; menu controls remain fixed.

Layouts are saved per reported controller profile and weapon hand. Use
**Restore This Layout** on the remap page, or **Restore Defaults for This Hand**
on the controls page, to undo changes. Check the displayed role labels after
changing handedness; references to left/right defaults may no longer apply.

## Movement and comfort

You start in run mode. With default Touch controls and **Tap to Walk** enabled,
tap the left stick to walk, and tap again to run. **Hold** that utility control
for a medkit; tapping and holding are different actions.

Use **Movement & Comfort** for play position, turning, turn speed, and comfort
options. Smooth turning defaults to 180 degrees/second; lower it or choose snap
turning to suit you. Review vignette and camera-driven-scene options before play.

## Choose a weapon-handling mode

**Grip & Holsters:** reach to a body slot and use Grip to draw a weapon. Weapon-
button taps and the selection wheel are intentionally unavailable. Reload acts
on a held firearm; pressing it while the gun is stowed does nothing. Adjust the
slot locations in calibration if reaching a holster is uncomfortable.

**Classic Sticky:** keeps conventional tap switching and hold-to-open weapon
selection, according to the selected layout. Locomotion is blocked while the
world-anchored weapon selector is open. Release the selector to resume movement.

Under **Immersion & Interaction**, **Visible Holstered Weapons** controls passive
body weapon/belt models. Setting it to No hides their presentation; the body
draw/reload locations still work. Calibration references remain visible.

## Reloading and interactions

Manual reload uses weapon-specific actions and contextual cards. Hold the gun,
use the reload/ammo-pouch interactions shown by the current lesson, and complete
any required chambering/racking step. Different weapons do not all reload in
the same way. For a rack or bolt pull, keep the support grip engaged and pull
along the mechanism relative to the gun, not relative to your head. A release
or tracking loss cancels an incomplete pull. Use the reload-mode option if you
prefer button reloads.

If a reload seems stuck, check the held weapon, reserve ammo, chamber/racking
state, and selected reload mode before repeatedly pressing buttons. Recalibrate
the pouch if its position is the problem. See [Troubleshooting](TROUBLESHOOTING.md#weapon-reload-holster-or-interaction-problem).

Physical pickups, weapon exchange, melee, and ladders depend on eligible objects
and free hands. A decorative prop is not necessarily grabbable. Clear held
objects/weapons when an interaction requires an empty hand. On physical ladders,
hold Grip at the ladder and move your hand to climb; releasing lets go. The
optional automatic-climb setting is separate from manual pulling.

Tutorial hints can be enabled in VR settings. **New Game** resets tutorial
progress; Continue and loading retain it. Reload cards wait until a reload is
actionable and withdraw when the weapon is full, stowed, or lacks reserve ammo.

## Aiming

**VR Aiming** provides aim-indicator and brightness options. **Dual Pistol Colors**
defaults to On to distinguish the two pistols; Off uses the shared main color.
Use **Weapon Grip Calibration** to change how the gun sits in your hand, and
**Advanced Sight Alignment** only when its aiming direction needs adjustment.
These are different calibrations with separate resets.
