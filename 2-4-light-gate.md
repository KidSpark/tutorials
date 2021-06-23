```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

```template
basic.forever(function () {
    serial.writeLine("")
    if (true) {
        sparkbitO.setLightModule(sparkbitO.__outputNumber(1), 100, Colors.Red)
    } else {
        sparkbitO.setLightModule(sparkbitO.__outputNumber(1), 100, Colors.Green)
    }
})
```

# Creating a Light Gate

## Step 1

Open the ``||sparkbitI:Spark:bit Inputs||`` container, select the ``||sparkbitI:IR Tx/Rx||`` block, and place it in the ``||serial:serial write line||`` block. Change receiver to **input 2**.

```blocks
basic.forever(function () {
    serial.writeLine("" + (sparkbitI.proximity(sparkbitI.__inputNumber(1), sparkbitI.__inputNumber(2))))
    if (true) {
        sparkbitO.setLightModule(sparkbitO.__outputNumber(1), 100, Colors.Red)
    } else {
        sparkbitO.setLightModule(sparkbitO.__outputNumber(1), 100, Colors.Green)
    }
})
```

## Step 2

Place another ``||sparkbitI:IR Tx/Rx||`` block after the ``||logic:if||`` replacing **true**. Change receiver to **input 2**.

```blocks
basic.forever(function () {
    serial.writeLine("" + (sparkbitI.proximity(sparkbitI.__inputNumber(1), sparkbitI.__inputNumber(2))))
    if (sparkbitI.proximity(sparkbitI.__inputNumber(1), sparkbitI.__inputNumber(2))) {
        sparkbitO.setLightModule(sparkbitO.__outputNumber(1), 100, Colors.Red)
    } else {
        sparkbitO.setLightModule(sparkbitO.__outputNumber(1), 100, Colors.Green)
    }
})
```

## Step 3

``|Download|`` the program to the Spark:bit and select **Show console Simulator**. Test and observe mechanism by placing your finger between the IR transmitter and receiver. Observe the boolean values in the serial monitor. 