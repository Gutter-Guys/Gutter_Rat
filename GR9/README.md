# Gutter_Rat 9mm Variant

This is the original modification. This mod is designed around 9mm belts with toothed GT2 pulleys and new steppers for X/Y, plus a new control board, however is designed to be the least destructive of the modifications and utilise as much of the E6 parts as possible. You will need to cut the X 2020 extrusion, but it will retain the stock mounting points in case you wish to roll back.

Currently it can be built to reuse the stock belts, stock pulleys and mounting gear, stock controller and stock motors. 

Of course, you can upgrade all these parts to better quality components, as the mod can be reconfigured easily. Please note the dimensions on the stock pulleys and spacers may vary from 3rd party options and require some further modification.

# Gutter_Rat 9mm Variant

This is the original modification. This mod is designed around 9mm belts with toothed GT2 pulleys and new steppers for X/Y, plus a new control board, however is designed to be the least destructive of the modifications and utilise as much of the E6 parts as possible. You will need to cut the X 2020 extrusion, but it will retain the stock mounting points in case you wish to roll back.

Currently it can be built to reuse the stock belts, stock pulleys and mounting gear, stock controller and stock motors. 

Of course, you can upgrade all these parts to better quality components, as the mod can be reconfigured easily. Please note the dimensions on the stock pulleys and spacers may vary from 3rd party options and require some further modification.


