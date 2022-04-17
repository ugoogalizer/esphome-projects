# esphome-projects

This is a collection of home projects done with the wemos d1 mini, this includes fully working:
 - [weather (temp, humidity and air pressure) sensor](weather-sensor.md)
 - [433MHz doorbell sensor](doorbell-sensor.md)
 - smart light switches



# Installing / Configuring esphome

## Pre-reqs
- You will require an existing installation of Home Assistant
- These steps presume you're running a Windows desktop environment

## Install Python 3
I used Python 3.9, but I presume any v3.x works.  [Download here](https://www.python.org/downloads/)

## Install a Wemos serial driver
You will likely have to install a serial driver to communicate with the WEMOS, this one worked well:
https://www.wemos.cc/en/latest/ch340_driver.html

## Setup Python Virtual Environment and install 
Plug your wemos into your Windows desktop, and run the following to upload the firmware the first time. After that (so long as you statically define the IP address) you can upload new firmware Over The Air (OTA) so long as it's on the network

``` cmd
set ESPHOME_PATH=D:\OneDrive\Coding\esphome-projects

:: Create venv:
Py -m venv %ESPHOME_PATH%

:: run and update venv:
D:
Cd %ESPHOME_PATH%
%ESPHOME_PATH%\Scripts\activate.bat
python.exe -m pip install --upgrade pip
pip install --upgrade esphome

:: To install or update an esphome firmware:
esphome run <file>.yaml

  :: for example:
  esphome run doorbell-sensor.yaml
  esphome run weather-sensor.yaml
  esphome run garage-light-switches.yaml

:: to view the logs of a firmware: 
esphome logs <file>.yaml

  :: for example:
  esphome logs doorbell-sensor.yaml
  esphome logs weather-sensor.yaml
  esphome logs garage-light-switches.yaml

:: leave the venv
deactivate

```