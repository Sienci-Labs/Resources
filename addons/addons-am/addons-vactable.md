---
title: Vacuum Table
menu_order: 3
post_status: draft
post_excerpt: Instructions for setting up the vacuum table for the 4x8 AltMill.
post_date: 2026-05-20 15:11:02
taxonomy:
    knowledgebase_cat: addons-am
    knowledgebase_tag:
        - addons
custom_fields:
    KBName: Add-ons
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: 
---

# Vacuum Table Assembly — AltMill 4×8

<!--
DRAFT — for Resources / Engineering review before publishing.
Source: Vacuum Table System Development Log > Resources tab (reviewed by Marcus, October 14, 2026).
Source images: 24 embedded pictures, represented below in their original order.
To insert a picture, replace its IMAGE comment with Markdown such as:
![Descriptive alt text](images/addons_vactable-description.jpg)
Adjust the relative image path for your Git/WordPress repository.
Do not publish until the REVIEW ITEMS at the end have been resolved.
-->

The Vacuum Table uses a pump and piping installed beneath your AltMill 4×8, along with a machined MDF grid board on top of the machine. This guide walks through installing the pump, assembling the piping, and cutting the grid board.

**Estimated time:** approximately 4.5 hours: 1.5 hours of assembly and about 3 hours of CNC cutting. Allow additional time for preparation and checks.

> **Important:** This is a draft based on the Resources assembly notes. Confirm the supplied hardware, electrical requirements, approved G-code, and cutting tools before using these instructions on a machine.

## Before you begin

- Make sure your AltMill 4×8 is assembled, connected, and able to home and run a job. You should be comfortable setting your work zero and running G-code in gSender.
- Leave room to access both sides and the underside of the machine while installing the pipe assemblies.
- If you are replacing an existing wasteboard, remove it before fitting the new MDF grid board.
- Have a **3/4-inch, 4×8-foot MDF sheet** ready for the grid board. If you plan to use a full-sheet bleeder board, have a second matching sheet ready.
- **Joinery configuration:** Cut 4 inches off the specified end of the MDF grid board (and bleeder board, if used) *before* beginning assembly. Confirm the correct end and orientation for your machine.
- Avoid storing the MDF in a humid shop for an extended period before cutting; swelling can affect alignment.
- The source notes specify a **single-phase 220 V, 30 A circuit**, separate from the spindle, CNC machine, and dust collection, and a pump connection rated **250 V / 30 A with an L6-30P plug**. Have a qualified electrician confirm the actual pump label, circuit, compatible receptacle, and any extension cord needed for your shop. Keep the pump unplugged during assembly.

### Tools and materials

- Drill and driver bits (Robertson and flathead)
- Allen key set
- **3/8-inch flat end mill, downcut**, for the locating pockets (verify against released G-code)
- **3/8-inch flat end mill, upcut**, for the grid (verify against released G-code)
- MDF grid board and, optionally, a separate MDF bleeder board
- Vacuum Table kit: pump, filter, fittings, pipe assemblies, short hoses, hose clamps, mounting hooks, positioning guides, screws and T-nuts, clamping flanges, and flange fastening tool

## Assembly

### 1. Place the pump beneath the machine

1. If an existing wasteboard is installed, unfasten it. It can rest on the machine temporarily while you prepare the underside.
1. From the **right side** of the machine, position the vacuum pump underneath the table, roughly between the front and rear legs.
1. Keep the pump toward the right-hand side rather than pushing it all the way left. Leave enough space to access the filter and hose connections.

<!-- IMAGE 01 — Pump placement under right side of the 4×8. Source image: kix.2xqumoozw2rc. Insert ![Pump positioned beneath the right side of the AltMill](images/addons_vactable-pump-position.jpg) -->

### 2. Install the pump fittings and filter

1. Remove the **red protective cap** from the vacuum pump inlet.

<!-- IMAGE 02 — Remove red pump cap. Source image: kix.gsnheelczal0. Insert ![Removing the protective cap](images/addons_vactable-pump-cap.jpg) -->

1. Attach the **larger fitting** to the connection at the back of the pump.
1. Connect the **vacuum filter** to that fitting.
1. Install the **smaller fitting** at the top of the filter. Position the assembly so the upper connection can receive the hose from the central pipe assembly.

