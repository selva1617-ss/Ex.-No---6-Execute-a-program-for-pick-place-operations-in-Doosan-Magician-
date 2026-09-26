# Ex.-No---6-Execute-a-program-for-pick-place-operations-in-Doosan-Magician-
Ex. No - 6 Execute a program for pick &amp; place operations in Doosan Magician 
# Aim
To execute pick and place operation using Dobot magician robot 
# Apparatus / Software required
1. Dobot magician robot 2. Blockly software 3. IR Sensor 4. Belt conveyor 5. colour cubes
## Procedure

1. **Set up the equipment** by placing the DOBOT Magician beside the conveyor belt and connecting the IR/photoelectric sensor and suction cup/gripper.

2. **Connect the DOBOT Magician to the computer** and open **DobotLab**. DobotLab supports Blockly programming for the Magician. ([Dobot][2])

3. **Home the robot** and make sure the robot is in a safe initial position.

4. **Define the required points** using the robot's teaching function:

   * **P1 – Home position**
   * **P2 – Pick-above position**
   * **P3 – Pick position**
   * **P4 – Place position**
   * If required, define an additional **Place-above position**.

5. **Place the colour cube on the conveyor belt** and position the IR/photoelectric sensor so that it detects the cube when it reaches the required location.

6. **Create the Blockly program** with the following sequence:

```text
START
   ↓
Move to P1 (Home)
   ↓
Start Conveyor
   ↓
Wait for IR Sensor = 1
   ↓
Stop Conveyor
   ↓
Move to P2 (Pick Above)
   ↓
Move to P3 (Pick)
   ↓
Turn ON Suction Cup
   ↓
Move to P2
   ↓
Move to Place Above
   ↓
Move to P4 (Place)
   ↓
Turn OFF Suction Cup
   ↓
Move to Place Above
   ↓
Start Conveyor
   ↓
Return to P1
   ↓
Repeat
```

7. **Run the program** in Blockly/DobotLab and observe the conveyor operation.

8. When the **IR sensor detects the cube**, the conveyor should stop and the robot should move to the predefined pick position. The DOBOT documentation notes that the photoelectric sensor outputs a detection state that can be read by Blockly. ([Dobot][3])

9. The robot **activates the suction cup**, picks up the cube, moves to the predefined placement position, and **deactivates the suction cup** to release the cube.

10. The robot returns to the **Home position**, the conveyor starts again, and the process is repeated for the next cube.

11. **Verify the pick-and-place operation** by checking that the cube is correctly detected, picked, transported, and placed at the desired location.

### Simple flow for your viva

**IR detects cube → Conveyor stops → Robot picks cube → Robot moves → Robot places cube → Robot returns Home → Conveyor restarts.**
# PROGRAM :
<img width="1334" height="1179" alt="image" src="https://github.com/user-attachments/assets/f5060191-d214-4bbb-addb-7d24126a8698" />

## Result:

 Thus, the pick-and-place operation using the DOBOT Magician was successfully executed using Blockly programming.

[1]: https://jp.dobot-robots.com/service/download-center-1?utm_source=chatgpt.com "Search for the Right Manual | Dobot Download Center"
[2]: https://www.dobot-robots.com/products/education/magician.html?utm_source=chatgpt.com "DOBOT Magician | Desktop Grade Robot For Advanced Education"
[3]: https://www.dobot-robots.com/service/faq/432.html?lang=en&utm_source=chatgpt.com "What to do when 2 programs are running, the block is at the photoelectric sensor but the robot does not execute picking action?"
