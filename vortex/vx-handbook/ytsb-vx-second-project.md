---
title: ytsb Your Second Project
menu_order: 2
post_status: draft
post_excerpt: Your second project will include generating g-code, using the faceplate and tailstock workholding, stock turning and tool changing.
post_date: 2023-08-23 08:41:18
taxonomy:
    knowledgebase_cat: vx-handbook
    knowledgebase_tag:
        - vortex
custom_fields:
    KBName: Vortex Rotary Axis
    basepress_post_icon: bp-caret-right
skip_file: no
featured_image: _images/post-image.jpg
---

So you've finished your first project and are ready to move onto carving more intricate things? This 'intermediate' project will guide you through creating a rotary carving feature with much more detail and complexity, while helping you learn the tools and skills to carve almost anything!

We'll cover several key concepts in this project, including:

- Fundamental **Limitations** of rotary carving
- Setting up **Tabs**
- **Tool changing** to use a roughing and finishing strategy
- Advanced **Workholding**
- **Stock Turning**

To complete this project, we will be using:

- **A 4" long piece of stock with a diameter of 2.5" which we'll make ourselves**
- <a href="https://drive.google.com/file/d/1Wh3XfmEBAeNMbF6ZqhM3hvReI7nSWJ4E/view?usp=drive_link">3D skull file</a>
- **VCarve Software**
- **¼" upcut end mill for roughing**
- <a href="https://resources.sienci.com/wp-content/uploads/2023/08/3D-Roughing-1.gcode" rel="noopener" download="">Roughing Pass</a> <b>g-code file</b>
- **¼" tapered ball end mill for finishing**
- <a href="https://resources.sienci.com/wp-content/uploads/2023/08/3D-Finish-1.gcode" rel="noopener" download="">Finishing Pass</a> <b>g-code file</b>
- **gSender**
- **LongMill with Vortex attachment**

## Model Selection

A big misconception of rotary carving is that only round objects are suitable. It's completely natural to attribute round things with a process that involves spinning, but rotary carving with the use of a CNC machine is quite unique.

Since we have full independent control of all three axes, we can do a lot more than a simple chess piece. The reason projects done on a rotary axis tend to be round or cylindrical in nature is simply because these are the types of projects that fit best within the footprint of a rotary axis. It's just as feasible to turn a cylinder into a cube on a rotary axis as it is to turn a cube into a cylinder.

[caption id="attachment_5743" align="aligncenter" width="850"]<img class="wp-image-5743 size-medium" src="https://resources.sienci.com/wp-content/uploads/2023/08/IMG_6029-1-850x638.jpg" alt="" width="850" height="638" /> Thor's hammer completed on the Vortex. Making round things square![/caption]

On that note, for our second project, we'll be carving something quite a bit more complex than the chess piece we did on our first project. This will be a skull which is asymmetrical (think lopsided, crooked or unbalanced) around any axis, and features tiny details and cavities.

<img class="nar aligncenter wp-image-5766 size-full" src="https://resources.sienci.com/wp-content/uploads/2023/08/Thing-files-for-3d-Scanned-Human-Skull-using-Creaform-Handyscan-by-djrevz-Thingiverse-Google-Chrome-2023-08-11_12-50-32.jpg" alt="" width="549" height="453" />

### Limitations of Wrapped Rotary Carving

We mention that we'll be able to make any sort of shape using a rotary axis, and this is generally true, however there are some caveats and limitations to this. Two limitations to be aware of are **overhangs**, and trying to **machine below the middle axis**.

**Overhang** isn't necessarily a limitation new to rotary axis carving, it's something we're limited by in any regular XYZ carving, but is a bit more apparent once we've taken this same carving and wrapped it around an axis for rotary carving.

If we simply import this 3d model without any repositioning, you can see that we will have a large overhang marked in yellow in the image below. This results in a model that is missing a lot of detail.

[gallery columns="2" size="large" ids="5768,5775"]

