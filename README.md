# esphome-projects

This is a collection of home projects done with the wemos d1 mini, this includes fully working:
 - [weather (temp, humidity and air pressure) sensor](weather-sensor.md)
 - 433MHz doorbell sensor
 - smart light switches



# Installing / Configuring esphome


## Install Python 3

## Install a Wemos serial driver
May have to install a serial driver first, the WEMOS driver was already installed for me from previous, and things worked well 
https://www.wemos.cc/en/latest/ch340_driver.html

## Setup Python Virtual Environment and install 

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
esphome run wemosd1_doorbell_sensor.yaml
esphome run humidity-sensor.yaml
esphome run garage-light-switches.yaml

:: to view the logs of a firmware: 
esphome logs <file>.yaml



:: leave the venv
deactivate

```