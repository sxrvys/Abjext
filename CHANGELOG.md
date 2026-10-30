# Release history

[Back to ABJEXT Studio](README.md) · [User guide](docs/USER_GUIDE.md)


### 1.0.4 · Creative variation and still images

- Fresh arrangement variations by default; clip-pool bags persist across cards and passes instead of repeating the same early choices. Repeat remains available. Saved timeline choices are not rerolled.
- Random FX pools accept individual effects and complete editable chains, with weighted/no-repeat/use-all choice rules, step Chance and gates. Step color cards follow successful FX gates.
- Timeline **Try another variation** can use any clip lane from any pattern, fitting the selected slot and preserving its position, outer effects and track. Only that replacement is prepared; Undo restores the previous section.
- **Shuffle selected sections** works on scattered selections across tracks. Destination positions and durations stay fixed, source treatments travel with their clips, and unselected sections and the independent soundtrack stay unchanged. Unequal lengths are fitted within supported playback-speed limits.
- Identification colors for sequencer lanes, timeline tracks and selected timeline clips; these labels do not alter the rendered image.
- Blank and Probability Pool starts, plus save/load sequencer templates without source media. Templates retain rhythm, probability, gates, FX and color setup.
- Audio modulation choices use a wider, scrollable panel. Timeline transfer progress appears in its own dialog.
- Still-image import for PNG/JPEG/TIFF/HEIC/BMP across media, pools and timeline. One durable, reusable 30-second prepared source per image; orientation applied, transparency retained, longest side capped at 4096 pixels. Image changes create a new source rather than changing existing edits. Keep Imported Stills media with transferred projects.
- Global Thermonuclear War AU 0.1.5: individual blends for repeats, shuffle, direction, Gristleizer, Percolator, destruction and EQ. Older sessions retain their previous sound at default stage blends.

Project format remains 33 with optional new fields. Older versions may ignore new creative settings; use 1.0.4 for full recall. No new account, network dependency or background update polling.

### 1.0.3 · Trackpad scrolling

- Direct horizontal trackpad routing in Timeline and Sequencer, preserving fractional movement and momentum.
- Buffered timeline drawing reduces repeated clip-control, ruler, grid and waveform rebuilds.
- Manual scrolling suspends playhead-follow until Play or re-enabling Follow.
- Pinned lane headers skip unchanged layout assignments.

Project format 33 is unchanged from 1.0.2. Includes all previous release features. This is a navigation fix; prepared-section rendering and export performance are unchanged. Targeted regression tests passed, live navigation was checked, and physical trackpad scrolling was confirmed improved.


### 1.0.2 · Timeline sections and pattern workflow

Timeline sections, faster editing, and a clearer pattern workflow.

#### Edit sections instead of thousands of hits

**Add to Timeline → Prepared sections** prepares one video section per lane for
each pattern pass. Choose one-, two- or four-bar divisions when you want smaller
pieces. Fractional final passes are retained. Trim, move, copy and warp these
sections as ordinary clips; right-click **Show original cuts** to reopen the
detail of just one section.

Preparation takes time once and creates ProRes media on disk. Keep those files
with your project. Source footage is not deleted. Existing edits are not
automatically consolidated. Masks and global processing remain live; blend
changes can require separate sections. Unsupported context-dependent effects
produce an explanation instead of a silently altered render. Linked sections
and individual-cut transfer remain optional workflows.

#### Timeline fixes

- Dense timeline views draw their compact clips together, with detailed controls
  restricted to visible larger clips. Lane headers remain fixed during scrolling.
- Timeline indexes and source metadata are reused. Edits reuse unaffected lanes'
  playback decoders; color-only edits do not rebuild them.
- **Command-J** replaces selected cuts on the same lanes and time span, with
  project backup and Undo. Multi-lane selections prepare separate lane sections.
- **Enable Warp** and warp markers operate inside one clip, without splitting
  the timeline into new placements.
- Range copy retains selected fragments and gaps. Paste uses the chosen lane and
  time, can trim overlapping neighbors, and supports Undo. The overwrite warning
  can be disabled.
- Reverse export reads bounded groups of frames, reducing repeated seeks while
  retaining original-resolution frames.
- Empty MIDI performance pads no longer trigger repeated workspace updates.
- Fast reversed trims remain within valid source bounds, and failed saves now
  show the error instead of leaving a previous render-success message visible.

#### Included from the private testing builds

- **Pattern Color Board:** compare representative stills side by side and edit
  each pattern's complete color look. These are color studies, not simulations
  of the full moving composite or every effect.
