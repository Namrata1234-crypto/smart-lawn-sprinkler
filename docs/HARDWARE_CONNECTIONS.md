
# Hardware Connections
## Smart Lawn Sprinkler System

**Student Name:** Namrata Santosh Babar  
**PRN:** 202301070101  
**Project Name:** Smart Lawn Sprinkler  
**Microcontroller:** NodeMCU ESP8266

---

## 1. Components Used

1. NodeMCU ESP8266
2. Soil Moisture Sensor
3. Rain Drop Sensor
4. 5V Single Channel Relay Module
5. 7805 Voltage Regulator
6. Two 9V Batteries
7. DC Water Pump
8. Connecting Wires and Breadboard

## 2. Pin Connections

| Component | NodeMCU Pin |
|---|---|
| Soil Moisture Sensor AO | A0 |
| Rain Sensor DO | D5 |
| Relay IN | D6 |

## 3. Power Supply Connections

- NodeMCU is powered through the laptop USB connection.
- The 7805 voltage regulator is used to provide a regulated 5V supply for the relay module.
- The water pump uses a separate battery supply through the relay contacts.

## 4. Working Principle

1. The soil moisture sensor checks the moisture condition of the soil.
2. The rain sensor detects rainfall.
3. NodeMCU ESP8266 reads the sensor signals.
4. The controller processes the sensor conditions.
5. The relay controls the DC water pump.
6. The pump should turn ON when the soil is dry and rain is not detected.
7. The pump should turn OFF when the soil is moist or rain is detected.

## 5. Pin Configuration

- Soil Moisture Sensor: A0
- Rain Sensor Digital Output: D5
- Relay Input: D6

## 6. Safety Precautions

- Check all connections before powering the circuit.
- Verify the relay trigger logic before connecting the pump.
- Keep the pump disconnected during initial relay testing.
- Use the correct voltage supply for each component.
- Check the sensor readings before setting the moisture threshold.

## 7. Conclusion

The NodeMCU ESP8266 acts as the main controller of the Smart Lawn Sprinkler system. It receives sensor inputs and controls the water pump through a relay module. The system is designed to reduce unnecessary water usage through automatic irrigation.

**Note:** Hardware connections and actual working conditions should be verified through practical testing.
