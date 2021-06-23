```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

```template
basic.forever(function () {
    serial.writeLine("" + (sparkbitI.bumpSensor(sparkbitI.__inputNumber(1))))
})
```

# If/Else Statements

## Step 1

Open the ``||logic:Logic||`` container, select the ``||logic:if-then-else||`` block, and connect it to the bottom of the ``||serial:serial write line||`` block.

```blocks
basic.forever(function () {
    serial.writeLine("" + (sparkbitI.bumpSensor(sparkbitI.__inputNumber(1))))
    if (true) {
    	
    } else {
    	
    }
})
```

## Step 2

Open the ``||sparkbitI:Spark:bit Inputs||`` container, select the ``||sparkbitI:bump sensor||`` block, and place it in the ``||logic:if-then-else||`` block by replacing **true**.

```blocks
basic.forever(function () {
    serial.writeLine("" + (sparkbitI.bumpSensor(sparkbitI.__inputNumber(1))))
    if (sparkbitI.bumpSensor(sparkbitI.__inputNumber(1))) {
    	
    } else {
    	
    }
})
```

## Step 3

Open the ``||sparkbitO:Spark:bit Outputs||`` container, select the ``||sparkbitO:set light module


```blocks
basic.forever(function () {
    serial.writeLine("" + (sparkbitI.bumpSensor(sparkbitI.__inputNumber(1))))
    if (sparkbitI.bumpSensor(sparkbitI.__inputNumber(1))) {
        sparkbitO.setLightModule(sparkbitO.__outputNumber(1), 100, Colors.Green)
    } else {
        sparkbitO.stopLight(sparkbitO.__outputNumber(1))
    }
})
```