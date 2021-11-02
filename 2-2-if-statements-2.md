```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

```template
basic.forever(function () {
    serial.writeLine("" + sparkbitI.angleSensor(SparkbitInPort.Input1, SparkbitAngle.Degree))
    if (true) {
    	
    }
    if (true) {
    	
    }
})
```

# If Statements

## Step 1 @showdialog

Follow the step-by-step instructions in the curriculum packet for this lesson to assemble the mechanism shown below. Then click the **Ok** button to proceed to the next step of the tutorial.

![if-statements-2](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/2-2-if-statements-2.png)

## Step 2

Open the ``||sparkbitI:Spark:bit Inputs||`` category, select the ``||sparkbitI:angle sensor||`` block with the equal sign and degrees, and place it in the top ``||logic:if||`` block by replacing **true**. Change the **equal sign (=) to greater than (>)** and adjust the **degrees to 200**.

``` blocks
basic.forever(function () {
    serial.writeLine("" + sparkbitI.angleSensor(SparkbitInPort.Input1, SparkbitAngle.Degree))
    if (sparkbitI.angleSensorCompareDegree(SparkbitInPort.Input1, SparkbitLogic.GT, 200)) {
    	
    }
    if (true) {
    	
    }
})
```

## Step 3

Open the ``||sparkbitO:Spark:bit Outputs||`` category, select the ``||sparkbitO:rotate motor module||`` block, and place it in the middle of the top ``||logic:if||`` block.

```blocks
basic.forever(function () {
    serial.writeLine("" + sparkbitI.angleSensor(SparkbitInPort.Input1, SparkbitAngle.Degree))
    if (sparkbitI.angleSensorCompareDegree(SparkbitInPort.Input1, SparkbitLogic.GT, 200)) {
        sparkbitO.rotateMotorModule(SparkbitOutPort.Output1, SparkbitDirection.Clockwise, 100)
    }
    if (true) {
    	
    }
})
```

## Step 4

Open the ``||sparkbitI:Spark:bit Inputs||`` category, select the ``||sparkbitI:angle sensor||`` block with the equal sign and degrees, and place it in the bottom ``||logic:if||`` block by replacing **true**. Change the **equal sign (=) to less than (<)** and adjust the **degrees to 200**.

```blocks
basic.forever(function () {
    serial.writeLine("" + sparkbitI.angleSensor(SparkbitInPort.Input1, SparkbitAngle.Degree))
    if (sparkbitI.angleSensorCompareDegree(SparkbitInPort.Input1, SparkbitLogic.GT, 200)) {
        sparkbitO.rotateMotorModule(SparkbitOutPort.Output1, SparkbitDirection.Clockwise, 100)
    }
    if (sparkbitI.angleSensorCompareDegree(SparkbitInPort.Input1, SparkbitLogic.LT, 200)) {
    	
    }
})
```

## Step 5

Open the ``||sparkbitO:Spark:bit Outputs||`` category, select the ``||sparkbitO:stop motor module||`` block, and place it in the middle of the bottom ``||logic:if||`` block.

```blocks
basic.forever(function () {
    serial.writeLine("" + sparkbitI.angleSensor(SparkbitInPort.Input1, SparkbitAngle.Degree))
    if (sparkbitI.angleSensorCompareDegree(SparkbitInPort.Input1, SparkbitLogic.GT, 200)) {
        sparkbitO.rotateMotorModule(SparkbitOutPort.Output1, SparkbitDirection.Clockwise, 100)
    }
    if (sparkbitI.angleSensorCompareDegree(SparkbitInPort.Input1, SparkbitLogic.LT, 200)) {
        sparkbitO.stopMotorModule(SparkbitOutPort.Output1)
    }
})
```

## Step 6

Follow the steps below to download and test the program:
* ``|Download|`` the program to the Spark:bit.
* Make sure the Spark:bit is powered on and connected to the USB cable.
* Select **Show console Device** located under the micro:bit simulator and observe the serial monitor and plotter.
* Rotate the angle sensor and observe the mechanism and the serial monitor/plotter.
* [Click here](https://kidsparkeducation.org/media/2362) to see a video of the mechanism and serial monitor in action.
* Power off the Spark:bit.

## Step 7

Click **Finish**, turn off the Spark:bit, and review the next section in the curriculum packet.