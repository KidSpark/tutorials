```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

```template
basic.forever(function () {
    serial.writeLine("" + (sparkbitI.proximity(1, 2)))
    if (true) {
        sparkbitO.setLightModule(1, 100, Colors.Green)
    } else {
        sparkbitO.setLightModule(1, 100, Colors.Red)
    }
})
```

# Creating a Proximity Sensor

## Step 1

Open the ``||logic:Logic||`` container, select the ``||logic:not||`` block, and place it after ``||logic:if||`` replacing **true**.

```blocks
basic.forever(function () {
    serial.writeLine("" + (sparkbitI.proximity(1, 2)))
    if (!(false)) {
        sparkbitO.setLightModule(1, 100, Colors.Green)
    } else {
        sparkbitO.setLightModule(1, 100, Colors.Red)
    }
})
```

## Step 2

Open the ``||sparkbitI:Spark:bit Inputs||`` container, select the ``||sparkbitI:IR Tx/Rx||`` block, and place it in the ``||logic:not||`` block.

```blocks
basic.forever(function () {
    serial.writeLine("" + (sparkbitI.proximity(1, 2)))
    if (!(sparkbitI.proximity(1, 2))) {
        sparkbitO.setLightModule(1, 100, Colors.Green)
    } else {
        sparkbitO.setLightModule(1, 100, Colors.Red)
    }
})
```

## Step 3

``|Download|`` the program to the Spark:bit and select **Show console Simulator**. Test and observe the mechanism by placing your hand in front of the IR transmitter. Observe the boolean values in the serial monitor. 