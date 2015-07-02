# garmin-heart-rate-monitor
nRF24AP1 - ANT Code - Garmin Heart-Rate Monitor

```
# ./ant /dev/ttyUSB0

TX: Success
txda: a4 01 4a 00 ef
TX: Success
txda: a4 02 4d 00 54 bf
TX: Success
RX: [sync]..[0x04]..[0x54]..[0x04]..[0x03]..[0x00]..[0x03]..[0xf0]
RX: msg received [7]
ID: MESG_CAPABILITIES_ID

[DEBUG] Device Capabilites
--------------------------
Max Ch                   4
Max Networks             3
Standard Opts         0x00
Advanced Opts1        0x03 [NETWORK_EN]
Advanced Opts2        0x00
Max Data Ch              0


txda: a4 02 4d 00 3d d6
TX: Success
RX: [sync]..[0x03]..[0x40]..[0x00]..[0x4d]..[0x28]..[0x82]
RX: msg received [6]
ID: MESG_RESPONSE_EVENT_ID
Response Handler (size=3)
Channel Num  0x00
Message ID   0x4d [unknown]
Message Code 0x28

txda: a4 03 42 00 00 01 e4
TX: Success
RX: [sync]..[0x03]..[0x40]..[0x00]..[0x42]..[0x00]..[0xa5]
RX: msg received [6]
ID: MESG_RESPONSE_EVENT_ID
Response Handler (size=3)
Channel Num  0x00
Message ID   0x42 [MESG_ASSIGN_CHANNEL_ID]
Message Code 0x00

new txda: a4 05 51 00 00 00 00 00 f0
old txda: a4 04 51 00 00 00 00 f1  --- Here was my problem!
TX: Success
RX: [sync]..[0x03]..[0x40]..[0x00]..[0x51]..[0x00]..[0xb6]
RX: msg received [6]
ID: MESG_RESPONSE_EVENT_ID
Response Handler (size=3)
Channel Num  0x00
Message ID   0x51 [MESG_CHANNEL_ID_ID]
Message Code 0x00

txda: a4 09 46 01 b9 a5 21 fb bd 72 c3 45 65
TX: Success
RX: [sync]..[0x03]..[0x40]..[0x01]..[0x46]..[0x00]..[0xa0]
RX: msg received [6]
ID: MESG_RESPONSE_EVENT_ID
Response Handler (size=3)
Channel Num  0x01
Message ID   0x46 [MESG_NETWORK_KEY_ID]
Message Code 0x00

txda: a4 02 44 00 0a e8
TX: Success
RX: [sync]..[0x03]..[0x40]..[0x00]..[0x44]..[0x00]..[0xa3]
RX: msg received [6]
ID: MESG_RESPONSE_EVENT_ID
Response Handler (size=3)
Channel Num  0x00
Message ID   0x44 [MESG_CHANNEL_SEARCH_TIMEOUT_ID]
Message Code 0x00

txda: a4 02 45 00 39 da
TX: Success
RX: [sync]..[0x03]..[0x40]..[0x00]..[0x45]..[0x00]..[0xa2]
RX: msg received [6]
ID: MESG_RESPONSE_EVENT_ID
Response Handler (size=3)
Channel Num  0x00
Message ID   0x45 [MESG_CHANNEL_RADIO_FREQ_ID]
Message Code 0x00

txda: a4 03 43 00 1f 86 7d
TX: Success
RX: [sync]..[0x03]..[0x40]..[0x00]..[0x43]..[0x00]..[0xa4]
RX: msg received [6]
ID: MESG_RESPONSE_EVENT_ID
Response Handler (size=3)
Channel Num  0x00
Message ID   0x43 [MESG_CHANNEL_MESG_PERIOD_ID]
Message Code 0x00

txda: a4 01 4b 00 ee
TX: Success
RX: [sync]..[0x03]..[0x40]..[0x00]..[0x4b]..[0x00]..[0xac]
RX: msg received [6]
ID: MESG_RESPONSE_EVENT_ID
Response Handler (size=3)
Channel Num  0x00
Message ID   0x4b [MESG_OPEN_CHANNEL_ID]
Message Code 0x00

RX: [sync]..[0x03]..[0x40]..[0x00]..[0x01]..[0x01]..[0xe7]
RX: msg received [6]
ID: MESG_RESPONSE_EVENT_ID
Response Handler (size=3)
Channel Num  0x00
Message ID   0x01 [unknown]
Message Code 0x01

----

RX: [sync]..[0x09]..[0x4e]..[0x00]..[0x58]..[0x60]..[0x36]..[0x18]..[0x4f]..[0x00]..[0x80]..[0x4d]..[0x77]
RX: msg received [12]
ID: Unknown [0x4e]

RX: [sync]..[0x09]..[0x4e]..[0x00]..[0x58]..[0x60]..[0x36]..[0x18]..[0x39]..[0x01]..[0x81]..[0x4d]..[0x01]
RX: msg received [12]
ID: Unknown [0x4e]

RX: [sync]..[0x09]..[0x4e]..[0x00]..[0x58]..[0x60]..[0x36]..[0x18]..[0x40]..[0x02]..[0x82]..[0x4d]..[0x78]
RX: msg received [12]
ID: Unknown [0x4e]

RX: [sync]..[0x09]..[0x4e]..[0x00]..[0x58]..[0x60]..[0x36]..[0x18]..[0x40]..[0x02]..[0x82]..[0x4d]..[0x78]
RX: msg received [12]
ID: Unknown [0x4e]

RX: [sync]..[0x09]..[0x4e]..[0x00]..[0x58]..[0x60]..[0x36]..[0x18]..[0x40]..[0x02]..[0x82]..[0x4d]..[0x78]
RX: msg received [12]
ID: Unknown [0x4e] 
```

For more information, see thread: https://forum.sparkfun.com/viewtopic.php?t=17017