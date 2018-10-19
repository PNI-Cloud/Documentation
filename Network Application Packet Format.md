
# PNI Network Application Packet Format #
The PNI network application packet format are a pair json documents that define data interchange between Lora network providers and the PNI PlacePod application.

This format is the same regardless of transport. The same JSON is sent/received over both MQTT and REST.

This format is for network providers only who wish to integrate with PNI's Generic Network Service.
 
## Downlink ##
Commands like "Recalibrate" sent to the PlacePod Sensor.

```
{
    "confirmed": true,            // Do we need an ack?
    "dataBase64": "QRda1==",      // Base64 encoded payload OR
    "dataHex": "0D"               // Hex encoded payload
    "devEUI": "008000000400069D", // Device EUI
    "fPort": 0,                   // LoRa port
    "reference": "string"         // recalibrate, configure etc. 
}
```

## Uplink ##
Car Presence messages and data from the sensor.

All fields are **required** unless stated otherwise

```
{
    "devEui": "008000000400069D",             // Placepod DevEUI						
    "freq": 903.3,                            // frequency used for transmission
    "gwEui": "00250C0001000262",              // DevEUI of receiving gateway
    "dataBase64": "FQEYAACoQckeZkAAAOq2r6I=", // Base64 encoded payload OR
    "dataHex": "023456789ABCDF"               // Hex encoded payload
    "rxtime": "2017-04-27T23:04:07.109Z"      // time received at gateway
    "snr": 10,                                // signal to noise ratio for packet
    "rssi": -25,                              // Rssi of packet 
    "count": 126                              // Frame Count. This field is optional.
    "port": 3                                 // LoRa port, used to know how to decode packet (required for R05)
    "per: 0                                   // Packet error rate. This field is optional.
}
```
