# Abbreviations in 360 Controls

2025-03-20 08:52:35 Arthur

## 2. What are the categories of the abbreivations.
The status of `Safety Circuits`, `Drives`, `Doors`, `Serial Links`, `Tape Reader`

### 360 Controls Screen <0>

1. `Call registers`:
   1. `HU`, Hall Up call
   2. `HD`, Hall Down call
   3. `CC`: Car Call 
2. `COP`: Cab operation panel
3. `Operation Status`: 
   1. `AUTO NORMAL`, 
   2. `IN CAR INSPECTION`, 
   3. `CAR TOP INSPECTION`, 
   4. `PHASE 1(PH1)`
   5. `PHASE 2(PH2)`
   6. `EMERGENCY LOWERING`
4. `Safety Circuits` (`SI`): if every safety is closed or not, all safety tests are required before a run
   1. `Slack rope switch`, is open or closed
   2. `pit switch`
   3. `Car Top Stop Switch`
   4. `Top Emergency Exit Switch`
   5. `Top Solid Stop Switch`
   6. `In car Stop Switch`
5. `Door Interlock` (`I`): good: k: if all door contacts are made; not good: one or more of the landing(floor) or car door contacts are open (system will not run)
6. `Front Door Status` (`FD`): `FD11`=door is closed, `FD00`=door is open, `FD<-`=door is in midway
7. `Rear Door Status` (`RD`): `RD11`, `RD00`, `RD<-`;
8. `Floor Position`: 1~N, `F1`=lowest landing 
9.  `car Pos. Count`: tap reader count (in reference to the `floor magnets`), 1st floor reads approx. 1000

### Screen <1> drive control circuits
1. `Motor drive system` operation status: 
   1. `smDriveUpOK`: good=ready, ng=not ready
2. `Drive Status`:
   1. `DriveFullUp`, `DriveLevelUp`, `DriveFullDn`, `DriveLevelDn`, `DriveStop`, `DriveStopReady`. 
3. `Valve Status`: two valves: 1=up and down , 2 up-and-down high speed. for each valve it has 3 status:
   1. `↑`=UP ON, `↓`=DN ON, `-`=OFF
4. `Motor Contactor` status (`MCR`): good=OK, not good=Not OK
5. `Run Status`: status of the car movement:
   1. `RN` = Run, `RU`=Run Up, `RD`=Run Down, `LU`= Level Up, `LD`=Level Down

### Screen <2> Front and rear cab door status

1. `Front Door Status`, `Rear Door Status`: Two doors
   1. `DCL`=Door Close Limit
   2. `DMW`=Door Mid Way
   3. `DOL`=Door Open Limit
1. `CG` or `Car Gate contact status`: good=closed, ng=open
2. `HI`: Hoistway Contact status: good=closed, ng=open
3. `FZ`,`RZ`: Front Door Zone, Rear Door Zone: good=in zone, not good=not in zone

### Screen <3> Drive status
`Drive System`: OK=ready to run or DriveFaults (Fault message will display)

### Screen <4> Door Status
`Door System`: OK=ready to run, DoorFaults(messages will appear)

### Screen <5> 
1. `Comms`: serial link between machine room and car, ready or not ready
2. `CarStopSw`: status of In car Stop Switch, ready or not ready
3. `LS_OK`: status of tape reader, ready or not ready

### Screen <6> additional system information
`FAULT` Fault messages
`drive OK`: System status

### Screen <9> Current software version of the controller
`Version`
`Build date`
`Build ID`


## 3. Auto Learn
`Pendant control`: 

LEDs in main board
1. `POK`
2. `MCR` 
3. `AUTS`
4. `OPOK`
5. `S1`
6. `DI`
7. `DLK`
8. `S2`
9. `CSTPC`

LEDs in car board:
1. `LCF`
2. `LCR`
3. `SEF`
4. `SER`
5. `CG`
6. `CSTP`
7. `CTNM`
8. `NORM(in-car insp)`
9. `S2`

## 4. Programming Menu
### Operating params
Parameters that can be adjusted on site to improve performances and to accommodate preferences
1. `CCall Door` = 3s
2. `HCall Door` = 3s
3. `Cab Light` = 5min
4. `Up SlowDist` = 8"
5. `Dn SlowDist` = 10"
6. `Up StopDist` = 1/8"
7. `Dn StopDist` =5/8"
8. `Nudging` = No

### Configuration
1. `Type` = LULA
1. `Start Type` = Direct / Star Delta / Soft Start
1. `Star D Time` = 0.5 
1. `Door` = Automatic
1. `Adv Door Open` = Yes
1. `Floors` = 3 , the number of floors the elevator will service
1. `Installed Doors`, choose which floors are front door opening (or rear door opening)
1. `Floor Positions`, not setting is needed, this shows the count from the tape reader.
1. `Reset Positions`, portal to put the controller into auto learn mode. 
1. `Home Landing` = No/Yes, to set if car will return to the selected home floor after preset time of elevator inactivity.
2. `Home Time` = 3~20min. time of no activity before going Home landing
3. `Recall` = F1, the main fire service recall landing.
4. `Recall Alt` = F2, alternate fire service recall landing.
5. `Indicator Bus` = No/Yes, if using Landing Digital Position indicators
6. `Pos Indicators`, 
7. `Hatch ATDL` = 48", Access Top Down Tralvel Limit: set the down travel limit for the top hoistway access,
8. `Hatch ABUL` = 48", Access Buttom Up Travel Limit: 
9. `Multiplex` = No, Signle or Duplex elevator. 


### Data Display
1. `RS485 Main`
1. `RS485 A`
1. `RS485 B`
1. `RS485 C`
1. `RS485 D`
1. `RS485 Counts`
1. `State Machines`











