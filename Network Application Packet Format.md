
# PNI Network Application Packet Format #
The PNI network application packet format are a set if json documents that define data interchange between Lora network providers and the PNI PlacePod application.

This format is the same regardless of transport. The same JSON is sent/received over both MQTT and REST.

This format is for network providers only. 
 
## Downlink ##
    {
      "confirmed": true, // Do we need an ack?
      "data": "string", // Base64 encoded payload
      "devEUI": "string", // Device EUI
      "fPort": 0, 
      "reference": "string" //  recalibrate, configure etc. 
    }

## Uplink ##
	{
	    "devEui": "008000000400069D", // Placepod DevEUI						
	    "freq": 903.3,                // frequency used for transmission
	    "gwEui": "00250C0001000262",  // DevEUI of receiving gateway
	    "data": "QD==",               // Base64 encoded payload
	    "rxtime": "2017-04-27T23:04:07.109Z" 
                                          // time received at gateway
            "snr": 10,                    // signal to noise ratio for packet
	    "rssi": -25,                  // Rssi of packet 
            "per": 0.0,                   // Packet error rate of gateway
	}
