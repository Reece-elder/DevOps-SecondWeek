# Models

Represent what processes are happening
OSI         - Open System Interconnection
TCP / IP    - Transmission Control Protocol / Internet protocol 

## OSI

7 layer model developed by the International Organisation for Standardisation (ISO)

1) Physical Layer
    What hard ware is being used, ethernet cables, hubs etc. Responsible for transmission of data from source to destination

2) Data Link Layer
    Checks the data from the physical layer, ensures no transmission errors and packages bits in 'data frames'

3) Network Layer
    Source and destination are checked to see if data reached final intended destination. 
    If correct destination, moved to transport
    Else destination address updated and sent back to lower levels

4) Transport Layer
    Checks that data has been recieved by the destination device and has no errors. Transmits the data
    TCP and UDP

5) Session layer
    Connections are maintained until a device disconnects, this is the layer for ensuring data keeps flowing, in charge of ports etc
    Can be thought of as a phone call

6) Presentation Layer
    Data is formatted here, encryption and decryption, packets made into usable data

7) Application
    Backend of a website, HTTP requests etc

## TCP

4 layer model combining some of the OSI layers into less layers

1) Network Access Layer
    Equivalent to Physical and data link, how is data transferred physically AND converted into usable data

2) Internet Layer
    Equivalent to network, data is put into packets which contain the addresses of packets.
    Also responsible for routing these packets

3) Transport Layer
    Equivalent to Transport, carries on the conversation and uses TCP / UDP

4) Application Layer
    How data is formatted to be useful, conversation is held and data is used by an application through HTTP requests etc.



## Differences

OSI is generic model
TCP is protocol based and developed off of existing real protocols. OSI is a suggestion of how it should be












