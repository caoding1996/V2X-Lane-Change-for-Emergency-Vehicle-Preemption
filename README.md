# V2X-Lane-Change-for-Emergency-Vehicle-Preemption
This is a simple demo of the paper: 
C. Ding, I. W. -H. Ho, E. Chung and T. Fan, "V2X and Deep Reinforcement Learning-Aided Mobility-Aware Lane Changing for Emergency Vehicle Preemption in Connected Autonomous Transport Systems," in IEEE Transactions on Intelligent Transportation Systems, vol. 25, no. 7, pp. 7281-7293, July 2024, doi: 10.1109/TITS.2024.3350334.

Polyu EIE 575 course students can use it as a reference code, please innovate your own contributions.

# Software Versions
SUMO 0.32.0
OMNeT++ 5.6.2
Veins 4.7.1

# How to Run
1. Download evtls.zip, unzip it in the omnetpp folder.
2. Create a new project and import it.
3. Input the following TraCI command to the mingwenv.cmd: (Change to your own path!)

C:/omnetpp-5.6.2/evtls/veins-veins-4.7.1/sumo-launchd.py -vv -c 'C:/Program Files (x86)/DLR/Sumo/bin/sumo-gui.exe'

4. Run the omnetpp.ini in the IDE.

# Functionality of the Code

1. Vehicles give way: There is an emergency vehicle (EV) behind, and the autonomous vehicles (AVs) in front will give way to it after receiving the WSM message.
![image](https://github.com/caoding1996/V2X-Lane-Change-for-Emergency-Vehicle-Preemption/blob/main/before.png)
![image](https://github.com/caoding1996/V2X-Lane-Change-for-Emergency-Vehicle-Preemption/blob/main/after.png)
3. Intelligent traffic light control (TLC): The EV will have green lights in advance when passing through the intersection, and traffic lights will return to normal after passing through the intersection.
![image](https://github.com/caoding1996/V2X-Lane-Change-for-Emergency-Vehicle-Preemption/blob/main/TLC.png)
# How to realize the functions

Check the EVTLS.CC file. The main codes are shown in the figures below.

![image](https://github.com/caoding1996/V2X-Lane-Change-for-Emergency-Vehicle-Preemption/blob/main/code.png)

# Preliminary Results

1. If both V2X LC and TLC are used, the EV travel time is (123.2-20) seconds.
2. If only V2X LC is used, the EV travel time is (127.8-20) seconds.
3. Without using any control algorithm, the EV travel time is (217.5-20) seconds.

![image](https://github.com/caoding1996/V2X-Lane-Change-for-Emergency-Vehicle-Preemption/blob/main/ev_speed.png)

# Conclusion
Both V2X LC and TLC can help the EV improve travel efficiency, and V2X LC improves efficiency more significantly than TLC.
