---
skip_file: yes
---

# AltMill MK2 assembly migration — pages 3–12

Prepared 24 November 2026 from the live Sienci Resources pages and the supplied **AltMill 2x4_4x4 Resource update.pdf**. The ten Markdown documents are complete working drafts. Technical questions and required replacement artwork below remain open; the original artwork has not been presented as newly corrected CAD.

## Files and installation

- Ten separate `.md` files preserve the published page slugs, titles and sequence. The metadata uses `am-mk2-assembly`, `KBName: AltMill CNC`, menu orders 4–13, and **`post_status: draft`** for review. No publication or repository change has been made.
- The image ZIP contains one shared image folder: `_images/_am/_assembly/`. Merge that folder into the matching repository location. Keep the page filenames shown below so the existing public slugs can be matched when migrating.
- All 160 image references use empty alt brackets and root-relative JPG paths: `![](/_images/_am/_assembly/...)`. There are 158 distinct image files, with filenames in lowercase. The obsolete partial X/Z controller hookup image was retired from the new text and is not included.
- Original image alignment/size classes are retained. Markdown-aware HTML wrappers retain the source display widths responsively; image height follows the original aspect ratio. This avoids putting raw HTML image paths outside Git it Write’s image-upload handling.
- Red notices stay as inline HTML. Centred captions stay as centred HTML. Existing heading levels, dropdown titles, open/closed states, links, downloads, and video embeds are retained. A separate older-kit motor-coupler dropdown was added.
- WordPress plugin shortcodes and custom image classes require a WordPress preview for final visual verification. Local conversion checks do not establish the exact behaviour of the installed WordPress theme/plugins.
- The Sienci repository README notes an image-sync limit of roughly 80 pictures per pull. With 158 images, repeat **Pull Changes** if the first sync does not import every image. Do not publish pages with missing images.
- Fill in the questions, supply the required artwork, check the WordPress preview, then change `post_status` to `publish` when ready. Match the existing page slugs to avoid duplicate posts.

## Remaining technical questions

| ID | Pages | Question to resolve | Current draft treatment |
| --- | --- | --- | --- |
| Q-MOTOR-01 | 5. Motors | Are the supplied spacers between motor and coupler retained or removed? If removed, when? Which kits use this arrangement? | Describes factory-fitted couplers/spacers but does not invent spacer handling. Older loose-coupler instructions are a separate dropdown. Add the confirmed step before Motor Installation. |
| Q-MOTOR-02 | 5. Motors; 11. Final Checks | Confirm the full Y-motor/end-plate sequence: plate flush and snug before coupler clamping, and precisely when/how the rear end-plate screws receive final tightening. Does the rubber-insert seating check also apply to X? | Applies the PDF’s flush/snug-before-clamping sequence and Y-coupler seating check. Retains the original final rear-plate tightening sentence after clamping until Engineering confirms the final sequence. No torque is invented. |
| Q-CONTROLLER-01 | 8. Controller Setup | Confirm the SLB-EXT board revision supplied with these kits, right-to-left axis order and intended motor-power-port allocation. Is any revised board/enclosure involved? | The published board images show signal pairs right-to-left X, Y1, Y2, Z. The draft connects one harness at a time using those printed labels and the existing top/bottom enclosure routes. Power ports remain interchangeable as documented; no unverified right-to-left power assignment or SLB-EXT V2/HV migration is asserted. The PDF’s “Y3” is corrected to Z. |
| Q-ATC-01 | 4. Z-axis Assembly; 7. Wiring and Spindle; 10. Spindle Kit Setup | Where should a new ATC build branch from standard assembly, and exactly where should it return? Account for Z mounting, Y2 routing, motor/sensor connections, covers, controller wiring and commissioning. | Adds the requested ATC link plus an earlier hardware heads-up. Explicitly says shared Y2 and motor/sensor work remains required. No instruction to skip the entire wiring page or invented return step. |
| Q-POWER-01 | 10. Spindle Kit Setup; 11. Final Checks | Supply approved circuit and extension-cord voltage/current requirements for each supported 1.5 kW, 2.2 kW and ATC/VFD variant. | Replaces the universal 1500 W extension-cord and 15 A spindle-circuit claims with kit-specific requirements. No replacement numeric rating is invented. |
| Q-WASTEBOARD-01 | 12. Surfacing Wasteboard | What is the preferred 2×4 sacrificial-sheet cut plan, and which part should be surfaced with the chosen bit? | Separates the 4×4 sheet examples from 2×4 guidance. Preserves the documented 34.3”×51.75” support-table dimensions and existing surfacing values; does not invent a new top-sheet cut size. |