# Table of Contents
- **Before You Start**
    - [**Important Checks**](#-important-checks)
    - [Required Equipment](#required-equipment)
- **Printing Parts**
    - [Print Settings](#print_settings)
    - [Materials](#materials)
- **Assembly**
    - [Printhead](#printhead)
    - [Idlers](#idlers)
    - [Gantry Mounts](#gantry_mounts)
    - [Motor Mounts](#motor_mounts)
    - [Rails](#Rails)
    - [Other Components](#other_components)
    - [Final Assembly](#final_assembly)
- **Tuning**
    - [Klipper](#klipper)
    - [Tuning](#tuning)


# Before You Start

## Important Checks
**This section may sound a little intimidating, but please take the time to read it before you do anything, including ordering parts.**

The most important thing to understand is that this is a significant change to your printer. I have made the upgrade as simple as possible and attempted to avoid any permanment changes to the printer in case you wish to roll back. You will need to be comfortable with wiring, basic mechanical principles and a fairly good understanding of Klipper and printer configurations. Any damage incurred to your printer is on you - you have beeen warned.

The second most important point is to understand that this is a modification. Depending on so many things, your results may vary. Different motors, belts, pulleys, hotends etc. will result in different outcomes. Maybe faster, maybe slower, maybe better, maybe worse, it will depend on what you do and how you do it. 

Lastly, please do not attempt this if it is your only printer. I have built this upgrade twice now and both times managed to either forget to print a part or break one. If I only had the E6 I would have been stopped completely. I can also recommend printing all parts in duplicate just in case but this is personal preference. 


## Required Equipment
**This list is not complete and does not include all fixing hardware yet**

To complete this upgrade you will need the following

### GR9 STOCK
- Order:
    - 2x MGN9 rails for Y gantry (MGN12 will not fit inside the panels)
    - 1x MGN9 rail for X gantry (EVA now only supports MGN12)
    - Rasberry Pi 3B+/4/Zero2 (I am runnig a Zero 2 Wireless with PA/IS and Accelerometer)
    - 1mm washers/spacers
    - Extruder of Choice (Please use a EVA2.4 supported extruder)
    - Hotend of Choice (Please use a EVA2.4 supported hotend)
    - M3 Heat Sets
- Reuse
    - Stock Belts (No cutting required)
    - Stock Motors  (Some testing required)
    - Stock controller board (Please note the Klipper Configs will need to be tweaked to work on a stock board)
    - Stock pulleys
    - X Extrusion (Cut down slightly to fit) *note: you can buy and cut a new one*

### GR9 Modified
- Order:
    - 2x MGN9 rails for Y gantry (MGN12 will not fit inside the panels)
    - 1x MGN9 rail for X gantry (EVA now only supports MGN12)
    - Rasberry Pi 3B+/4/Zero2 (I am runnig a Zero 2 Wireless with PA/IS and Accelerometer)
    - 1mm washers/spacers
    - Extruder of Choice (Please use a EVA2.4 supported extruder)
    - Hotend of Choice (Please use a EVA2.4 supported hotend)
    - GT2 Belts
    - 2x Nema17 motors of your choice
    - Controller with at least 4x TMC2209 (Example config is with SKR E3 v2)
    - M3 Heat Sets
- Reuse
    - Stock pulleys
    - X Extrusion (Cut down slightly to fit) *note: you can buy and cut a new one*

# Printing Parts

## Print Settings
Not going to lie, the best parts settings I have worked with yet are the Voron settings. Its a good base to start from, but please feel free to tune in what works for you:
- Layer height: 0.2mm
- Extrusion width: 0.4mm
- Infill percentage: 40%
- Infill type: Gyroid
- Wall/Perimeters: 4
- Top/Bottom layers: 5
- Supports: Brim only if required

## Materials
I have succesfully printed this upgrade in both PETG and ABS.

### PETG
PETG is a crazy material, and the layer adhesion is amazing. For this reason it is quite a good option for printing the parts for this modification. I would strongly suggest the wider fan duct option thouoh, as mine did sag a little over time. If you plan to enclose the printer long term, then PETG can be used for a short period. At chamber temps over 50c the PETG *will sag* and can cause problems, but it might be enough to get a reprint in ABS.

### ABS
I love and hate ABS. 99% of my prints are in ABS and my printer is fully enclosed, so ABS parts were a must. The parts are fine with a little bit of shrinkage so no scaling is required, however some screw holes may need to be cleared with a drill bit. The EVA parts are usually supplied from RatRig in PETG but I have had no issues with them printed in ABS. Just be aware that ABS can delamiinate easily, so be careful with the trapped nuts in the EVA parts.

### PLA
Don't bother. It won't work and aside from some of the cosemtic parts, it just isn't worth the hassle or risk.

### Other Materials
No idea. Could work, might not. Let me know if you try something and it works, I will update the notes. 

### Colours 
Up to you, but I have marked each part as A (Accent) or B (Base) so you can do a two tone look. Otherwise go crazy :)


# Assembly

## Printhead
The EVA printhead system is amazingly well designed and very flexible. It was the sole reason this upgrade was completed. For the moment, this is compatible with EVA 2.4 setups so go crazy. If it fits EVA, it will fit this setup. I will not be duplicating any of their work here, please go directly to the EVA website and get all you need from there, including BOM and print configurations. 

Mouint it to the X rail now as it can be pain to add later when the rail is in the printer, but do not add the Hotend as you will need access to the belt mounts.

## Idlers
The idler setup is very simple and easy to put together.

### Stock Pulleys
The two vertical M5x10mm screws will need to insert first as they can be hard to get in once the pulleys are in place.

From the top, you will need:
- 1mm washer/spacer
- 2mm spacer (small black one reeused from E6 parts)
- Stock pulley
- Compression washer (reused from E6)
- Stock pulley

Then, simply reuse the long screw from the E6 to fix it together, with a washer on the bottom below the nut. It may seem a little loose in the idler, so tighten until it no longer wobbles, then apply loctite (or clear nail polish) to the remaining thread to hold the nut in place.

Repeat for the other side. Then mount with M5x10mm screws and M5 drop nuts.

## Gantry
A little more complicated than the idlers, but simple enough. 

First, mount the Gantry Mounts to the Y Rail carriages. This is straight forward, and makes the final assembly easier.

Then, add the two heat sets to each Gantry Bracket. Again, fairly straight forward. 

Now the complicated part. Alight the Gantry Mounts in front of you so they sit as they would in printer. You will notice that one side of the Mounts has a slot and the other side is inclosed. They are set up as follows: (refer to pictures to confirm)

### Slotted side
From the top you will need:
- Printed spacer
- Stock pulley
- 1mm washer

### Enclosed side
From the top you will need:
- 1mm washer
- Stock pulley
- Printed spacer

Then, simply reuse the long screw from the E6 to fix it together, with a washer on the bottom below the nut. It may seem a little loose in the idler, so tighten until it no longer wobbles, then apply loctite (or clear nail polish) to the remaining thread to hold the nut in place.

## Motor Mounts
There are two options

### Version 1 (One piece design)
Simply mount the Motor via the screw points. From there, use M5x10mm screws and M5 drop nuts to mount securely to the frame

### Version 2 (Clam shell design)
TBC

## Rails
I am no guru, please refer to online guides for mounting and and cleaning rails. MGN9 for Y and MGN12 for X. Nothing special needed, just center them as best you can. It is easier to mount the Y rails after you have mounted the Motor Mounts.

## Other Components
Similar to the rails, I will leave to you and the internet to work out how to mount things like custom controllers, Raspberry Pi etc. I only suggest to keep it simple and don't take too much on at one time as it will make trouble shooting hard.

## Final Assembly
Now for the fun part - putting it all together.

### Mounting Hardware
At this point, you should have the motors mounted, the ilders completed and mounted, Gantry Brackets completed, EVA and only the Gantry Mounts in place on the Y rails. If not, go back and finish these steps first.

First, add the two Gantry Brackets to the X extrusion. They should slip on and be firm but able to be moved without to much effort. You will need to adjust these later on, so its important they can move. Add the two M5x10mm screws and drop nuts now but do not over tighten yet. 

Now, position the X extrusion in the printer so that it sits on the two Gantry Mounts attached to the Y rails. Use M3 screws to attach to the Gantry Mounts. You should now have the X extrusion mounted and it should slide easily on the Y rails. If not, adjust the Gantry Brackets on the X extrusion until it does move easily. **DO NOT FORCE IT!**

**Once the X is moving freely, we need to de-rack the gantry. This is super, super important. For reference, Nero3DP has a great video on YouTube that I highly recommend you watch as an explanation, even though it references a Voron 2.4 printer.**

To de-rack the E6, slide the X all the way to the front of the printer. Both Gantry Brackets should be touching the idlers evenly. Typically, one will be touching and one won't. This twist is what we need to remove. Gently, while all mounting screws are loose, fiddle with the various mounts until both Gantry brackets are hard up against the Idlers. Now go back over *every* screw and tighten them in place. Check the X is still square to the two idlers and slide it back and forth all the way to the Motor Mounts to ensure there is no binding. 

Once De-racked, it is time to add the belts. This is my way of mounting them, but you are welcome to do it however it works for you. Add one end of each belt to the tensiner blocks on the EVA printhead, making sure the belts are fully in the blocks. Insert them into the printhead and tighten until they are both even with the back of the EVA printhead. **Take the time to make sure they are even at this point**

Now route the belts through the printer and back to the print head. Put the end of each belt on printhead so that 1-2 ridges extend past the belt grabbers. **Make both sides the same**.

The belt should be fairly loose if you have used the stock belts. If you bought new belts, over hang as much as needed, but keep the lengths the same. Slowly tighten the belt tensioner screws until the belts are the correct tension. Again, you need to Google this as there are dozens of suggested methods floating around out there and everyone has a recommended tension.

If the belts are done, make sure the XY motors are disconnected and move the X back and forth, checkin the racking at the same time. If the X has misaligned again, change the belt tension until it is de-racked again. 

After this is dine, you can mount your Hotend to the Printhead and congrats!

# Tuning

## Klipper
Klipper is both amazing and magical to most. I do not claim to be any good with Klipper, however I have attached a sample config if you wish to look over it. You will need to adjust the pin IDs for your controller, as well as sensorless homing if you went that way. Otherwise, ask questions on Discord and we will help where we can.

## Tuning
There are many wasy to skin a cat, and many ways to tune a printer. What I do recommend is to start with Superslicer. Its well supported and better yet, it allows you to use what I think is the best tuning guide you there - Andrew Ellis Print Tuning Guide. It is written for a Voron, but it is the most detailed and simple guide out there. 

I have attached a copy of the SuperSlicer profile I use, which was based on the above guide. With 1.8 motors and Sherpa Mini, I can sit comfortably at the following print settings;

150mm/s outer walls at 5k acc
250mm/s inner at 9k acc
300mm/s infill at 12k acc
120mm/s top infill/surface at 5k acc
ABS with 80% cooling fixed speed
10% infill retic
Mono surface
