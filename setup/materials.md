---
layout: page
title: Materials
---

# Bill of Materials

This document provides an overview of the hardware components and approximate costs for different configurations of the Local Community Network (LCN), based on actual project implementation.


## Core Setup 
This setup includes no solar power and no wind sensors.

| Component                  | Price (€) | Price (FCFA) | Shop / Link |
|---------------------------|----------|-------------|-------------|
| Raspberry Pi 5 (incl. SD) | 184.90    | ~83,900     | https://www.rasppishop.de/Raspberry-Pi-5-mit-8-GB-RAM |
| Cooling (fan)             | 5.55     | ~4,100      | https://www.reichelt.de/de/de/shop/produkt/raspberry_pi_-_luefter_fuer_raspberry_pi_5-360116 |
| Wi-Fi Adapter / Antenna   | 19.95    | ~13,100     | https://www.reichelt.de/de/de/shop/produkt/wlan-adapter_usb_1300_mbit_s-279758 |
| RTC Battery               | 4.8      | ~3,100      | https://www.reichelt.de/de/de/shop/produkt/raspberry_pi_-_rtc_batterie_fuer_raspberry_pi_5-360117 |
| USB-C Cable (90°)         | 4.0      | ~2,600      | https://www.amazon.de/Rechtwinklige-Stecker-Stromkabel-installiert-Reparatur/dp/B0D8PBBHS6 |
| teleAgriCulture Board     | ~30.00     | ~65,600     | https://teleagriculture.org/ |
| Display (1.8” TFT)        | 4.95     | ~3,200      | https://www.ebay.de/itm/389456784599 |
| BME280 Sensor             | 19.94    | ~13,100     | https://eckstein-shop.de/Adafruit-BME280-I2C-or-SPI-Temperature-Humidity-Pressure-Sensor |
| Multigas Sensor V2        | 27.3     | ~17,900     | https://www.reichelt.de/de/de/shop/produkt/arduino_-_gassensor_v2_mehrkanal-328573 |
| DHT22 Sensor              | 11.89     | ~6,200      | https://eckstein-shop.de/WaveShare-DHT22-Temperature-Humidity-Sensor-for-Raspberry-Pi-Arduino |
| 3D Filament (Enclosure)   | ~17      | ~11,200     | https://www.reichelt.de/de/de/shop/produkt/filament_abs_natural_weiss_1_75_mm_750_g-420023 |
| Mounting hardware         | ~25      | ~16,400     | — |

**Estimated Cost:** ~350–380 € (~230,000 – 250,000 FCFA)
*Prices in FCFA are approximate (1 € ≈ 655 FCFA). Local sourcing may differ.*

## Solar Power Add-on
This setup enables off-grid operation of the Local Community Network using solar energy.

| Component                      | Price (€) | Price (FCFA) | Shop / Link |
|-------------------------------|----------|-------------|-------------|
| Solar Panel (30W, 18V)        | ~6.15    | ~4,030      | — |
| Battery (12V 24Ah)            | ~46.15   | ~30,200     | — |
| Charge Controller (PWM)       | ~12.31   | ~8,060      | — |
| Voltage Regulator (12V → 5V)  | 14.99    | ~9,820      | https://www.amazon.de/Zorblix-Spannungs-wandler-spannungsregler-einstellbar-Spannungs-stabilisator/dp/B0FNWMCZKM |
| Solar Cables                  | ~12.31   | ~8,060      | — |
| Mounting / installation       | ~20      | ~13,100     | — |

**Estimated Add-on Cost:** ~110–120 € (~73,000 – 80,000 FCFA)

## Wind Measurement Add-on
This setup adds wind sensing capabilities to the Local Community Network, enabling the measurement of wind speed and direction as part of environmental monitoring

| Component                      | Price (€) | Price (FCFA) | Shop / Link |
|-------------------------------|----------|-------------|-------------|
| Wind Direction & Speed Kit    | 105.50   | ~69,100     | https://botland.de/wetterstationen/16258-wetterstation-mit-windrichtungs-und-geschwindigkeitsmessung-sparkfun-sen-15901-845156010141.html |
| Additional connectors         | ~5       | ~3,300      | — 

**Estimated Add-on Cost:** ~110 € (~72,000 FCFA


## Lightweight Setup (Raspberry Pi 4 – No LLM)
This setup uses a Raspberry Pi 4 and does not support local LLM functionality. It is designed for reduced cost, lower power consumption, and more lightweight deployments.

| Component                  | Price (€) | Price (FCFA) | Shop / Link |
|---------------------------|----------|-------------|-------------|
| Raspberry Pi 4 (2GB)      | 57.90    | ~37,900     | https://www.rasppishop.de/Raspberry-Pi-4-Modell-B-2GB-SDRAM |
| SD Card (32 GB)           | 6.14     | ~4,020      | https://www.rasppishop.de/Sandisk-32-GB-Noobs |
| Cooling (fan)             | 9.99     | ~6,550      | https://www.reichelt.de/de/de/shop/produkt/raspberry_pi_-_luefter_fuer_compute_module_4-364272 |
| Power Supply              | 12.00    | ~7,860      | https://www.reichelt.de/de/de/shop/produkt/raspberry_pi_netzteil_usb_c_27w_weiss-360118 |
| Wi-Fi Adapter / Antenna   | 19.95    | ~13,070     | https://www.reichelt.de/de/de/shop/produkt/wlan-adapter_usb_1300_mbit_s-279758 |
| RTC Battery               | 4.80     | ~3,140      | https://www.reichelt.de/de/de/shop/produkt/raspberry_pi_-_rtc_batterie_fuer_raspberry_pi_5-360117 |
| teleAgriCulture Board     | 30.00    | ~19,650     | https://teleagriculture.org/ |
| Display (1.8” TFT)        | 4.95     | ~3,250      | https://www.ebay.de/itm/389456784599 |
| BME280 Sensor             | 19.94    | ~13,060     | https://eckstein-shop.de/Adafruit-BME280-I2C-or-SPI-Temperature-Humidity-Pressure-Sensor |
| Multigas Sensor V2        | 27.30    | ~17,880     | https://www.reichelt.de/de/de/shop/produkt/arduino_-_gassensor_v2_mehrkanal-328573 |
| DHT22 Sensor              | 11.89    | ~7,780      | https://eckstein-shop.de/WaveShare-DHT22-Temperature-Humidity-Sensor-for-Raspberry-Pi-Arduino |
| 3D Filament (ABS)         | ~17.00   | ~11,130     | https://www.reichelt.de/de/de/shop/produkt/filament_abs_natural_weiss_1_75_mm_750_g-420023 |
| Mounting hardware         | ~25.00   | ~16,380     | — |

**Estimated Cost:** ~247 € (~162,000 FCFA)



