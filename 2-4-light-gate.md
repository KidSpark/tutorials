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

## Step 1

Open the ``||sparkbitI:Spark:bit Inputs||`` container, select the ``||sparkbitI:IR Tx/Rx||`` block, and place it in the ``||serial:serial write line||`` block.

```blocks
basic.forever(function () {
    serial.writeLine("" + (sparkbitI.proximity(1, 2)))
    if (true) {
        sparkbitO.setLightModule(1, 100, Colors.Red)
    } else {
        sparkbitO.setLightModule(1, 100, Colors.Green)
    }
})
```

## Step 2

Place another ``||sparkbitI:IR Tx/Rx||`` block after the ``||logic:if||`` replacing **true**.

```blocks
basic.forever(function () {
    serial.writeLine("" + (sparkbitI.proximity(1, 2)))
    if (sparkbitI.proximity(1, 2)) {
        sparkbitO.setLightModule(1, 100, Colors.Red)
    } else {
        sparkbitO.setLightModule(1, 100, Colors.Green)
    }
})
```

## Step 3

``|Download|`` the program to the Spark:bit and select **Show console Simulator**. Test and observe the mechanism by placing your finger between the IR transmitter and receiver. Observe the boolean values in the serial monitor. 