The same question IDs appear as HTML comments at the relevant locations in the `.md` files. They are editorial notes, not customer-facing instructions. Keep affected pages in draft until the questions and illustrations are resolved.

## Required image revisions

These are **still open**. Included images are the existing source artwork, converted to JPG where needed.

| ID | Page | Image task | Existing asset / placement |
| --- | --- | --- | --- |
| R03 | 5 | Replace the parts-needed layout with three motors carrying pre-installed couplers; show supplied spacers. | `am_assembly_motor-installation.jpg` |
| R04 | 5 | Add a spacer close-up showing the confirmed retained/removed condition. Depends on Q-MOTOR-01. | New asset; place with the confirmed spacer instruction. |
| R05 | 5 | Verify/revise rear-end-plate artwork so the motor is already installed while the plate is brought flush and snugged. | `am_assembly_am4x4-fasten-back-scaled.jpg`, moved ahead of coupler clamping. |
| R06 | 5 | Show both coupler halves seated against the rubber insert and identify the ball-screw-side clamping screw. | `am_assembly_tightening-y-motor-coupler-on-ballscrew-1-1.jpg` or a new inset. |
| R07 | 6 | Correct the end facing upper left to have tabs/studs instead of holes. Check overview and page 7 routing images for matching ends. | `am_assembly_x-axis-drag-chain-ends-install.jpg`. Current image remains marked for replacement; text specifies the correction. |
| R08 | 8 | Supply a single labelled port overview for the confirmed board revision. | Existing X/Z and Y1/Y2 maps retained as interim references. |
| R09 | 8 | Show one complete X harness: green power, black motor control, white sensor, and its enclosure entry route. | New illustration; the old partial X/Z hookup view was removed. |
| R10 | 8 | Refresh completed wiring to match the confirmed power assignment and make each Y motor/sensor pair traceable. | `am_assembly_y1y2-motor-cable-plugging.jpg`. |

## Page-by-page change log

### 3. Gantry

File: `am-mk2-x-and-y-gantries.md`

Added removal of temporary painter’s tape after table assembly; retained the separate ball-screw support-clip step. Consolidated duplicated integrated X-sensor preparation/installation into one instruction while retaining all three sensor illustrations and both bump-stop variants. Explicitly secured the sensor using the prepared nut and washer.

Source: https://resources.sienci.com/view/am-mk2-x-and-y-gantries/

### 4. Z-axis Assembly

File: `am-mk2-z-axis-assembly.md`

Added an early ATC hardware callout and an editorial handoff comment. Retained both threaded and unthreaded Z-sensor variants, dates and red warnings unchanged.

Source: https://resources.sienci.com/view/am-mk2-z-axis-assembly/

### 5. Motors

File: `am-mk2-motors.md`

Introduced factory-fitted couplers/spacers; moved loose-coupler installation into an older-kit dropdown. Corrected the Y-motor mounting face to the rear end plate, put end-plate snugging before coupler clamping, and added rubber-insert seating. Moved the rear-plate illustration to match. Preserved original final-tightening text pending Q-MOTOR-02, X-motor steps, fit checks and DIP-switch settings. R03–R06 remain artwork/review items.

Source: https://resources.sienci.com/view/am-mk2-motors/

### 6. Drag Chain Ends 🔗

File: `am-mk2-drag-chain-ends.md`

Added the PDF’s upper-left studded-end correction in text; marked the contradictory original illustration R07 for replacement. Kept the existing 51/51-link (4x4) and 51/36-link (2x4) lengths unchanged.

