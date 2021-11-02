```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

```template
basic.forever(function () {
    serial.writeLine(sparkbitI.irTransmitterIsReceived(SparkbitInPort.Input1, SparkbitInPort.Input2))
    if (true) {
        sparkbitO.setLightModule(SparkbitOutPort.Output1, SparkbitColor.Green, 100)
    } else {
        sparkbitO.setLightModule(SparkbitOutPort.Output1, SparkbitColor.Red, 100)
    }
})
```

# Creating a Proximity Sensor

## Step 1 @showdialog

Follow the step-by-step instructions in the curriculum packet for this lesson to assemble the mechanism shown below. Then click the **Ok** button to proceed to the next step of the tutorial.

![proximity-sensor](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/2-5-proximity-sensor.png)

## Step 2

* Open the ``||logic:Logic||`` category, select the ``||logic:<not>||`` block, and place it after ``||logic:if||`` replacing **true**.
* Open the ``||sparkbitI:Spark:bit Inputs||`` category, select the ``||sparkbitI:IR Tx/Rx||`` block, and place it in the ``||logic:<not>||`` block.

```blocks
basic.forever(function () {
    serial.writeLine(sparkbitI.irTransmitterIsReceived(SparkbitInPort.Input1, SparkbitInPort.Input2))
    if (!(sparkbitI.irTransmitterIsReceived(SparkbitInPort.Input1, SparkbitInPort.Input2))) {
        sparkbitO.setLightModule(SparkbitOutPort.Output1, SparkbitColor.Green, 100)
    } else {
        sparkbitO.setLightModule(SparkbitOutPort.Output1, SparkbitColor.Red, 100)
    }
})
```

## Step 3

Follow the steps below to download and test the program:
* ``|Download|`` the program to the Spark:bit.
* Make sure the Spark:bit is powered on and connected to the USB cable.
* Select **Show console Device** located under the micro:bit simulator and observe the serial monitor.
* Test and observe the mechanism by placing your hand in front of the IR Tx/Rx, and observe the boolean values in the serial monitor.
* [Click here](https://kidsparkeducation.org/media/2366) to see a video of the mechanism in action.
* Power off the Spark:bit.

## Step 4

Click **Finish**, turn off the Spark:bit, and review the next section in the curriculum packet.