<!-- IMAGE 03 — Pump-to-filter fitting. Source image: kix.sfvlrmhuwqhu. Insert ![Attaching the larger pump fitting](images/addons_vactable-filter-fitting-1.jpg) -->

<!-- IMAGE 04 — Filter installation detail. Source image: kix.1znwyjpxnaww. Insert ![Connecting the vacuum filter](images/addons_vactable-filter-fitting-2.jpg) -->

<!-- IMAGE 05 — Completed pump/filter arrangement. Source image: kix.mx2l856fe9m0. Insert ![Installed vacuum pump fittings and filter](images/addons_vactable-filter-complete.jpg) -->

### 3. Install the MDF positioning guides

1. Find the **six positioning guides** supplied with the kit.
1. Prepare **four side guides** with **one M5 × 14 mm screw and one T-nut each**.
1. Prepare **two rear guides** with **two M5 × 14 mm screws and two T-nuts each**. Check that the T-nuts face the proper direction to engage the machine T-slots.

<!-- IMAGE 06 — Positioning guide hardware. Source image: kix.p28bdli9yv1t. Insert ![Screws and T-nuts on the positioning guides](images/addons_vactable-guides-hardware.jpg) -->

1. Mount **two guides along the back** of the machine and **two along each side**. Space them reasonably evenly.
1. Align each guide with its T-slot so it sits against the machine rail, then tighten it securely. These guides act as stops to locate the MDF board consistently.

<!-- IMAGE 07 — Guide placement overview. Source image: kix.f412h81zt4mi. Insert ![Positioning guide locations on the machine](images/addons_vactable-guides-overview.jpg) -->

<!-- IMAGE 08 — Guide positioning detail. Source image: kix.76n7nfpbqdm4. Insert ![Side guide installed against the rail](images/addons_vactable-guides-side.jpg) -->

<!-- IMAGE 09 — Another guide positioning view. Source image: kix.52h3bjh3qj9e. Insert ![Rear guide installed against the rail](images/addons_vactable-guides-rear.jpg) -->

### 4. Secure the MDF and cut the pipe locating pockets

1. Set the new MDF grid board against the positioning guides.
1. Fasten the board from underneath using the machine's crossbeams. The Resources notes recommend **at least two fasteners per crossbeam** because holes will be machined into the MDF. Check fastener lengths and locations to avoid interference with the cutting area.
1. Connect to the machine and home it.
1. Remove the dust shoe as needed to set the **work zero at the front-left corner, on the top surface of the MDF**. Reinstall the dust shoe before cutting.
1. Install the specified **3/8-inch downcut flat end mill** and load the correct **pocketing G-code** for either the standard or joinery configuration.
1. Confirm tool clearance, work zero, stock security, and toolpath before running the program. Cut the pipe locating pockets. **Estimated cutting time: 15 minutes.**

<!-- IMAGE 10 — Completed pocket cuts / pocketing layout. Source image: kix.qauu9d75vfcc. Insert ![Locating pockets machined in the MDF grid board](images/addons_vactable-pocketing.jpg) -->

**Keep the same X/Y work-zero reference for the later grid-cutting operation.**

### 5. Remove the MDF and prepare the mounting hooks

1. Remove the screws from beneath the MDF and lift the board off the machine, keeping the positioning guides in place.
1. Feed the hose clamps through the slots in each mounting hook. Orient the clamp tightening screws **outward** so they will be accessible after installation.

<!-- IMAGE 11 — Hose clamp inserted through mounting hook. Source image: kix.eea5an5z5ldz. Insert ![Hose clamp threaded through a mounting hook](images/addons_vactable-hook-clamp.jpg) -->

1. Install the supplied screws and T-nuts into the mounting hooks, following the kit configuration. Do not fully tighten the hooks to the machine yet; they must still move for alignment.

<!-- IMAGE 12 — Mounting hook screw and T-nut details. Source image: kix.5uj8d3ro9fzs. Insert ![Mounting hook with screws and T-nuts](images/addons_vactable-hook-hardware.jpg) -->

### 6. Install the front pipe assembly — Position 1

1. Attach **two mounting hooks** to the front side of the first crossbeam at **Position 1**. Leave their T-slot fasteners loose.

