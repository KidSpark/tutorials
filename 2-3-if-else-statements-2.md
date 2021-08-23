```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

```template
basic.forever(function () {
    serial.writeNumber(sparkbitI.readAngleSensorDeg(DegreePercent.Percent, 1))
    if (true) {
        sparkbitO.setLightModule(1, 100, Colors.Red)
    } else {
        sparkbitO.stopLight(1)
    }
})
```

# If/Else Statements

## Step 1 @showdialog

Follow the step-by-step instructions in the curriculum packet for this lesson to assemble the mechanism shown below. Then click the **Ok** button to proceed to the next step of the tutorial.

![if-else-statements-2](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/2-3-if-else-statements-2.png)

## Step 2

Open the ``||sparkbitI:Spark:bit Inputs||`` container, select the ``||sparkbitI:angle sensor||`` block with the equal sign and percent (%), and place it after ``||logic:if||`` replacing **true**. Change the **equal sign (=) to greater than (>)** and adjust the **percent to 70**.

```blocks
basic.forever(function () {
    serial.writeNumber(sparkbitI.readAngleSensorDeg(DegreePercent.Percent, 1))
    if (sparkbitI.testAngleSensorPercent(1, LogicCompare.LogicCompareGT, 70)) {
        sparkbitO.setLightModule(1, 100, Colors.Red)
    } else {
        sparkbitO.stopLight(1)
    }
})
```

## Step 3

Follow the steps below to download and test the program:
* ``|Download|`` the program to the Spark:bit.
* Make sure the Spark:bit is powered on and connected to the USB cable.
* Select **Show console Device** located under the micro:bit simulator and observe the serial monitor and plotter.
* Rotate the angle sensor and observe the mechanism and the serial monitor.
* [Click here](https://youtu.be/T2kGSDISaqw) to see a video of the mechanism and serial monitor in action.
* Power off the Spark:bit.

## Step 4

Click **Finish** and review the next section in the curriculum packet.