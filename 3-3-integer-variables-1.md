```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

```template
basic.forever(function () {
    if (sparkbitI.bumpSensor(1)) {
    	
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
let count = 0
```

```blocks
basic.forever(function () {
    if (sparkbitI.bumpSensor(1)) {
        
    }
})
```

## Step 3

Open the ``||variables:Variables||`` container, select the ``||variables:change count||`` block, and connect it below ``||logic:then||``.

```blocks
let count = 0
```

```blocks
basic.forever(function () {
    if (sparkbitI.bumpSensor(1)) {
        count += 1
    }
})
```

## Step 4


Add a ``||serial:serial write number||`` block to ``||basic:on start||`` below the ``||variables:set count||`` block.


```blocks
let count = 0
serial.writeNumber(0)
```

```blocks
basic.forever(function () {
    if (sparkbitI.bumpSensor(1)) {
        count += 1
    }
})
```

## Step 5

Add a ``||serial:serial write number||`` block and a ``||basic:pause||`` block to the ``||logic:if||`` statement. Change pause to **500 ms**.

```blocks
let count = 0
serial.writeNumber(0)
```

```blocks
basic.forever(function () {
    if (sparkbitI.bumpSensor(1)) {
        count += 1
        serial.writeNumber(0)
        basic.pause(500)
    }
})
```

## Step 6

Open the ``||variables:Variables||`` container, select the ``||variables:count||`` block, and add it to both of the ``||serial:serial write number||`` blocks.

![set-serial-1](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/3-3-set-serial-1.png)

```blocks
count = 0
serial.writeNumber(count)
```

```blocks
basic.forever(function () {
    if (sparkbitI.bumpSensor(1)) {
        count += 1
        serial.writeNumber(count)
        basic.pause(500)
    }
})
```

## Step 7

Follow the steps below to download and test the program:
* ``|Download|`` the program to the Spark:bit.
* Make sure the Spark:bit is powered on and connected to the USB cable.
* Select **Show console Device** located under the micro:bit simulator and observe the serial monitor.
* Press the bump sensor and observe the mechanism and the serial monitor.
* [Click here](https://youtu.be/i9J7VC1TM9U) to see a video of the mechanism and serial monitor in action.
* Power off the Spark:bit.

## Step 8

Click **Finish** and review the next section in the curriculum packet.