Since our rotary carving is essentially a regular 3-axis carving wrapped around a single axis, we have the same limitations as before - this means no overhanging geometry that our tool won't be able to reach from directly above.

We can see a red cylinder passing through the entire model, showing us the current rotating axis relative to the model's orientation.

The question is of course: where should this red cylinder lie relative to our model? Simply put, this red cylinder should ideally pass through as much of the model as possible, across its entire length. Any section where this red cylinder sticks out from outside the model, there will be an unmachined area below.

If we rotate the model on the Z axis, we can raise the chin, allowing the bit to maximize its coverage. This way we produce a clean front to the model and eliminate our overhang. In the example below, we rotate the model and then resize it to fit our stock. **Overhang eliminated!**

<img class="aligncenter wp-image-5776 size-full" src="https://resources.sienci.com/wp-content/uploads/2023/08/2023-08-23_09-29-59.gif" alt="" width="1280" height="720" />

It's also important to remember that since we've wrapped our model around an axis, the actual axis represents the bottom of the model as far as the machine is concerned, therefore we won't be able to machine below this.

Where the chin of the model prevented us from carving out the overhang, the middle of the model limitation prevents us from coming at the overhang from above. We can't go lower than the middle axis.

<img class="nar aligncenter wp-image-5769 size-medium" src="https://resources.sienci.com/wp-content/uploads/2023/08/VCarve-Pro-11.506-Sienci-Labs-Andy-Lee-Demo-Licence-New-2023-08-11_13-18-353-850x414.jpg" alt="" width="850" height="414" />

Sometimes these limitations might be small details you can clean up by hand after the fact, or they may force you to choose an entirely different model.

Sometimes this is more of a fundamental limitation, like being unable to carve out the slots inside this dagger blade completely. This was finished after the carve, by hand.

<img class="aligncenter size-full wp-image-5778" src="https://resources.sienci.com/wp-content/uploads/2023/08/Dagger-Gif.gif" alt="" width="640" height="360" />

With all this in mind, we'll move on to creating our project in VCarve.

## Generating g-code

Just like in our first project where we made a chess piece, we'll start out by sizing our project in the job setup tab, as well as of course selecting this as a rotary job type. We'll then go on to import our model for this carve.

### Optimizing Your Model's Orientations

Like we've just gone over previously, we'll want to orient our model in a way that allows us to machine most overhanging features, or at the very least - the overhanging features we care about most.

In our case with the skull, we have a few options for orienting the model - each with their own result. Obviously, there are many more options than shown below, but we'll go through the 3 most obvious options below:

<p style="text-align: center;"><b>Option 1</b> - Skull model oriented sideways (A-axis is the red cylinder going ear to ear)</p>

<img class="nar aligncenter wp-image-5770 size-thumbnail" src="https://resources.sienci.com/wp-content/uploads/2023/08/VCarve-Pro-11.506-Sienci-Labs-Andy-Lee-Demo-Licence-New-2023-08-11_15-41-50-250x250.jpg" alt="" width="250" height="250" />

This option allows us to get just about all geometry carved, but won't be very efficient in terms of fitting this skull into our material. You'll usually find that finding round stock of a certain **length** is much easier than finding stock of a certain **diameter** - we generally prefer to orient models in a way that will maximize the utilization of the length of stock we have. Since this skull model is quite a bit longer than it is wide, we'll prefer to orient this model differently.

<p style="text-align: center;"><b>Option 2</b> - Skull model is oriented in it's longest orientation (A-axis is going from chin to back-top of skull head)</p>

[gallery columns="2" size="large" ids="5783,5782"]

By passing the A-axis through the longest section possible, which is the path from the chin to the top of the head, we're able to make this model **as large as possible**. This orientation also allows us to machine almost all of the important front-facing features such as the teeth and nose. There will be unmachined areas at the back of the skull behind the jaw, but of course these areas aren't all that important so we're okay with this detail missing.

