```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

```template
basic.forever(function () {
    if (sparkbitI.bumpSensor(1)) {
        if (true) {
            sparkbitO.setLightModule(1, 100, Colors.Red)
        } else {
            sparkbitO.setLightModule(1, 100, Colors.Green)
        }
        basic.pause(500)
    }
})
```

# Boolean Variables

## Step 1

Open the ``||variables:Variables||`` container and **Make a Variable** called **toggle**. Add the ``||variables:toggle||`` block as the condition for the ``||logic:if-else||`` statement.

```blocks
basic.forever(function () {
    if (sparkbitI.bumpSensor(1)) {
        let toggle = 0
        if (toggle) {
            sparkbitO.setLightModule(1, 100, Colors.Red)
        } else {
            sparkbitO.setLightModule(1, 100, Colors.Green)
        }
        basic.pause(500)
    }
})
```

## Step 2

Open the ``||variables:Variables||`` container, select the ``||variables:set toggle||`` block, and connect it below the top ``||sparkbitO:set light module||`` to red block.

```blocks
let toggle = 0
basic.forever(function () {
    if (sparkbitI.bumpSensor(1)) {
        if (toggle) {
            sparkbitO.setLightModule(1, 100, Colors.Red)
            toggle = 0
        } else {
            sparkbitO.setLightModule(1, 100, Colors.Green)
        }
        basic.pause(500)
    }
})
```

## Step 3

Open the ``||logic:Logic||`` container, select the ``||logic:<false>||`` block, and place it in the ``||variables:set toggle||`` block.

```blocks
let toggle = false
basic.forever(function () {
    if (sparkbitI.bumpSensor(1)) {
        if (toggle) {
            sparkbitO.setLightModule(1, 100, Colors.Red)
            toggle = false
        } else {
            sparkbitO.setLightModule(1, 100, Colors.Green)
        }
        basic.pause(500)
    }
})
```

## Step 4

Add a ``||variables:set toggle||`` block below the bottom ``||sparkbitO:set light module||`` to green block, and set to ``||logic:<true>||``.

```blocks
let toggle = false
basic.forever(function () {
    if (sparkbitI.bumpSensor(1)) {
        if (toggle) {
            sparkbitO.setLightModule(1, 100, Colors.Red)
            toggle = false
        } else {
            sparkbitO.setLightModule(1, 100, Colors.Green)
            toggle = true
        }
        basic.pause(500)
    }
})
```

## Step 5

Add a ``||serial:serial write line||`` for ``||variables:toggle||`` at the end of the ``||logic:if||`` statement below the ``||basic:pause||`` block.

```blocks
let toggle = false
basic.forever(function () {
    if (sparkbitI.bumpSensor(1)) {
        if (toggle) {
            sparkbitO.setLightModule(1, 100, Colors.Red)
            toggle = false
        } else {
            sparkbitO.setLightModule(1, 100, Colors.Green)
            toggle = true
        }
        basic.pause(500)
        serial.writeLine("" + (toggle))
    }
})
```

## Step 6

Add a ``||serial:serial write line||`` for ``||variables:toggle||`` to ``||basic:on start||``.

And inilize the variable ``||variables:toggle||`` by adding ``||variables: set toggle||`` to ``||logic:<false>||`` to ``||basic:on start||``.

```blocks
let toggle = false
serial.writeLine("" + (toggle))
basic.forever(function () {
    if (sparkbitI.bumpSensor(1)) {
        if (toggle) {
            sparkbitO.setLightModule(1, 100, Colors.Red)
            toggle = false
        } else {
            sparkbitO.setLightModule(1, 100, Colors.Green)
            toggle = true
        }
        basic.pause(500)
        serial.writeLine("" + (toggle))
    }
})
```

## Step 7

``|Download|`` the program to the Spark:bit and select **Show console Simulator**.
* Press the bump sensor and observe the mechanism (light module) and the serial monitor.
* Press the bump sensor a second time and observe the mechanism and the serial monitor.