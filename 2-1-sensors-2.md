```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

```template
basic.forever(function () {
    serial.writeLine("")
})
```

# Analog vs. Digital Sensors

## Step 1 @showdialog

Connect a bump sensor to Input 1 on the Spark:bit. Then select **Ok** to proceed to the next step of the tutorial.

![sensors-2](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/2-1-sensors-2.png)

## Step 2

Open the ``||sparkbitI:Spark:bit Inputs||`` container, select a ``||sparkbitI:bump sensor||`` block, and place it in the ``||serial:serial write line||`` block. 

```blocks
basic.forever(function () {
    serial.writeLine(sparkbitI.bumpSensorIsPressed(1))
})
```

## Step 3

Follow the steps below to download and test the program:
* ``|Download|`` the program to the Spark:bit.
* Make sure the Spark:bit is powered on and connected to the USB cable.
* Select **Show console Device** located under the micro:bit simulator and observe how the serial monitor displays the text **false**.
* Press the bump sensor and observe how the serical monitor displays the text **true**.
* [Click here](https://youtu.be/_F_F8L9VedE) to see a video of program in action.
* Power off the Spark:built

## Step 4

Click **Finish** and review the next section in the curriculum packet.