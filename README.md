# ESPHome OpenTherm

This is an example of a integration with a OpenTherm boiler using ESPHome and the Ihor Melnyk or DIYLESS OpenTherm Adapter
Based on rsciriano. Fon Bosch Gaz 6000 WBN 24H

Add Error code.

Installation
Copy the content of this repository to your ESPHome folder
Make sure the pin numbers are right, check the file opentherm_component.h in the esphome-opentherm folder.

Edit the opentherm.yaml file:
Make sure the board and device settings are correct for your device
Set the sensor "entity_id: sensor.temp_k2"  with the home temperature sensor's name from Home Assistant. (The ESPHome sensor name is temperature_sensor).
Change address for you dallas temperature sensor
sensor:
  - platform: dallas
    name: "temperature_kot"
    address: "0x073C01D607EA1628"

Flash the ESP and configure in Home Assistant. It should be auto-discovered by the ESPHome Integration.

