# Zabbix template for Shelly 2.5 IoT Device

## Import Steps

1. Save the template XML file to your computer
2. Log in to your Zabbix web interface
3. Navigate to **Configuration** → **Templates**
4. Click on the **Import** button in the top right corner
5. Click **Choose File** and select the saved template XML file
6. Select the import options:
   - Make sure "Templates" is checked in the "Import" section
   - Select "Create new" for "Update existing"
   - Click **Import**

## Creating Hosts for Your Shelly Devices

1. Navigate to **Configuration** → **Hosts**
2. Click **Create host** button
3. Enter the required information:
   - **Host name**: A descriptive name (e.g., "Shelly 2.5 - Living Room")
   - **Groups**: Add to an appropriate host group (e.g., "IoT Devices")
   - **Interfaces**: Add an Agent interface with the IP address of your Shelly device
   - **Templates**: Link to the "Template Shelly Smart Relay" template
4. Click **Add** button at the bottom of the page

## Template Customization

You might need to adjust some thresholds based on your specific Shelly model and environment:

- Temperature triggers (70°C by default)
- WiFi signal strength warning threshold (-70 dBm by default)
- Memory and filesystem usage warnings (20% by default)

## Monitored Metrics

This template will monitor the following aspects of your Shelly device:

### General
- Device uptime
- Firmware version
- Update availability

### Network
- WiFi connection status
- WiFi SSID
- WiFi IP address
- WiFi signal strength (RSSI)
- Cloud connection status
- MQTT connection status

### Temperature
- Temperature in Celsius and Fahrenheit
- Temperature status
- Overtemperature condition

### Power
- Input voltage
- Power consumption per relay
- Total energy consumption per relay
- Total energy consumption (relay1 + relay2)

### Relays
- Relay status (on/off)
- Relay overpower protection status

![image](https://github.com/user-attachments/assets/62161f49-12fe-41ca-a845-cff9441d12f1)

