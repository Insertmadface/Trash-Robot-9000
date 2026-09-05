# Trash-Robot-9000
I'm working on a robot that picks up trash.

## Summary
The Trash-Robot-9000 (aka. Trash Destroyer 9000 and Trash Destroyer-9000) is a human-driven, 6-wheel, electric-powered robot concept capable of collecting primarily recycling off of even and uneven surfaces.

The robot will consist of a few main parts, namely the intake, indexer, hopper, and drivebase. The inspiration for this design has largely been FRC Robots (In specific the 2026 REBUILT season), which have influenced the subsystem-based approach the project is taking.

The preliminary CAD model of the entire robot has been completed, and the robot is in the prototyping stage. At the time of writing, the intake prototype has been built, and is currently being tested to measure how the pivot mechanism, built-in intake compliance, and intake drive mechanism work in real life compared to the CAD, along with the viability of the motors and their current gearbox setups.

As time goes on and possibly after the completion of the Stardance project, software upgrades and iterations include adding remote driver vision through cameras and wifi-based control via a mobile device. Hardware upgrades include redesigning the drivebase for increased off-road capibilities, increasing waterproofing of design for faster washing, and the addition of a bag to increase hopper size and storage ability.

## Design Process

### Problem Statement and Design Scenario
Many areas in the Mississauga community, such as parks, trails, community areas, and even schools have litter around them, making our neighbourhoods less clean, less friendly to visitors, and further convincing people not to put in the effort of disposing of their trash and recyling properly.

While small-scale "roomba-style" vaccum cleaners exist, and larger human-driven machine disposers also work to help with the problem, there currently is no better medium-scale solution to the litter problem than a human. Humans who clean trash off of parks often put in extreme effort for either low, or no compensation, with a painfully slow workflow of picking up individual pieces of trash and putting it in bags.

The solution to this problem is a medium-scale robot able to effieciently collect and store trash in smooth to medium terrain, before offloading for disposal and recyling.
### Solution Criteria
The Solution Criteria for this design is noted below:

+ Robot must be able to intake trash from the size of a wrapper to a standard 2L plastic bottle
+ Hopper must be able to be detatched and reatached within 1 minute consistently
+ Robot must be able to traverse a minimum of a 8" gap
+ Robot must have at least 1/2" of clearance
+ Robot drivebase should be able to drain water from all areas
+ Battery and electrical components must be isolated from water and debris
### Ideation Process
The idea and brainstorming section of the robot began on whiteboards, starting with abstract concepts and various designs on how to pick up, store, and dispose of trash. The final iteration of the sketched designs came to a compliant intake, indexer to move the recyling through the bot, and a detachable hopper attached to the rear to store the recyling.

![Ideation Whiteboard Image 1](Assets/Whiteboard%20Ideation%20Image%201.png)
<div align="center">Crude Concept Sketches</div>
<br>

### Design Philosophy
Generally the design and development were modeled after the workflow of an FRC team, with a distinct Ideation and Brainstorming phase followed by the priliminary CAD designs. These CAD designs can further be grouped into stages: 
+ Master Sketches - 2D design of mechanisms, pivoting movement, and geometry relations
+ Subsystem design - Modeling the intital subsystems which make up the robot
+ Subsystem Assembly - Taking the modeled parts of each subsystem and assigning the movement relations between them to give the mechanism the proper degrees of freedom
+ Prototyping - Creating standalone versions of each system to prototype and test with
+ Modification - Changing various elements in mechanisms to adjust to prototype findings
+ Top Layer CAD - Putting all mechanisms together and making final changes
+ Top Layer Assembly - Taking all of the mechanisms and modeling all mechanical movement in the design
#### Standardization
Before the CAD stage, structural materials, fasteners, roller module materials, and COTS parts were agreed upon, standardizing the succeeding design in the CAD platform.
##### Structrual Materials
+ PLA was agreed to as the main prototyping and structural material, for it's quick speed, printability, cost, and finally the ability to print on bedslingers without an enclosure and the worry of very harmful VOCs when rapidly fabricating parts
+ PETG was agreed to as the material reserved for final iterations of internal shafts, gears, pulleys and other power transmission related parts. This was because it is less brittle and significantly more impact resistant. Additionally, these pieces are more  UV resistant, though these shouldn't be problems these pieces should have to face
+ TPU was used for both roller wheels and belts, because of it's flexibility, layer adhesion, and general ability for elastic deformation far beyond regular plastic's stress-strain curves
##### Fasteners
The standard bolt used for fastening of pieces was the M3 (3mm) bolt, allowing the use of standardized bolts, nuts, washers, spacers and heat-set inserts in the project. This helped with ordering a steamlined amount of pieces with less waste at the end of the project.
##### Belts and gears
While 3D Printed In-house using an FDM printer, pulley and belt designs came from standard HTD 5mm designs from the internet. For belts, the design of the belt was slightly adjusted to accomodate TPU by making the belt thinner.
##### COTS Parts
COTS (Commercial Off-The-Shelf) parts on the robot included bearings mainly. Originally, 1/8" Flanged 1/2" ID bearings were what was used on the CAD, but these were changed for 8mm ID 608 bearings to reduce the cost of the project.

