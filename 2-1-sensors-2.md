```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

```template
basic.forever(function () {
    serial.writeLine("")
})
```

# Analog vs. Digital Sensors

## Step 1

Open the ``||sparkbitI:Spark:bit Inputs||`` container, select a ``|sparkbitI:bump sensor||`` block, and place it in the ``||serial:serial write line||`` block. 

```blocks
basic.forever(function () {
    serial.writeLine("" + (sparkbitI.bumpSensor(sparkbitI.__inputNumber(1))))
})
```

## Step 2

``|Download|`` the program to the Spark:bit and select **Show console Simulator**. Observe how the serial monitor displays the text **false**. Press and hold the bump sensor and observe the serial monitor.