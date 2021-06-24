```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

```template
basic.forever(function () {
    if (sparkbitI.bumpSensor(sparkbitI.__inputNumber(1))) {
    	
    }
})
```

# Integer Variables

## Step 1

Open the ``||variables:Variables||`` container, select **Make a Variable**, name it **count**, and select ``||game:Ok||``. Select the ``||variables:change count||`` block and connect it below ``||logic:then||``.

```blocks
let count = 0
basic.forever(function () {
    if (sparkbitI.bumpSensor(sparkbitI.__inputNumber(1))) {
        count += 1
    }
})
```

## Step 2

Add a ``||serial:serial write line||`` block to ``||basic:on start||``.

```blocks
let count = 0
serial.writeLine("")
basic.forever(function () {
    if (sparkbitI.bumpSensor(sparkbitI.__inputNumber(1))) {
        count += 1
    }
})
```

## Step 3

Add a ``||serial:serial write line||`` block and a ``||basic:pause||`` block to the ``||logic:if-then||`` statement. Change pause to **500 ms**.

```blocks
let count = 0
serial.writeLine("")
basic.forever(function () {
    if (sparkbitI.bumpSensor(sparkbitI.__inputNumber(1))) {
        count += 1
        serial.writeLine("")
        basic.pause(500)
    }
})
```

## Step 4

Open the ``||variables:Variable||`` container, select the ``||variables:count||`` block, and add it to both of the ``||serial:serial write line||`` blocks.

```blocks
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

## Step 5

``|Download|`` the program to the Spark:bit and select **Show console Simulator**. Press the bump sensor and observe the serial monitor.