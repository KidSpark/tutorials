```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

```template
let count = 0
serial.writeLine("" + (count))
basic.forever(function () {
    if (sparkbitI.bumpSensor(1)) {
        count += 1
        serial.writeLine("" + (count))
        basic.pause(500)
    }
})
```

# Integer Variables

## Step 1 @showdialog

Follow the step-by-step instructions in the curriculum packet for this lesson to assemble the mechanism shown below. Then click the **Ok** button to proceed to the next step of the tutorial.

![integer-variables-1](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/3-3-integer-variables-1.png)

## Step 2

Right click on the ``||logic:if||`` statement and select **Duplicate**. Add the second ``||logic:if||`` statement to the ``||basic:forever||`` funcation.

```blocks
let count = 0
serial.writeLine("" + (count))
basic.forever(function () {
    if (sparkbitI.bumpSensor(1)) {
        count += 1
        serial.writeLine("" + (count))
        basic.pause(500)
    }
    if (sparkbitI.bumpSensor(1)) {
        count += 1
        serial.writeLine("" + (count))
        basic.pause(500)
    }
})
```

## Step 3

On the bottom ``||logic:if||`` statement, change bump sensor to **input 2** and change count to **-1**.

```blocks
let count = 0
serial.writeLine("" + (count))
basic.forever(function () {
    if (sparkbitI.bumpSensor(1)) {
        count += 1
        serial.writeLine("" + (count))
        basic.pause(500)
    }
    if (sparkbitI.bumpSensor(2)) {
        count += -1
        serial.writeLine("" + (count))
        basic.pause(500)
    }
})
```

## Step 4

Follow the steps below to download and test the program:
* ``|Download|`` the program to the Spark:bit.
* Make sure the Spark:bit is powered on and connected to the USB cable.
* Select **Show console Device** located under the micro:bit simulator and observe the serial monitor.
* Press the bump sensors and observe the mechanism and the serial monitor.
* [Click here](https://youtu.be/reTxeG6eODU) to see a video of the mechanism and serial monitor in action.
* Power off the Spark:bit.

## Step 5

Click **Finish** and review the next section in the curriculum packet.