<!-- IMAGE 13 — First two hooks at Position 1. Source image: kix.jdl7fwwd67uo. Insert ![Front crossbeam mounting hook locations](images/addons_vactable-front-hooks-1.jpg) -->

1. Rest the **front pipe assembly** in their hose clamps. The **gate faces the right side of the machine**, and the **inlets point upward** toward the MDF pockets.
1. Position the clamps in the grooves **between the pipe fittings**.

<!-- IMAGE 14 — Front pipe assembly orientation. Source image: kix.2o9krms8f6ej. Insert ![Front pipe with gate facing right and inlets up](images/addons_vactable-front-pipe-orientation.jpg) -->

1. Fit the **other two hooks** on the back side of the same crossbeam. Adjust the pipe so it rests correctly inside all four hose clamps.

<!-- IMAGE 15 — Rear-side hooks supporting front pipe. Source image: kix.wujsy1tz6vqt. Insert ![Additional hooks on opposite side of front crossbeam](images/addons_vactable-front-hooks-2.jpg) -->

<!-- IMAGE 16 — Front pipe mounting detail. Source image: kix.1zrsnaunrx1d. Insert ![Front pipe seated within hose clamps](images/addons_vactable-front-pipe-detail-1.jpg) -->

<!-- IMAGE 17 — Front pipe mounting detail. Source image: kix.oqfarzsn81ro. Insert ![Front pipe mounting clamp detail](images/addons_vactable-front-pipe-detail-2.jpg) -->

1. Tighten the **hose clamps** slowly with the appropriate driver, but **leave the mounting hooks loose in their T-slots** so the pipe can still align with the pockets above.

<!-- IMAGE 18 — Additional front-pipe / hook illustration. Source image: kix.mm3tqssnqyvz. Insert ![Front mounting hook and clamp arrangement](images/addons_vactable-front-pipe-detail-3.jpg) -->

### 7. Install the rear pipe assembly — Position 2

1. At **Position 2**, attach **two mounting hooks on each side** of the crossbeam, for **four hooks total**. Leave the T-slot fasteners loose.

<!-- IMAGE 19 — Four rear pipe mounting hooks. Source image: kix.xwuwbxxv7f6b. Insert ![Rear crossbeam mounting hook positions](images/addons_vactable-rear-hooks.jpg) -->

1. Place the **rear pipe assembly** in the hose clamps, again with the **gates toward the right** and the **inlets upward**.
1. Seat the designated mounting hook in the groove between the pipe fittings. Position the remaining hooks as shown in the approved assembly images.
1. Tighten the hose clamps, while leaving the mounting hooks loose for final alignment.

<!-- IMAGE 20 — Rear pipe mounting and clamp location. Source image: kix.h0spyzgc2j4y. Insert ![Rear pipe assembly held in mounting hooks](images/addons_vactable-rear-pipe.jpg) -->

### 8. Align and secure both pipe assemblies

1. Place the MDF grid board back against its positioning guides and refasten it in the same screw holes.
1. Move the front and rear pipe assemblies until the upward-facing inlets are **centred beneath the machined pockets**.
1. Using the provided tool, screw a **threaded clamping flange** into each pocket and its matching pipe connection.
1. Check that every flange sits **flush with or below the MDF surface**. If a flange protrudes or sits crooked, readjust the pipe assembly before proceeding.

<!-- IMAGE 21 — Threaded flange installed. Source image: kix.5nosez8ru8l4. Insert ![Threaded clamping flange fitted into a pipe pocket](images/addons_vactable-flange-install.jpg) -->

<!-- IMAGE 22 — Correct flange height / alignment. Source image: kix.rsatbgofsbqr. Insert ![Clamping flange sitting flush with MDF](images/addons_vactable-flange-flush.jpg) -->

1. Once everything is aligned, securely tighten **all eight mounting hooks** to the machine.
1. Gently push and pull on the gates to confirm that the pipe assemblies do not shift.

### 9. Connect the front, rear, and central piping

1. Fit the **short hoses** onto the front and rear pipe assemblies and tighten their hose clamps.
1. Connect the **central pipe assembly** between the front and rear assemblies and the fitting on top of the vacuum filter.
1. Check that the central pipe and hose connections are routed without undue strain, then tighten the remaining hose clamps.

