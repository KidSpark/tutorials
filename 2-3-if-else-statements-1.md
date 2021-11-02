```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

```template
basic.forever(function () {
    serial.writeLine(sparkbitI.bumpSensorIsPressed(SparkbitInPort.Input1))
})
```

# If/Else Statements

## Step 1 @showdialog

Follow the step-by-step instructions in the curriculum packet for this lesson to assemble the mechanism shown below. Then click the **Ok** button to proceed to the next step of the tutorial.

![if-else-statements-1](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/2-3-if-else-statements-1.png)

## Step 2

Open the ``||logic:Logic||`` category, select the ``||logic:if-else||`` block, and connect it to the bottom of the ``||serial:serial write line||`` block.

```blocks
basic.forever(function () {
    serial.writeLine(sparkbitI.bumpSensorIsPressed(SparkbitInPort.Input1))
    if (true) {
    	
    } else {
    	
    }
})
```

## Step 3

Open the ``||sparkbitI:Spark:bit Inputs||`` category, select the ``||sparkbitI:bump sensor||`` block, and place it after ``||logic:if||`` by replacing **true**.

```blocks
basic.forever(function () {
    serial.writeLine(sparkbitI.bumpSensorIsPressed(SparkbitInPort.Input1))
    if (sparkbitI.bumpSensorIsPressed(SparkbitInPort.Input1)) {
    	
    } else {
    	
    }
})
```

## Step 4

Open the ``||sparkbitO:Spark:bit Outputs||`` category, select the ``||sparkbitO:set light module||`` block, and connect it below ``||logic:then||``.

```blocks
basic.forever(function () {
    serial.writeLine(sparkbitI.bumpSensorIsPressed(SparkbitInPort.Input1))
    if (sparkbitI.bumpSensorIsPressed(SparkbitInPort.Input1)) {
        sparkbitO.setLightModule(SparkbitOutPort.Output1, SparkbitColor.Green, 100)
    } else {
    	
    }
})
```

## Step 5

Open the ``||sparkbitO:Spark:bit Outputs||`` category, select the ``||sparkbitO:turn off light module||`` block, and connect it below ``||logic:else||``.

```blocks
basic.forever(function () {
    serial.writeLine(sparkbitI.bumpSensorIsPressed(SparkbitInPort.Input1))
    if (sparkbitI.bumpSensorIsPressed(SparkbitInPort.Input1)) {
        sparkbitO.setLightModule(SparkbitOutPort.Output1, SparkbitColor.Green, 100)
    } else {
        sparkbitO.stopLightModule(SparkbitOutPort.Output1)
    }
})
```
## Step 6

Follow the steps below to download and test the program:
* ``|Download|`` the program to the Spark:bit.
* Make sure the Spark:bit is powered on and connected to the USB cable.
* Select **Show console Device** located under the micro:bit simulator and observe the serial monitor and plotter.
* Press the bump sensor and observe the mechanism and the serial monitor.
* [Click here](https://kidsparkeducation.org/media/2363) to see a video of the mechanism and serial monitor in action.
* Power off the Spark:bit.

## Step 7

Click **Finish**, turn off the Spark:bit, and review the next section in the curriculum packet.