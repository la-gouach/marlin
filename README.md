# Commande Index

| Action            | Gcode               |
| ------------------|:-------------------:|
| Save Settings     | ```M500```          |
| Applied Settings  | ```M501```          |
| Set Z Offset      | ```M851 Z X.XX```   |
| Unlock Axis Limit | ```M211 S0```       |
| Set Home          | ```G28```           |
| Bed Leveling      | ```G29```           |

---
---
---

# 1)Set Slicer Profile

->Dowload Basic-Profile for Cr10s 5 and Pla Or add ```M501``` before ```G28``` and ```M420 S1``` After on your profile

---

# !!! prerequisites !!! 

##### heat the bed and the nozzle to the desired temperature

![alt text](https://camo.githubusercontent.com/aa815961f73cb245d6608cca9becabd869124d13/68747470733a2f2f662e636c6f75642e6769746875622e636f6d2f6173736574732f3230333932322f313939393937372f36623465343035322d383534652d313165332d383336372d3836653836373462643733332e706e67)

---

# 2)set printer

### Go on Gcode Terminal
![alt text](http://www.marvinstuart.com/wp-content/uploads/OctoPrint/screenshot-terminal.png) 

##### 1) Set 3D print Home on entering ``` G28 ```  

##### 2) Extend the Z axis to 0  
To pass a paper under the nozzle if the catch and perfect to pass to step 3, if not follow the approach.  
-> Send ```M211 S0``` to unlock the axis limit  
-> move your Z axis so that the nozzle is perfect (Get New Z position)  
-> Use ```M851 Z X.XX``` for set the difference between the sensor and the nozzle (Ex: New_Z = -3.5 -> M851 Z-3.5)
-> Use ```M500``` for register and ```M501``` for applied  
-> Re checked and redone if needed 

##### 3) IF and ONLY IF your bed it's at the good Temperature
-> Launch a Bed-Leveling ```G29```  
-> ```M500``` for Save and ```M501``` for applied

## Finish

---
