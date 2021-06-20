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
    Hardware version 1.06<br />
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
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
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
     

### Built With

* [Qt](https://www.qt.io/)
* [PlatformIO](https://platformio.org/)

<!-- GETTING STARTED -->
## Getting Started

To get a project running in your environment follow these simple steps:
1. Read [Project description](https://vk6nx.net/RATU_T_v0.5-en.html) to understand the components, requirements and to map the expectations.
2. Download and install [MQTT](https://mosquitto.org/) for your OS.
3. Download [TCI-MQTT-Gateway](https://github.com/dkaukov/tci-mqtt-gateway/releases/tag/v.0.1) for your OS.
4. Download [ESP32 firmware](https://github.com/dkaukov/ratu-v2-esp32-firmware). Make sure you understand and verify supported platforms. Please note that ESP32 firmware is currently mapped to ATU HW version 0.4. There are minimaladjustments required to remap is to HW version 0.5. Either remap it yourself or requiest update via Issues. 
5. Download [ATUconnect for Windows](https://mega.nz/file/rZ52UKoS#Yd4YlUi8J-FDt0VwyPb2aQxXN920G49z77tg9XmMaF0) or [ATUconnect for macOS]()

### Prerequisites

* SunSDR2, SunSDR2 Pro or SunSDR DX
* ATU 8x8x8 based on printed boards as described in [Project home](https://vk6nx.net/RATU_T_v0.5-en.html).

<b>if you are going to use pre-build binaries</b>, then the only needed tools will be any IDE which can handle loading ESP32 firmware. For this project it is recommended to use Visual Studio Code (either OS) with PlatformIO to load firmware to ESP32. All nesessary libraries are linked in ini file.

<b>If you are going to be using source codes</b>, the obvious set of tools will be required, such as
* git
* node.js
* npm
* VSC
* PlatformIO

Dependend on the OS and environment you may also need Python, Perl, Xcode and other tools.

### Installation

1. Clone the repo
   ```sh
   git clone https://github.com/github_username/repo_name.git
   ```
2. Install NPM packages
   ```sh
   npm install
   ```



<!-- USAGE EXAMPLES -->
## Usage

Use this space to show useful examples of how a project can be used. Additional screenshots, code examples and demos work well in this space. You may also link to more resources.

_For more examples, please refer to the [Documentation](https://example.com)_



<!-- ROADMAP -->
## Roadmap

See the [open issues](https://github.com/github_username/repo_name/issues) for a list of proposed features (and known issues).



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request



<!-- LICENSE -->
## License

Distributed under the [`BSD LICENSE`][license-url].



<!-- CONTACT -->
## Contact

Your Name - [@twitter_handle](https://twitter.com/twitter_handle) - email

Project Link: [https://github.com/github_username/repo_name](https://github.com/github_username/repo_name)



<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements
* [TCI protocol](https://github.com/maksimus1210/TCI)
* [ESP32 Firmware V0.8](https://github.com/VK6NX/RemoteATU-T-match/tree/main/ATU_universal_v0.8.6)
* [ESP32 Firmware V2](https://github.com/dkaukov/ratu-v2-esp32-firmware)
* [TCI-MQTT Gateway](https://github.com/dkaukov/tci-mqtt-gateway/releases/tag/v.0.1)
* [Tandem calibration Tool](https://github.com/dkaukov/log-power-meter)
* [Eclipse Mosquitto](https://mosquitto.org/)
* [Best-README-Template](https://github.com/othneildrew/Best-README-Template)




<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/github_username/repo.svg?style=for-the-badge
[contributors-url]: https://github.com/github_username/repo/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/github_username/repo.svg?style=for-the-badge
[forks-url]: https://github.com/github_username/repo/network/members
[stars-shield]: https://img.shields.io/github/stars/github_username/repo.svg?style=for-the-badge
[stars-url]: https://github.com/github_username/repo/stargazers
[issues-shield]: https://img.shields.io/github/issues/github_username/repo.svg?style=for-the-badge
[issues-url]: https://github.com/github_username/repo/issues
[license-shield]: https://img.shields.io/github/license/github_username/repo.svg?style=for-the-badge
[license-url]: https://github.com/VK6NX/Remote_ATU/blob/main/LICENSE.txt
