const fz = require('zigbee-herdsman-converters/converters/fromZigbee');
const tz = require('zigbee-herdsman-converters/converters/toZigbee');
const exposes = require('zigbee-herdsman-converters/lib/exposes');
const reporting = require('zigbee-herdsman-converters/lib/reporting');
const extend = require('zigbee-herdsman-converters/lib/extend');
const e = exposes.presets;
const ea = exposes.access;
const tuya = require('zigbee-herdsman-converters/lib/tuya');

const definition = {
    fingerprint: [
        {
            modelID: 'TS0601',
            manufacturerName: '_TZE200_eanjj2pa',
        },
    ],
    model: 'IFS-STD001',
    vendor: 'iFEEL+',
    description: 'Temp+Hum Screen Sensor',
    fromZigbee: [tuya.fz.datapoints],
    toZigbee: [tuya.tz.datapoints],
    onEvent: tuya.onEventSetTime,
    configure: tuya.configureMagicPacket,
    exposes: [
        e.humidity(),
        e.temperature(),
    ],
    meta: {
        tuyaDatapoints: [
            [2, 'humidity', tuya.valueConverter.raw],
            [1, 'temperature', tuya.valueConverter.divideBy10],
        ],
    },
};

module.exports = definition;
