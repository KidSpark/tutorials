```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

```template
basic.forever(function () {
    if (sparkbitI.bumpSensor(1)) {
        if (true) {
            sparkbitO.setLightModule(1, Colors.Red, 100)
        } else {
            sparkbitO.setLightModule(1, Colors.Green, 100)
        }
        basic.pause(500)
    }
})
```

# Boolean Variables

## Step 1 @showdialog

Follow the step-by-step instructions in the curriculum packet for this lesson to assemble the mechanism shown below. Then click the **Ok** button to proceed to the next step of the tutorial.

![boolean-variables](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/3-4-boolean-variables.png)

## Step 2

* Open the ``||basic:Basic||`` container and add ``||basic:on start||`` to the workspace.
* Open the ``||variables:Variables||`` container and **Make a Variable** called **toggle**.
* Select the ``||variables:set toggle||`` block and add it to ``||basic:on start||``. Open the ``||logic:Logic||`` container, select ``||logic:<false>||`` and add it to the ``||variables:set toggle||`` block. 
 
```blocks
toggle = false
basic.forever(function () {
    if (sparkbitI.bumpSensor(1)) {
        if (true) {
            sparkbitO.setLightModule(1, Colors.Red, 100)
        } else {
            sparkbitO.setLightModule(1, Colors.Green, 100)
        }
        basic.pause(500)
    }
})
```

## Step 3

Add the ``||variables:toggle||`` block as the condition for the ``||logic:if-else||`` statement.

```blocks
toggle = false
basic.forever(function () {
    if (sparkbitI.bumpSensor(1)) {
        if (toggle) {
            sparkbitO.setLightModule(1, Colors.Red, 100)
        } else {
            sparkbitO.setLightModule(1, Colors.Green, 100)
        }
        basic.pause(500)
    }
})
```

## Step 4

Open the ``||variables:Variables||`` container, select the ``||variables:set toggle||`` block, and connect it below the top ``||sparkbitO:set light module||`` to red block.

Set the value to ``||logic:<false>||`` using the block from the ``||logic:Logic||`` container.

```blocks
toggle = false
basic.forever(function () {
    if (sparkbitI.bumpSensor(1)) {
        if (toggle) {
            sparkbitO.setLightModule(1, Colors.Red, 100)
            toggle = false
        } else {
            sparkbitO.setLightModule(1, Colors.Green, 100)
        }
        basic.pause(500)
    }
})
```

## Step 5

Add a ``||variables:set toggle||`` block below the bottom ``||sparkbitO:set light module||`` to green block, and set to ``||logic:<true>||``.

```blocks
toggle = false
```

```blocks
basic.forever(function () {
    if (sparkbitI.bumpSensor(1)) {
        if (toggle) {
            sparkbitO.setLightModule(1, Colors.Red, 100)
            toggle = false
        } else {
            sparkbitO.setLightModule(1, Colors.Green, 100)
            toggle = true
        }
        basic.pause(500)
    }
})
```

## Step 6

Add a ``||serial:serial write line||`` for ``||variables:toggle||`` at the end of the ``||logic:if||`` statement below the ``||basic:pause||`` block.

```blocks
toggle = false
```

```blocks
basic.forever(function () {
    if (sparkbitI.bumpSensor(1)) {
        if (toggle) {
            sparkbitO.setLightModule(1, Colors.Red, 100)
            toggle = false
        } else {
            sparkbitO.setLightModule(1, Colors.Green, 100)
            toggle = true
        }
        basic.pause(500)
        serial.writeLine(toggle)
    }
})
```

## Step 7

Add a ``||serial:serial write line||`` for ``||variables:toggle||`` to ``||basic:on start||``.

```blocks
toggle = false
serial.writeLine(toggle)
```

```blocks
basic.forever(function () {
    if (sparkbitI.bumpSensor(1)) {
        if (toggle) {
            sparkbitO.setLightModule(1, Colors.Red, 100)
            toggle = false
        } else {
            sparkbitO.setLightModule(1, Colors.Green, 100)
            toggle = true
        }
        basic.pause(500)
        serial.writeLine(toggle)
    }
})
```

## Step 8

Follow the steps below to download and test the program:
* ``|Download|`` the program to the Spark:bit.
* Make sure the Spark:bit is powered on and connected to the USB cable.
* Select **Show console Device** located under the micro:bit simulator and observe the serial monitor.
* Press the bump sensor and observe the mechanism (light module) and the serial monitor.
* Press the bump sensor a second time and observe the mechanism and the serial monitor.
* [Click here](https://youtu.be/X5Tcty-1vLA) to see a video of the mechanism and serial monitor in action.
* Power off the Spark:bit.

## Step 9

Click **Finish** and review the next section in the curriculum packet.