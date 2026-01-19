---
title: Router vs Spindle
menu_order: 7
post_status: publish
post_excerpt: Learn about router and spindle options for a CNC, with consideration for noise, speed control, cost.
post_date: 2026-01-14 16:23:12
taxonomy:
    knowledgebase_cat: the-basics
    knowledgebase_tag:
        - cnc fundamentals
custom_fields:
    KBName: Fundamentals
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/_cnc-fun/_the-basics/cnc_ba_router-vsspindle.jpg
---

## Cutting Basics

Before comparing routers and spindles, it’s important to understand how cutting works. When cutting material with a rotating bit, you can imagine that going too slow will dull or break the bit very quickly. For example, imagine trying to cut through a plank of wood with a saw except instead of moving the saw back and forth you're just trying to push it directly through. Similarly, a bit that's moving too fast can burn or melt the material that you're cutting. Finding a happy medium between these two extremes is a balancing act and depends on balancing three main factors:

1. **Feed rate / plunge rate** – how fast the tool moves through the material  
2. **Spindle speed** – how fast the bit spins (RPM)  
3. **Depth of cut & step over** – how much material is removed per pass  

Each of these factors must be suited to the properties of the material that you're cutting; cutting through foam can happen much faster than cutting aluminum. We generalize these variables under the term 'feeds and speeds', and each cutting tool has a different set of ideal feeds and speeds. Learning how to tie a tool's size and shape to its movement, rotation speed, material type, and material removal rate is nearly an art form. There are engineers whose job is knowing how to properly balance all these numbers and apply them based on part geometry, desired finish, and the total job cutting time. Without the proper planning, you can expect many headaches along the way including broken tools, broken material, and an uneven or rough surface finish on your project. Feed and speed choice depends on the material you are cutting, the type of tool you use, the speed of the router, the rigidity of the machine, and even the geometry of the model. In order to balance speed, finish quality, and precision you must account for bit deflection and material hardness. When cutting, the tool can be pushed away from where it should be since it's not able to cut the material fast enough. Harder materials require a more rigid machine and longer milling times to steadily cut the material away. Sometimes it will take some trial and error to dial-in the right settings for your desired setup and materials.

**Higher tool RPM produces smaller chips, while higher feed rates produce larger chips. Overall, if the chips are too large, your bit will be likely to break, but if your chips are too small (like fine powder), you will be dulling your bit. It’s all about getting the right balance.**

This balance called *Feeds and Speeds* varies by material, bit size, and machine rigidity.  

- Too slow = dull or broken bits  
- Too fast = burning or melting  
- Chips too large = broken bits  
- Chips too fine = dull bits  

Finding the sweet spot takes some trial and error, but it’s critical for both performance and tool life. Read more about [Feeds & Speeds Here.](https://resources.sienci.com/view/lmk2-feeds-and-speeds/)

> **Tip:** Install your bit as deeply as possible in the collet, with at least 3/8" inserted for light cuts.  

## Spindles vs Routers

For most hobby CNC users, a trim router strikes the best balance of cost, simplicity, and performance. A spindle is an upgrade worth considering once you’ve outgrown the router, especially if you value quieter operation, precision, and automation.

![](/_images/_cnc-fun/_the-basics/cnc_ba_router-vsspindle.jpg){.aligncenter .size-medium}

### Routers

Most hobby CNCs use compact trim routers like the **Makita RT0700/RT0701**, which offer:  

- **Affordable price** – widely available, under $150 USD  
- **Plenty of power** – 1-1/4 HP is enough for most woods and plastics  
- **Wide RPM range** – 10,000–30,000 RPM, adjustable by dial  
- **Durability** – metal body, long runtime capability  

![](/_images/_cnc-fun/_the-basics/cnc_ba_router-makita.jpg){.alignleft .size-medium}

Routers are simple to set up—just plug into the wall and go. The trade-off is that speed control is manual, they’re noisier than spindles, and motor brushes eventually wear out.

A router offers a more *analog* experience, where users must manually set the router speed using a physical dial, and turn on/off the router at the start and end of a cutting program.

Most hobby CNC routers, will utilize an off-the-shelf trim router. Although these are suitable for hobby use, they have some limitations both in regards to reliability over long periods of time, and a lack of ability to automate their control. Despite this, a trim router such as the popular Makita RT0701C router has a proven track record of being a very capable, easy to install option for relatively little cost.

### Spindles

Spindles are the next step up in CNC cutting. A key difference between routers and spindles is that a router houses all of its electronics inside of itself and plugs into a wall outlet directly, but a high speed spindle contains only the motor and rotating elements, while an intermediate **VFD (Variable Frequency Drive)** unit is used to direct power from the wall outlet to the spindle motor.

![](/_images/_cnc-fun/_the-basics/cnc_ba_router-pkg.jpg){.aligncenter .size-medium}

**Advantages:**  

- Quieter operation  
- More power and torque  
- Lower runout (greater precision)  
- Brushless = longer life  
- Can be software-controlled (on/off, speed, direction)  

**Disadvantages:**

- More expensive  
- Heavier (may need sturdier mounts)  
- Setup is more complex  

### Comparison

| Feature     | Router (e.g. Makita RT0701) | Spindle (with VFD) |
|-------------|------------------------------|--------------------|
| Price       | Low ($100–$150)             | Higher ($300–$1000+) |
| Noise       | Loud                        | Quiet |
| Control     | Manual dial                 | Software controlled |
| Longevity   | Brushes wear out            | Long life |
| Setup       | Plug-and-play               | Requires wiring/VFD |
| Power       | 1–1.25 HP                   | 1.5+ HP common |

### Why Not Dremels or Handheld Rotary Tools?

Handheld tools like Dremels are **not recommended**. They are highly underpowered for use on most CNC machines, since they do not have internal hardware that allows them to support the high lateral and axial forces. In addition, these tools are fabricated for hand use, and as such aren't designed for the minimal runout required to cut precisely.

## Recommendations

- **Beginners:** Start with a router like the Makita RT0701. Affordable, easy, and reliable.  
- **Advanced users / heavy use:** Consider upgrading to a spindle for quieter, more precise, and longer-lasting performance.  

If you are a beginner user, we highly recommend sticking with a Makita RT0701. The Makita RT0701 offers plenty of power and speed control for this application. Installing a spindle can be very technically challenging and may cost significantly more. If you plan on adding a spindle we recommend checking our <a href="https://forum.sienci.com/" target="_blank" rel="noopener">Forum</a> and <a href="https://www.facebook.com/groups/mill.one" target="_blank" rel="noopener">Facebook Group</a> for more info.
