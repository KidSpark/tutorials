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
})
```

# Integer Variables

## Step 1

Right click on the ``||logic:if-then||`` statement and select **Duplicate**. Add the second ``||logic:if-then||``statement to the ``||basic:forever||`` funcation.

```blocks
let count = 0
serial.writeLine("" + (count))
basic.forever(function () {
    if (sparkbitI.bumpSensor(sparkbitI.__inputNumber(1))) {
        count += 1
        serial.writeLine("" + (count))
        basic.pause(500)
    }
    if (sparkbitI.bumpSensor(sparkbitI.__inputNumber(1))) {
        count += 1
        serial.writeLine("" + (count))
        basic.pause(500)
    }
})
```

## Step 2

On the bottom ``||logic:if-then||`` statement, change bump sensor to **input 2** and change count to **-1**.

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
})
```

## Step 3

``|Download|`` the program to the Spark:bit and select **Show console Simulator**. Press bump sensor 1 and observe how the count increases in the serial monitor. Press bump sensor 2 and observe how the count decreases in the serial monitor.