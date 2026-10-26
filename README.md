# ABJEXT Studio

**Formerly Semiotic Studio. This is the official home of ABJEXT Studio.**

Due to a naming conflict Semiotic Studio is now Abjext Studio. The owner of Semiotic Studio reached out and because he had chosen the name first the only sensible thing to do was change the name. 

Same project, new name. We’re adopting ABJEXT as our lasting identity as development continues. Existing Semiotic projects, presets, preferences, and MIDI mappings remain compatible. All future beta releases and update checks live here at **[sxrvys/Abjext](https://github.com/sxrvys/Abjext)**. The old Semiotic repository hosts one final transition release and historical downloads.

### Moving from Semiotic to ABJEXT

1. Save your project. In Semiotic, choose **Check for Updates** and download the final **0.8.2 transition release**, or download ABJEXT directly from this repository’s [Releases](https://github.com/sxrvys/Abjext/releases).
2. Quit Semiotic. Open the DMG and drag **ABJEXT Studio.app** into **Applications**.
3. Launch **ABJEXT Studio** and open your saved project. Your settings and mappings use the same storage as before; `.semiotic.json` project names remain valid.
4. After confirming everything is available, you may remove **Semiotic Studio.app** and replace its Dock shortcut with ABJEXT. Because the app’s name changed, macOS may keep both apps rather than replace the old one automatically. **Keep your project files, media, and application-support folders.**
5. From now on, **ABJEXT → Check for Updates** checks only this repository. Checks and downloads remain optional; no account or signup is needed.

The installer on the old repository keeps a `Semiotic-Studio-…` filename so existing updaters recognize it. It contains the same ABJEXT app as the installer here.

ABJEXT Studio is a native Mac application for experimental music videos, glitch art, and live visual performance. It brings a multitrack timeline, a playable clip sampler, and a video effects and synthesis engine into one workspace.

Build precise edits, layer and distort footage, map visual parameters to music or MIDI, and record a pad performance back into an editable timeline. From restrained processing to harsh feedback and rhythmic noise, the emphasis is on making the picture something you can perform.

**[Download the latest beta](https://github.com/sxrvys/Abjext/releases)** · **[Report an issue](https://github.com/sxrvys/Abjext/issues)**

This repository hosts beta installers, release notes, and user documentation. Application source is maintained separately. ABJEXT is under active development; save a copy of important projects before trying a new beta.

**New here?** [Install](#install) → [Make your first video](#start-here-your-first-video) → [Learn the workspace](#unified-workspace). [Shortcuts](#default-shortcuts) · [Troubleshooting](#if-something-seems-wrong) · [What changed in 0.9.8](#changelog)

**Current beta: 0.9.8.** Adds detailed timeline waveforms, draggable beat-grid alignment, video warp anchors, and **⌘J Bounce Selection** for turning a finished passage into one clip you can retime. Includes the export sync fix reported by **@mvbrtr** and the optional **[Global Thermonuclear War](#optional-bonus-global-thermonuclear-war)** audio plug-in.

## Requirements

- An **Apple Silicon Mac**: M1, M2, M3, or newer.
- **macOS 14 Sonoma or later**, unless an individual release specifies a newer requirement.
- Your own video and audio files. A MIDI controller is optional.

No Terminal commands, Python, pip, Xcode, TouchDesigner, Max, Ableton, additional codec package, or separate VCR-font installation are required. The app includes its resources and uses the media and graphics frameworks supplied with macOS. BlackHole is optional for routing audio from another application into ABJEXT's visual reactivity controls; ordinary editing, playback, export, MIDI, and soundtrack reactivity work without it.

## Install

1. Open **[Releases](https://github.com/sxrvys/Abjext/releases)** and choose the newest beta. Download the file ending in **`AppleSilicon.dmg`** under Assets. GitHub's automatic “Source code” archives are not the application.
2. Open the DMG and drag **ABJEXT Studio.app** onto **Applications**.
3. Eject the DMG and open ABJEXT Studio from Applications. For an update, save your project and quit the old app before replacing it; launch the copy in Applications, not the copy inside the DMG.
4. If macOS says the developer cannot be verified, first attempt to open the app, then go to **System Settings → Privacy & Security → Open Anyway** and confirm. These beta builds are locally signed but are not yet notarized by Apple. Only approve an installer from this repository or the developer.

If macOS instead reports malware or a damaged application, keep the warning intact and report the exact message. You do not need to disable Gatekeeper or run a quarantine-removal command. See [Apple's instructions for opening an app from an unidentified developer](https://support.apple.com/102445).

Allow access to folders containing your media when macOS asks. Microphone permission is needed only when using live audio input, including a virtual audio device.

## Optional bonus: Global Thermonuclear War

ABJEXT 0.9.8 includes **Global Thermonuclear War 0.1.4**, a separate Audio Unit effect for your DAW. Look inside the DMG's **Bonus - Global Thermonuclear War** folder, or download the **plug-in-only ZIP** from the same release. Installing the ABJEXT app does not automatically install this optional plug-in.

Five simultaneous repeat engines, waveform shuffle and reversing feed a three-oscillator Gristleizer, Percolator-inspired saturation, and digital destruction. Add wavefolding, hard chopping and CD skips, or turn stages off individually. Four presets provide starting points; **Wet / dry** and **Output** control the final blend and level. It captures incoming audio live, so no sample preparation is needed.

**Install:** save and quit your DAW. In Finder, choose **Go → Go to Folder…** and enter `~/Library/Audio/Plug-Ins/Components`. Copy **ABJEXT Global Thermonuclear War.component** there, then reopen the DAW. Create the Components folder inside Plug-Ins if it is missing. The included **Read Me - Audio Plugin.txt** walks through installation and use.

- **Ableton Live:** enable Audio Units in its Plug-Ins settings if needed, then search **Global Thermonuclear War** under **Audio Units → ABJEXT**.
- **Logic Pro:** look in an Audio FX slot under **Audio Units → ABJEXT → Global Thermonuclear War**. An actual Logic session has not yet been verified; the plug-in passes Apple's AU validation and has been used locally in Ableton.
- **Requirements:** Apple Silicon, macOS 14 or later, and an AU host. This download is not an Intel, Windows or VST3 build. Locally signed beta, not yet notarized by Apple.

Start with **Broken Playback** and a low wet amount. Click a stage title to toggle it. For parallel processing, use 100% wet on the effect track and blend with its track fader. **Six-band EQ…** opens a graph: drag numbered points for frequency/gain, scroll for the selected band's width/Q, or type exact values. Gray shows the spectrum before EQ, red after EQ, and white the combined response curve. The left scale is EQ gain; the right is spectrum level in dBFS. The EQ and analyzer operate on the **processed signal before Wet / dry and Output**, not on your final master bus.

This bonus processes **audio in a DAW**. ABJEXT's video effects continue to leave soundtrack audio untouched. You do not need the bonus to make or export videos. Send plug-in feedback to **abjextstudio@gmail.com**, including your DAW, macOS version and plug-in version.

## Stay current

In a build with the updater, open **Settings → Updates → Check for Updates**, or choose **ABJEXT Studio → Check for Updates…** from the menu bar.

Read the release notes and choose **Download DMG…**. ABJEXT downloads the installer directly and verifies its size and SHA-256 checksum before saving it. Use **Show Installer in Finder** when it is ready.

Save your project, quit ABJEXT, then open the DMG and replace the older copy in Applications. Your project files, source media, and saved preferences remain in their existing locations. A new beta may need macOS approval again. Older builds without the updater can download directly from Releases.

Update checks and installation are **manual and optional**. No GitHub account, signup, or background update service is required. The updater sends no project or media data. GitHub receives the ordinary network request needed to check or download a release.

## Start here: your first video

You only need a mouse/trackpad, **two or three video clips**, and optionally a song. Start small and add complexity once you can see and hear your first sequence. No MIDI controller is required.

### 1. Make a project and bring in media

1. Choose **New Project** on the welcome screen or **File → New Project**. Save it with **⌘S**.
2. Show **Media** in the top toolbar. Drag video files and your song from Finder into **Project Media**, or use **File → Import Media… (⌘I)**. You can also drag a Finder folder into the bin to keep that collection together.
3. The bin is your collection of sources; importing alone does not place them in the video. Click a thumbnail while stopped to audition it. **Program** returns the viewer to the project output.
4. The bin's **+** opens your configured library folder in a normal Finder window. Use the folder button to organize items inside the project.

A project is a readable **`.semiotic.json`** file containing your edits and settings. It references the original media; it does not pack those movies and songs inside itself. Keep source files available, and send the referenced media along with a project when collaborating. Save a copy before trying a new beta.

### 2. Put your song on the timeline

1. Choose **Timeline** in the working-view switch beneath the preview.
2. Drag the song onto **A1**, the first audio track. If you want it to begin at zero, place it against the left edge of the timeline.
3. Press **Space** to play/pause. **Enter** stops; press Enter twice to return to the beginning. Keyboard shortcuts leave text fields alone while you are typing.
4. In **Settings → Audio → Playback output**, select your headphones, speakers or audio interface. **Effects follow → Timeline audio** is the default visual-reactivity source.
5. Set the project **BPM** to your song's tempo for beat-based editing. Tempo is shared by the timeline and sequencer; set it deliberately rather than assuming importing a song establishes its BPM.

Audio stays on the timeline when you switch to Sequencer. Video FX never process the sound. Audio has its own trim, move, level and stretch controls.

### 3. Choose how to make the picture

| Start with… | Use it for… | First action |
| --- | --- | --- |
| **Timeline** | Arranging specific shots at specific times | Drag video onto V1 |
| **Sequencer** | Rhythmic cuts, repeating phrases and controlled randomness | Drag video onto a step |
| **Pads** | Playing clips by hand or MIDI | Drag video onto a pad |

These are connected parts of one project. Start in either view:

- **Timeline → Sequencer:** select video clips or enable a Work range, then choose **Send to Sequencer → Create Pattern from This Edit…**. Choose the subdivision and review the conversion. This makes an independent pattern; the original edit and music stay in place.
- **Sequencer → Timeline:** stop, choose **Add to Timeline…**, and choose **Independent clips** for hand editing or **Linked sections** to keep following pattern changes. Review the start, duration and passes before adding. The timeline opens after successful placement by default.
- **Timeline → clip pool:** choose **Send to Sequencer → Add Excerpts to a Clip Pool…** to reuse trimmed footage without converting the arrangement.

Switching tabs changes the working view; it does not itself copy or convert anything. Conversion constraints and omitted material are described in the transfer dialog.

**A straightforward timeline edit:** drag two clips onto V1. Normal drops append to the end of that track; Option-drop places at the pointer. Move clips to arrange them, drag an edge to trim, and use **⌘B** to split selected clips at the playhead. Select a clip to access speed/reverse and **Inspector → Appearance** for transform, crop and text. The track **+** adds more tracks.

**A first sequencer pattern:**

1. Switch to **Sequencer**. Keep **1 bar × 1/16** for sixteen steps in 4/4. Keep **Chance at 100%** while learning.
2. Drag one video onto **Clips A, step 1**. Select that step and set **Timing → Gate length** to **8**; press Enter to commit numeric edits.
3. Drag another video onto **step 9**, then set its gate to **8** too. This makes two sustained shots across the bar. The next successful hit on the same destination takes over from the previous one.
4. Press **Prepare Clips** while paused and wait for the readiness count. Press the main **Play** button or Space. The pattern loops while the timeline song advances.
5. Click a **step** for its controls in the lower-left inspector. Click the **lane header**—the box labeled Clips A—for defaults that apply across that lane. Step overrides can differ from those defaults.
6. For a longer phrase, change **Bars** in the sequencer toolbar: **2 bars × 1/16 = 32 steps**. Choose **All lanes** to resize them together. The current maximum is 64 steps per lane.

**Gate** is duration, measured in steps; it is not a count of repeats. A default gate of 1 only sustains for one step, so placing a single hit on step 1 can leave the rest of the bar black. **Retriggers** restarts the clip within a step. **Chance** decides whether the hit happens. For three repeats within a step, try Retriggers 3×; use a triplet subdivision for a triplet grid. Very short hits are limited by video frame rate.

To add overlapping footage, put clips on **Clips B**. New patterns use **Layer Stack**: each clip lane plays independently, the top row appears in front, and dragging lane headers changes the stacking order. There are up to **eight total sequencer rows**, including masks and FX. More simultaneous footage costs more decoding/rendering work; start small and use Prepare Clips. Existing patterns retain **Shared Targets** to preserve their appearance; switch them to Layer Stack while paused when ready. In Shared Targets, lanes aimed at the same destination replace each other's clips. Use lane/step opacity and blend settings, or **Appearance → Framing, Text & Split Screen** on a clip step for timed split-screen layouts. Rename a lane through its inspector or context menu.

**Use a moving mask:** drop a black-and-white video onto a **Masks** lane step. White reveals its target video layer; black hides it. Click the Masks lane header to choose its **Mask target** and default framing/transform. Select a mask step → **Appearance** for:

- **Mask target:** Follow lane, or choose a named clip lane for this hit.
- **Mask framing:** Follow lane, Fit, or Fill. Open **Transform & Crop** for scale, position, rotation, flips and crop. Editing a transform creates a step override; **Use lane transform** returns to the lane defaults.
- **Invert mask:** swap which source areas reveal or hide the video. Threshold and Softness shape the matte; mask opacity controls its strength.

Changes apply on the next mask hit. Each new hit replaces the previous mask from that Masks lane, even if its target changes. Use separate Masks lanes for overlapping masks on different targets. Recording and Add to Timeline preserve the chosen target and transform; timeline mask clips expose the same transform controls. Scaling or moving a mask leaves uncovered canvas hidden, including when inverted. Older masks keep their previous framing until you edit it.

**Make pattern variations:** use the **+** menu beside the pattern selector → **Duplicate Pattern**, then edit the copy. The selector lets you return to either pattern. Save the project with **⌘S** to keep all its patterns together; a project supports up to 16 patterns.

### Keep your song visible while sequencing

Expand **Song** below the sequencer toolbar to see your timeline soundtrack, markers, playhead and work range without leaving the pattern. The bar/beat readout uses your project BPM and beat-grid offset (4/4); importing music does not detect its tempo automatically.

- **While paused, click the waveform** to move the shared song playhead. **Drag across it** to set the work range; this follows the Timeline Snap setting.
- **Markers → a marker name** offers **Go to marker** and **Use section as work range**. A section runs to the next marker, or the timeline end.
- **Focus range** zooms into the selected passage; **Go to In** returns to its beginning. The readout tells you how many full passes of the current pattern fit, plus any remaining beats. It does not calculate a chain of differently sized patterns.
- Enable the existing **Loop** control to repeat that song range while developing your pattern. Pause before changing the range or seeking from the strip.
- **Add to Timeline…** starts at the enabled range's In point. Choose the number of passes in that dialog; Out does not crop the resulting pattern placement. The same work range also limits file export.
- **Edit audio in Timeline** returns to the full audio-editing view at the shared position. Collapse **Song** when you want more space for steps.

The strip reuses the existing waveform analysis and audio playback. It does not create a second soundtrack or change your pattern just because you navigate the song.

### 4. Make it react, then make it unpredictable

**Add an effect:** show **Inspector**, select the **Effects** tab and choose **Global** to process the combined picture. Use **+ Add**, choose an effect and raise its Mix/Amount as needed. Start with one effect so you can hear the music and see exactly what that control changes. New projects start dry; bypassed effects or Mix at zero do not change the image.

**Let the music drive it:** in **Settings → Audio**, choose **Effects follow → Timeline audio** and enable audio reactivity. Click the **music-note button** beside an FX parameter, choose Bass, Mids, Highs or Level, then set its Low/High response range. Play the song. Adjust **Sensitivity** and **Release** in Audio settings if the motion is too weak or too jumpy. A live input such as BlackHole is optional; your imported song is enough.

**Save a Colorizer setting:** open **Color → Creative color → Save Colorizer Preset…**. Recall it from **My Colorizer presets**; the same presets are available in the Effects inspector. This saves the creative Colorizer, including its modulation and automation. Use a saved chain for a look combining several effects.

**Give a step its own effect:** select the step and its **Effects** tab to open the full-sized step FX inspector. Its parameter changes become locks for that hit. An **FX lane** can schedule effect gates without changing the footage. Keep Chance at 100% initially and check the target rack is enabled. Global, layer, clip and step targets have different scopes—check the inspector heading before turning a control.

**Try a random pool:**

1. Click **Clips A's lane header**. Its named **Lane Clip Pool** appears directly in the inspector; drop several clips anywhere in that pool, including over existing choices.
2. Choose **Use all before reshuffling** to cycle through choices in changing order, or **No immediate repeat** to avoid the previous choice when alternatives exist.
3. Select empty steps (click the first, then Shift-click the last) and set **Timing → Chance**, for example 40%. Those steps now draw from the lane pool whenever their chance succeeds. **You do not need to Populate first.**
4. A fixed clip or a step's own pool takes precedence. Choose **Use lane pool for selected steps**, or the lane's **Use this pool for all steps**, to remove those overrides while keeping Chance, gate, FX and timing settings.
5. Play it. Each successful visit chooses from the pool; missed hits do not consume its choice history. A previous clip can continue through a miss until its gate ends.

**Populate / shuffle steps** remains optional for generating a rhythm with density and other controls. Choose **Choose from pool on every visit** for fresh draws; fixed assignments keep the generated clip. Populate replaces unprotected hits, so use Undo or a spare pattern while experimenting.

**Random durations:** in the lane inspector, enable **Random gate range** and set Min/Max, such as 1–5. **Whole steps** picks integer durations; turn it off for fractional values. In a step's **Timing → Gate mode**, choose **Follow lane**, **Fixed**, or **Random range**. Typing a manual gate makes that step Fixed. The next successful clip on the same lane/destination still takes over if it arrives before the previous gate ends. Recording and timeline placement use the same seeded gate decisions.

**Extend a phrase:** change to **4 bars × 1/16** for 64 steps. Click step 1, Shift-click step 32, then choose **Duplicate Steps** or press **⌘D** to copy into 33–64. This copies step pools, Chance, gates and overrides while keeping lane-pool inheritance live. Destination steps must already exist and be unedited; duplication is one Undo action. It copies the probability settings, not a recording of past random outcomes.

**Copy a phrase anywhere:** select any range (click the first step, then Shift-click the last), press **⌘C**, click its destination start, and press **⌘V**. Steps 3–5 pasted at 23 become 23–25. Multi-lane selections keep their lane offsets; nonadjacent selections keep their spacing. Paste replaces the corresponding destination settings, and **⌘Z** restores them. The whole selection must fit in existing compatible lanes; nothing is partially pasted. Pools, Chance, timing, gates, FX locks and appearance are retained. Same-lane pastes keep lane inheritance; cross-lane copies retain source pool choices and playback/mask settings. Copy/paste works within the current project, including between patterns. The selection-count menu and step context menu provide mouse equivalents. **Duplicate Steps / ⌘D** remains the way to repeat a phrase immediately after itself, into unedited steps.

**Move steps:** drag a step to another step in the same lane to move its complete settings. Drag any member of a selection to move the whole group, keeping its spacing and lane offsets. Occupied destination steps are replaced; the source is cleared. **⌘Z** restores both. The entire group must fit in compatible lanes, and moves are unavailable while recording. Right-click → **Move selection here** is a mouse-menu alternative.

**Shuffle a lane:** click any clip, mask or FX lane header and choose **Shuffle Steps** in its inspector, or right-click the header. Whole steps and rests move anywhere within that lane, carrying their pools, Chance, gates, FX, step automation and parameter locks. Protected steps stay fixed; lane-wide settings stay with the lane. **⌘Z** restores the previous arrangement. Duplicate a pattern first to keep the original as a separate variation.

**Keep a clip playing until the next hit:** select clip steps → **Timing → Gate mode → Until next clip**. Empty steps and probability misses leave the current clip playing, even across pattern loops. The source loops as needed. A successful replacement clip, Stop, or a song-section change ends it. For a lane default, click its header and enable **Lane Gate → Until next clip**, then leave the desired steps in **Follow lane**. Fixed or Random range steps still override that default. Recording and timeline placement preserve the finite result; placement ends any held clip at the chosen end boundary. The mode is for clip lanes; masks and FX retain timed gates.

**Weight** displays as a relative percentage: 100% is normal, 50% is half as likely and 200% is twice as likely. Equal weights share selections equally; these are not absolute probabilities. Weight changes how likely a clip is relative to other choices; **Chance** changes whether the step fires at all. A step's own **Random clip choices** pool is independent of the shared lane pool. **Shuffle clips** changes assignments on existing hits without moving their timing. **Variation… → Store** saves a pattern checkpoint, **Mutate** creates a variation, and **Restore** returns to the checkpoint. The control beside Mutate selects allowed categories and amount; protect steps you want kept.

For a locally off-kilter phrase, click one step and Shift-click another to select the range. Use **Timing → Swing, movement & microtiming**. The rest of the lane keeps its defaults. Reverse traversal reverses the order of steps, not the movie inside each step. Ping-pong adds return visits, so it lengthens the cycle.

### 5. Arrange sections and keep a result you love

Use **+ beside the pattern selector → New pattern** or **Duplicate pattern** for another section. The selector lets you return to edit earlier patterns. Open **Song Arrangement**, drag named patterns into the arrangement, and set their pass counts—for example Verse ×4 → Chorus ×2. Enable **Play song arrangement** to follow those cards. **Loop song** repeats the arrangement; otherwise it stops at the end. The first clip lane defines each pattern's master duration.

To work on only part of the music, set and enable a **Work range**, enable **Loop**, then use the sequencer against that section. Both views honor the same audio range. With a range enabled, placement starts at its In point.

| To keep… | Use… |
| --- | --- |
| Patterns that stay linked to the timeline | Stop, then **Add to Timeline… → Linked sections** |
| Independent editable cuts from the current pattern/song | **Add to Timeline… → Independent clips** |
| The particular choices and live actions you perform | Sequencer **Record to Timeline**, then **Stop & Keep Take** |
| A moment that just happened, with preview history armed | **Keep That** |
| A movie of the processed preview from now onward | **File → Capture Preview…** |
| A finished timeline movie at delivery resolution | **File → Export Mix…** |

**Linked sections:** named blocks appear above the timeline. Click a block for its inspector; double-click to edit its pattern. Pattern edits update linked occurrences once playback stops. Drag a block to move its clips, masks and FX together. **Play from Section** starts timeline playback there. **Make Unique** gives that occurrence its own pattern.

- **Linked** follows pattern edits while retaining a stable random seed.
- **Evolve** chooses a fresh variation when timeline playback starts. Export uses the currently resolved variation; it does not reroll it.
- **Locked** keeps the resolved clips and FX even when the pattern changes. Use **New Variation** before locking to try another result.

Changing a linked pattern's length moves subsequent song sections to make room; unrelated clips and audio stay fixed. Collisions or locked tracks prevent an update and produce a message. Hand-editing generated clips protects those edits by locking the section on its next refresh. Use **Refresh Links** after resolving an obstruction. Up to 128 timeline sections and 16 source patterns are supported; very large hit/fragment expansions are checked before placement.

**Independent clips** resolves probability into ordinary clips, masks and FX automation. Those clips no longer follow the pattern. **Record** keeps actual live choices. Switching views alone does not transfer a sequence: place or record it before a timeline export. If a take cannot be placed, read the message and use **Take → Place pending take** after resolving the issue.

**Keep That:** open the arrow beside Keep That and enable **Arm preview history** before experimenting. Choose the last 1, 2, 4, 8 or 16 bars (4/4), then click Keep That after a good moment. It saves the actual processed preview, feedback, random outcomes and knob moves, with timeline audio, to your configured recording folder (Movies by default). It is a flattened movie at preview quality, not editable clips or a full-resolution rerender. Live-input audio must first be recorded onto the timeline. The rolling encoded-video buffer is capped at 120 seconds / 128 MB; encoding and temporary saved output use additional resources. Disarm it when not needed. Changing preview format or opening another project disarms history.

Before exporting, switch to **Timeline**, return to the beginning and play the result. Check the soundtrack, picture, work range and end point. Open **File → Export Mix…**, choose a destination and format—H.264 MP4 is a convenient first delivery—and include timeline audio if wanted. A range enabled for export limits the portion rendered. Export resolution is independent of preview quality; Capture Preview uses the preview quality instead.

## If something seems wrong

| What you see | First things to check |
| --- | --- |
| A source previews, but the sequence is black | Is a hit enabled and assigned? Is its lane visible and its destination opacity above zero? Try Chance 100%, a longer Gate, and Prepare Clips. Source audition is separate from project playback. |
| Black between hits | Gate may end before the next hit. Increase it or add hits; a probability miss is intentional silence in the sequence unless a previous gate is still sustaining. |
| The music is silent | Check the audio clip's position, track mute/level, Settings → Audio → Playback output, and the interface/headphone volume. |
| FX do nothing | Check Global/layer/clip/step target, rack/effect bypass, Mix/Amount, and whether that step is currently active. |
| Audio mapping does nothing | Check Effects follow → Timeline audio, Enable audio reactivity, that audio is playing, the selected band and Low/High range. |
| A click edits the wrong thing | Lane headers select lane defaults; step cells select local controls; the right inspector heading identifies the FX target. |
| Clips are preparing or playback skips | Pause, choose Prepare Clips, and inspect readiness details. “Ready ahead” means the upcoming window is prepared; it does not mean every project source is resident. Use 360p · Light and keep media drives connected. |
| Your exported result differs from the sequence | Confirm you placed or recorded it onto the timeline. With probability below 100%, a fresh Add to Timeline can make different decisions from a live performance; Record keeps what you actually played. |

**⌘Z** is your friend. Save versions as you experiment, and report confusing behavior as well as outright bugs. Start with the short recipe above before stacking many layers, long feedback histories and large random pools.

## Unified workspace

**Timeline / Sequencer** switches the lower working view without stopping playback. **Media**, **Pads**, and **Inspector** toggle independently in the top toolbar. **FX Controls** and **Automation** open above/below the working view. FX Controls is optional and starts collapsed; live recording/scenes/controller tools are grouped under its **Live tools** toggle. Sequencer **Record to Timeline** remains directly available without opening those tools. Macros and automation take turns in the detail space so the working area stays usable. **Focus** collapses the browser and inspector while keeping pads available; panel visibility is remembered. Source and canvas controls live in **Settings → General**. Project actions, export, and preview capture live in **File**.

### Editing

- **Multitrack editing:** video and independent audio tracks; trim, split, move, duplicate, copy/paste, ripple delete, and group editing.
- **Timing:** clip speed and reverse, Shift-drag rate stretching, beat grid, tap tempo, and video quantization. Video edits do not automatically rearrange your audio.
- **Compositing:** stacked clips, blend modes, opacity, split-screen placement, track visibility/solo/lock, and dedicated mask clips.
- **Automation:** editable parameter envelopes, audio-reactive mappings, and recorded control changes. Arm the relevant Write controls when recording parameter or macro automation.
- **Color and effects:** neutral grading plus global or per-clip FX chains. Reorder effects, save individual presets, and save complete Looks and playable racks.
- **Monitoring:** adjustable preview quality, a larger popout preview, and fullscreen output to an available secondary display.

Dragging a clip edge normally trims or reveals source material. **Shift-drag the edge** to stretch its duration and change playback rate. Audio stretching offers **Vinyl** (speed and pitch together) and **Tempo** (preserve pitch) modes.

### Crop, transform, and text

Open **Inspector → Appearance** in the right inspector, then select the video you want to edit. The **Editing** selector identifies the current target: Timeline, Media, Pad, or Step.

- **Media:** set source defaults before placement. New timeline clips and newly assigned pads copy these settings; existing placements stay unchanged.
- **Timeline:** edit selected clips. Multi-selection patches the control you changed while preserving each clip’s other settings. Split, duplicate, copy/paste, and project save retain the appearance.
- **Pad:** adjust that pad’s source snapshot without changing the original media-pool item.
- **Step:** override framing/text for a clip-lane hit, including clips selected from a weighted pool. **Use source appearance** restores inheritance for the selected steps. Play the sequence to see a step’s settings.

**Editing several items:** select a range of steps with Shift-click, then change an Appearance control. Only the changed fields are applied: for example, scaling two steps keeps their separate text, rotation and Noir settings. Undo reverses the batch together. Timeline video opacity and Direction show **Mixed** when selected clips differ; timeline mask opacity does too, and the mask target readout identifies whether the selection affects different targets.

**Appearance from a pool:** a step follows its source defaults until you override it. If pool members have different defaults, the inspector names the clip it is showing and says **Varies by clip choice**. Editing creates one appearance override for all choices on that step. **Use source appearance** removes the override and restores each source’s own defaults.

Expand **Transform & Crop** for scale, X/Y, rotation, flips, and frame-edge cropping. Position and crop values are normalized to the canvas; crop happens before transform. Transparent areas reveal lower video tracks. These are numeric/slider controls; direct on-preview transform handles are not included in this beta.

Expand **Text** to enter multiline text and choose a font, size, color, alignment, position, wrapping width, opacity, black outline, and black background. A compact font list includes bundled **VCR OSD Mono**; **More Fonts…** opens the installed system-font list when needed. System Bold is the default. Missing fonts fall back to the system font; fonts are not embedded in project files. Text is attached to its clip or step gate. For a title during only part of a timeline clip, split that section and add text to that fragment. Standalone title tracks and phrase sequencing are not included in this beta.

**Send text through clip FX** puts typography into the clip processing chain. Leave it off for text after clip FX; global FX still affect the complete image. Source audition shows framing and text; it does not apply timeline/global FX. All edits are nondestructive.

### Playing clips and sequences

Open **Pads** and **FX Controls → Live tools** to play clips while keeping either the timeline or sequencer available. There is no separate Performance mode.

- Drag a Project Media thumbnail onto a pad to assign it. Use Gate, Toggle, or One shot behavior to suit the clip.
- Ten pad banks provide space for clips and assignable performance actions.
- Eight macros can control individual FX parameters or combinations of parameters. Save a rack to reuse a setup.
- Use the performance **Record** control to write pad performances into the timeline for later editing and quantization.
- Play three independent live layers. Choose **A**, **B**, or **C** before triggering a pad, or assign a fixed layer in Pad Settings. Each has its own FX rack, opacity and blend mode. The crossfader controls A/B; C remains independent. Lanes assigned to the same target replace one another rather than adding another simultaneous layer.
- Layer **FX** opens its own rack. Global FX process the combined picture. MIDI Map can assign layer parameters, opacity, the crossfader, or scene recall without replacing existing SP-404 mappings.
- **Scenes** saves named snapshots of clip assignments, the live layers, the global rack and macros, and the selected pattern. Recall uses the Launch interval while playing; new pad hits use the recalled assignments. Recorded scene changes replay on the timeline and can be edited in Scenes → Recorded rack changes.
- **Sequencer** opens the step lanes in the timeline area, keeping the preview visible. Start with two clip rows, a mask row, and an FX row; expand to eight independent rows with 1–64 steps each.
- **Reorder sequencer lanes:** drag the entire lane header (the “Clips A / Drop a clip here” box) onto another header, or right-click it and choose **Move Up / Move Down**. The row’s clips, steps, masks and FX move together. In Layer Stack, clip-row order also controls front-to-back composition; Shared Targets keeps its explicit routing. Order is saved with the project and supports undo. Audio is arranged in **Timeline** and continues playing with the sequencer. Select a step to edit its **Timing / Appearance / Source / Effects / Pattern** controls in the left sidebar beneath Media and Pads.
- **Media** and **Inspector** in the top toolbar collapse independently. **Focus** above the working view hides both; **Restore panels** brings back the previous combination. The divider above the performance controls adjusts preview versus sequencer height.
- Drag Project Media or a pad onto a lane to choose its source, or onto a step to assign a different clip. Click empty steps to add hits; select a lit step to edit it, then click it again to disable it. The left sidebar groups controls into Timing, Appearance, Source, Effects and Pattern. Weighted clip pools are available under **Source → Random Clip Pool**. Drop clips anywhere in the expanded pool, including on an existing entry, to append choices. A higher Weight makes a choice more likely; Chance determines whether the step triggers at all.
- Steps support weighted clip pools, probability, gate length, retriggers, frame-aligned microtiming, per-step source starts, first/every-N/previous-result conditions, and Fill. Mask and FX rows can run at different lengths from the clip rows.
- FX steps can gate an effect or saved chain and lock individual parameters without retriggering the footage. Use **Use for lane** to give new steps the same default FX assignment.
- Open **Variation…**, then hold **Fill**, or enable **Latch fill**, for Fill-only steps. **Store → Mutate → Restore** offers a reversible way to try variations. These performance buttons can be assigned through MIDI Map without changing existing controller mappings.
- **Independent clips:** choose **Add to Timeline… → Independent clips**, then enter **1–64 passes per pattern**. Each pass evaluates clip probability, weighted pools and FX gates independently using the saved seed/current Fill state. Chained patterns use the same loop count. This writes resolved clips, masks and FX automation, rather than duplicating the first pass. At less than 100% Chance a step can legitimately be absent; set Chance to 100% for guaranteed hits (Wet/Dry still controls effect strength). **Record** captures the actual live choices; stopping places editable clips, masks, and FX automation on the timeline. Probability never rerolls a recorded take during export.
- Open **Settings → Control Surfaces** to enable MIDI and select a detected input. The SP-404MKII setup provides clip triggering and performance controls; generic MIDI Learn supports other controllers.
- Use **MIDI Map** in the top toolbar, click a highlighted software control, then move or press the hardware control you want to assign. Existing assignments are preserved unless explicitly changed. Settings retain the selected controller and saved mappings.

Pad-bank and knob behavior depends on the controller profile and your mappings. Check the on-screen labels when changing macro pages or assigning utility pads.

**Selecting and moving steps:** click the first step and Shift-click the last for an inclusive range. ⌘-click toggles individual cells. Drag any selected step to move the group; right-click a destination → **Move selection here** aligns the first selected cell with that destination. Existing hits are protected from accidental replacement. Empty cells can carry lane-wide gate values without blocking a move.

**Build visuals against a section of music:** set and enable the work range in Timeline (In/Out or Loop Selection), enable **Loop**, then switch to Sequencer. Both views use the same audio range. Sequencer also exposes **Loop** and **Work range…** beside the tempo. Stop, then use **Add to Timeline…** to write at the range’s In point. Placement length follows the pattern/chain and chosen loop count. Recording finishes at Out rather than overwriting its own take on subsequent audio loops.

**Reuse a precise timeline excerpt:** select a trimmed video clip and click **Send to Sequencer → Add Excerpts to a Clip Pool…** in the timeline toolbar (also **Timeline → Send Timeline Selection to Sequencer Pool…**). To extract just part of it, enable **Work range**, mark In/Out, and choose **Selected clips within work range**. Choose a pattern and clip/mask lane, then **Add to Pool**. This opens that lane's inspector; use its pool and Populate steps to build a sequence. Multiple selections become separate pool choices. The same file can contribute several different excerpts, each labeled with source times. Existing steps and weights stay intact; identical excerpts are not added twice.

The transfer keeps source marks, speed, reverse and framing without making another media file. A longer gate loops within the excerpt. Lane/step playback overrides still take precedence. Audio, timeline FX, opacity and blending stay on the timeline; use Create Pattern for an arrangement conversion or Render in Place when you want clip processing baked into the source. One Undo removes a transfer. Maximum 160 choices per lane pool and 4096 sequencer sources per project still apply.

**Timeline and patterns:** switching views does not convert cuts into steps. Sequencer clips temporarily replace timeline footage on their destination video track while playing. Linked song sections follow pattern changes; Independent clips creates an independent edit. Hand-editing a generated section protects it from later replacement.

## Preparing larger arrangements

Create separate patterns for sections such as a verse, chorus, and bridge, then arrange them in **Song Arrangement**. The older pattern **Then** control remains available when Play song arrangement is off. Each lane can contain up to 64 steps; independent lane lengths and divisions are supported. Different patterns can use different clips and random pools.

Before performing, pause and choose **Prepare Clips** in the Sequencer toolbar. Click the readiness count for source details and Retry/Replace controls. A small linked chain shows **N/N ready**. A larger chain shows **N/N ready ahead**: only the upcoming window is loaded, while later choices remain **On demand**. This is normal. The eight-second forecast uses the saved random seed and weighted choices without changing the probability decisions.

The project supports up to 4,096 sequencer source slots in addition to the controller pads. This storage allowance is separate from the shared 64-player preparation cache and is not a promise that thousands of sources can play at once. Layer Stack supports independent clip layers within the eight-row sequencer limit; masks and FX rows count toward that limit. Masks, timeline playback, and FX/history have additional resource costs. A new hit on a destination cuts the previous clip; different destinations can overlap.

Start at **360p · Light** for complex performances. Preview resolution does not reduce the resolution of an Export Mix render. Keep external source drives connected. Slow drives, difficult codecs, heavy FX, or an abrupt jump to an unprepared pattern can still cause late or missed hits. If a source is unavailable, pause, open readiness details, and retry or replace it rather than repeatedly starting playback.

## Effects and video synthesis

The toolbox includes delay and feedback, reverse and stutter processing, gated tremolo, CRT and tape character, dithering, colorization, spatial distortion, kaleidoscopic geometry, and flipbook-style animation.

The synthesis tools extend that into **Raster Synth**, scan-line displacement, **Video FM**, **Wavefolder**, **Ring Modulator**, **Polar Oscillator**, **Vector Scope**, **Clocked Noise**, and **Video Logic Mixer**. Combine oscillators, beat-clocked patterns, masks, and footage into shifting textures and geometry. Factory presets and playable racks offer starting points; individual controls remain available for automation, MIDI, and audio modulation.

**Effects, chains, racks, and macros:** an effect is one processor; a chain is the ordered collection of processors. **Save Chain / Rack…** stores the chain together with its macro assignments and envelopes. **Saved Chains & Racks…** recalls that setup, adds the complete chain as one FX slot, or assigns it to one macro. A macro is a playable control that moves one or several parameters. **Save FX Preset…** stores only the selected effect. These controls are in the Effects inspector; **Racks** above the working view also offers factory performance setups.

### Your first FX Control

FX Controls are optional shortcuts for moving several visual parameters with one slider. You can use them with a mouse, automation, or MIDI; you do not need to be performing live.

1. Open **FX Controls** above the working view. Click **Assign FX…** on an empty slot, or click a named slot to edit it.
2. Choose **Add effect from library…**. This adds the effect and immediately maps its wet/dry control. To control an effect already in your chain, expand **Map a parameter from the current chain**, select its Effect and Parameter, then click **Map parameter**.
3. Set **At 0%** and **At 100%** for each assignment. These are the parameter values at the two ends of the macro slider; swapping them reverses its movement. Move **Try it** to see the result. Add more assignments if one gesture should change several things.
4. Give the control a useful name. **Save your project** to keep the setup there. Choose **Save Chain & Controls…** to reuse the complete chain and its controls in another project. This is a whole-setup save, not an individual effect preset.
5. To connect hardware, use the top-toolbar **MIDI Map** button, select the control and move a knob. MIDI mapping chooses the hardware; the FX Control editor chooses what that hardware changes.

Mapped assignments override those same parameters in the FX inspector. If a parameter seems to keep returning to a value, check its macro assignments and automation. For a single effect's reusable settings, use **Save FX Preset…** in the Effects inspector instead.

**All FX process video only.** Audio tracks keep their own editing, level, and stretch controls.

For music-driven visuals, start with the timeline soundtrack, then use the **music-note button** beside an FX parameter to assign level, bass, mids, or highs. Set the response range in that popup; choose the audio source and global sensitivity in **Settings → Audio**. The same popup offers beat, oscillator, and random modulation. Live input from BlackHole or another audio device is a secondary option for following Ableton or another application.

### Optional lightweight preview copies

If compressed source media is expensive to seek/decode, pause and click the **bolt-circle button in Project Media**. Choose **Prepare Selected Media** or **Prepare Project Video**. ABJEXT makes 360p/30 fps ProRes preview copies one at a time, with a 4 GB disk budget. Timeline and pad/sequencer playback use available copies; offline export still reads the originals. Audio is unchanged. Alpha-channel sources remain original. Live capture/Keep That naturally reflects the preview quality.

This is separate from **Prepare Clips**, which warms the upcoming sequencer voices. Proxies reduce decoding work; they cannot remove heavy FX processing costs. **Clear Preview Copies** removes only the generated cache while stopped. Original media remains required. The status bar's clickable millisecond reading shows recent median/p95 frame completion time; it is not a measurement of total MIDI-to-display latency. Preview remains 30 fps; export frame-rate choices are unchanged.

## Align music and video precisely

**The song stays unchanged throughout this workflow.** Adjust the beat grid to the recording, then retime video actions to those beats.

1. Open **Timeline** and zoom into the audio waveform. You can now zoom to 2,000 pixels per second; the waveform retains short transients instead of becoming a sparse set of bars.
2. Click **Align Grid** beside BPM. Drag **◆ 1** onto the first musical hit. This moves the grid origin while keeping BPM fixed.
3. Drag a later numbered beat onto its corresponding hit. This adjusts BPM around beat 1. Use a hit farther into the song for a more precise estimate. The project uses one constant BPM, not a variable tempo map. Existing timeline clips and the audio do not move; sequencer timing follows the updated BPM.
4. For a specific visual action, select its timeline video clip, seek to the action, choose **Warp** in the edit-tool selector, and click **Add Warp Anchor**. You can also right-click the clip and choose **Add Warp Anchor at Playhead**.
5. Drag the new diamond onto the intended beat. The adjacent video sections stretch while surrounding anchors stay fixed. **Option** bypasses beat snapping. Add more anchors wherever needed; there is no arbitrary count limit. Sections must remain at least one timeline frame and within **¼×–4× speed**. Audio stays fixed. Undo restores each edit.

Warp anchors appear as boundaries between editable, source-preserving sections. They are saved with the project. This changes playback speed; it does not synthesize new in-between frames.

### Turn a sequencer passage into one warpable clip

Use the sequencer's **Add to Timeline** to place your chosen result, then select the timeline video clips that define the passage and press **⌘J**, or choose **Timeline → Bounce Selection…**.

**Bounce Passage** renders the complete visible picture over that time range: all overlapping video tracks, masks, local and global FX, and automation. It replaces the selected clips with one ProRes movie on a new top track. Other clips remain underneath, and the soundtrack remains separate. You can now add warp anchors inside the finished mix.

The finished clip is marked **MIX / FX BAKED**. **Global FX are bypassed while it is visible**, so baked effects are not applied twice. That bypass also affects other layers visible alongside the finished mix. Clip-level effects remain available. Use **Render in Place** instead when you want individual clip processing baked while global effects stay live.

Save the project before bouncing. The app needs one free top video track. Bounces use the chosen export resolution at 30 fps; ProRes files are larger than delivery MP4s. Keep the adjacent **Renders** folder: it contains the new movie and a complete pre-bounce project backup. **⌘Z** restores the selected originals. Select a bounced clip and choose **Timeline → Reveal Pre-Bounce Project** to locate the backup and reopen the full original arrangement later. New saves use project format 28 and require ABJEXT 0.9.8 or newer.

## Default shortcuts

These are the factory bindings. Timeline commands apply when you are editing the timeline, not typing into a text field. Customize them in **Settings → Shortcuts**; the Timeline menu shows current bindings.

### Transport and navigation

| Action | Shortcut |
| --- | --- |
| Play / Pause | Space |
| Stop | Enter |
| Return playhead and timeline view to the beginning | Enter twice |
| Shuttle backward / stop / forward (silent) | J / K / L |
| Previous / next frame | ← / → |
| Back / forward ten frames | Shift + ← / → |
| Previous / next cut | ↑ / ↓ |
| Previous / next beat division | [ / ] |
| Zoom in / out | = / − |
| Fit entire timeline | Shift + Z |
| Zoom to selection | Option + Z |
| Match frame in source viewer | F |

### Editing and timing

| Action | Shortcut |
| --- | --- |
| Split at playhead | ⌘B |
| Delete selected clips, leaving a gap | Delete |
| Ripple delete on selected tracks | Shift + Delete |
| Duplicate selection | ⌘D |
| Copy / Cut / Paste at playhead | ⌘C / ⌘X / ⌘V |
| Paste video attributes | ⌘Shift + V |
| Select all clips | ⌘A |
| Undo / Redo | ⌘Z / ⌘Shift + Z |
| Nudge selection one frame | Option + ← / → |
| Nudge selection ten frames | Option + Shift + ← / → |
| Nudge selection one beat division | Option + [ / ] |
| Toggle snapping | S |
| Quantize video | Shift + Q |
| Set work-range In / Out | I / O |
| Go to range In / Out | Shift + I / O |
| Clear work range | Option + X |
| Loop selection | ⌘L |
| Add marker | M |
| Selection / Slip / Roll tool | V / Y / R |

Ripple delete removes the selected material and closes its gap on the affected tracks. Quantization uses the project's tempo and chosen beat division; it does not analyze the musical intention of each cut. Preview the result and undo if needed.

### Projects and mouse gestures

| Action | Shortcut or gesture |
| --- | --- |
| New / Open project | ⌘N / ⌘O |
| Save / Save As | ⌘S / ⌘Shift + S |
| Import clips | ⌘I |
| Settings | ⌘, |
| Quit | ⌘Q |
| Scrub | Drag the playhead |
| Rate stretch | Shift-drag a clip edge |
| Zoom timeline | Trackpad pinch |
| Larger preview window | Double-click the preview |
| Add or manage tracks | Timeline + or track context menu |

## Black & White and Film Noir

Select a video clip and open **Inspector → Appearance**. For a sequencer clip step, choose **Appearance → Clip Appearance…** in the step inspector to open the full controls on the right.

- **Black & White** converts the picture to neutral grayscale.
- **Film Noir** adds deeper blacks and brighter whites, starting at **0.65 Noir strength**.
- **Noir strength** adjusts the contrast from neutral monochrome at 0 to a harder look at 1.
- **Original** removes this monochrome adjustment without resetting framing, text or other effects.

The **Editing** selector identifies whether you are changing a timeline clip, media source defaults, a pad or a step. Media defaults are copied into new placements; existing placements retain their own settings. Step appearance overrides also apply to clips drawn from that step's random pool. The adjustment is saved with the project and follows clips into timeline placement, preview and export. Source media files are never rewritten.

This is a source appearance adjustment **before clip and global FX**. A later Colorizer or other effect can add color again. Text keeps its own color. Masks retain their separate threshold, inversion and framing controls.

## Media and export

Common verified inputs include **H.264 MP4/MOV**, **HEVC MOV**, and **ProRes 422 MOV**, plus **MP3, WAV, FLAC, AIFF, AAC/M4A, ALAC/M4A, and CAF** audio. Import uses macOS decoders and checks the actual file; an extension alone does not guarantee compatibility. DRM-protected files are unsupported.

**Export Mix** produces **H.264 MP4**, **ProRes 422 MOV**, or **ProRes 422 HQ MOV**, with **AAC audio** when included. Choose 720p, 1080p, or 4K-class resolution; 23.976, 24, 25, 29.97, 30, 50, 59.94 or 60 fps; and landscape, square, or portrait framing. Instagram-oriented presets are included. Export renders the original sources at the chosen output size, independently of the lighter interactive preview.

The current pipeline targets SDR Rec.709 delivery. Transparent video export and HDR mastering are not currently offered. ProRes files are larger than H.264 files. For unsupported input, convert to H.264 MP4, ProRes MOV, or PCM WAV before importing.

**Capture Preview** records the processed preview plus the timeline soundtrack. Enable or disable audio in **Settings → Export**. Pauses and seeks are captured; finishing streams the retained soundtrack into the movie. Live input drives visual reactivity; record it onto an audio track first if you want it included. Video effects never process audio.

For lighter machines, start with **360p preview**, shorter feedback/rewind histories, and fewer simultaneous layers. Use 720p preview when judging fine masks and texture. Live capture follows preview quality; use Export Mix for delivery resolution.

## Feedback

Open **Settings → Beta Feedback** or **Help → Send Beta Feedback…** to write a subject and notes, then choose **Open Email Draft**. Your mail app opens a message to **abjextstudio@gmail.com**; review it and press Send there. ABJEXT itself sends nothing. There is no GitHub account requirement.

**Include app version, macOS and memory** is optional and off by default. Its exact contents appear in the form before you open the email. Projects, media, file paths and logs are never attached automatically. The subject and notes are saved locally on your Mac so you can return to an unfinished draft.

If you use Gmail or another webmail service, choose **Copy Feedback** and paste it into a new email to **abjextstudio@gmail.com**. This also works for long reports that will not fit in an email link. If your default mail app is not configured, use this copy option.


Found a problem or an awkward workflow? [Open an issue](https://github.com/sxrvys/Abjext/issues) with:

- ABJEXT's version and build number from About or Settings → Updates.
- Your Mac model and macOS version.
- Steps to reproduce, what you expected, and what happened.
- A screenshot or a short sample you have permission to share, if helpful.

Issues here are public. Avoid posting client footage, private project paths, or other confidential material. Small reproducible examples are especially useful during the beta.

## Playing the new interruption effects

Open **FX → Add → Signal damage** to find **Signal Emergence**, **Halftone / Print Damage**, and **Pixel Sorting**. Each has three factory presets. Raise **Wet / dry** to engage it; zero returns to the incoming picture immediately.

For a ready-to-play set, open **Racks → Signal Interruptions**. Its eight macros start dry. With the SP-404 profile, hold an assigned FX macro pad and turn CTRL 3 to adjust that macro; release the momentary pad to restore its previous value. Toggle pads deliberately remain engaged until pressed again.

In the sequencer, use an FX step and its gate to interrupt all footage for a chosen duration, or put FX on an individual clip step. Open that step’s FX inspector to set parameter locks. Click a parameter’s music note to map it to bass, mids, highs, level or beat modulation.

- **Signal Emergence:** sweep Signal reveal to make forms appear in static; use Density to starve the image and Scatter to tear it apart. Beat sync holds a random pattern for each division. Free rate zero freezes the random pattern while footage keeps moving.
- **Halftone:** start with Bootleg photocopy, then play Screen size and Ink spread. Choose Color screens to enable misregistration. Paper damage and New chaos pattern produce repeatable broken print.
- **Pixel Sorting:** play Sorted cell width and the brightness limits. Horizontal/Vertical and Reverse change the direction; Sort by chooses brightness or a color channel. Out-of-range cells remain in place. Block scatter can change on the beat. Width is rounded to physical pixels at the current render resolution.

The new effects do not add automatic decay or frozen tails. Draw a wet/dry envelope for a fade-out, or deliberately combine them with existing delay/freeze tools. Video FX never process your soundtrack.

## Physical and analog interruptions

Add these from **FX → Add**, or load **Racks → Physical Violence** / **Analog Breakdown**. Racks start dry and preserve MIDI mappings; loading one replaces the eight macro assignments and is undoable.

| Effect | What to expect |
| --- | --- |
| Frame Breaker | Tiles from a captured frame bank, running forward, backward or frozen |
| Impact / Aftershock | Zoom, displacement, inversion and diminishing jolts |
| Contour Shredder | Jagged tears following image boundaries |
| Motion Corruption | Displaced blocks and smears in moving regions |
| Signal Dropout | Missing scan bands and held, damaged fragments |
| Temporal Collision | Difference/subtraction against an earlier frame |
| Sync Strike | Tears and rolling picture that recover into alignment |
| Dirty Mixer | Unstable competition with an earlier image or underlying layer |
| Chroma Unlock | Crawling color bands, displaced chroma and color loss |
| Feedback Slam | A sudden injection into an expanding, rotating feedback return |
| Key Chatter | Unstable brightness switching with hysteresis |
| Tape Snatch | Picture yank, skew and a travelling damaged strip |

Each has five mappable controls and three presets. All process video only. Motion Corruption approximates compression damage; it does not use optical flow or corrupt your media files.

**Trigger & recovery**, beneath Wet / dry in the FX and sequencer FX inspectors, adds a shared **Burst** option. A rise from zero fires attack, hold and decay, in beats or seconds, with 1–8 hits and seeded hit-strength variation. Releasing the pad lets the burst finish. Return the gate to zero to rearm it; consecutive sequencer gates without a zero gap are one trigger. Record the gates to reproduce the same envelope on the timeline and in export. Clear Tails cancels active bursts.

Choose **Follow gate / latch** for normal wet/dry control: Gate pads hold an effect; Toggle pads latch it. Trigger configuration belongs to the effect instance, so steps sharing it share the envelope. Duplicate an instance for another shape. Processor parameters still support step locks and music-note mappings. The new racks preconfigure their impact/recovery effects as bursts.

Temporal effects capture a bounded history after activation, so the very first short hit has less past footage available. Returning to dry releases that history. Multiple temporal effects at high resolution still use more resources; use the light preview while performing and Render in Place for finished heavy passages.

### Dot Matrix and Contour Scan

Open **FX → Add → Video synthesis**:

- **Dot Matrix** rebuilds the picture as dense illuminated dots against black. Start with **Ember matrix** for red/orange silhouettes. Play **Dot columns**, **Dot size**, **Dither texture**, and **Black cutoff**. Luma deflection bends the grid; Signal breakup tears holes in it.
- **Contour Scan** draws glowing lines that bend around source brightness. Start with **Ember contours**, then play **Luma deflection**, **Carrier lines**, **Line width**, and **Signal breakup**.

Each includes three presets, adjustable phosphor hue and highlight heat, glow, and signed drift. **Screen drift = 0** holds the screen still. Map **Screen phase** to Beat sine, or map deflection/breakup to bass or another audio band using the music-note button. Use 720p preview to inspect fine marks: very dense screens are limited to resolvable cells at the current render resolution.

For immediate pad/knob use, load **Racks → Phosphor Screens**. Dot Matrix and Contour Scan occupy macro slots 1 and 2, followed by Sync Bend, Signal Emergence, Wavefolder, RGB Split / Delay, Tremolo / Gate, and Video Delay. The rack starts dry; raise a macro or hold its mapped FX pad to engage it. Loading a rack changes the macro assignments; Undo restores the prior rack. Existing MIDI bindings are preserved. Both new effects also work as clip or step FX, with parameter locks, saved presets, automation and audio reactivity. Video effects do not process audio.

## Prepare sources and organize pools

While playback is stopped, click a **Project Media** thumbnail to audition it in the large viewer. The controls directly below the picture let you scrub, **Mark In**, **Mark Out**, enter exact seconds, restore **Full** length, and enable **Source audio**. Press Enter after typing a number. **Crop, scale & text…** opens source Appearance. Expand **Place marked source on timeline** to choose a track and edit operation. Source marks affect new placements; existing timeline clips retain their own trims. Selecting media does not interrupt an actively playing timeline or sequence. Choose **Program** to return to the composition.

Use **⌘-click** for individual media selections or **Shift-click** for a range. Drag the group onto a project folder, or use **Move To**. Right-click **Remove from Project Media**, the trash button, **Delete**, **⇧Delete**, or **⌘Delete** removes the selected group while the grid has focus. This removes bin entries, never files from disk or existing timeline/pattern placements. **⌘Z** restores the removal.

Lane and step random pools now have selectable lists too. Select rows with ⌘/Shift, then delete the group or use **Move To**. Drag selected pool rows onto a **lane header** to move them into that lane’s pool, or onto a **step** to move them into that step’s pool. Moves retain weights and are one Undo action. Dropping new media into a pool adds choices; moving existing pool rows removes them from the original pool. A step pool list edits that individual step; when multiple steps are selected, the inspector explains which add operations apply to the group.

## New creative controls in 0.9.5

**Video Gristleizer:** choose **Effects → Add → Video synthesis → Video Gristleizer**. Try **Discipline**, **Hostile circuitry**, or **Total refusal**, then adjust its wet/dry amount. Circuit mode offers amplitude chopping, spatial-detail filtering, or both; Bias, Depth, Drive and Signal fold shape the damage. Select **One, Two or Three oscillators** and increase Cross-modulation to make them interact. **Sync to project beat** follows the musical clock; free-running mode uses Hz. **New chaos pattern** changes the seed. It supports FX steps, parameter locks, macros, audio mappings and saved presets/chains. This is an independent video homage, not an endorsed or circuit-accurate hardware emulation. Strong settings can flash rapidly.

**Half- and double-time:** pause and use **Timing ½× / 1× / 2×** beside Sequencer BPM. With a 50 BPM song, steps run at an effective 25, 50 or 100 BPM. Audio and individual clip playback speed stay unchanged. Gates, retriggers and pattern duration follow the multiplier; the setting saves per pattern and carries into timeline placement.

**Different footage on each hit:** select a clip or mask lane, enable **Random start position**, and choose minimum/maximum percentages. Each successful trigger picks a position inside that source’s marked In/Out range. A step can override it under **Source → Start position → Random range**, or keep a Fixed start. Retriggers choose again. Playback, recorded takes and timeline placement use the same seeded choice logic.

## Changelog

### 0.9.8 beta — October 25, 2026 · Waveforms, beat alignment, video warp and bounce

- High-resolution audio waveforms preserve brief hits at deep zoom, with cached peak summaries and viewport-only drawing.
- **Align Grid:** drag the first beat to set the origin; drag a later beat to adjust BPM without changing the soundtrack.
- **Timeline video warp anchors:** align visual moments to music by stretching adjacent sections; supports repeated anchors, beat snapping, Undo and project recall.
- **⌘J Bounce Selection:** capture all visible layers, masks and FX across a selected passage as one warpable ProRes movie, with a full pre-bounce project backup. Audio remains separate.
- The export audio-sync repair and optional Global Thermonuclear War 0.1.4 AU remain included.

See [the timing walkthrough](#align-music-and-video-precisely) for use, speed limits, backup files and how baked global FX behave.

### 0.9.7 beta — October 25, 2026 · Sync fix + optional audio bonus

- Carries forward the **export audio-sync correction** from 0.9.6. Thanks again to **@mvbrtr**: audio that could arrive about 44 ms late in FFmpeg-based decoding now retains its correct encoder-delay timing. Re-export older videos to apply the fix; no manual offset is needed.
- Includes **Global Thermonuclear War 0.1.4** as an optional AU in the DMG and a separate plug-in-only ZIP, with installation and getting-started instructions.
- The audio plug-in includes the corrected sliders, graphical six-band EQ, and live before/after frequency spectra.
- Video-app behavior and project compatibility are unchanged from 0.9.6. The bonus is installed separately in your DAW.

### 0.9.6 beta — October 25, 2026 · Export audio sync hotfix

- Fixed exports whose audio could decode approximately **44 ms late through FFmpeg** while appearing aligned through Apple's decoder. The final movie now preserves the audio encoder's timing information.
- Rendered video is copied without re-encoding. Corrected an AAC-source edge case that could trim the soundtrack tail.
- Added Apple/FFmpeg regression checks covering full and trimmed exports, H.264, ProRes 422/4444, and WAV/MP3/AAC source audio.
- **Huge thanks to @mvbrtr for finding and reporting the sync issue!**
- Applies to new exports: re-export your project to correct an older movie. No manual audio offset is required. Existing projects remain compatible.

### 0.9.5 beta — October 25, 2026 · Gristleizer, creative timing and faster source preparation

- **Video Gristleizer**, including one, two or three coupled oscillators, amplitude/filter modes, drive/folding, scan fracture, beat sync, seeded instability and three starting presets. Supports existing automation, mappings, sequencer FX and export.
- Saved **½× / 1× / 2× pattern timing**, independent of song tempo and clip playback speed.
- **Random source start ranges** on clip/mask lanes and individual steps, including retriggers, recording and timeline placement.
- **Large source preparation viewer:** scrub, mark or type In/Out, audition audio, open source Appearance and place the marked source from controls under the main picture.
- **Project Media group removal** now honors the selection, including right-click and Delete/Shift-Delete/Command-Delete. Group folder moves remain available; source files and existing placements are preserved.
- **Lane and step pool multi-selection**, group removal and moves with weights preserved, plus Undo. Number fields retain text-editing keyboard behavior.
- Corrected a floating-point boundary case when marking a source range exactly one frame long.
- Includes all previous Song strip, inspector, Film Noir, editing and export improvements. Existing projects, presets and MIDI mappings remain compatible.


### 0.9.4 beta — October 24, 2026 · Selection and appearance fixes

- Batch Appearance edits on sequencer clip steps preserve unrelated settings. Changing scale across a selection keeps each step’s text, rotation, monochrome and other untouched values; the batch is one Undo action.
- Source appearance follows the actual step-pool, fixed-clip and lane-source priority. Pools with different appearance defaults show a named representative and explain the override behavior.
- **Use source appearance** clears overrides across selected clip steps, including when the focused step already follows its source.
- Timeline video opacity and playback direction display **Mixed** for differing selections. Mask opacity does too; target readouts identify the affected clip/track or mixed targets.
- Clearer selection guidance and step override summaries, including source start and mask threshold, softness and inversion.
- Includes the Song strip, Black & White / Film Noir, beta feedback and prior features. Existing projects, presets and MIDI mappings remain compatible.

### 0.9.3 beta — October 24, 2026 · Song context and clearer inspectors

- New collapsible **Song** strip in Sequencer: timeline waveform, markers, shared playhead, range selection, focus zoom and pattern-pass count.
- Click to seek or drag to set a shared work range while paused; jump back to Timeline for audio edits. Range changes support Undo and honor Timeline Snap.
- Inspector headings now identify the editing scope and selection. Source/inheritance readouts distinguish lane defaults, step overrides, fixed clips and pools; gate readouts show the effective fixed, random or held behavior.
- Selecting a lane clears stale step FX/appearance controls. Multi-selection guidance and reset labels are clearer.
- Large step selections reuse resolved lane data; the Song strip reuses existing audio analysis and keeps transport updates separate from waveform drawing.
- Existing projects and playback behavior are retained. Includes 0.9.2 Black & White / Film Noir and 0.9.1 beta feedback.


### 0.9.2 beta — October 24, 2026 · Black & White / Film Noir

- One-click **Black & White** and **Film Noir** in clip Appearance, with adjustable Noir strength and an **Original** reset.
- Available for timeline clips, media defaults, pads and sequencer clip steps; retained during pattern placement and export.
- Noir contrast is applied around perceptual mid-gray to preserve useful midtone detail. Uses image filters without rebuilding a color lookup table.
- Monochrome settings follow Copy/Paste, Paste Color Attributes, project saving and Undo. Existing projects keep their original appearance.
- Includes the **Settings → Beta Feedback** and **Help → Send Beta Feedback…** workflow from 0.9.1, sending user-reviewed drafts to **abjextstudio@gmail.com**.

### 0.9.1 beta — October 24, 2026 · Email feedback

- Added **Settings → Beta Feedback** and **Help → Send Beta Feedback…** for suggestions, confusing workflows and bug reports.
- Open a user-reviewed email draft addressed to **abjextstudio@gmail.com**, or copy the report for webmail. Nothing is sent automatically; no GitHub login is needed.
- Optional app/macOS/memory details are off by default and shown before inclusion. No automatic project, media or log attachments.
- Draft notes remain on your Mac between sessions. Long reports can be copied in full without truncation.
- Includes the 0.9.0 editing and responsiveness improvements below.


### 0.9.0 beta — October 24, 2026 · Editing and responsiveness

This release brings the recent step-editing and memory improvements to the public beta. Existing projects, presets and controller mappings remain compatible. Save a copy of important work before updating.

- **Move complete steps:** drag a step or selected group, with its pools, Chance, gates, appearance and FX locks, to another compatible position. Occupied destinations are replaced; Undo restores the edit.
- **Copy and paste any selection:** select a range with Shift-click, press **⌘C**, select a destination and press **⌘V**. Multi-lane spacing and offsets are retained. **⌘D** duplicates the selected span into unedited destination steps and explains conflicts.
- **Shuffle a lane:** use **Shuffle Steps** in a clip, mask or FX lane's inspector or header menu. It rearranges complete steps and rests; protected positions stay in place. Undo/Redo works normally.
- **Hold until another clip arrives:** choose **Until next clip** in Timing → Gate mode. Empty steps and probability misses let the current source continue across loops until a replacement hit, Stop or section boundary. Recording and placement resolve that performance into finite clips.
- **More responsive color editing:** global color changes no longer rebuild the entire sequencer grid.
- **Lower editing overhead:** bounded thumbnail decoding and cache, cancellation of unneeded thumbnail work, first-frame preparation at preview resolution, shared inspector rendering resources, and a fix for effect-editor objects remaining allocated after closing.
- Export still uses the original media at the selected output resolution. This update does not add effects or change the project format.

**For a first session:** follow [Make your first video](#start-here-your-first-video), then try a short pattern with a song before adding large random pools. Use 360p · Light preview on a smaller-memory Mac; preview resolution does not reduce export resolution. This remains a beta: please report your Mac, macOS, exact build and reproduction steps with problems.


### 0.8.7 local preview — October 24, 2026 · Responsiveness and memory

- Global color adjustments no longer rebuild the sequencer's entire step grid. Step edits and effect labels still update normally.
- Timeline thumbnails use a bounded two-job preparation queue and a 24 MiB cache, sharing requests for identical source fragments.
- Clip preparation uses the selected preview size for its first-frame images, reducing their memory cost in Light preview. Export continues to use original media at the chosen export resolution.
- Effect inspector helpers share rendering resources, reducing redundant setup when opening and editing effects.
- Fixed a retained effect-inspector renderer after closing the inspector, preventing those helper objects from accumulating across repeated editing sessions.
- Includes the step clipboard, Shuffle Steps and Until next clip improvements below. No new effects or project-format changes in this maintenance update.

### 0.8.6 local preview — October 23, 2026 · Step clipboard and held gates

- **Shuffle Steps** on every clip, mask and FX lane rearranges complete steps and rests, retaining attached settings and protected positions. Available in the lane inspector and header context menu, with Undo/Redo.
- Copy any sequencer step selection with ⌘C and paste at a chosen step with ⌘V. Multi-lane offsets, spacing, pools, Chance, gates, appearance and FX locks are preserved. Paste replaces destination settings with Undo.
- Drag a step or selected group onto any compatible destination, including occupied steps. All step settings move together; destination steps are replaced and Undo restores both.
- Fixed sequencer ⌘D routing and Shift-click modifier capture. Duplicate repeats the selected span into unedited steps; a visible explanation now identifies blocked destinations.
- Added **Until next clip** for clip steps and lane defaults. Empty steps and probability misses keep the source playing across loops until a replacement hit, Stop or section boundary. Recording and placement retain the resulting finite duration.


### 0.8.5 beta — October 23, 2026 · build 20261024.011533 · Mask transforms and step targets

- **Per-step mask targets:** follow the Masks lane’s target or choose a named clip lane in **Appearance**. Targets remain attached when clip lanes are reordered.
- **Mask transforms:** scale, position, rotation, flips, crop and Fit/Fill framing for lane defaults, step overrides and timeline masks. Use lane transform restores inheritance; Reset transform returns to neutral settings.
- **Invert mask** remains alongside Threshold, Softness and mask opacity. Transformed masks keep uncovered canvas hidden, including when inverted.
- Live playback, recording, timeline placement and export use the same resolved mask controls. Older projects retain their existing mask appearance.
- Verified save/reopen of target, scale and inversion, plus rendering/export, Undo, duplication, lane reordering and recording/placement checks.

### 0.8.4 beta — October 23, 2026 · build 20261023.223452 · Layers, pools and random gates

- **Layer Stack** is the default for new patterns: independent clip lanes, top row in front, and drag-to-reorder compositing. Up to eight total sequencer rows. Existing patterns keep Shared Targets until explicitly switched.
- Rename lanes; automatic names continue A, B, C, D instead of wrapping.
- **Chance directly triggers lane-pool choices** on empty steps. Populate is optional. Clear step overrides for a selection or use the lane pool across all steps.
- **Random gate ranges** at lane and step scope, whole/fractional durations, and explicit Follow lane/Fixed/Random range controls. Playback, recording and placement share seeded duration decisions.
- Lane pools now show their lane name/count prominently and reset their list position when switching lanes. Step-owned pools are clearly distinguished. Asynchronous imports stay attached to the original target steps even if selection changes.
- **Duplicate Steps / ⌘D** copies selected phrases with their pools, probabilities, gates and overrides into unedited destination steps; lane inheritance remains live and one Undo restores the edit.
- **Save Colorizer Preset…** and **My Colorizer presets** are accessible directly from Color → Creative color and share the Effects preset library.

### 0.8.3 beta — October 23, 2026 · UI workflow refinement

- Fixed a project-switch crash when a sequencer view briefly retained a clip reference absent from the newly opened project.
- Clear transfers in both directions: Timeline **Send to Sequencer**, Sequencer **Add to Timeline…** with linked/independent choices, placement preview and editable pass count. The timeline opens only after successful placement.
- Step controls organized into **Timing, Appearance, Source, Effects and Pattern**. Opacity is displayed/entered as percent; lane controls identify their scope.
- Duplicate clip controls beneath preview removed; selection controls stay in the lower-left inspector, including masks and audio playhead access.
- Optional **FX Controls** panel with visible assign/edit actions, compact percentage readouts, a Try it slider, 0%/100% parameter endpoints, and direct **Save Chain & Controls** access. Existing macros and controller mappings are retained.
- Live tools collapse separately. Sequencer **Record to Timeline** remains visible for keeping actual probability decisions. Store, mutation and Fill are grouped under **Variation…**.



### 0.8.2 beta — October 23, 2026 · ABJEXT transition

- Semiotic Studio is now **ABJEXT Studio**, with a new wordmark, app icon, splash screen, and a consistent near-black, warm-white, oxide-red, and slate interface.
- ABJEXT checks for updates exclusively at **sxrvys/Abjext**. The Semiotic repository receives this final bridge installer so existing users can make the transition through Check for Updates.
- Existing projects, media references, presets, controller mappings, and preferences remain in place. No project conversion or new account is required.
- The installer includes the VCR font and application resources. Apple Silicon / macOS 14+ requirements and manual installation remain unchanged.
- This release carries forward 0.8.1’s features; it is a branding and distribution transition.

### 0.8.1 beta — October 23, 2026 · build 20261023.152235 · Phosphor Screens

- Added **Dot Matrix**, with luminous dot grids, crushed silhouettes, dithering, luma deflection and seeded breakup.
- Added **Contour Scan**, with luminous brightness-bent carrier lines, adjustable line width, drift, color and glow.
- Six factory presets and a **Phosphor Screens** playable rack; all new controls support the existing MIDI, macro, sequencer, automation and audio-modulation workflows.
- Both processors are stateless GPU effects: no frame-history buffers, CPU color-table rebuilds or audio processing.


### 0.8.0 beta — October 22, 2026 · build 20261023.022845 · Playable song sections

- Linked timeline sections with pattern editing, repeat counts, dragging, Make Unique, stable/Evolve/Locked variations, hand-edit protection and Undo/Redo. Section FX gates play and export with the resolved clips.
- Keep That: opt-in, bounded retrospective preview capture with timeline audio.
- Optional lightweight ProRes playback proxies with a bounded disk cache; offline exports use original media.
- Contextual timeline clip/mask/section inspectors and clearer effect-chain/rack saving labels.
- Indexed section-FX lookup and unchanged-definition detection avoid unnecessary work. Recent frame-cost diagnostics make heavy scenes easier to identify.
- Full musical section length is retained even when probability leaves its final steps empty.


### 0.7.1 beta — October 22, 2026 · build 20261023.012813 · Timeline excerpts and tighter quantization

- Video clip boxes span their full duration without an artificial two-pixel gap. Video beat lines match the frame boundaries used by snapping and quantization; audio beat lines retain exact musical timing.

- Fixed cumulative frame-rounding drift when quantizing consecutive timeline clips. Each cut now stays anchored to the musical grid. Starts-only quantization no longer skips a beat because a preceding edge rounded up. Cuts use the editor's 30 fps frame grid; set the song's BPM and beat offset, then use Quantize Video to update existing edits.

- **To Pool…** sends selected timeline clips or work-range excerpts into a chosen pattern's lane pool.
- Retains exact source marks, playback speed, reverse and framing. Separate excerpts from one file remain independent; repeated additions preserve existing weights.
- Transfer is undoable and leaves timeline clips, audio, controller mappings and programmed steps intact. Invalid ranges or full pools are explained before any changes.

### 0.7.0 beta — October 22, 2026 · build 20261022.195342 · Physical & Analog Interruptions

- Twelve new effects, 60 mappable controls and 36 presets; two playable eight-macro racks.
- Shared Burst envelopes with attack/hold/decay, retriggers, beat or second timing, seeded hit variation, sequencer access and recorded playback.
- Bounded history with release cleanup; video-only processing.
- Project format 25; earlier projects still open, but older app versions cannot open new saves.


### 0.6.1 beta — October 22, 2026 · build 20261022.185833 · Signal Interruptions

- **Signal Emergence:** make footage emerge from particles and static. Play reveal, density, particle size, contours, threshold and scatter, with source color and background controls. Static can change on the beat or at a free rate.
- **Halftone / Print Damage:** dot, line and color-screen patterns, with screen size/angle, contrast, ink spread, color misregistration, paper damage and inverted print.
- **Pixel Sorting:** sort groups of 16 image cells by brightness or RGB channel, horizontally or vertically. Select a brightness range, reverse the order and scatter sorting blocks on the beat. Cell width controls streak length; this is a bounded block sort, not an unlimited whole-row sort.
- **Signal Interruptions factory rack:** eight named macros, starting dry, with the three new effects plus Sync Bend, Wavefolder, RGB Split, Tremolo and Stutter. Existing controller mappings stay connected. Loading a factory rack replaces its macro assignments/effect instances and can be undone.
- All new controls support the existing MIDI/macros, music mappings, automation, saved presets/chains and sequencer locks. The three new effects have immediate wet/dry release and no temporal frame-history buffers. Their random patterns use saved seeds for repeatable playback/export. Audio remains untouched.
- Projects now save as format 24; earlier projects still open. Update ABJEXT before opening a project saved by this release.


### 0.6.0 beta — October 22, 2026 · build 20261022.175944

- Clip-pool weights now display as percentages with a visible Weight label: 100% is normal, 50% is half as likely, and 200% is twice as likely. Both lane and per-step pools use the clearer display. Existing selection behavior and saved weights are unchanged.
- Added a ground-zero beginner walkthrough, troubleshooting table and quick navigation above the reference guide.

Validation: release build and package checks passed; a native UI edit confirmed that typing 50 and pressing Enter displays 50% and saves the existing 0.5 weight correctly.


### 0.6.0 beta — October 21, 2026 · build 20261022.012123

- **Song arranger:** open Song in the Sequencer toolbar, drag named patterns into the strip, set each section's repeat count, and reorder the cards. The strip shows relative musical/time positions, the current pass and the next section. Enable Play song arrangement to follow it; Loop song repeats it. Place Song commits one complete arrangement, including resolved probability choices, masks and FX.
- **Reusable lane pools:** click a lane header to build a weighted clip pool. Enabled steps can inherit it, so you can build a pattern before choosing individual clips. Existing per-step pools remain available.
- **Randomness with memory:** choose weighted random, no immediate repeat, use all before reshuffling, or contrast every N passes. Chance/condition misses do not consume the choice history. Lane-pool steps share memory; each explicit step pool has its own. Memory resets when a pattern section starts or transport restarts.
- **Populate and Shuffle:** in the lane inspector, open Populate / shuffle steps. Choose density, gate and chance, optionally distribute hits evenly with Euclidean rotation, then Populate steps. Shuffle clips changes source assignments on existing hits while retaining their other settings.
- **Selective mutation:** the control beside Mutate chooses clip choices, gates, timing/retriggers, probability and existing FX locks. Set an amount and protect any steps you want preserved. Populate, Shuffle and Mutate support Undo and Store/Restore.
- **Swing and movement:** pattern swing, lane swing overrides and four-part groove offsets shape timing. Select a range of steps and use General → Swing / traversal overrides for a local swing, reverse-order or ping-pong section. Outside that section, lane defaults resume. Traversal changes step order; source-video reverse remains separate.
- **Step explanations:** small outcome marks distinguish triggered hits, probability/condition misses and unavailable/expired hits. Select a step for its last-visit explanation and inherited/local settings.
- **Preparation stays bounded:** forecasting copies the same scheduling state used by playback, including choice memory, without consuming live choices. The shared 64-player cache and two-worker preparation queue remain in place.

#### Timing and compatibility

Ping-pong adds return visits and lengthens the cycle; it does not squeeze those visits into the original bar. The first clip lane defines the master pattern duration. Other lanes run independently until the next section boundary. Gate bars are hidden for reordered traversal because a straight grid span would be misleading. Very short rhythmic changes remain limited by video frame rate.

Place Song writes one finite arrangement regardless of Loop song. An enabled work range determines its start; otherwise existing timeline placement rules apply. Large placements are checked before allocation. Live Fill changes can alter future source choices and may require a source that was not forecast.

Projects now save format **23**. Earlier projects open; keep a copy if returning to an older app, which cannot open the new format. macOS 14+, Apple Silicon, bundled fonts and the normal drag-to-Applications installation remain unchanged. All FX remain video-only.

Validation: 538 regression tests, 28 optional checks skipped, zero failures; the unchanged exhaustive effect-parameter audit was excluded. A final focused run covered 44 tests with 3 optional skips and no failures. Live checks covered song video playback and automatic stopping, timeline placement, lane controls, Populate, protected steps and Undo. Project-format artifacts match the native schema.

### 0.5.2 beta — October 21, 2026 · build 20261022.000934

- **Reverse export fix:** some valid MP4 files cannot decode their nominal zero-time frame. A narrowly bounded retry uses the first readable source frame at the reverse endpoint, without seeking outside the clip's trim. The previously failing 138-second project now completes with video and audio.
- **Render in Place:** select video clips, then choose **Timeline → Render in Place…** (also in the timeline's Edit menu). Speed/reverse, framing/text, clip FX and automation are baked into ProRes 4444 movies. Each clip retains its duration and position. Opacity, blend, split screen, track masks, global FX and all audio stay live. Music-reactive clip processing is frozen against the current song.
- **Restore originals:** use **Timeline → Restore Unrendered Originals**, or Undo. Original media and edit settings are preserved in the project; restoring resets trim/speed/FX to the pre-render edit at the current position and track. Save the project before rendering. Keep the generated **Renders** folder beside it when moving/backing up the project. These movies use disk space and are not automatically deleted on Undo.
- **Render boundaries:** no extra delay tails are added. Clip masks, underlay-dependent Key/Logic Mixers, macro-driven opacity, and incomplete selections of a shared feedback performance are refused with an explanation; use Export Mix for these combinations. Render in Place reuses clip processing on later playback/exports, but global FX still require rendering.
- **Clearer export failures:** errors identify the failed stage and underlying codes. Soundtrack inputs are held stable during the render. If audio finishing fails after the video completes, a video-only recovery file is retained and can be revealed from **Export details…**.
- **Create Pattern from Timeline Selection:** copy selected video clips or the enabled work range into a new independent pattern. Choose subdivision, preview lane/step counts, and optionally set the shared work range. Source marks, rate/reverse, clip FX/automation, opacity, masks and framing travel with the copied clips. Audio and the original timeline stay in place. Up to three routed video layers and 64 steps; unsupported overlaps or timing are explained before any changes.
- Projects now save format **22**, including persistent original-clip snapshots. Earlier project versions still open. Bundled VCR OSD Mono and normal installation requirements are unchanged.


Validation: 522 regression tests, 27 optional checks skipped, zero failures. The unchanged exhaustive effect-parameter audit was excluded. A previously failing 138-second project completed with audio; final frames and both tracks were verified. Native Render in Place, playback, save, Restore Originals and Undo checks passed. Timeline-to-pattern conversion was also verified in the app.

### 0.5.1 beta — October 21, 2026 · build 20261021.221913

- **Select a phrase:** click step 1, then Shift-click step 12 to select all twelve. ⌘-click adds/removes individual steps. Shift-click across lanes selects a rectangle.
- **Move the whole selection:** drag any selected step to move the group with its spacing, clips, gates, probability pools, appearance and FX locks. For a distant destination, right-click a step and choose **Move selection here**. Overlapping moves preserve their own source steps; incompatible, occupied or out-of-bounds destinations leave the pattern untouched. One Undo restores the whole move. Empty cells with lane-wide gate settings remain valid destinations.
- **Shared audio work range:** Timeline and Sequencer honor the same enabled In/Out range and Loop setting, including when sequencing continues behind Timeline view. The Sequencer toolbar now exposes those controls. Short loops explicitly reposition the soundtrack instead of waiting for normal drift correction.
- **Place into the selected section:** Place Pattern starts at the enabled work range’s In point, including an audio-only timeline. Its duration still follows the selected pattern/chain and number of passes; the range does not crop the placed result.
- **Recording within a range:** recording finishes one pass at Out so captured clips and automation cannot wrap backwards over the take. Ordinary audition loops while Loop is enabled. Without a work range, live performance continues as before.

Validation: 496 regression tests, 25 optional checks skipped, zero failures. This pass covered selection, overlapping group moves, one-action Undo, shared range playback, short audio loops, and recording at Out. The unchanged exhaustive effect-parameter pixel audit was excluded from this pass.

### 0.5.1 beta — October 21, 2026 · build 20261021.193442

- **Larger verse/chorus/bridge arrangements:** linked patterns share an advance-loading cache. Small chains keep all choices prepared; larger chains forecast weighted clip choices up to eight seconds ahead and rotate them through at most 64 prepared players, with two preparation jobs at a time. **64 is a cache limit, not a project-wide clip limit.** Pause and use **Prepare Clips**, then wait for the current window to read **N/N ready ahead**. The readiness panel explains which sources are ready, queued, on demand, or unavailable.
- **Three live video layers:** A, B, and C have independent opacity, blending, FX, masks, and timeline recording. New clip lanes choose an unused target. The A/B crossfader leaves C independent; lanes targeting the same layer replace each other's clips.
- **Faster editing and preparation:** background clip-readiness changes no longer redraw the entire editor during sequencing. Color palette processing runs on the GPU instead of rebuilding a 32³ lookup table while controls move. Preview/status updates stay isolated from the larger workspace.
- **Random pools:** drop one or more media clips anywhere inside the expanded pool, including over existing entries, to add choices. The whole drop area highlights. Existing entries and their weights are retained.
- **Group editing:** timeline masks support Shift-click and rectangle selection, moving, duplicate, copy/paste, batch settings, and Undo. Sequencer steps support batch edits, full-step copy/paste, and dragging steps between compatible lanes.
- **Step control:** lane/step speed and reverse stay independent of gate length. Step FX expose audio/beat mapping and random parameter ranges; placed performances preserve their resolved choices and mappings.
- **Media workflow:** thumbnails show usage, can filter unused sources, and help locate timeline/sequencer uses. Source controls expose marked ranges, crop/scale, and text. Audio drops retain the pointer's timeline position; the first pattern placed on an empty visual timeline begins at zero. Track headers remain accessible during horizontal scrolling.
- **Clearer readiness:** the footer reports sequence readiness in Sequencer view instead of the unrelated controller-pad bank count. Failed sources retain their explanation and wait for Retry; preparation warnings refer to the current pattern chain.
- **Compatibility:** projects saved by this build use project format 20. Older project formats remain readable; keep a backup before opening/saving in a newer beta. VCR OSD Mono is bundled; no separate font or developer-tool installation is needed.

Validation included a 484-test suite (25 optional checks skipped, zero failures), sustained real-media playback, sequencer FX transfer, preview capture with stereo audio, and a 1080p export. A separate large-chain check covered 1,080 assignments across 128 distinct files. These are tested scenarios, not a guarantee of uninterrupted playback for every codec, drive, or FX load; occasional rendering spikes remain possible.

### 0.5.1 — October 19, 2026

- **Clip preparation (build 20261019.201106):** the Sequencer now has **Prepare Clips** and an **N/N ready** count beside Bars/Subdivision. Pause and wait for all choices to be ready before playing. Patterns retain up to 64 possible clip choices, including probability pools; only two prepare at once. This fixed repeated eviction/rebuilding in patterns exceeding the old 32-player cache. The October 21 build extends this to rolling preparation for larger linked chains. A file that cannot prepare times out with a reason and waits for an explicit retry instead of repeatedly competing with playback. Hover the readiness count for details; Prepare Clips retries unavailable sources. Masks prepare separately. High-resolution sources, complex FX, and active layer count still affect performance.

- **Multi-loop placement (build 20261019.193420):** choose **1–64 loops** beside Place Pattern. Each pass evaluates probability, weighted clip pools and conditional FX independently, then writes fixed, editable clips, masks and FX automation. Chained patterns use the same loop count. Set a step’s Chance to 100% for a guaranteed hit; Wet/Dry controls effect strength.

- **Playback hotfix (build 20261019.185837):** active sequencer clips prepare while paused and stay ahead of unrelated pads in the bounded decoder cache. Fixes repeated preparation/skipped hits in larger sets without increasing the memory limit.

- Mask lanes and mask steps now have opacity controls. 100% applies the full matte; 0% leaves the target unmasked. Lane and step amounts multiply and persist through recording, placement, and export. Timeline mask clips expose the same control. The step inspector’s Timing tab is now **General**, with opacity/blend at the top.

- Click a sequencer **lane card** for lane-wide mute, routing, opacity/blend and **Apply to all** gate length. Click a step for its own controls: **General → Step opacity / Step blend**. Step opacity multiplies lane/layer opacity; step blends inherit unless explicitly overridden. Lane mix changes take effect on the next clip trigger and are preserved by Record, Place Pattern and export.
- Fixed Gate numeric entry showing a stale value after Return or clicking away. **Apply** buttons also commit a number that is still being typed, without requiring Return first. Native inspector tests check the displayed value as well as the stored value.

- Numeric fields allow normal clearing/replacement, negative and decimal entry, selection and clipboard editing. Return or clicking away applies the value once; Escape cancels, and incomplete/invalid entries restore the previous value. This covers sequencer Gate/layout duration, FX, grading, crop/transform, tempo, trims, masks and automation coordinates.
- While typing, ⌘Z / ⇧⌘Z use the text editor’s undo/redo history instead of changing the project. Trim panels with an **Apply** button still use that button to apply the prepared trim.
- Clip text uses a compact nine-font chooser, including bundled **VCR OSD Mono**. **More Fonts…** loads installed fonts only when opened; custom fonts already saved in projects remain selectable. Selecting clips no longer builds the entire system-font catalog in the inspector.
- Source audition avoids rebuilding an unchanged video composition and publishing unchanged playback state.

- Sequencer length is now **Bars × Subdivision** in the main toolbar, with the resulting step count displayed. All lanes is the default; choose Selected lane for independent lengths. Two bars at 1/16 is 32 steps; eighth-note triplets give 12 steps per bar. Each lane supports up to 64 steps. New steps default to a one-step gate; existing patterns keep their gates.
- Temporary split-screen commands: select a clip-lane step → **General → Screen Layout…** to open the Clip inspector. Enable Timed screen layout, choose Top/Bottom/Left/Right/corners, and set its duration in steps independently of the clip gate. For a six-step split, set Clips A to Top and Clips B to Bottom for six steps. Commands survive intervening clip changes, restore the previous layout when finished, and are retained in Record/Place Pattern and export.
- Step inspector labeling and retrigger guidance make Gate, Hits and their frame-rate limits clearer. Project format 18 stores timed layout commands; older projects still open.

- Drop Finder folders into Project Media to import their audio/video into same-named project folders. Subfolder media is included in the root folder’s bin, non-media files are skipped, existing source trims are preserved, and one Undo removes the whole import. Source files stay in their original locations.

- Enter now works in the Sequencer as it does in the Timeline: press once to stop, then again to return the song and sequencer clock to zero and scroll the view to the beginning. Space toggles playback in either view; typing in parameter fields keeps normal keyboard behavior.

- Selecting a sequencer step’s **FX** tab opens **Effects → Selected step** in the full inspector. The effect’s parameter sliders and numeric fields write step locks automatically; blue lock buttons clear individual overrides. Gate/timing and the existing Lock parameter / Use for lane controls remain in the left step panel. Shared rack values and neighboring steps stay unchanged.
- Sequencer Gate length spans 0.05–64 steps, with numeric entry and common lengths. Long clips sustain across empty/missed steps; new hits take over without old tails reappearing in placed patterns.
- Switching from a playing timeline to Sequencer starts the pattern at the current song position while keeping soundtrack playback continuous. Patterns repeat while the song progresses; Record captures repeated passes, and Stop leaves the playhead at the end of the take for the next section.

- **Settings → Audio → Playback output** selects any audio output exposed by macOS, independently of the live input. The app remembers the device, refreshes on connection changes, and mutes playback if a chosen device disconnects until it returns or another output is chosen. System Default follows macOS. Export and capture audio are unchanged.

### 0.5.0 beta — October 19, 2026

- Unified Timeline / Sequencer workspace with independent Media, Pads, FX, Macros, and Automation visibility. Common project, export, and capture actions live in File; source/canvas setup lives in Settings.
- Sequencer lanes in the main working area, with step controls in the left sidebar. Drag lane headers to reorder; layer routing and playback order stay intact. Pattern creation/duplication, chaining, Fill, Store/Mutate/Restore, probability, weighted clip choices, retriggers, and parameter locks support repeatable performances.
- Contextual **Clip inspector** for timeline clips, media-source defaults, pads, and clip-lane steps. Add scale, position, rotation, flips, transparent edge cropping, and multiline text with installed fonts, color, alignment, wrapping, opacity, outline, and background.
- Source defaults are copied into new placements. Individual clip/pad/step changes remain independent; sequencer capture and Place Pattern retain their appearance. Text can be placed before or after clip FX; global FX always process the composite.
- Weighted clip choices now live in a collapsed **General → Random clip choices** section, leaving General, FX, and Lane as the main step tabs.
- Welcome-screen focus cleanup, visual-only undo for framing/text, and cached text rendering at preview/export resolution.
- Project format 16 preserves the new appearance fields. Existing projects open; projects saved in this version require an updated app. Keep a copy if returning to an older beta.

This release includes changes developed since the public 0.2.0 beta. The macro rack remains collapsible with **Macros**; its sizing behavior is unchanged.
