---
layout: page
title: A Small TEA Nitrogen Laser
description: Investigations into transversely excited atmospheric nitrogen lasers - starting small
img: assets/img/nitrogen_laser/tea_laser_small.jpg
importance: 1
category: Nitrogen Lasers
related_publications: false
#permalink: /projects/nitrogen_lasers.md
---
# Background
Built in 2022, this laser has an electrode length of 8.8 cm, and uses the power supply from an older LSI VSL-337 nitrogen laser purchased on eBay. Although the tube in the that laser no longer lased due to outgassing, the high voltage power supply, high voltage trigger circuit, and triggerable spark gap were repurposed to drive this laser. 

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/nitrogen_laser/small_laser_1.jpg" title="example image" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/nitrogen_laser/small_laser_2.jpg" title="example image" class="img-fluid rounded z-depth-1" zoomable=true%}
    </div>
</div>
<div class="caption">
    The end product, minus the power supply
</div>

## Version 1
The laser design is inspired by Leslie Wright, owner of the [Les' Lab YouTube channel](https://www.youtube.com/@LesLaboratory). The laser uses a charge transfer circuit to provide a short duration pulse of high voltage to the laser channel. The main capacitor (aka dumper capacitor) is an 800 pF Murata doorknob capacitor, and the foil peaker capacitor is ~430 pF. The peaker cap uses 0.002" brass foil and 0.010" polyethylene sheet for the dielectric. I found that the brass foil is much more mechanically robust than standard aluminum foil making assembly/disassembly easier during tuning.

Since the laser re-uses the power supply from the LSI laser, the high voltage is fixed at roughly 18 kV. TEA nitrogen lasers operate most efficently when the electric field to gas pressure ratio (E/P ratio) in the laser channel is between 100 - 200 V/(cm*Torr). The laser is designed so that the gap between the electrodes in the laser channel is adjustable using M3 screws. During testing, the highest energy output was obtained with a gap of 1.55 mm, yielding an E/P ratio of 153 when run on pure nitrogen at 760 Torr (atmospheric pressure).

### Version 1 - Performance
The laser operates smoothly using the LSI power supply, and the firing rate is completely controllable thanks to the re-use of the triggered spark gap and associated LSI analog control circuitry. Repetition rates up to 20 hz are possible. The glow discharge in the main laser channel is highly uniform and without large sparks, which has been noted in the literature as signs of high performance. The laser is capable of operation on either air or pure nitrogen fed in to the center of the laser channel. When operated on air, the output is roughly 20-25% of the energy compared to operation on a nitrogen feed. Below are two shots of it in action running on nitrogen.

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/nitrogen_laser/small_n2_laser_discharge.jpg" title="example image" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/nitrogen_laser/small_n2_laser_highlighter.jpg" title="example image" class="img-fluid rounded z-depth-1" zoomable=true%}
    </div>
</div>
<div class="caption">
    The laser in action. Long exposure shots of the main channel plasma discharge and optical pumping of fluorescein highlighter ink in a quartz cuvette - without any focusing optics!
</div>

The effect of electrode spacing on UV energy output was investigated by adjusting the laser channel gap to specific distances and measuring energy output with a pyroelectric energy sensor from XX, model YY. The figure below shows the measured laser pulse energy as a function of electrode spacing when operated on pure nitrogen. Note the maximum energy occuring with an electrode spacing of 1.55 mm, corresponding to an E/P ratio of 153 V/cm*Torr at 760 Torr atmospheric pressure.

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/nitrogen_laser/small_laser_energy_vs_electrode_spacing.png" title="example image" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>

Note the maximum energy of 34 uJ occuring with an electrode spacing of 1.55 mm, corresponding to an E/P ratio of 153 V/cm*Torr at 760 Torr atmospheric pressure.

### Version 1 - Construction
The base of the laser is a 1/4" thick piece of 6061 aluminum plate X inches square. The laser electrodes are hexagonal aluminum bar stock X" in major diameter. The electrode edges forming the laser channel are slightly rounded off at each end to reduce the electric field strength which would otherwise concentrate there and promote sparking. The electrically grounded electrode (nearest to the plate edge) is secured to the plate with 2 M3 screws to ensure a low impedance electrical path. The other electrode (high voltage one) sits atop the peaker capacitor foil, and is forced into contact with the foil from the pressure exerted by the Lexan plate above it. The Lexan plate is secured to the ground electrode with 2 M3 screws, which when tightened forces the Lexan plate down onto the high voltage electrode due the higher height of that electrode generated by the peaker capacitor foil and dielectric stackup. 

The high voltage electrode adjustment system is copied from Leslie Wright's design, and uses two M3 screws for adjustment along with 2 spring loaded M3 screws that tap into the high volage electrode and exert a counterforce to allow for electrode gap increase when the M3 adjustment screws are loosened. The electrode adjustment system is 3D printed from PETG and secured to the Lexan top cover with screws.

## Version 2 - Increasing the dumper capacitance
Laser output energy performance was improved by moving to a larger dumper capacitor, rated at 1300 pF. With the larger capacitance, the peak output energy was found to occur at a slightly larger electrode spacing of 2.2 mm. Additionally, the laser channel was re-made to include guide pins and thumbscrews, which allow for easy loosening of the high voltage electrode when adjusting the gap spacing. The foil peaker capacitor was also changes to 0.002" thick brass foil, which is substantially more robust than the previous aluminum foil used in V1.

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/nitrogen_laser/small_laser_v2_overview.jpg" title="example image" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/nitrogen_laser/small_laser_v2_guide-pins.jpg" title="example image" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/nitrogen_laser/small_laser_v2_guide-sleeves.jpg" title="example image" class="img-fluid rounded z-depth-1" zoomable=true%}
    </div>
</div>
<div class="caption">
    Details of the guide pins used to ensure consistent spacing between teardowns
</div>

### Version 2 - Performance
The plot below shows the output energy of the laser with the previous smaller 880 pF dumper capacitor, and the updated larger 1300 pF dumper capacitor. Note the overall shift of the energy towards larger electrode spacing with the 1300 pF dumper capcitor.

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/nitrogen_laser/small_laser_energy_vs_electrode_spacing 2.png" title="example image" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>

Peak output energy is a remarkable 89 uJ, or 55 kW assuming a 1.5 nS FWHM pulse duration! The laser is easily capable of pumping a cuvette dye cell to super-irradiance without the need for a focusing lens.

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/nitrogen_laser/small_laser_v2_dye_pumping.jpg" title="example image" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>