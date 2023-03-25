# CPOSC 2023: Open House - Open Source Home Automation

## About

This repository contains the information and details related to
the CPOSC 2023 talk:

**Open House - Open Source Home Automation**

This talk is targeted at beginners and hardcore PCB-making home-lab audiences alike,
aimed to provide a high-level overview of the existing ecosystem which can be
used to safely, easily, and securely manage your home Internet-of-Things devices.
The talk will focus on Home Assistant, a free and open source home automation
platform, and how it is possible to create useful, seamless and complex home automations.


This code is hosted on both [GitHub](https://github.com/tomswartz07/CPOSC2023)
and [GitLab](https://gitlab.com/tom.swartz07/CPOSC2023).

## Learning Objectives

The ideal audience member is someone who is interested in using Home Automation,
has the desire to centrally manage multiple vendor's product, or is interested
in making their own home sensors.

The talk covers a number of topics and common issues observed by those who
use Internet-of-Things devices, such as:

- Central management of multiple devices/platforms
- Physical and Digital Security Concerns
- Creation of your own, custom sensor devices

## Session Outline
- Introduction
  - Brief explanation on current state of various IoT platforms
  - Overview of software stack
- HomeAssistant and Friends
  - Overview of Home Assistant
  - Architecture and Design of Home Assistant
  - Overview of ESPHome
- Integration with existing Internet-of-Things devices and Services
  - Various Device Integrations
  - Making certain locked-down devices even better
  - Integration with External Services
- Security Discussion
  - Network Security
  - Physical Security
- Making Custom Sensors
  - Custom Temperature Sensors
  - Printing Custom PCBs
  - Integration with ESPHome and HomeAssistant

## Expectations for Attendees

Attendees will gain knowledge necessary to install/deploy Home Assistant and other
associated tools, learn how to integrate it with existing IoT devices, and finally
have a brief look at the (insignificant) level of effort necessary to create their
own IoT sensors.

## Files in this Repository:

- `presentation/cposc2023.tex`: LaTeX Beamer presentation files

## Making the presentation

### Option 1: Docker
Assuming you have Docker installed, you can simply run the following:

```sh
cd presentation
docker build -t latex:latest .
make
```

### Option 2: Direct LaTeX
Assuming you have `pdflatex` installed, or TeXLive
simply run the following command:

```sh
cd presentation
pdflatex cposc2023.tex
```

The PDF document will be generated and viewable for you.


## External Resources

There are a number of projects and external resources which were referenced in this
presentation.
They can be found here:

- [Home Assistant](https://www.home-assistant.io/)
- [ESPHome](https://www.esphome.io/)