Source: https://resources.sienci.com/view/am-mk2-drag-chain-ends/

### 7. Wiring and Spindle

File: `am-mk2-wiring-and-spindle.md`

Added the requested ATC callout immediately after the Cable Management and Spindle VFD parts image, with a reminder that shared Y2 and motor/sensor work remains necessary. Preserved both VFD dropdowns, routing steps and motor-cover instructions; ATC return points await confirmation.

Source: https://resources.sienci.com/view/am-mk2-wiring-and-spindle/

### 8. Controller Setup

File: `am-mk2-controller-setup.md`

Replaced grouped X/Z and Y1/Y2 text with complete-harness X, Y1, Y2, Z steps; retained enclosure entry routes and Y-harness pairing warning. Corrected source-PDF Y3 to Z. Used existing labelled board maps as references, removed the obsolete partial X/Z hookup view, and flagged revised artwork and target revision. Added a skip-ahead instruction for an E-stop already mounted with the enclosed VFD.

Source: https://resources.sienci.com/view/am-mk2-controller-setup/

### 9. First Movements

File: `am-mk2-first-movements.md`

Converted without technical instruction changes. Preserved both gSender-version dropdowns, red homing warnings and Y1-left/Y2-right troubleshooting guidance for consistency with Controller Setup.

Source: https://resources.sienci.com/view/am-mk2-first-movements/

### 10. Spindle Kit Setup

File: `am-mk2-spindle-kit-setup.md`

Made standard-spindle scope explicit and linked ATC configuration separately. Fixed the First Movements link to MK2. Replaced the universal 1500W extension-cord claim with requirements for the actual kit, pending approved ratings. Preserved all three gSender-version dropdowns, firmware configuration downloads, spindle speeds, break-in/warm-up files and startup order.

Source: https://resources.sienci.com/view/am-mk2-spindle-kit-setup/

### 11. Final Checks

File: `am-mk2-final-checks.md`

Clarified factory-fitted coupler inspection and the rear-end-plate check, linking back to Motors. Replaced the blanket 15A spindle-circuit claim with kit-specific voltage/current requirements. Other mechanical, DIP-switch, software and homing checks remain unchanged.

Source: https://resources.sienci.com/view/am-mk2-final-checks/

### 12. Surfacing Wasteboard 🟫

File: `am-mk2-wasteboard.md`

Separated 4x4 sacrificial-sheet examples from 2x4 fit guidance and distinguished table size from machinable area. Flagged the preferred 2x4 cut plan for confirmation. Corrected the reversed stepover explanation and made 40% refer to tool diameter rather than overlap. Fixed option links to sections on this MK2 page. Retained existing surfacing dimensions, cut depth, RPM/feedrate, homing, limits-disable and limits-reenable steps.

Source: https://resources.sienci.com/view/am-mk2-wasteboard/

## Verification performed

- All ten converted documents were compared against their updated source content. No substantive text was lost during conversion; list numbering and text split across HTML spans were checked separately.
- All 160 image references resolve to files in the shared image folder. Each JPG was opened successfully. Source URLs and hashes are recorded in `image-manifest.csv` in the image ZIP.
- All 15 source colour spans and 107 centred text captions are preserved. Original nonempty heading levels are preserved.
- All nine existing dropdowns retain their titles and open/closed state; the older-kit motor-coupler section adds one more, for ten total. Both embedded videos and all linked configuration/g-code downloads remain present.
- Wasteboard in-page links resolve to preserved/cleaned anchors, including the Surfacing anchor. The older MK1 First Movements link in Spindle Kit Setup now points to MK2.
- Checked Markdown rendering locally, including images inside Markdown-aware wrappers. The installed WordPress renderer and live pages have not been modified or tested.

## Source and attribution

Sienci Labs Resources: https://github.com/Sienci-Labs/Resources — source documentation is shared under CC BY-SA as stated in its README. Retained photos, CAD renders and screenshots are Sienci source assets, not newly generated illustrations. The supplied November resource-update PDF supplies the requested technical changes; the separate assembly-update review identifies the dependent consistency edits and outstanding decisions.
