<div align="center"><h1 style="font-family: courier;" align="center">satsha-ttl</h1></div>

<div align="center"><img src="media/satsha-ttl5.jpg" width="100%"></div>
<div align="center"><i>An open source & fabbable USB to serial converter board.</i></div>


satsha-ttl
--

After some time of buying expensive FDTI cables (about 20$ nowadays) and having the need to use several USB to serial converters for my **[Fab Academy](http://fabacademy.org/)** students, I developed my own fabbable solution. satsha-ttl features a **[CH340G USB to serial chip](https://cdn.sparkfun.com/datasheets/Dev/Arduino/Other/CH340DS1.PDF)** and it is designed to be cheap, reliable and easy to be reproduced. It uses an LDO voltage regulator and a **jumper to switch between 3.3V and 5V**, both for power and logic levels of TX/RX. The design of the satsha-ttl also allows to easily integrate it into existing boards requiring an USB communication without having a dedicated hardware implemented into the microcontroller (eg the 328p).

Here are the **features of the satsha-ttl:**

- **CH340G** USB to serial chip
- selectable voltage of **3.3V and 5V** (both for power and serial)
- **250mA** current on 3.3V
- **USB power** for 5V
- **CTS and DTR** pins
- **mini USB** connector
- **no drivers** needed for latest Windows/MacOS/Linux
- size of **45x28mm**
- cost **1.3€/1.6$** (buying the components from China, **[BOM](https://gitlab.fabcloud.org/satsha/satsha-ttl/raw/master/docs/satsha-ttl-BOM.xlsx)**)

satsha-ttl **PCB**:

<img src="media/pcb1.jpg" width="60%">

satsha-ttl **schematic**:

<img src="media/satsha-ttl-schematic.png" width="100%">

satsha-ttl **board**:

<img src="media/satsha-ttl-board.png" width="100%">

Downloads
--

**downloads (right click download as):**

- **[satsha-ttl schematic](https://github.com/satsha-utilities/satsha-ttl/raw/master/eagle/satsha-ttl/satsha-ttl.sch)**
- **[satsha-ttl board](https://github.com/satsha-utilities/satsha-ttl/raw/master/eagle/satsha-ttl/satsha-ttl.brd)**
- **[satsha-ttl internal traces png 0.1mm](https://github.com/satsha-utilities/satsha-ttl/raw/master/media/internal.png)**
- **[satsha-ttl cutout png 0.1mm](https://github.com/satsha-utilities/satsha-ttl/raw/master/media/cut.png)**
- **[satsha-ttl internal traces png 0.2mm](https://github.com/satsha-utilities/satsha-ttl/raw/master/media/internal_02.png)**
- **[satsha-ttl cutout png 0.2mm](https://github.com/satsha-utilities/satsha-ttl/raw/master/media/cut_02.png)**
- **[satsha-ttl BOM ods](https://github.com/satsha-utilities/satsha-ttl/raw/master/docs/satsha-ttl-BOM.ods)**
- **[satsha-ttl BOM xlsx](https://github.com/satsha-utilities/satsha-ttl/raw/master/docs/satsha-ttl-BOM.xlsx)**

Getting started with satsha-ttl
--
Before connecting satsha-ttl to your computer is really important to **check if the connections are ok**, as it could damage the USB port of our computer if they are wrong. A smoke test can also be done beforehand with an **USB hub or an USB power supply**.  Install the **drivers** for the CH340G if satsha-ttl is not recognized automatically from your OS. In case you are using Windows 8 or older, or older versions of MacOS/Linux download and install the **[drivers from here](https://sparks.gogo.co.nz/ch340.html)**. 

 Find below the **satsha-ttl pinout**:

<img src="media/satsha-ttl-pinout.png" width="70%">

satsha-ttl can be used to **supply power** to another microcontroller board, other than connecting the serial. In case of supplying power to another board make sure its voltage and current requirements matches the **selected voltage** on the satsha-ttl jumper and the **maximum current** the satsha-ttl/USB port can output. It is possible to use the satsha-ttl as a **programmer for AVR** microcontrollers with installed the Arduino bootloader, in this case the **DTR** is used **software reset** pin.

Here is an example scheme on how to connect **satsha-ttl to program a satshakit:**

<img src="media/satsha-ttl-programming.png" width="100%">

Media
--

satsha-ttl pictures:

<img src="media/satsha-ttl4.jpg" width="70%">

<img src="media/satsha-ttl3.jpg" width="70%">

<img src="media/satsha-ttl2.jpg" width="70%">


satsha-ttl connected with a satshakit:

<img src="media/satsha-ttl-conn.jpg" width="70%">

satsha-ttl 1 million lines gcode test:

<a href="http://www.youtube.com/watch?feature=player_embedded&v=dIH6fnEvGS4
" target="_blank"><img src="http://img.youtube.com/vi/dIH6fnEvGS4/0.jpg" 
alt="http://img.youtube.com/vi/dIH6fnEvGS4/0.jpg" width="240" height="180" border="10" /></a>

satsha-ttl 2 uploading to a satshakit using serial 5V:

<a href="http://www.youtube.com/watch?feature=player_embedded&v=kN5nttG7nbE
" target="_blank"><img src="http://img.youtube.com/vi/kN5nttG7nbE/0.jpg" 
alt="http://img.youtube.com/vi/kN5nttG7nbE/0.jpg" width="240" height="180" border="10" /></a>

satsha-ttl receiving data from software serial 3.3V:

<a href="http://www.youtube.com/watch?feature=player_embedded&v=gNB7xQKvWcM
" target="_blank"><img src="http://img.youtube.com/vi/gNB7xQKvWcM/0.jpg" 
alt="http://img.youtube.com/vi/gNB7xQKvWcM/0.jpg" width="240" height="180" border="10" /></a>

satsha-ttl streaming gcode to grbl satshakit @250000 bauds 5V:

<a href="http://www.youtube.com/watch?feature=player_embedded&v=7HWK96QzLX8
" target="_blank"><img src="http://img.youtube.com/vi/7HWK96QzLX8/0.jpg" 
alt="http://img.youtube.com/vi/7HWK96QzLX8/0.jpg" width="240" height="180" border="10" /></a>

Author
--

- Daniele Ingrassia

Contact
--
- **ingrassiada@gmail.com**
- **[linkedin](http://it.linkedin.com/in/danieleingrassia)**


Thanks
--
[Fablab Kamp-Lintfort](http://fablab.hochschule-rhein-waal.de/index.php/de/)<br />
Hochschule Rhein-Waal<br />
Friedrich-Heinrich-Allee 25, 47475 Kamp-Lintfort, Germany<br />
fablab@hochschule-rhein-waal.de

License
--
This work is licensed under the terms of Attribution-NonCommercial-ShareAlike 4.0 International ([CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)).

Disclaimer  
--

<div class="align-justify">
This hardware/software is provided "as is", and you use the hardware/software at your own risk. Under no circumstances shall any author be liable for direct, indirect, special, incidental, or consequential damages resulting from the use, misuse, or inability to use this hardware/software, even if the authors have been advised of the possibility of such damages.</div>
