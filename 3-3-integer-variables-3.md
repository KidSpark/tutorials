```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

```template
let count = 0
serial.writeLine("" + (count))
basic.forever(function () {
    if (sparkbitI.bumpSensor(sparkbitI.__inputNumber(1))) {
        count += 1
        serial.writeLine("" + (count))
        basic.pause(500)
    }
    if (sparkbitI.bumpSensor(sparkbitI.__inputNumber(2))) {
        count += -1
        serial.writeLine("" + (count))
        basic.pause(500)
    }
    if (true) {
        sparkbitO.setLightModule(sparkbitO.__outputNumber(1), 100, Colors.Green)
    } else {
        sparkbitO.stopLight(sparkbitO.__outputNumber(1))
    }
})
```

# Integer Variables

## Step 1

Open the ``||logic:Logic||`` container, select the ``||logic:comparison||`` block with the equal sign, place it in the bottom ``||logic:if-then||`` statement.

```blocks
let count = 0
serial.writeLine("" + (count))
basic.forever(function () {
    if (sparkbitI.bumpSensor(sparkbitI.__inputNumber(1))) {
        count += 1
        serial.writeLine("" + (count))
        basic.pause(500)
    }
    if (sparkbitI.bumpSensor(sparkbitI.__inputNumber(2))) {
        count += -1
        serial.writeLine("" + (count))
        basic.pause(500)
    }
    if (0 == 0) {
        sparkbitO.setLightModule(sparkbitO.__outputNumber(1), 100, Colors.Green)
    } else {
        sparkbitO.stopLight(sparkbitO.__outputNumber(1))
    }
})
```

## Step 2

Add the ``||variables:count||`` variable to the first part of the ``||logic:comparison||`` block, and change the second part of the ``||logic:comparison||`` block to **5**.

```blocks
let count = 0
serial.writeLine("" + (count))
basic.forever(function () {
    if (sparkbitI.bumpSensor(sparkbitI.__inputNumber(1))) {
        count += 1
        serial.writeLine("" + (count))
        basic.pause(500)
    }
    if (sparkbitI.bumpSensor(sparkbitI.__inputNumber(2))) {
        count += -1
        serial.writeLine("" + (count))
        basic.pause(500)
    }
    if (count == 5) {
        sparkbitO.setLightModule(sparkbitO.__outputNumber(1), 100, Colors.Green)
    } else {
        sparkbitO.stopLight(sparkbitO.__outputNumber(1))
    }
})
```

## Step 3

``|Download|`` the program to the Spark:bit and select **Show consule Simulator**.
* Press bump sensor 1 five times and observe the mechanism (light module) and the serial monitor.
* Press bump sensor 2 and observe the machanism (light module) and the serial monitor.