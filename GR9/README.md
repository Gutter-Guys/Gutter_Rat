# Gutter_Rat 9mm Variant

This is the original modification. This mod is designed around 9mm belts with toothed GT2 pulleys and new steppers for X/Y, plus a new control board, however is designed to be the least destructive of the modifications and utilise as much of the E6 parts as possible. You will need to cut the X 2020 extrusion, but it will retain the stock mounting points in case you wish to roll back.

Currently it can be built to reuse the stock belts, stock pulleys and mounting gear, stock controller and stock motors. 

Of course, you can upgrade all these parts to better quality components, as the mod can be reconfigured easily. Please note the dimensions on the stock pulleys and spacers may vary from 3rd party options and require some further modification.

**Currently the there is a design limitation when using the stock pulleys. The stock pulleys are ~2mm wider than a standard 20t pulley. This adds 2mm to the space between the two belts, leaving a Z deflection of 2mm from front to back on the belt path. I have been running this for nearly 500hrs with no visible issues, however I can't promise this will be the case for everyone, so if possible, please look at the cheap upgrade to 20t pulleys.**


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


<img src="Images/GR9_Render.png" alt="GR9">

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
    - 2x MGN9H 350mm rails for Y gantry (MGN12 will not fit inside the panels)
    - 1x MGN12H 350mm rail for X gantry (EVA now only supports MGN12)
    - Rasberry Pi 3B+/4/Zero2 (I am runnig a Zero 2 Wireless with PA/IS and Accelerometer)
    - 1mm washers/spacers
    - Extruder of Choice (Please use a EVA2.4 supported extruder)
    - Hotend of Choice (Please use a EVA2.4 supported hotend)
    - M3 Heat Sets (4 needed for mounting, more maybe needed for your EVA)
- Reuse
    - Stock Belts (No cutting required)
    - Stock Motors  (Some testing required)
    - Stock controller board (Please note the Klipper Configs will need to be tweaked to work on a stock board)
    - Stock pulleys
    - X Extrusion (Cut down slightly to fit, 400mm mininum, 420mm maximum) *note: you can buy and cut a new one*

### GR9 Modified (Preferred)
- Order:
    - 2x MGN9 rails for Y gantry (MGN12 will not fit inside the panels)
    - 1x MGN12 rail for X gantry (EVA now only supports MGN12)
    - Rasberry Pi 3B+/4/Zero2 (I am runnig a Zero 2 Wireless with PA/IS and Accelerometer)
    - 1mm washers/spacers
    - Extruder of Choice (Please use a EVA2.4 supported extruder)
    - Hotend of Choice (Please use a EVA2.4 supported hotend)
    - GT2 Belts
    - 2x Nema17 motors of your choice
    - Controller with at least 4x TMC2209 (Example config is with SKR E3 v2), 6x TMC2209 required for Tri-Z modifications
    - M3 Heat Sets (4 needed for mounting, more maybe needed for your EVA)
    - 13mm wide 20t idlers (6 toothed and 2 smooth)
- Reuse
    - X Extrusion (Cut down slightly to fit, 400mm mininum, 420mm maximum) *note: you can buy and cut a new one*

### Can I fit MGN12H on my Y if I already have them?
Short answer: Yes it can be made to work

Longer answer: You can use the GR9_MGN12_Gantry_Mount_TEST file for fitting the X gantry to the E6 via MGN12H rails. The issue is the over hang of the carriage is 2-3mm each side, which conflicts with the stock side panels. If you choose this change, you will need to *very* carefully space out the side panels. A couple check washers will work, or print a small spacer. Just be **very careful as this will add tension to the panels and may crack the acrylic if not tensioned properly!!!** Please, please be aware of this and take care. I would suggest adding spacers of varying depth down the side to avoid a shape bend on the last part of the panel. 

<img src="Images/Panel_Spacer.png" alt="MGN12H Spacer">

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

## X Extrusion
If you are using the stock X extrusion, it will need to be shortened before it can be used. This can be done by cutting it down to between 400mm to 420mm. We designed the Gantry Brackets to not need an exact measurement, however if you remove a little bit from each end to get to 400mm, you can avoid the original E6 mounting holes allowing the X extrusion to used if you roll back to stock later on. Or simply use a fresh extrusion, completely your choice. 

<img src="Images/X_2020.png" alt="X 2020">

## Rails
Please refer to online guides for mounting and and cleaning rails. MGN9 for Y and MGN12 for X. Nothing special needed, just center them as best you can. It is easier to mount the Y rails after you have mounted the Motor Mounts. Mounting guides are included in the STL folder to make alignment easier. 

## Printhead
The EVA printhead system is amazingly well designed and very flexible. It was the sole reason this upgrade was completed. For the moment, this is compatible with EVA 2.4 setups so go crazy. If it fits EVA, it will fit this setup. I will not be duplicating any of their work here, please go directly to the EVA website and get all you need from there, including BOM and print configurations. 

