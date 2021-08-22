```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

# Analog vs. Digital Sensors

## Step 1 @showdialog

Follow the step-by-step instructions in the curriculum packet for this lesson to assemble the mechanism shown below. Then click the **Ok** button to proceed to the next step of the tutorial.

![sensors-1](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/2-1-sensors-1.png)

## Step 2

Expand the **Advanced** section, open the ``||serial:Serial||`` container, select the ``||serial:serial write line||`` block, and connect it to the ``||basic:forever||`` function.

```blocks
basic.forever(function () {
    serial.writeLine("")
})
```
## Step 3

Open the ``||sparkbitI:Spark:bit Inputs||`` container, select the ``||sparkbitI:angle sensor||`` block, and place it in the ``||serial:serial write line||`` block. Change **degrees (°)** to **percent (%)**.

```blocks
basic.forever(function () {
    serial.writeLine("" + (sparkbitI.readAngleSensorDeg(DegreePercent.Percent, 1)))
})
```

## Step 4

Open the ``||sparkbitO:Spark:bit Outputs||`` container, select the ``||sparkbitO:rotate motor module||`` block, and connect it to the bottom of the ``||serial:serial write line||`` block.

``` blocks
basic.forever(function () {
    serial.writeLine("" + (sparkbitI.readAngleSensorDeg(DegreePercent.Percent, 1)))
    sparkbitO.rotateMotorDuration(1, 100, Directions.Clockwise)
})
```

## Step 5

Open the ``||sparkbitI:Spark:bit Inputs||`` container, select the ``||sparkbitI:angle sensor||`` block, and place it in the speed portion of the ``||sparkbitO:rotate motor module||`` block. Change **degrees (°)** to **percent (%)**.

```blocks
basic.forever(function () {
    serial.writeLine("" + (sparkbitI.readAngleSensorDeg(DegreePercent.Percent, 1)))
    sparkbitO.rotateMotorDuration(1, sparkbitI.readAngleSensorDeg(DegreePercent.Percent, 1), Directions.Clockwise)
})
```

## Step 6

Follow the steps below to download and test the program:
* ``|Download|`` the program to the Spark:bit.
* Make sure the Spark:bit is powered on.
* Select **Show console Device** located under the micro:bit simulator and observe the serial monitor and plotter.
* Rotate the angle sensor and observe the speed of the motor, as well as, the serial monitor and plotter.
* [Click here](https://youtu.be/SUECpRQ2Mxs) to see a video of the mechanism and serial monitor in action.
* Power off the Spark:built

## Step 7

Click **Finish** and review the next section in the curriculum packet.