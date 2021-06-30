```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

# If Statements

## Step 1

Open the ``||logic:Logic||`` container, select the ``||logic:if-then||`` block, and connect it to the ``||basic:forever||`` function.

``` blocks
basic.forever(function () {
    if (true) {
    	
    }
})
```

## Step 2

Open the ``||sparkbitI:Spark:bit Inputs||`` container, select the ``||sparkbitI:bump sensor||`` block, and place it in the ``||logic:if-then||`` block by replacing **true**.

```blocks
basic.forever(function () {
    if (sparkbitI.bumpSensor(1)) {
    	
    }
})
```

## Step 3

Open the ``||sparkbitO:Spark:bit Outputs||`` container, select the ``||sparkbitO:rotate motor module||`` block, and place it in the middle of the ``||logic:if-then||`` block.

```blocks
basic.forever(function () {
    if (sparkbitI.bumpSensor(1)) {
        sparkbitO.rotateMotorDuration(1, 100, Directions.Clockwise)
    }
})
```

## Step 4

``|Download|`` the program to the Spark:bit. Press the bump sensor and observe the mechanism.