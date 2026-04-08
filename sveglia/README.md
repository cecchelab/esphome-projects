# sveglia

Sveglia da comodino con ESP32-C3, display SH1106 128x64 e buzzer piezo. Configurabile da Home Assistant, funziona in autonomia via NTP.

Articolo: [cecchelab.dev](https://cecchelab.dev/blog/2026-04-sveglia-01)

## Hardware

| Componente | Modello |
|---|---|
| MCU | ESP32-C3 Mini |
| Display | SH1106 128x64 I2C |
| Buzzer | Piezo passivo |
| Pulsante | Normalmente aperto, pullup interno |

| Funzione | GPIO |
|---|---|
| I2C SDA | GPIO6 |
| I2C SCL | GPIO7 |
| Buzzer PWM | GPIO10 |
| Pulsante stop | GPIO4 |

## Utilizzo

```bash
cp secrets.example.yaml secrets.yaml
# compila secrets.yaml con i tuoi dati
esphome run sveglia.yaml