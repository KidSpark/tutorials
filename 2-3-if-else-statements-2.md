```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

```template
basic.forever(function () {
    serial.writeLine("" + sparkbitI.angleSensor(SparkbitInPort.Input1, SparkbitAngle.Percent))
    if (true) {
        sparkbitO.setLightModule(SparkbitOutPort.Output1, SparkbitColor.Red, 100)
    } else {
        sparkbitO.stopLightModule(SparkbitOutPort.Output1)
    }
})
```

# If/Else Statements

## Step 1 @showdialog

Follow the step-by-step instructions in the curriculum packet for this lesson to assemble the mechanism shown below. Then click the **Ok** button to proceed to the next step of the tutorial.

![if-else-statements-2](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/2-3-if-else-statements-2.png)

## Step 2

Open the ``||sparkbitI:Spark:bit Inputs||`` category, select the ``||sparkbitI:angle sensor||`` block with the equal sign and percent (%), and place it after ``||logic:if||`` replacing **true**. Change the **equal sign (=) to greater than (>)** and adjust the **percent to 70**.

```blocks
basic.forever(function () {
    serial.writeLine("" + sparkbitI.angleSensor(SparkbitInPort.Input1, SparkbitAngle.Percent))
    if (sparkbitI.angleSensorComparePercent(SparkbitInPort.Input1, SparkbitLogic.GT, 70)) {
        sparkbitO.setLightModule(SparkbitOutPort.Output1, SparkbitColor.Red, 100)
    } else {
        sparkbitO.stopLightModule(SparkbitOutPort.Output1)
    }
})
```

## Step 3

Follow the steps below to download and test the program:
* ``|Download|`` the program to the Spark:bit.
* Make sure the Spark:bit is powered on and connected to the USB cable.
* Select **Show console Device** located under the micro:bit simulator and observe the serial monitor and plotter.
* Rotate the angle sensor and observe the mechanism and the serial monitor.
* [Click here](https://kidsparkeducation.org/media/2364) to see a video of the mechanism and serial monitor in action.
* Power off the Spark:bit.

## Step 4

Click **Finish** and review the next section in the curriculum packet.