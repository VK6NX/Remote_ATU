<!--
***
***
***
*** 
*** readme template created from https://github.com/othneildrew/Best-README-Template
-->


<!-- PROJECT LOGO -->
<br />

  <h3 align="center">Remote ATU T-match</h3>
  <p align="center">  

  <p align="center">
    T-match remote ATU based on ESP32 / ADS1115 / AD8310 with TCI (ESDR) integration and MQTT control. <br />
    ATU Hardware version 0.05<br />
    <br />
    <a href="https://github.com/VK6NX/Remote_ATU/issues">Report Bug</a>
    ·
    <a href="https://github.com/VK6NX/Remote_ATU/issues">Request Feature</a>
    ·
    <a href="https://vk6nx.net/RATU_T_v0.5-en.html" target="_blank">Project Home</a>
  </p>
</p>
  

<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary><h2 style="display: inline-block">Table of Contents</h2></summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
      </ul>
    </li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgements">Acknowledgements</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

Remote ATU can be used either in remote mode (mounted on mast directly connected to Antenna input) or in common mode (at transceiver end).<br />

###  Features highlights
* Capability of T-match and 2x L-match configurations within same device. It either operates in classic T-match C1-L-C2 mode, or C1-L, or L-C2 mode.
* Multi-algorithm: each described above mode operates via two different tuning algorithms.
* From 0.01W to 200W tuning power and from 0.01W to 2KW operational power. 
* Unlimited ATU type presets and Antenna presets (unlimited).
* "Follow VFO" function (TCI-based) allows automated selection of antenna preset while moving the operational frequency.
* Automated tuning mode and Manual tuning mode.
* WiFi (primaty communication media) and CAN wire (in development).
* 5V operations.

More detais please see at <a href="https://vk6nx.net/RATU_T_v0.5-en.html" target="_blank">Project Home</a><br />

####  Changes in current hardware verisoon
** CAN bus module embeddeed (software development is in progress).<br />
** ESP32D (30-pin) and ESP32U (38-pin) dev boards are supported. 

<!-- GETTING STARTED -->
## Getting Started

To get a project running in your environment follow these simple steps:
1. Read [Project description](https://vk6nx.net/RATU_T_v0.5-en.html) to understand the components, requirements and to map the expectations.
2. Download and install [MQTT](https://mosquitto.org/) for your OS.
3. Download [TCI-MQTT-Gateway](https://github.com/dkaukov/tci-mqtt-gateway/releases/tag/v.0.1) for your OS.
4. Download [ESP32 firmware](https://github.com/dkaukov/ratu-v2-esp32-firmware). Make sure you understand and verify supported platforms. Please note that ESP32 firmware is currently mapped to ATU HW version 0.4. There are minimaladjustments required to remap is to HW version 0.5. Either remap it yourself or requiest update via Issues. 
5. Download [ATUconnect for macOS](https://mega.nz/file/yBx13K5Y#tBbAfUoyLWk4kNJXm96MKQzaUcxuMHGairCRVFzlkgs) (tested on 10.15.7) or [ATUconnect for Windows](https://mega.nz/file/vAgyDBAS#2wv1d2AfN-vfjV7i0eCdowJ2e-1jZt2NGiQugIcPx9M) (tested on Win10 x64). 
***Please note that at this stage Windows application is supplied as standalone folder. To use it unzip and run .exe file from the folder. 

### Prerequisites

* SunSDR2, SunSDR2 Pro or SunSDR DX
* ATU 8x8x8 based on printed boards as described in [Project home](https://vk6nx.net/RATU_T_v0.5-en.html).

### Using project with binaries 
if you are going to use pre-build binaries, then the only needed tools will be any IDE which can handle loading ESP32 firmware. For this project it is recommended to use Visual Studio Code (either OS) with PlatformIO to load firmware to ESP32. All nesessary libraries are linked in ini file.

MQTT, TCI-MQTT-Gateway and ATUconnect are recommended to run on a same PC with ESDR2/3.

At this stage MQTT can be configured only in non-login mode. Use vendor installation guide to pre-configure MQTT, before running first time. The login/pass option will be activated in later releases of ATUconnect.

Run ESDR, MQTT, TCI-MQTT-Gateway - those will not require any additional configuration.
Run ATUconnect and configure MQTT, ATU1 and Antenna1. Make sure ATU1 name is matching ESP32 name.   

### Using project with build from source 
<b>If you are going to be using source codes</b>, the obvious set of tools will be required, such as
* git
* node.js
* npm
* VSC
* PlatformIO

Dependend on the OS and environment you may also need Python, Perl, Xcode and other tools.

<!-- ROADMAP -->
## Roadmap

See the [open issues](https://github.com/VK6NX/Remote_ATU/issues) for a list of proposed features (and known issues).

<!-- LICENSE -->
## License

Distributed under the [`BSD LICENSE`][license-url].

<!-- CONTACT -->
## Contact

Use [QRZ.com](https://www.qrz.com/) contact details.
Alternatively you may ask questions in the following thread at [EE forum ](https://eesdr.com/en/forum-en/remote-control/8674-remote-atu-w-tci)


<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements
* [TCI protocol](https://github.com/maksimus1210/TCI)
* [ESP32 Firmware V2](https://github.com/dkaukov/ratu-v2-esp32-firmware)
* [TCI-MQTT Gateway](https://github.com/dkaukov/tci-mqtt-gateway/releases/tag/v.0.1)
* [Tandem calibration Tool](https://github.com/dkaukov/log-power-meter)
* [Eclipse Mosquitto](https://mosquitto.org/)
* [Best-README-Template](https://github.com/othneildrew/Best-README-Template)

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[license-url]: https://github.com/VK6NX/Remote_ATU/blob/main/LICENSE.txt
