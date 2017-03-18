# Arduino Power Meter Modbus Client
Acts as a Modbus master device to collect data from a slave Power Meter device.
Readings are taken every second and then output in YAML format.

## Hardware Interface
MAX485 with the following pin connections:

| MAX485 | Arduino Micro |
| ------ | ------------- |
| VCC    | +5V           |
| GND    | ⏚ (GND)       |
| DI     | 0 (TX)        |
| RO     | 1 (RX)        |
| DE     | 4             |
| RE     | 5             |

# Supported Power Meters
* Rayleigh Instruments RI-D19-80-C: 230V 5/80A LCD Single Phase Energy modbus – 80A Direct With RS485 Output

# Sample Output
```yaml
meter: {model: "RI-D19-80-C",serialNumber: "############",reading: {voltage: 2471e-1,current: 3e-1,frequency: 500e-1,activePower: 81,reactivePower: 28,apparentPower: 90,powerFactor: 1000e-1,temperature: 31,activeEnergy: 88e-2}}
```
