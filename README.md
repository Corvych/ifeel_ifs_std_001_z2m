# External Zigbee2MQTT Converter For iFEEL+ IFS-STD001
## Supported Devices
| Model | Photo | Is Supported |
|-----------------|:-------------------------------:|:---------:|
|iFEEL+ IFS-STD001|<img src="https://cdn1.ozone.ru/s3/multimedia-9/wc1000/6267204177.jpg" width="150">|✅|
## What works
| Function | Is working |
|-------------------|:------:|
|Getting temperature|✅|
|Getting humidity|✅|
|Setting time|❌|
|Low Battery alert|❌|
## How to make it work
1. Download [ifeelplus_std_001.js](https://github.com/Corvych/ifeel_ifs_std_001_z2m/blob/stable/ifeelplus_std_001.js) external converter
2. Bind device to your Zigbee network
3. Add this into your Zigbee2MQTT `configuration.yaml` file
```
external_converters:
  - ifeelplus_std_001.js
```
4. Restart Zigbee2MQTT extension and you're ready to go!
