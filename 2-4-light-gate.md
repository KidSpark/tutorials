```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

```template
basic.forever(function () {
    serial.writeLine("")
    if (true) {
        sparkbitO.setLightModule(1, 100, Colors.Red)
    } else {
        sparkbitO.setLightModule(1, 100, Colors.Green)
    }
})
```

# Creating a Light Gate

## Step 1 @showdialog

Follow the step-by-step instructions in the curriculum packet for this lesson to assemble the mechanism shown below. Then click the **Ok** button to proceed to the next step of the tutorial.

![light-gate](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/2-4-light-gate.png)

## Step 2

Open the ``||sparkbitI:Spark:bit Inputs||`` container, select the ``||sparkbitI:IR Tx/Rx||`` block, and place it in the ``||serial:serial write line||`` block.

```blocks
basic.forever(function () {
    serial.writeLine(sparkbitI.proximity(1, 2))
    if (true) {
        sparkbitO.setLightModule(1, 100, Colors.Red)
    } else {
        sparkbitO.setLightModule(1, 100, Colors.Green)
    }
})
```

## Step 3

Place another ``||sparkbitI:IR Tx/Rx||`` block after the ``||logic:if||`` replacing **true**.

```blocks
basic.forever(function () {
    serial.writeLine(sparkbitI.proximity(1, 2))
    if (sparkbitI.proximity(1, 2)) {
        sparkbitO.setLightModule(1, 100, Colors.Red)
    } else {
        sparkbitO.setLightModule(1, 100, Colors.Green)
    }
})
```

## Step 4

Follow the steps below to download and test the program:
* ``|Download|`` the program to the Spark:bit.
* Make sure the Spark:bit is powered on and connected to the USB cable.
* Select **Show console Device** located under the micro:bit simulator and observe the serial monitor.
* Test and observe the mechanism by placing a finger between the transmitter and receiver.
* Observe the boolean values (true and false) in the serial monitor.
* [Click here](https://youtu.be/LfntBsh-KXE) to see a video of the mechanism in action.
* Power off the Spark:bit.

## Step 4

Click **Finish** and review the next section in the curriculum packet.