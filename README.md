# galletti-fm-esphome

## ITALIANO
Questo firmware ESPHome permette di integrare i ventilconvettori [Galletti FM](https://www.galletti.com/terminali-idronici/ventilconvettori-a-parete-alta/parete_alta_FM) in Home Assistant attraverso ESPHome Modbus e Wi-Fi.

Il firmware è stato provato e scritto per il seguente hardware, può comunque essere adattato ad altre schede di sviluppo compatibli ESP in base alle proprie esigenze e spazi (io li ho inserti nel ventilconvettore):
- D1 Mini NodeMcu ESP8266-12F
- TTL RS485

Per scrivere il firmware senza dover ripetere codice comune nel caso si debbano integrare più ventilconvettori è stata utilizzata la funzione ESPHome dei [package](https://esphome.io/components/packages/)

Link alla documentazione ESPHome [Modbus](https://esphome.io/components/modbus_controller/)

### Controlli implementati
- Accensione/Spegnimento
- Modalità (Raffreddamento - Deumidificazione - Ventilatore - Riscaldamento - Automatico)
- Velocità ventola (Auto - Bassa - Media - Alta)
- Angolo deflettore (1 - 2 - 3 - 4 - Auto)
- Temperatura desiderata (16C° - 30C°)

### Sensori implementati
- Manadata acqua fredda
- Temperatura impostata
- Temperatura stanza (sensore)
- Temperatura stanza (scheda principale)

### Configurazione
- Riavvio ESP

### Diagnostica
- Segnale Wi-Fi (dBm)

## INGLESE
This ESPHome firmware allows you to integrate  [Galletti FM](https://www.galletti.com/en/hydronic_indoor_units_446/high-wall_mounted-fan-coil-units/high_wall_FM-EN) fan coils into Home Assistant via ESPHome Modbus and Wi-Fi.

The firmware has been tested and written for the following hardware, but it can still be adapted to other ESP-compatible development boards according to your own needs and space (I inserted them into the fan coil):
- D1 Mini NodeMcu ESP8266-12F
- TTL RS485

To write the firmware without having to repeat common code in case multiple fan coil units need to be integrated, the ESPHome function for [packages](https://esphome.io/components/packages/) was used.

ESPHome [Modbus](https://esphome.io/components/modbus_controller/) documentation link.

## Implemented controls
- Turning On/Off
- Mode (Cooling - Dehumidification - Fan - Heating - Automatic)
- Fan speed (Auto - Low - Medium - High)
- Deflector angle (1 - 2 - 3 - 4 - Auto)
- Desired temperature (16C° - 30C°)

## Implemented sensors
- Cold water supply
- Set temperature
- Room temperature (sensor)
- Room temperature (main PCB)

## Configuration
- ESP restart

## Diagnostics
- Wi-Fi Signal (dBm)