<!-- IMAGE 23 — Central pipe / hose connections. Source image: kix.ghuhun2rw8j3. Insert ![Central piping connecting the front and rear assemblies](images/addons_vactable-central-pipe-1.jpg) -->

<!-- IMAGE 24 — Completed central piping. Source image: kix.5krrdx94v9s5. Insert ![Central pipe connected to the vacuum filter](images/addons_vactable-central-pipe-2.jpg) -->

### 10. Cut the MDF vacuum grid

1. Confirm that the MDF grid board is firmly fastened to the machine.
1. **Remove all threaded clamping flanges** so the cutting tool cannot strike them.
1. Change to the specified **3/8-inch upcut flat end mill** and load the correct **grid-cutting G-code** for the standard or joinery machine configuration.
1. **Do not change the X/Y work zero** established for the locating pockets. Because the cutting tool has changed, verify the Z reference / tool length for the new bit according to the approved program and machine setup before running the grid.
1. Check the toolpath, clamps, travel clearance, and cut depth, then run the grid program. **Estimated cutting time: 2.5 hours.**
1. When the cutting is complete and the machine is stopped, reinstall the threaded clamping flanges. Check again that they sit flush with or below the MDF surface.

<!-- IMAGE NEEDED — Finished grid board showing pattern and inlet flanges. This image is not present in the Resources tab's 24 assembly pictures. Suggested filename: images/addons_vactable-grid-finished.jpg -->

## Final inspection

- [ ] Pump and filter are accessible beneath the right side of the machine.
- [ ] All eight mounting hooks and all hose clamps are securely tightened.
- [ ] Front and rear pipe inlets align with the MDF pockets.
- [ ] All clamping flanges are installed and sit flush or below the board surface.
- [ ] MDF is fastened securely, and the grid has been cut without damaging piping or hardware.
- [ ] Power supply and pump installation have been checked against the product rating and local electrical requirements.

Before using vacuum hold-down for cutting, follow the separate **Vacuum Table Usage Guide** for gate selection, material preparation, proper use of primary/secondary pump switches, hold-down verification, and maintenance. **Never operate the secondary pump switch on its own.**

<!--
REVIEW ITEMS BEFORE PUBLISHING
1. Add approved standard and joinery pocketing/grid G-code files or links.
1. Confirm 3/8-inch downcut pocketing bit and 3/8-inch upcut grid bit against released files. An older "Assembly Order of Operation" tab specifies a 1/4-inch bit for pockets, conflicting with the more recent Resources tab.
1. Confirm tool-change / Z-zero instructions so both jobs use a safe, consistent coordinate reference.
1. Confirm electrical label, NEMA L6-30 receptacle requirement, circuit rating and cord guidance.
1. Confirm hardware list, screw lengths, and final mounting-hook location markings for production kits.
1. Confirm joinery-board 4-inch trim direction and board orientation.
1. Replace all 24 source-image comments with the corresponding exported pictures. Add a photo of the finished grid if available.
1. Confirm which instructions belong in a separate Usage / Maintenance Guide.
-->


![](/_images/_addons/addons_am/vactable/addons_vactable-am4x8-vac-pump-no-filter.jpg){.aligncenter .size-medium}

![](/_images/_addons/addons_am/vactable/addons_vactable-remove-red-cap.jpg)

![](/_images/_addons/addons_am/vactable/addons_vactable-larger-fitting-at-vac-pump.jpg)

![](/_images/_addons/addons_am/vactable/addons_vactable-vac-pump-attach.jpg)

![](/_images/_addons/addons_am/vactable/addons_vactable-small-fitting-vac-pump.jpg)

![](/_images/_addons/addons_am/vactable/addons_vactable-bad-t-nut-orientation.jpg)

![](/_images/_addons/addons_am/vactable/addons_vactable-guide-rail-side.jpg)

![](/_images/_addons/addons_am/vactable/addons_vactable-guide-back.jpg)

![](/_images/_addons/addons_am/vactable/addons_vactable-guide-back-and-side.jpg)

![](/_images/_addons/addons_am/vactable/addons_vactable-4x8-zero.jpg)

![](/_images/_addons/addons_am/vactable/addons_vactable-hose-clamp-direction.jpg)

![](/_images/_addons/addons_am/vactable/addons_vactable-mounting-hook-fasteners.jpg)

