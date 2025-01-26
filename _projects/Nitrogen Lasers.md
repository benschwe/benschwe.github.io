---
layout: page
title: A small TEA nitrogen laser
description: Investigations into transversely excited atmospheric nitrogen lasers - starting small
img: assets/img/nitrogen_laser/tea_laser_small.jpg
importance: 1
category: Nitrogen Lasers
related_publications: false
#permalink: /projects/nitrogen_lasers.md
---
## **Background**
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

## **Details**
The laser design is inspired by Leslie Wright, owner of the [Les' Lab YouTube channel](https://www.youtube.com/@LesLaboratory). The laser uses a charge transfer circuit to provide a short duration pulse of high voltage to the laser channel. The main capacitor (aka dumper capacitor) is an 800 pF Murata doorknob capacitor, and the foil peaker capacitor is ~430 pF. The peaker cap uses 0.002" brass foil and 0.010" polyethylene sheet. I found that the brass foil is much more mechanically robust than standard aluminum foil making assembly/disassembly easier during tuning.

Since the laser re-uses the power supply from the LSI laser, the high voltage is fixed at roughly 18 kV. TEA nitrogen lasers operate most efficently when the electric field to gas pressure ratio (E/P ratio) in the laser channel is between 100 - 200 V/(cm*Torr). The laser is design so that the gap between the electrodes in the laser channel is adjustable using M3 screws. During testing, the highest energy output was obtained with a gap of 1.55 mm, yielding an E/P ratio of 153 when run on pure nitrogen at 760 Torr (atmospheric pressure).

## **Performance**
The laser operates quite smoothly using the LSI power supply, and is firing rate is completely controllable thanks to the re-use of the triggered spark gap. Repetition rates up to 20 hz are possible. The glow discharge in the main laser channel is highly uniform and without large sparks, which has been noted in the literature as signs of high performance. Below are two shots of it in action.

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/nitrogen_laser/small_n2_laser_discharge.jpg" title="example image" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/nitrogen_laser/small_n2_laser_highlighter.jpg" title="example image" class="img-fluid rounded z-depth-1" zoomable=true%}
    </div>
</div>
<div class="caption">
    The laser in action. Long exposure shots of the main channel plasma discharge (left), and optical pumping of fluorescein highlighter ink in a quartz cuvette - without any focusing optics!
</div>