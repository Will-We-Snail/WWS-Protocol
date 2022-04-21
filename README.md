# Will We Snail Protocol

## How it works:
This protocol defines the structure of data sent over the lidgren managed connection. It defines the structure of all of them, then each individual packet type has it's own document in [packets](/packets/).

## Basic packet format
For the core (this), each packet begins with 0 (as a u16). After this is a u128 byte guid that is generated once on the client side before connection, then used by other clients to identify each individual client. After this is a u8 packet type, used to tell what type of packet it is. After this is the packet data, defined by the packet.
```
{
    u16 0;
    u128 guid;
    u16 PacketType;
    ...packet data
}
```
