# Azeron Companion by BurntSoap420

An on-screen overlay for Azeron keypads. It shows your device's buttons on top of your game, lights them as you press, and lets you add bindings that Azeron Software doesn't offer.

Unofficial fan project. Not made by or affiliated with Azeron.

## What you need

- Windows 10 (version 2004 or later) or Windows 11, 64-bit
- Azeron Software installed, with your device set up and at least one profile
- An Azeron Cyro, Cyro Lefty, Cyborg II or Keyzen on current firmware

## Getting started

1. Run `AzeronCompanion.exe`. The overlay appears on your screen and its icon appears in the system tray.
2. Companion detects your device by itself and loads its profiles and button grid.

**Keyzen and Cyborg II: grid drawn for the wrong hand?** In Settings, click **Themes**. Under **CELL LAYOUT**, pick **Other Hand (Azeron's mirrored grid)**.

## Opening Settings

- Press **Ctrl+Shift+F12**, or
- right-click the tray icon and choose **Settings**, or
- click the small button on the corner of the overlay.

You can change the hotkey in Settings, under **Hotkeys**.

## How Companion works with Azeron Software

**Read this first. Everything else depends on it.**

There are two kinds of profile:

- **Azeron profiles** are the ones you make in Azeron Software. Companion reads them, shows them on the overlay, and lets you add bindings to their blank buttons.
- **Software profiles** are ones you make in Companion. On a software profile, any button can be bound. See *Software profiles* below.

The rule for Azeron profiles:

**On an Azeron profile, Companion can only bind a button that has nothing assigned to it in Azeron Software.**

- A button with an Azeron binding keeps doing what Azeron set. Companion will not bind it.
- To give a button to Companion, clear its binding in Azeron Software first. It then shows as blank in Companion, and you can bind it.
- On any one Azeron profile, each button belongs to Azeron Software or to Companion, not both.

This is per profile. A button can be blank on one Azeron profile and bound on another, so what Companion can do with it changes from profile to profile.

## The Settings window

The left side is your device's button grid, showing one profile at a time. The buttons down the side open the other pages: **Combo**, **Hotkeys**, **Appearance**, **Themes**, **OBM**, **Advanced**, **Profiles**, **Button Covers**, **Integrations**.

**Viewing:** at the top picks which profile the grid shows, and so which profile you are editing.

- **Live** follows whatever profile your device is on right now.
- Pick a profile by name to edit it without switching your device to it.

## Bind a key to a single button

1. Set **Viewing:** to the profile you want to edit.
2. Click a blank button on the grid. A window opens beside Settings.
3. The tabs **Solo**, **Hold** and **Double** are the three things one button can do: a normal press, holding it, and double-tapping it. Pick the tab you are setting.
4. Set what it sends. Either:
   - click the **Set Key...** box, which changes to **Press a key...**, then press the key or mouse button, or
   - click one of the six icons to pick from a list: **Keyboard**, **Mouse**, **Layers**, **Media**, **OBS**, **App**.
5. Click **Apply**.

If the window opens with only colour options, that button has an Azeron binding on this profile. Clear it in Azeron Software to bind it here.

Also in that window:

- **Clear** empties the tab you are on.
- **Hold delay** (Hold tab) is how long you keep the button down before it counts as a hold.
- **Double-tap window** (Double tab) is how fast the two taps must be.
- **Any Profile** makes the binding work on every profile, not only the one you are viewing.

On the grid itself:

- **Drag** a button onto another to move its binding. If the other one has a binding, they swap.
- **Right-click** a button for **Copy Binding**, **Paste Binding**, **Unbind**, **Copy Color** and **Paste Color**.

## Combos

A combo is 2 to 4 buttons pressed together.

**Make one**

1. Click **Combo**. You get the list of your combos.
2. Click **+ Add New Combo**. The editor opens with your button grid in it.
3. Click the buttons that make up the combo. Each click adds that button; click it again to take it off.
   - Buttons shown in red can't be used: they already have an Azeron binding on that profile.
4. Set what the combo sends. Either:
   - click the box under **Firing command**, which changes to **Press a key...**, then press the key, or
   - click one of the six icons next to it to pick from a list.
5. **Profile scope** is where the combo works. It starts on the profile you were viewing. Change it to another profile, a software profile, or **Any Profile**.
6. Click **Save**. It stays greyed out until at least two buttons are picked.

**Change or remove one**

- Double-click a combo in the list to open it.
- Untick **Enabled** to switch it off without deleting it.
- **Delete** removes it.
- **< Back** leaves the editor without saving.

**Timing**

**Combo timing window** is how close together the presses must land to count as a combo. Raise it if combos don't register. Lower it if single presses on those buttons feel late.

## Software profiles

A software profile is an extra set of bindings that takes over while you hold a button.

1. Set **Viewing:** to the Azeron profile it belongs with.
2. Click **+ New Profile**, type a name, click **Create**.
3. Give it a trigger: click a blank button, click the **Layers** icon, choose your new profile, **Apply**. Holding that button now switches to it.
4. Set **Viewing:** to the new profile and bind its buttons the same way as any other.

To rename or delete one, open the **Viewing:** list and right-click it there.

If you bind a button on a software profile that also has an Azeron binding on the profile underneath, Companion warns you. It works, but release order matters: let go of the software profile's trigger button first and the Azeron binding fires.

**Wait for 2nd tap** appears when a trigger button also has a Double binding. Off, the profile switches the instant you press. On, it waits to see whether a second tap is coming first.

If you don't use software profiles on a particular Azeron profile, untick **Include software profiles** while viewing it. That hides them, and the **+ New Profile** button, for that profile only.

## Colours and covers

- Click a button, then **Fill Color...** or **Border Color...**
- **Button Covers...** in the same window puts an image on that button.

## Heatmap

Tick **Heatmap** to colour the buttons by how often you press them. While it is ticked, clicking a button shows its press counts instead of the binding window. Untick it to go back to binding.

## WoW spell icons (optional)

1. Install the **Azeron Companion** addon from CurseForge. In-game it is called *Azeron Bridge*.
2. In Companion: **Advanced**, then tick **Show WoW spell icons in overlay**.
3. In WoW: Options, Keybindings, AddOns, Azeron Bridge. Bind a key to **Reload UI**, then type `/reload` once.

Icons refresh each time you `/reload`.

## Good to know

- Your settings are saved in `%APPDATA%\Azeron Companion\`.
- Companion keeps no log of what you press.
