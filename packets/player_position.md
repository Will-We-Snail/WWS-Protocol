### The player Position packet (ID 1)

The player position packet (currently) includes only x and y position data.
```
When sending to server:
Send the x and y position as doubles
packet data format (sending)
{
    int32 level;
    double PosX;
    double PosY;
    boolean LookDir; (right = true)
}

When recieving from server:
Put snail for the guid of the moved player in the recieved level at the x and y position, facing in the correct direction. Create the snail if there is not one already.
```