<p style="text-align: center;"><b>Option 3</b> - Skull model is oriented looking down (A-axis is passing through direct bottom to top of skull, sort of how a spine would be oriented)</p>

[gallery columns="2" size="medium" ids="5756,5785"]

This last option is not all that different from option 2, but has the skull oriented in a more 'upright' orientation across the A-axis. This doesn't change much in our model fundamentally, but we start to notice some areas have an **overhang**, with more unmachined material at the back of the skull.

*This orientation may be the best for exposing as much of the detailed face as possible, allowing for great detail, however we are using this example to show a large overhang you may want to avoid. You may opt for this orientation for your project, as the skull is more upright.*

Asides from this, we'll utilize a bit less of the length of the material which means we'll end up with a **slightly smaller scale** finished model.

Given our three main options for orienting this model, we'll be going with **option #2** for this project, since it gives us the best results overall, as well as enlarging the scale of this model as much as possible.

### Adding Tabs

In our first project carving a chess piece, we were able to hold this chess piece from one end, while the model was machined from left to right. This is because the widest part of the chess piece was at its base where we held the model in the chuck.

The skull model is quite a bit different, since both the left and right ends taper into a much smaller point from which we can hold it. This time around, we'll approach holding our model by using what we'll call **Tabs**. These are a bit like the tabs you might use while cutting our parts from a sheet of material in regular XYZ cutting, since they serve to hold the model in place as it's machined to its final form.

You can see the space where we will be putting in our tabs below. These will fill up the remaining space of our stock material which sticks out from our model.

Although this project is using a tailstock and tabs, with a model this short, you don't really need them. We wanted to show you this concept as an example in this project, but you may quickly realize they aren't really needed with small projects like this.

<img class="nar aligncenter wp-image-5773 size-medium" src="https://resources.sienci.com/wp-content/uploads/2023/08/VCarve-Pro-11.506-Sienci-Labs-Andy-Lee-Demo-Licence-New-2023-08-11_15-53-29-850x429.jpg" alt="" width="850" height="429" />

When looking at the 2d view, you will see your model in the middle, with a white border on each side. This is where we will be adding our rectangle tabs. Ensure that the tabs reach the entire width and length of the material.

[gallery columns="2" size="medium" ids="5786,5757"]

Navigate to the Clipart tab, and you will see a Library Folder called 3D Tabs. Select this folder and then click and drag your **_Rectangular tab** icon to your 2d view.

<img class="nar aligncenter wp-image-5758 size-medium" src="https://resources.sienci.com/wp-content/uploads/2023/08/VCarve-Pro-11.506-Sienci-Labs-Andy-Lee-Demo-Licence-New-2023-08-11_16-12-55-850x488.png" alt="" width="850" height="488" />

Reposition it to ensure that it touches the edge of the project, and the project itself.

<img class="aligncenter size-full wp-image-5745" src="https://resources.sienci.com/wp-content/uploads/2023/08/2023-08-21_11-30-00.gif" alt="" width="1280" height="720" />

With two tabs in place, you can see our model is now supported on both sides. You can adjust the spacing and size of the tabs to ensure you have a firm hold on the model, while at the same time, reducing the amount of material you will have to remove once the carve is done.

### Full Length Single Tab

We can also add a single tab that runs along the entire length of your model. This is great if you are using a hollow model or looking to have a bust display.

Drop your '_Rectangle' tab on your 2d model again, but this time, we will make it cover the entire workspace, then click on the component properties to downsize it and reveal our model.

<img class="aligncenter size-full wp-image-5746" src="https://resources.sienci.com/wp-content/uploads/2023/08/2023-08-21_11-58-53.gif" alt="" width="1280" height="720" />

This is helpful to give a hollow model a 'bottom' to prevent the end mill from trying to carve out below the center axis. In the example below, we have a model of a knight helmet which is completely hollow inside. The full length tab serves to hold the piece in place, and give us something in the center of our hollow model to prevent the bit from trying to machine all the way through.