- **Copy this look to…** transfers the color settings to another pattern for
  further adjustment. Rename is available on the board and beside the pattern
  selector.
- Pattern color changes can update associated timeline color ranges without
  replacing resolved clip choices or timing. Older ranges require explicit linking.
- Arrangement cards accept fractional passes and **From / To** song boundaries,
  including Beginning of song, named markers and Soundtrack end. Fitting computes
  the needed duration at the current tempo; refit after changing tempo or order.
- Explicit **Pattern / Song arrangement** preview choices and scrollable
  sequencer controls make the active playback mode easier to find.
- Effect menus are organized into families. Reverse preview preparation is cached,
  with loading/progress and playhead-follow improvements.

Projects save as format 33. Keep a copy before upgrading if you need to return
to an older build. Apple Silicon / macOS 14 or later; optional Global Thermonuclear
War AU remains a separate installation.

#### Performance and verification

The regression suite passed 783 tests (40 optional skips). Subsequent focused
checks covered MIDI idle behavior, pinned headers and saveable reverse trims.
Live checks exercised same-lane bounce, overwrite paste and Undo, internal warp
anchors, prepared transfer, single-section expansion, and save/reopen.

A 3:34 project with thousands of existing cuts exported at 1080p60 in 6:13 on
the development Mac; it is not a real-time export guarantee. Prepared sections
reduce repeated work during later editing, but initial preparation and complex
effects still take time. Older timelines retain their original cuts until you
explicitly bounce or regenerate them.


### 1.0.1 · Reception faults, your palette, faster clip preparation

**Twelve new interruption effects**, organized into three families:

- **Analog reception:** Analog Sparkles, RF Interference, Sync Slip, Signal Echo, Channel Collision and Line Scramble.
- **Tape and film damage:** VHS Tracking Error, Tape Dropout, Film Gate Jump and Film Splice.
- **Digital reception:** Satellite Breakdown and DVD Skip.

Start with **Readable faults** to retain the subject. Use Strength, Coverage, Size, Instability, Interval in beats, Duration, Recovery and Chance to shape brief faults or sustained interference. The stronger **Unstable reception** and **Signal collapse** presets are available too. These are artistic interpretations of signal failures, not certified broadcast simulations or products endorsed by FCC/DISH.

**Channel Collision** uses the actual picture underneath the affected clip; in Global scope it uses the composite beneath the top clip. It needs overlapping visible footage. Without a lower image it leaves the input unchanged; it does not choose a second source from your pools.

**Breathing and live memory:** Moth Lung maps configured audio level or bass/mid/treble energy to scale and exposure swells. Audio Playhead / Live Memory scrubs a bounded recent-picture buffer (up to one second, 16 snapshots at 15 captures/second). Configure Audio Reactive input first. This is separate from the timeline clip's whole-source Audio Playhead control. Live microphone reactions cannot be reconstructed from a silent export source.

**Your colors stay yours:** Halftone, Dot Matrix and Contour Scan now offer **Use incoming colors**. Put Colorizer earlier in the chain to use its output palette. New starter looks use incoming colors; existing saved settings retain their previous look. Halftone also has cleaner balanced dot/line coverage. RGB Split has three optional custom channel colors.

**Prepare clips without leaving the pool:**

1. Pause playback, then click a clip in a lane or step pool. Its picture opens in the main viewer with controls underneath. Preparation temporarily uses the center workspace; Done or starting playback returns to the sequencer.
2. Set **In / Out** to exclude unwanted footage. Adjust **Black point, White point and Contrast**, Black & White / Film Noir, framing, inversion, speed or direction.
3. Click **Apply** to update just that pool entry, with Undo. Other pool entries and source files remain unchanged.
4. Select several entries to work through them individually with **Back, Skip, Apply & Next**. Unapplied drafts survive switching entries or starting playback; apply changes before replacing the project. Done asks before discarding remaining drafts.

Random starts stay within the entry's trim; reverse, speed and resolved timeline captures retain it. Explicit step overrides still take priority. **Project Media → Move To → Add to Lane Pool** adds the whole media selection to a chosen pool while keeping it in Project Media.

**Compatibility:** older projects open normally. Newly saved projects use format 32 and need 1.0.1 or newer to preserve pool trims and levels. Keep a copy before saving if you need to return to an older build. Apple Silicon, macOS 14+. Optional Global Thermonuclear War AU remains version 0.1.4; its installation is separate.


### 1.0.0 beta — October 26, 2026 · Pattern looks and continuous FX audition

- **Developer ID signed and Apple-notarized:** the app and DMG carry attached tickets, and the bonus AU is signed and accepted by Apple’s notarization service.

