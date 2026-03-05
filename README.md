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

# Instruzioni per l'utilizzo del codice
1. Nella directory esphome (homeassistant/esphome) creare le directory hardware e common
2. Copiare nella directory common i file wifi.yaml e modbus_galletti.yaml
3. Copiare nella directory hardware il file d1_mini_galletti_fm.yaml
4. Editare il file secrets.yaml di esphome (utilizzare un editor o direttamente da ESPHome Builder) per aggiungere wifi_ssid e wifi_password oltre alle password OTA ed AP, se si utilizza la configurazione IP Statico (consigliata) inserire anche i dati della rete (net_subnet per la sunbet, net_gtw per il gateway, net_dns1 per il primo DNS net_dns2 per il secondo DNS)
5. Creare un nuovo device con ESPHome Builder
6. Utilizzare il file fancoil-galletti-fm.yaml per popolare il proprio file .yaml, il file deve essere personalizzato impostando
   - fc_name
   - fc_friendly_name
   - fc_comment
   sostituire <REDACT> con la key api fornita in fase di creazione del device con ESPHome Builder
   sostituire le variabili subito dopo !secret per OTA, configurazione rete ed AP

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

# Instructions for using the code
1. In the esphome directory (homeassistant/esphome) create the directories hardware and common
2. Copy the files wifi.yaml and modbus_galletti.yaml into the common directory
3. Copy the file d1_mini_galletti_fm.yaml into the hardware directory
4. Edit the esphome secrets.yaml file (using an editor or directly from ESPHome Builder) to add wifi_ssid and wifi_password along with the OTA and AP passwords; if using a Static IP configuration (recommended), also enter the network data (net_subnet for the subnet, net_gtw for the gateway, net_dns1 for the first DNS, net_dns2 for the second DNS).
5. Create a new device with ESPHome Builder
6. Use the file fancoil-galletti-fm.yaml to populate your own .yaml file, the file must be customized by setting
   - fc_name
   - fc_friendly_name
   - fc_comment
   replace <REDACT> with the api key provided during the device creation phase with ESPHome Builder 
   replace the variables immediately after !secret for OTA, network configuration, and AP