Mouint it to the X rail now as it can be pain to add later when the rail is in the printer, but do not add the Hotend as you will need access to the belt mounts.

<img src="Images/EVA2_4.png" alt="EVA2.4">

## Idlers
The idler setup is very simple and easy to put together.

### Stock Pulleys
The two vertical M5x10mm screws will need to insert first as they can be hard to get in once the pulleys are in place.

From the top, you will need:
- 5mm printed spacer
- Pulley
- Compression washer (reused from E6)
- Pulley

<img src="Images/Idler_config_stock.png" alt="Stock Idler Config">

Then, simply reuse the long screw from the E6 to fix it together, with a washer on the bottom below the nut. It may seem a little loose in the idler, so tighten until it no longer wobbles, then apply loctite (or clear nail polish) to the remaining thread to hold the nut in place.

Repeat for the other side. Then mount with M5x10mm screws and M5 drop nuts.

### After market pulleys
The two vertical M5x10mm screws will need to insert first as they can be hard to get in once the pulleys are in place.

The current configuration has been tested successfully with standard 20t ilders. You will need a 5mm bore, 13mm width idler. Anything more than 13mm width will require you to adjust the spacer configuration. 

From the top you will need:
- 6mm printed spacer
- Pulley
- 1mm spacer
- Pulley

<img src="Images/Idler_config_AM.png" alt="20t Idler Config">

## Gantry
A little more complicated than the idlers, but simple enough. 

First, mount the Gantry Mounts to the Y Rail carriages. This is straight forward, and makes the final assembly easier.

Then, add the two heat sets to each Gantry Bracket. Again, fairly straight forward. 

Now the complicated part. Align the Gantry Mounts in front of you so they sit as they would in printer. You will notice that one side of the Mounts has a slot and the other side is inclosed. They are set up as follows: (refer to pictures to confirm)

### Stock Pulleys


#### Left - Slotted side
From the top you will need:
- 2mm Printed Spacer
- Stock pulley
- 13mm Printed Spacer

#### Left - Enclosed side
From the top you will need:
- 15mm Printed Spacer
- Stock pulley
- 1mm washer/shim

<img src="Images/Ganty_Pulley_Config_Stock_Left.png" alt="Gantry Stock Pulley Config Left Side">

#### Right - Slotted side
From the top you will need:
- 15mm Printed Spacer
- Stock pulley
- 1mm washer/shim

#### Right - Enclosed side
From the top you will need:
- 2mm Printed Spacer
- Stock pulley
- 13mm Printed Spacer

<img src="Images/Ganty_Pulley_Config_Stock_Right.png" alt="Gantry Stock Pulley Config Right Side">

Then, simply reuse the long screw from the E6 to fix it together, with a washer on the bottom below the nut. It may seem a little loose in the idler, so tighten until it no longer wobbles, then apply loctite (or clear nail polish) to the remaining thread to hold the nut in place.

### After market pulleys
The current configuration has been tested successfully with standard 20t ilders. You will need a 5mm bore, 13mm width idler. Anything more than 13mm width will require you to adjust the spacer configuration. 

#### Left - Slotted side
From the top you will need:
- 3mm Printed Spacer
- Pulley
- 14mm Printed Spacer

#### Left - Enclosed side
From the top you will need:
- 16mm Printed Spacer
- Pulley
- 1mm washer/shim

<img src="Images/Ganty_Pulley_Config_AM_Left.png" alt="Gantry 20t Pulley Config Left Side">

#### Right - Slotted side
From the top you will need:
From the top you will need:
- 16mm Printed Spacer
- Pulley
- 1mm washer/shim

#### Right - Enclosed side
- 3mm Printed Spacer
- Pulley
- 14mm Printed Spacer

<img src="Images/Ganty_Pulley_Config_AM_Right.png" alt="Gantry 20t Pulley Config Right Side">

## Motor Mounts
The motor mount comes in two peices. Mount the stepper to the  base with M3 bolts, then attach firmly to the frame with M5's. Make sure the motor orientation is such that th cables face towards the  back for easy access.

Then, make sure the motor pulleys are orientated correctly. The left pullet will be as per the picture, with the pulley a fraction above flush with the top of the stepper. The right one will be inverted and 10mm from the stepper motor. 

It is easier to run the belts now, before you add the top half - trust me it will be so much easier. Come back to the next bit once they are done. 

Finally, attachedthe top half and fix with M5's. Once attached, use the M3x40mms to anchor the two halves to the stepper motor. 

<img src="Images/Motor_Mount.png" alt="Motor Mount">


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

<img src="Images/Full_Gantry_Render.png" alt="Completed Gantry">

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
