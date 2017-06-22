
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
	    "channel": 5,
	    "datarate": 3,
	    "devEui": "008000000400069D",
	    "dup": false,
	    "freq": 903.3,
	    "gwEui": "00250C0001000262",
	    "joinId": 9,
	    "maxSnr": 15,
	    "minSnr": 6,
	    "pdu": "1503180000C8419A9969400000F7B7B501",
	    "port": 1,
	    "rssi": -25,
	    "seqno": 75,
	    "snr": 10,
	    "statusMsg": "Uplink Received",
	    "success": true,
	    "txpower": 30,
	    "txtime": "2017-04-27T23:04:07.109Z"
	}