- **A color look for each pattern:** in Sequencer, open **Color → Pattern / Project** and choose **Use pattern color**. Adjust Colorizer, grading, black/white points and hue for that pattern. **Follow project color** restores inheritance. Duplicates keep their look, and Timeline placement, linked sections, recording and export preserve color changes between patterns. Explicit step FX overrides still take priority while active.
- **Get inside a saved FX chain:** select a step, open **Effects**, choose its chain, then expand an effect name. Adjust its numeric parameters and Wet / dry as step-specific locks without changing the saved preset or other steps. Random ranges and modulation remain available. Chain routing and bypass switches stay part of the saved rack; a step can hold up to 64 parameter overrides.
- **Audition FX continuously:** click **Audition FX** in the step inspector. The sequence plays while the selected effect stays active, with live parameter edits. Footage continues through short gates and loops as needed. **End FX Audition** restores normal triggers; playback stops only if audition started it. Stop, leaving the inspector, changing patterns or beginning recording also ends audition. Knob edits are saved; the temporary audition is never written to a recording or export.

Includes the pool editing, random playback, tonal controls, startup and output recovery changes described below. Projects now use format 31. Older projects remain readable; save a backup before upgrading.

### 0.9.9 beta — October 25, 2026 · Pool clip editing, playback variation and tonal levels

- **Edit a pool clip without assigning it to a step:** select one entry in a clip lane or step pool and choose **Edit Clip…**, or double-click it. Preview the source and set fixed speed (¼×–10×), forward/reverse, scale, position, rotation, flips, crop, color inversion and Black & White / Film Noir. **Apply** saves one undoable change; **Cancel** discards it. Settings belong to that entry, so the same source in other pools/patterns and existing timeline edits stays unchanged. Moves and copies carry entry settings with them.
- **Random speed and direction:** lane controls choose speed within a range when the Speed-change chance passes, and choose reverse independently. Choices stay fixed for each hit and are preserved by Record and Add to Timeline. Fixed pool-entry playback settings take precedence over lane randomness; explicit step settings take precedence over both. Use **Use lane speed / random speed** and **Use lane / random direction** in the pool editor to inherit. Gates and soundtrack speed are unchanged. Extremely short marked excerpts limit speed to preserve one video frame.
- **Black point / White point:** under **Color → Color Grading**, raise Black point to deepen washed-out shadows or lower White point to brighten dull highlights. These work independently of Creative Colorizer without replacing its palette or settings. Enable Color Grading to see the changes. Grading runs before artistic FX by default; reorder it after Colorizer if you want to adjust the finished colors. This is manual tonal control, not automatic per-clip exposure matching. Presets, automation and export preserve the values.
- **Startup and precision:** a stopped sequencer prepares and resolves its initial events before starting the soundtrack; BPM now displays up to five decimal places for precise grid alignment.
- **Audio-output recovery:** output route, hardware data-source and sample-rate changes rebuild the playback connection while retaining the soundtrack position and honoring Pause/Stop. **Settings → Audio → Reconnect Output** retries the selected device without restarting ABJEXT. System Default follows macOS; an explicitly selected disconnected device stays muted until it returns or another output is selected.
- Projects now save as **format 30**. Older projects open normally; keep a backup if you need to return to an older app version. The blackletter A app icon and optional Global Thermonuclear War 0.1.4 AU remain included.

### 0.9.8 beta — October 25, 2026 · Waveforms, beat alignment, video warp and bounce

- High-resolution audio waveforms preserve brief hits at deep zoom, with cached peak summaries and viewport-only drawing.
- **Align Grid:** drag the first beat to set the origin; drag a later beat to adjust BPM without changing the soundtrack.
- **Timeline video warp anchors:** align visual moments to music by stretching adjacent sections; supports repeated anchors, beat snapping, Undo and project recall.
- **⌘J Bounce Selection:** capture all visible layers, masks and FX across a selected passage as one warpable ProRes movie, with a full pre-bounce project backup. Audio remains separate.
- The export audio-sync repair and optional Global Thermonuclear War 0.1.4 AU remain included.

See [the timing walkthrough](docs/USER_GUIDE.md#align-music-and-video-precisely) for use, speed limits, backup files and how baked global FX behave.

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

**For a first session:** follow [Make your first video](docs/USER_GUIDE.md#start-here-your-first-video), then try a short pattern with a song before adding large random pools. Use 360p · Light preview on a smaller-memory Mac; preview resolution does not reduce export resolution. This remains a beta: please report your Mac, macOS, exact build and reproduction steps with problems.


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