[gallery columns="4" size="medium" ids="5796,5795,5793,5794"]

This is what our final skull tabs look like:

1. **Full Length** tab that serves as a spine and connects the Workholding and Base tabs.
1. **Workholding** tab that protects the faceplate and screws at the top of the model.
1. **Base** tab that secures the bottom of the model in the tailstock, and holds the full length tab in place.

<img class="nar aligncenter wp-image-5761 size-medium" src="https://resources.sienci.com/wp-content/uploads/2023/08/2023-08-21_13-01-55-850x447.jpg" alt="" width="850" height="447" />

### Generating Toolpaths

A larger stock size will typically take longer to carve, so for this project we'll use a **roughing path** strategy before we run our **finishing toolpath**. This is really no different than regular XYZ 3D carving, where you'll typically use a roughing pass on larger projects to save some time and reduce the load on your finishing tool.

In our first project where we made a simple chess piece, we were able to get away with carving this without any roughing pass, this is because we were able to have the bit enter the material from the base of the chess piece, and only remove a small amount of material at a time.

This time around, the bit will be milling away lots of material at both the bottom and top of the model so we'll need to have a **Roughing pass** and then a **Finishing Pass**.

Select the roughing pass toolpath icon.

<img class="nar aligncenter wp-image-5763 size-medium" src="https://resources.sienci.com/wp-content/uploads/2023/08/2023-08-21_13-04-47-850x530.jpg" alt="" width="850" height="530" />

And select Model Boundary with a 3D Raster roughing strategy. We will enter 90 degrees to carve from right to left, along the A-axis.

<img class="nar aligncenter wp-image-5749 size-medium" src="https://resources.sienci.com/wp-content/uploads/2023/08/2023-08-21_13-13-48-850x730.jpg" alt="" width="850" height="730" />

Once the roughing pass is complete, run a finishing pass just like we did in <a href="https://resources.sienci.com/view/vx-first-project/">Your First Project</a>. Here you can see a preview of the roughing pass, and then the finishing pass.

[gallery size="medium" columns="2" ids="5765,5764"]

Save and export your g-code for your roughing and finishing toolpaths with the new post processor just like we did in <a href="https://resources.sienci.com/view/vx-first-project/">Your First Project</a>.

## Preflight Checklist

What we've done so far:

- <a href="https://resources.sienci.com/view/vx-first-project/#prepping-material">Measured and Prepped</a> your material (we will do even more prep)
- <a href="https://resources.sienci.com/view/vx-first-project/#exporting-g-code">Exported 2 g-code files</a> w Vortex post processors
- <a href="https://resources.sienci.com/view/vx-first-project/#y-axis-alignment">Align</a> the Y axis
- Enter <a href="https://resources.sienci.com/view/vx-first-project/#rotary-mode">Rotary Mode</a>
- Have the <a href="https://sienci.com/product/1-4-spiral-up-cut-end-mill/">Correct Bit</a> in place
- Set the <a href="https://resources.sienci.com/view/vx-first-project/#setting-x-amp-z-axis">X &amp; Z axis</a>

Before we take off:

- Examine Workholding using the Tailstock and Faceplate
- Use the Stock Turning tool
- Explore Tool Changing options

### Workholding

In Your First Project, because our stock diameter was 1"we used the **chuck's jaws** to clamp the wood directly into the chuck. For this project, we will be using the **screw-on workholding face plate**, because we are using tabs. We will also be using the tailstock to add some support to our job.

#### Faceplate

The face plate can use four #4 - #6 sized screws that are not included. The center hole is great for centering the faceplate on your stock, but not necessary for running your job.

We want to find the middle of our stock, and mount the center screw as close to that as possible. To find the center, simply run a line from corner to corner. Where the lines cross is where we want to pre-drill a small hole to allow the screw to grab in the correct spot.

[gallery columns="2" size="medium" ids="5799,5800"]

