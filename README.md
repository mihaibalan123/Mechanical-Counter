# Mechanical Counter

This project features a fully functional, 3D-printable mechanical counter, designed entirely in Autodesk Fusion 360. Inspired by classic odometers, the mechanism relies on a system of spur gears, a pawl, and an actuator to sequentially count inputs.

## Inspiration & Ideas

* [https://www.printables.com/model/718967-mechanical-counter](https://www.printables.com/model/718967-mechanical-counter)
* [https://www.youtube.com/watch?v=rjWfIiaOFR4](https://www.youtube.com/watch?v=rjWfIiaOFR4)

## How it Works

* **The Input:** The core mechanism is driven by a linear actuator. When pressed, it pushes a driving pawl that engages with the teeth of the unit gear, advancing it by one position.
* **The Transfer:** Once the unit gear completes a full rotation (reaching 9), a smaller transfer gear engages the next gear in line (the tens, and subsequently the hundreds), successfully incrementing the total count.

## Resources Used

To design, simulate, and document this mechanical counter, the following resources and tools were utilized:

* **CAD Software:** Autodesk Fusion 360 - Used for all 3D modeling, joint assembly, and motion study simulations.
* **Mechanical Inspiration:** Reference materials and diagrams of classic mechanical odometers and ratcheting mechanisms.
* **3D Printing / Slicing:** PrusaSlicer - Used for preparing and slicing the models for FDM 3D printing.

## Simulation & Kinematics

The Fusion 360 assembly includes fully configured **Motion Links** and a **Motion Study** to accurately visualize the mechanism's real-world behavior:
* The timeline is animated so that every 3 frames, the unit gear rotates exactly **36 degrees** (incrementing one number).
* Through the defined Motion Links, the gear ratios are mathematically constrained. The tens gear moves at a **1/10** ratio, and the hundreds gear moves at a **1/100** ratio relative to the unit gear's rotation, perfectly simulating the mechanical carry-over.

## Design for Manufacturing

The model has been optimized for FDM 3D printing. Clearances have been carefully considered, and key components—such as the pins, gear faces, and inner rotational holes—feature chamfers. This design choice mitigates the "elephant's foot" effect on the first printed layer, ensuring smooth assembly and frictionless rotation without the need for heavy post-processing.

## Hardware Requirements

While all structural parts and gears are entirely 3D printed, the mechanism requires one piece of external hardware to function perfectly:
* **1x Metal compression spring** (approx. 2.6mm diameter, 65mm height). This must be placed on the actuator shaft to push the driving mechanism back to its resting position after each press.

## Components List

Here is a detailed breakdown of all the 3D printed components required for this assembly, including the quantities needed:

* **Actuator (Slider) - [Qty: 1]** 
  The primary input mechanism. It slides vertically within the frame to drive the mechanism forward.
  <p align="center"><img src=".png/actuator.png" width="300" alt="Actuator"></p>

* **Driving Pawl (Piedica) - [Qty: 1]** 
  The ratcheting arm that interacts with the unit gear's teeth to advance it by one position per press.
  <p align="center"><img src=".png/piedica.png" width="300" alt="Pawl"></p>

* **Units Gear (Roata Unitati) - [Qty: 1]** 
  The first numerical wheel (0-9). It receives the direct input from the actuator's pawl.
  <p align="center"><img src=".png/roata_unitati.png" width="300" alt="Units Gear"></p>

* **Tens & Hundreds Gears (Roti Zeci & Sute) - [Qty: 2]** 
  The subsequent numerical wheels that are incrementally driven by the transfer gears to count higher digits.
  <p align="center"><img src=".png/roti_zeci_sute.png" width="300" alt="Tens and Hundreds Gears"></p>

* **Transfer Gear (Roata Mica / Pinion) - [Qty: 2]** 
  The small intermediate gear responsible for the carry-over mechanism. It automatically turns the next wheel when the previous one completes a full rotation.
  <p align="center"><img src=".png/roata_mica.png" width="300" alt="Transfer Gear"></p>

* **Main Shaft (Tija) - [Qty: 3]** 
  The central axis rod on which the main number gears freely rotate.
  <p align="center"><img src=".png/tija.png" width="300" alt="Shaft"></p>

* **Spacer (Distantier) - [Qty: 2]** 
  Placed on the shafts to ensure the gears maintain the correct distance and alignment from each other.
  <p align="center"><img src=".png/distantier.png" width="300" alt="Spacer"></p>

* **Pin - [Qty: 2]** 
  Small connectors used for securing and aligning the frame components together.
  <p align="center"><img src=".png/pin.png" width="300" alt="Pin"></p>

* **Display Window (Cadran Numere) - [Qty: 1]** 
  The cover panel that frames the numbers so the current count can be easily read.
  <p align="center"><img src=".png/cadran_numere.png" width="300" alt="Number Dial"></p>

* **Left Frame Panel (Rama Stanga) - [Qty: 1]** 
  The left-side structural wall of the housing, which also guides the actuator.
  <p align="center"><img src=".png/rama_stanga.png" width="300" alt="Left Frame"></p>

* **Right Frame Panel (Rama Dreapta) - [Qty: 1]** 
  The right-side structural wall of the housing.
  <p align="center"><img src=".png/rama_dreapta.png" width="300" alt="Right Frame"></p>

* **Front & Back Frame Panels (Rama Fata/Spate) - [Qty: 2]** 
  The structural plates that enclose and secure the entire mechanism from the front and rear.
  <p align="center"><img src=".png/rama_fata_spate.png" width="300" alt="Front and Back Frame"></p>

## Full Assembly Views

Below are several views of the fully assembled mechanical counter, showcasing how all the components fit and interact together:

<p align="center">
  <img src=".png/ansamblu1.png" width="600" alt="Assembly View 1"><br><br>
  <img src=".png/ansamblu2.png" width="600" alt="Assembly View 2"><br><br>
  <img src=".png/ansamblu3.png" width="600" alt="Assembly View 3"><br><br>
  <img src=".png/ansamblu4.png" width="600" alt="Assembly View 4"><br><br>
  <img src=".png/ansamblu5.png" width="600" alt="Assembly View 5">
</p>

## Functionality Showcase

To better illustrate how the mechanical counter operates, I have recorded a video showcasing its full functionality. The video demonstrates the Fusion 360 motion links in action, verifying the gear ratios and showing how the components are assembled to work together.

[![Mechanical Counter Functionality Showcase](https://img.youtube.com/vi/mkegou3ErKw/maxresdefault.jpg)](https://youtu.be/mkegou3ErKw)

*Click on the image above to watch the video demonstration, or [click here for the direct YouTube link](https://youtu.be/mkegou3ErKw).*

## Conclusion & Limitations

This project successfully demonstrates the design, simulation, and assembly of a 3D-printable mechanical counter. By utilizing Fusion 360's precise modeling and motion studies, combined with careful DfAM (Design for Additive Manufacturing) considerations, the resulting mechanism effectively replicates a classic odometer system using basic printed parts and a single metal spring. 

**Limitations: Manual Reset**
The primary limitation of this current iteration is the absence of an automatic or mechanical reset button. The counter is designed strictly for continuous upward incrementing. 

Because there is no dedicated reset lever, returning the counter to zero requires manual intervention:
* The user must physically lift and hold the actuator in its highest upward position. This ensures the driving pawl is disengaged from the gears.
* While holding the actuator up, the user must manually rotate each individual number gear by hand until the top display window perfectly aligns to read **"0, 0, 0"**.
