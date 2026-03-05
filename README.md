# galletti-fm-esphome
## Italiano
Questo firmware ESPHome permette di integrare i ventilconvettori Galletti FM in Home Assistant attraverso ESPHome Modbus e WiFi
Il firmware è stato provato e scritto per il seguente hardware, può comunque essere adattato ad altre schede di sviluppo compatibli ESP in base alle proprie esigenze e spazi (io li ho inserti nel ventilconvettore)
- D1 Mini NodeMcu ESP8266-12F
- TTL RS485

Per scrivere il firmware senza dover ripetere codice comune nel caso si debbano integrare più ventilconvettori è stata utilizzata la caratteristica di ESPHome di utilizzare i package

Link alla documentazione ESPHome Modbus [https://esphome.io/components/text_sensor/modbus_controller](https://esphome.io/components/modbus_controller/)

### Controlli implementati
- Accensione/Spegnimento
- Modalità (Raffreddamento - Deumidificazione - Ventilatore - Riscaldamento - Automatico)
- Velocità ventola (Auto - Bassa - Media - Alta)
- Angolo deflettore (1 - 2 - 3 - 4 - Auto - Stop) N.B.: verificare se possibile integrarlo
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