Once the center screw is in, you can continue by putting the 4 smaller screws around to secure the faceplate.

<img class="nar aligncenter wp-image-5803 size-medium" src="https://resources.sienci.com/wp-content/uploads/2023/08/2023-08-21_14-44-21-850x589.jpg" alt="" width="850" height="589" />

Once the faceplate is secured, place it into the chuck so that the screws are between the teeth, and tighten the jaws down.

<img class="nar aligncenter wp-image-5856 size-medium" src="https://resources.sienci.com/wp-content/uploads/2023/08/8.p30_Faceplatev2-850x581.jpg" alt="" width="850" height="581" />

#### Tailstock

Once your stock is held firmly in the headstock, you can slide the tailstock towards the center, by keeping the red flange up. Check that the live center is flush against the tailstock, and not extended yet.

Ensure that the live center is aligned with the center punch and then push the red flange down to lock the tailstock in place.

[gallery columns="2" size="medium" ids="5801,5806"]

Now you can spin the tailstock live center away from you to tighten it down. Once the pin has made solid contact with the project, you can secure the red knob on the back. Just finger tight is fine here.

<img class="nar aligncenter wp-image-5805 size-medium" src="https://resources.sienci.com/wp-content/uploads/2023/08/IMG_6096-850x638.jpg" alt="" width="850" height="638" />

Congrats! Your material is in place, let's turn it into stock we can use for our roughing pass now.

### Rotary Surfacing

Now it's time to turn that square stock down to a cylinder and reduce the strain on our end mill for the roughing pass. We will be using a **¼ inch upcut end mill** for turning stock, as it's the most efficient. Fire up gSender and focus on the Rotary tab.

<img class="nar aligncenter wp-image-5841 size-full" src="https://resources.sienci.com/wp-content/uploads/2023/08/Rotary-Surfacing.jpg" alt="" width="517" height="309" />

You will need to be in <a href="https://resources.sienci.com/view/vx-first-project/#rotary-mode">Rotary Mode</a> to use the stock turning wizard.

<img class="nar aligncenter wp-image-5810 size-medium" src="https://resources.sienci.com/wp-content/uploads/2023/08/2023-08-22_14-11-50-850x637.jpg" alt="" width="850" height="637" />

Rotary surfacing is similar to the regular XYZ surfacing wizard. Let's explore this a bit further.

<ol>
  <li>Your <b>start height</b> is the largest diameter on your stock. Usually this means the diagonal distance from opposite corners if you're starting with square or rectangular stock.<img class="nar aligncenter wp-image-5812 size-full" src="https://resources.sienci.com/wp-content/uploads/2023/08/2023-08-10_10-01-28.jpg" alt="" width="218" height="213" /></li>
  <li>Your <b>final height</b> is determined by the short side of your stock, although it can be even smaller if needed.<img class="nar aligncenter wp-image-5809 size-full" src="https://resources.sienci.com/wp-content/uploads/2023/08/Final-Diameter.jpg" alt="" width="300" height="200" /><img class="nar aligncenter wp-image-5813 size-thumbnail" src="https://resources.sienci.com/wp-content/uploads/2023/08/2023-08-22_12-51-17-250x250.jpg" alt="" width="250" height="250" /></li>
  <li>With a starting height of 90mm and a finished height of 63.5mm, we are removing 26.5mm of material. <b>However</b>, since we have the Z axis set at the center of the material, we will need to divide that 26.5mm in half. We are basically taking 13.25mm off of the top and the bottom.If you want a <b>single pass</b>, your stepdown would be 13.25mm. Dividing that by two and setting the stepdown to 6.625mm, means that we will be doing <b>two</b> passes. This will produce a piece of round stock with the maximum diameter possible.</li>
</ol>

<p style="text-align: center;"><b>(Start Height - Finishing Height) / 2 = Total Stepdown for ONE pass</b></p>

