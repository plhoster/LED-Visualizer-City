---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---

- Project by <a href="https://picoluetjens.github.io/">Pico Lütjens</a>
- Source Code is available <a href="https://github.com/PicoLuetjens/LED-Visualizer-City">here</a>

![Image](img/IMG_1522.jpg)

LED-Visualizer-City uses an Arduino Mega with a Spectrum-Module to adress around 600 LEDs in a long String that. In some places the LED String is cut off and rewired because of some rotational issues. Additionally at the end of the String there is a 8x8 LED-Wall that sits on top of the big Building an displays some live text. Audio input needs to be connected over a normal audio cable and the output after going through the module is also via normal audio cable which can be connected to a box for example.

![Image](img/IACX0778.JPG)

Even though Arduinos are incredibly fast, sending data to nearly 600 LEDs 60 times a second is a thing even an Arduino Mega can struggle with even though it is one of the fastest Arduinos out there. So i decided to adress the LEDs using two Arduinos because in some more complex modes you could notice a little response lag. Also the Source Code uses the FastLED-Library which is pretty much the fastest Library to adress LEDs that is available for Arduinos.

![Image](img/IESA8119.JPG)

I needed to add an additional Power supply input around every 150 LEDs because otherwise when just supplying Power from the normal input at the beginning of the LED-String the LEDs at the end would just not lit up at all since the electricity can not distribute evenly throughout the String. All the Power inputs are combined together again so that you just need to provide one Power supply to Power all of the Arduinos and all of the LEDs.

![Image](img/IMG_1649.jpg)

When there is not Audio input at all the Buildings will lit up in yellow, resembling Windows and the Streets will have red cars driving on them between the Buildings. When there is Audio input the whole city will switch to visualization mode.
There are a variaty of different modes to visualize which will be randomly cycled through. The Modes are:

- Visualize_seven_spectrum
- Visualize_seven_spectrum_Bereiche
- Scroller
- RainbowWithGlitter
- juggle
- Bereiche_layout1
- Bereiche_layout2
- Bereiche_layout3
- Bereiche_layout4
- Bereiche_layout5
- Fade_to_white
- Fade_to_black
- random_wipe
- wipe_von_beiden_seiten
- pulse_blink