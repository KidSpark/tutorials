```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

```template
basic.forever(function () {
    sparkbitO.rotateMotorDuration(sparkbitO.__outputNumber(2), 100, Directions.Clockwise)
})
```

# Introduction to MakeCode

## Step 1

Open ``||sparkbitO:Spark:bit Outputs||`` container and select the ``||sparkbitO:set light module||`` block and connect it to the bottom of the ``||sparkbitO:rotate motor module||`` block.

```blocks
basic.forever(function () {
    sparkbitO.rotateMotorDuration(sparkbitO.__outputNumber(2), 100, Directions.Clockwise)
    sparkbitO.setLightModule(sparkbitO.__outputNumber(1), 100, Colors.Green)
})
```

## Step 2

``|Download|`` the program to the Spark:bit and observe the mechanism. Tip - Make sure Spark:bit is powered on.

## Step 3

Adjust the color and brightness values of the ``||sparkbitO:set light module||`` block.

## Step 4 

``|Download|`` the program to the Spark:bit and observe the mechanism.