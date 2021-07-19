---
layout: project
type: project
image: images/projects/custom_keypad.jpg
title: Custom Keypad Prototype
permalink: projects/custom-keypad-1
# All dates must be YYYY-MM-DD format!
date: 2021-06-28
labels:
  - C/C++
  - Embeded
  - Arduino
  - 3D Printing
  - Keyboard
summary: 3x3 custom keypad
---


{::options parse_block_html="true" /}

<!-- <img class="ui image centered inline" src="{{ page.image }}" style="max-width: 256px"> -->


<!-- ![Image of the Keypad Prototype](/{{ page.image }})
{: .ui .image .centered .inline style="max-width: 256px"} -->

<p>
	<img class="ui image" src="/{{ page.image }}" style="max-width: 300px; float: left; margin-right: 1em;">

  When building a project like this, typically [QMK](https://qmk.fm/) is used. QMK is a powerful keyboard firmware that allows many people from around the world to build whatever kind of funky keyboard their hearts desire.
	It's open source and there are endless projects to start. However, I wanted to make mine from the ground up -- partially as a challenge and an exercise to learn C++ better.
</p>



Microcontroller firmware
------------------------
This firmware was designed to provide only what is required. The features include key repetition, full keystroke emulation, and auto numlock.
While commonly desired, N-Key rollover or modifier keys were not required or necessary for this project.

The keystrokes are modelled after a series of physical key presses using a linked list. If you wanted a key to open task manager, the keystroke definition would then look like so:
```c++
(new Keystroke(KEY_LEFT_CTRL))->with(KEY_LEFT_SHIFT)->with(KEY_ESC)
```

This project challenged me to dive deeper into C++ gaining a better understanding of pointer arithmetic, references, and linked lists.



3D Printed Enclosure
--------------------

Not only is the enclosure 3D printed, but the keycaps themselves are also 3D printed!

For the design, I decided to go with integrating the key plate into the enclosure itself. This makes the number of pieces needed to print smaller and allows for more rapid prototyping of key types.

The base design looks like a table top; the bottom is open and there are gaps on the lower half of each side to form "legs".
For my next design, I want to include more keys and integrate the audio control from my [Sliders](/projects/volume-slider-1) Project.
I also want to experiment with artificially increasing the weight of the prototype using lead beads or metal infused 3D printing filament.
