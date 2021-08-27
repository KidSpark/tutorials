```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

```template
count = 0
serial.writeLine("" + count)
basic.forever(function () {
    if (sparkbitI.bumpSensorIsPressed(1)) {
        count += 1
        serial.writeLine("" + count)
        basic.pause(500)
    }
    if (sparkbitI.bumpSensorIsPressed(2)) {
        count += -1
        serial.writeLine("" + count)
        basic.pause(500)
    }
    if (true) {
        sparkbitO.setLightModule(1, SparkbitColor.Green, 100)
    } else {
        sparkbitO.stopLightModule(1)
    }
})
```

# Integer Variables

## Step 1 @showdialog

Follow the step-by-step instructions in the curriculum packet for this lesson to assemble the mechanism shown below. Then click the **Ok** button to proceed to the next step of the tutorial.

![integer-variables-1](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/3-3-integer-variables-1.png)

## Step 2

Open the ``||logic:Logic||`` container, select the number ``||logic:<comparison>||`` block with the equal sign <0 = 0>, place it in the bottom ``||logic:if||`` statement.

```blocks
count = 0
serial.writeLine("" + count)
```

```blocks
basic.forever(function () {
    if (sparkbitI.bumpSensorIsPressed(1)) {
        count += 1
        serial.writeLine("" + count)
        basic.pause(500)
    }
    if (sparkbitI.bumpSensorIsPressed(2)) {
        count += -1
        serial.writeLine("" + count)
        basic.pause(500)
    }
    if (0 == 0) {
        sparkbitO.setLightModule(1, SparkbitColor.Green, 100)
    } else {
        sparkbitO.stopLightModule(1)
    }
})
```

## Step 3

Add the ``||variables:count||`` variable to the first part of the ``||logic:<comparison>||`` block, and change the second part of the ``||logic:<comparison>||`` block to **5**.

```blocks
count = 0
serial.writeLine("" + count)
```

```blocks
basic.forever(function () {
    if (sparkbitI.bumpSensorIsPressed(1)) {
        count += 1
        serial.writeLine("" + count)
        basic.pause(500)
    }
    if (sparkbitI.bumpSensorIsPressed(2)) {
        count += -1
        serial.writeLine("" + count)
        basic.pause(500)
    }
    if (count == 5) {
        sparkbitO.setLightModule(1, SparkbitColor.Green, 100)
    } else {
        sparkbitO.stopLightModule(1)
    }
})
```

## Step 3

Follow the steps below to download and test the program:
* ``|Download|`` the program to the Spark:bit.
* Make sure the Spark:bit is powered on and connected to the USB cable.
* Select **Show console Device** located under the micro:bit simulator and observe the serial monitor.
* Press bump sensor 1 five times and observe the mechanism (light module) and the serial monitor.
* Press bump sensor 2 and observe the machanism (light module) and the serial monitor.
* [Click here](https://youtu.be/zS4ByCWoqPA) to see a video of the mechanism and serial monitor in action.
* Power off the Spark:bit.

## Step 4

Click **Finish** and review the next section in the curriculum packet.