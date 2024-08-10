ltspice-lm2596-buck-converter
=============================
![](./circuit.jpg)
### Docs
- [LM2596 data sheet, product information and support | TI.com](https://www.ti.com/product/LM2596)
- [LM-2596 DC-DC 降壓模組 ( 帶數字顯示 )](https://github.com/dirkarnez/ltspice-lm2596-buck-converter/blob/main/docs/2430000010453.pdf)
  - From https://jin-hua.com.tw/upload/product/2430000010453.pdf
 
### Tutorials
- [matthiasdittmer/diy_bench_power_supply_lm2596: A DIY two channel bench power supply based on Texas Instruments LM2596](https://github.com/matthiasdittmer/diy_bench_power_supply_lm2596)
  - [diy_power_supply_lm2596 - EasyEDA open source hardware lab](https://oshwlab.com/matthiasdittmer/diy_power_supply_lm2596)

### Poe
```
To step down a regulated 12V supply to 5V using a buck converter, here are the recommended component values:

**Inductor Value:**
The inductor value for a buck converter is typically calculated using the following formula:

`L = (Vin * (Vout - Vin)) / (Vin * Iout * f)`

Where:
- `Vin` is the input voltage (12V)
- `Vout` is the output voltage (5V)
- `Iout` is the maximum output current
- `f` is the switching frequency of the buck converter

Assuming a maximum output current of 2A and a switching frequency of 200 kHz, the inductor value would be:

`L = (12 * (5 - 12)) / (12 * 2 * 200000) = 22 μH`

**Capacitor Value:**
The output capacitor value is typically calculated using the following formula:

`C = (Iout * D) / (Vout * ΔV * f)`

Where:
- `Iout` is the maximum output current
- `D` is the duty cycle (Vout / Vin)
- `Vout` is the output voltage
- `ΔV` is the maximum allowed output voltage ripple (typically 1% of Vout)
- `f` is the switching frequency of the buck converter

Assuming a maximum output current of 2A, a duty cycle of 0.417 (5V / 12V), a maximum output voltage ripple of 50 mV, and a switching frequency of 200 kHz, the output capacitor value would be:

`C = (2 * 0.417) / (5 * 0.05 * 200000) = 83.4 μF`

You can use a 100 μF or 220 μF capacitor for the output.

**Diode Value:**
The diode used in a buck converter should be a Schottky diode with a voltage rating higher than the input voltage (12V) and a current rating higher than the maximum output current. A common choice would be a 1N5817 or 1N5818 Schottky diode, which have a reverse voltage rating of 20V and a forward current rating of 1A.

Remember to choose components with appropriate voltage and current ratings for your specific application. Additionally, consider the overall efficiency, heat dissipation, and transient response of the buck converter when selecting the components.
```
```
Okay, with a maximum output current of 3A, the recommended component values for the buck converter would be:

**Inductor Value:**
Using the formula:
`L = (Vin * (Vout - Vin)) / (Vin * Iout * f)`

with:
- `Vin = 12V`
- `Vout = 5V`
- `Iout = 3A`
- `f = 200 kHz`

The inductor value would be:
`L = (12 * (5 - 12)) / (12 * 3 * 200000) = 15 μH`

You can use a 15 μH or 22 μH inductor.

**Capacitor Value:**
Using the formula:
`C = (Iout * D) / (Vout * ΔV * f)`

with:
- `Iout = 3A`
- `D = Vout / Vin = 0.417`
- `Vout = 5V`
- `ΔV = 50 mV (1% of Vout)`
- `f = 200 kHz`

The output capacitor value would be:
`C = (3 * 0.417) / (5 * 0.05 * 200000) = 125 μF`

You can use a 150 μF or 220 μF capacitor for the output.

**Diode Value:**
The diode should be a Schottky diode with a reverse voltage rating higher than 12V and a forward current rating higher than 3A. Some suitable options would be:
- 1N5819 (30V, 3A)
- MBRS340 (40V, 3A)
- MBR320 (20V, 3A)

Choose a diode with appropriate voltage and current ratings for your application.

Remember to consider the overall efficiency, heat dissipation, and transient response of the buck converter when selecting the components.
```
