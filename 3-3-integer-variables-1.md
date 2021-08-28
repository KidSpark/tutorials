```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

```template
basic.forever(function () {
    if (sparkbitI.bumpSensorIsPressed(1)) {
    	
    }
})
```

# Integer Variables

## Step 1 @showdialog

Follow the step-by-step instructions in the curriculum packet for this lesson to assemble the mechanism shown below. Then click the **Ok** button to proceed to the next step of the tutorial.

![integer-variables-1](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/3-3-integer-variables-1.png)

## Step 2

* Open the ``||basic:Basic||`` container and add ``||basic:on start||`` to the workspace.
* Open the ``||variables:Variables||`` container, select **Make a Variable**, name it **count**, and select **Ok**.
* Select the ``||variables:set count||`` block and add it to ``||basic:on start||``. Confirm the initial **value is 0**. 

```blocks
count = 0
```

```blocks
basic.forever(function () {
    if (sparkbitI.bumpSensorIsPressed(1)) {
        
    }
})
```

## Step 3

Add a ``||serial:serial write line||`` block to ``||basic:on start||`` below the ``||variables:set count||`` block.
Open the ``||variables:Variables||`` category, select the ``||variables:count||`` block, and add it to the ``||serial:serial write line||`` block.

```blocks
count = 0
serial.writeLine("" + count)
```

```blocks
basic.forever(function () {
    if (sparkbitI.bumpSensorIsPressed(1)) {
        
    }
})
```

## Step 4

Open the ``||variables:Variables||`` category, select the ``||variables:change count||`` block, and connect it below ``||logic:then||`` in the if statement.
Add a ``||serial:serial write line||`` block to the ``||logic:if||`` statement. Place a variable ``||variables: count||`` block in the ``||serial:serial write line||`` block.

```blocks
count = 0
serial.writeLine("" + count)
```

```blocks
basic.forever(function () {
    if (sparkbitI.bumpSensorIsPressed(1)) {
        count += 1
        serial.writeLine("" + count)
    }
})
```

## Step 5

Add a ``||basic:pause||`` block to the ``||logic:if||`` statement. Change pause to **500 ms**.

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
})
```

## Step 6

Follow the steps below to download and test the program:
* ``|Download|`` the program to the Spark:bit.
* Make sure the Spark:bit is powered on and connected to the USB cable.
* Select **Show console Device** located under the micro:bit simulator and observe the serial monitor.
* Press the bump sensor and observe the mechanism and the serial monitor.
* [Click here](https://youtu.be/i9J7VC1TM9U) to see a video of the mechanism and serial monitor in action.
* Power off the Spark:bit.

## Step 7

Click **Finish** and review the next section in the curriculum packet.