### Drivebase

####    Ideation
It was agreed upon that to maximise manuverability, simplicity, and redundancy that the drivebase would consist of 6-wheel tank drive, driven by two independent motors, uptorqued via gearbox.

The powertrain was to be built with belts instead of expensive and heavy chains (traditionally the power transmission mechanism for FRC drivetrains) for their lack of backlash, and the lower power situation in comparison to FRC.


####    Research

##### Shafts
Before the project, it was decided to use circular shafts, mirroring the 608 bearing's internal profile. For maximum accuracy when 3D printing with an FDM printer, these designs were originally printed vertically, with the profile facing up/down. This made for tighter tolerances when assembling. During testing and initial part fabrication, the PLA 7.8mm shafts would snap often. The decision was made to print shafts horizontaly, so that the layer lines were perpendicular to the axes of stress. This strengthens the shaft across the thin cylinder [1]. Unfortunately, this reduced tolerances significantly. However, a solution was found: by cutting the design's top and bottom, the areas which had poor print quality could be removed, reducing print accuracy while keeping a majority of the strength gained through horazontal printing[2].

[1] Markforged, "3D Printing Settings Impacting Part Strength", 2026. 
https://markforged.com/resources/learn/design-for-additive-manufacturing-plastics-composites/understanding-3d-printing-strength/3d-printing-settings-impacting-part-strength

[2] Aaron Zhan, "Tutorial on Using Bearings in 3D Prints | Shafts & Shaft Collars," Youtube, 2026. https://www.youtube.com/watch?v=TsC96mXMejA&t=14s

####    Master Design
The beginning steps for each mechanism were the Master Sketches, determining the core geometry of the mechanisms. The first was the drivebase, determining the speed, size, and other structural factors.

It was decided on to use 3" wheels with a distance of aproximately 4.134" - the exact distance determined by the width needed to keep a 60T HTD 5mm belt taut. This would allow for a drivebase with a width of 13-16" comfortably, enough to store a sizable amount of rubbish. This length would be extended later to accomodate more storage.

![Master Sketch: Drivebase Image 1](Assets/Drivebase%20Mastersketch%20Image%201.png)

<div align="center">Drivebase Mastersketch</div>
<br>

####    CAD Process

####    Prototypes and Iterations


####    Finalized Design

### Intake

####    Ideation

####    Research

####    Master Design

The next step was to design the compliant intake, which was designed to be capable of expanding from 0.079" (2mm) of ground clearance up to roughly 3.6" when fully expanded. This expansion would be unpowered and mainly articulated by gravity, so the wheels would always have some level of contact with the object being intaked. Additionally, the intake has powered pivoting to either be in an active or stowed position. This reduces the wear on the intake, and takes the intake away from contract with the ground when not being used.

![Master Sketch: Intake Image 1](Assets/Intake%20Mastersketch%20Image%201.png)

<div align="center">Intake Mastersketch - highlighted circles model roller wheels in positions: active, active: compliant, stowed, stowed: compliant</div>


####    CAD Process

####    Prototypes and Iterations
![Intake Prototype and Mounting Gearbox](Assets/Intake%20Prototype%20Image%201.webp)
####    Finalized Design

### Indexer

####    Ideation

####    Research

####    Master Design
<br>

<br>
Indexer modeling required creating a belt in an area where it was deterimined that the trash would be able to move to and be picked up easily. It was also decided that to increase grip, additional blocks would be fastened to the belt to increase the pulling power of the belt conveyors.
<br>
<br>

![Master Sketch: Indexer Image 1](Assets/Indexer%20Mastersketch%20Image%201.png)

<div align="center">Indexer Mastersketch - Modeling the belt that takes trash from intake to hopper</div>
<br>

####    CAD Process

####    Prototypes and Iterations

####    Finalized Design

## Electronics

## Coding

###Future Upgrades

## Materials List

+ 3 770 DC Motors
+ 1 JGB 57 Motor with 90:1 gearbox
+ 7 kg PLA
+ 500g PETG
+ ___ M3 Heat Set Inserts
+ ___ M3 _mm Screws
+ ___ M3 _mm Screws
+ ___ M3 _mm Screws
+ ___ M3 _mm Screws
+ ___ M3 Washers
+ ___ M3 Nuts
+ ___ Male to Male Pin Connectors
## Contributors
