---
layout: project
type: project
image: images/projects/volume_slider.jpg
title: 3D Printed Volume Slider
permalink: projects/volume-slider-1
# All dates must be YYYY-MM-DD format!
date: 2021-06-27
labels:
  - C/C++
  - Embeded
  - Arduino
  - 3D Printing
summary: Physical volume slider to control the Windows Audio Mixer
---


{::options parse_block_html="true" /}

<!-- <img class="ui image centered inline" src="{{ page.image }}" style="max-width: 256px"> -->


<!-- ![Image of the Sliders](/{{ page.image }})
{: .ui .image .centered .inline style="max-width: 256px"} -->

<p>
  <img class="ui image" src="/{{ page.image }}" style="max-width: 300px; float: left; margin-right: 1em;me">

  This project was created to improve audio control within Windows.
  This provides the ability to change various audio levels without digging into the sound settings each time. It improves productivity by reducing distractions and interruptions.
</p>

<br>
<br>
<br>


<!-- <div> -->
This project consists of three main parts.

<br>
<br>

Windows Software
----------------

The software consists of the Open Source project called <a href="https://github.com/omriharel/deej">Deej</a>.
Deej takes data from a serial port and applies the desired volume levels to the selected audio devices. You can change the volume globally, per device, or per program using the executable name.
With my limited experience using the <a href="https://golang.org/">Go</a> language, I was able to modify the program and compile my own build. I added some debugging functionality to better aid in writing the firmware.


Microcontroller firmware
------------------------

Each slider is represented as an object that knows when itself has changed.
On each update, the program will loop through an array of sliders and if any of them have changed, it will send the new values through serial to Deej.
The serial data is represented as values separated by the pipe character like so: __"0..1024|0..1024|...".__
Currently, the sliders firmware has been merged with my [Custom Keypad](/projects/custom-keypad-1) project.


3D Printed Enclosure
--------------------

The enclosure is a simple design to allow for rapid prototyping of the hardware. The lid consists of two M2 screws per slider and sits snugly on top of the base.
The base is hollow with a cutout hole for cables.
The enclosure is 3D printed out of marble PLA on my custom Ender 5.
<!-- </div> -->