<img class="aligncenter size-full wp-image-5808" src="https://resources.sienci.com/wp-content/uploads/2023/08/IMG_6104.gif" alt="" width="424" height="238" />

**Congrats!** You have prepped your stock for its roughing pass. Since we are using the same ¼" end mill, you can simply load up your roughing g-code and hit start.

### Tool Changing

Since we've got two separate toolpaths, with two separate cutting tools used for roughing and finishing, we'll have to decide on how we'll be changing out these tools. This is no different than any regular tool changing you might do with a regular XYZ CNC project, we can either:

<ul>
  <li>Use two separate files exported with each tool in its own file, then load and run each of these files on its own.</li>
</ul>
<img class="nar aligncenter wp-image-5822 size-full" src="https://resources.sienci.com/wp-content/uploads/2023/08/2023-08-22_14-37-05.jpg" alt="" width="672" height="794" />
<ul>
  <li>Use one single file which contains an M6 command to prompt a tool change. When the time comes to change tools, gSender will pause the program to allow you to change the cutting tool, probe the new tool, then resume again once ready. More information on how gSender can help you perform tool changes can be found within the <a href="https://resources.sienci.com/view/gs-additional-features/#tool-changing">gSender Resources</a>.</li>
</ul>

<img class="nar aligncenter wp-image-5823 size-full" src="https://resources.sienci.com/wp-content/uploads/2023/08/2023-08-22_14-37-25.jpg" alt="" width="664" height="801" />

Which of these two options you'd like to use likely depends on your personal preference and experience between the two, but either will work the same.

During the tool change, one thing to be **very mindful** of is to not bump into the Vortex chuck or mounted stock. Similar to how you'd want to make sure the X or Y axis doesn't move when changing tools, you'll want to pay special attention to not rotate the A-axis.

One way to do this is to enable **holding current** in your firmware settings. Simply navigate to your Firmware tab and ensure that you have $1 set for 255. This will keep the A-axis stiff and prevent you from bumping it out of alignment. If you're unsure of this setting and what it does, leave this unchanged as it could cause more issues than good.

<img class="nar aligncenter wp-image-5824 size-medium" src="https://resources.sienci.com/wp-content/uploads/2023/08/2023-08-22_14-43-00-850x492.jpg" alt="" width="850" height="492" />

This possibility of losing the A-axis position is one of the main reasons for using the A-axis limit switch to allow for homing this axis along with the others. If this gets thrown off by accident and you've already homed the machine before starting, you can simply run the homing cycle again and get everything repositioned exactly as before.

[caption id="attachment_5838" align="aligncenter" width="850"]<img class="nar wp-image-5838 size-medium" src="https://resources.sienci.com/wp-content/uploads/2023/08/Roughing-Skull-850x420.jpg" alt="" width="850" height="420" /> Roughing Pass[/caption]

After you've switched the tool, you'll simply re-zero the new bit onto the top of the Vortex chuck the same way you've <a href="https://resources.sienci.com/view/vx-first-project/#setting-x-amp-z-axis">done before</a>.

Now you can load up your finishing pass g-code and hit the start button to run your final pass.

[caption id="attachment_5836" align="aligncenter" width="850"]<img class="nar wp-image-5836 size-medium" src="https://resources.sienci.com/wp-content/uploads/2023/08/Finishing-Pass-850x412.jpg" alt="" width="850" height="412" /> Finishing Pass[/caption]

Congratulations! You now have a Spooky Skull. Back off the tailstock and remove the faceplate from the chuck and admire your second project success.

<img class="nar aligncenter wp-image-5837 size-medium" src="https://resources.sienci.com/wp-content/uploads/2023/08/Scary-Skull-516x850.jpg" alt="" width="516" height="850" />

Finally we cut off the top tab and sand with 220 grit. Mission accomplished! You now have that skull on a stick that you've always wanted. 🤩

[gallery columns="4" size="medium" ids="5835,5834,5832,5833"]
