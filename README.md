# 1)Set Slicer Profil

-> Edit Basic Profil

```
M501 ;
G28 ;
M420 S1 ;
```

# 2)set printer

```
M200 D1.128
M500
M501

G28 // define Home

G29 // bed leveling
M500 // Save setting
M501 // applied setting

M503 // Print Setting -> get acutal Z offset

M211 S0
G1 F60 Z0 // go to Z0

//Insert a sheet of paper under the nozzle and test for a perfect Z position

M851 Z X.XX // New Position for Z Axe (~~ -2.2)
M500
M501
```

## Finish