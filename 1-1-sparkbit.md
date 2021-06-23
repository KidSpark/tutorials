```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

```template
basic.forever(function () {
    if (sparkbitI.bumpSensor(sparkbitI.__inputNumber(1))) {
        sparkbitO.setLightModule(sparkbitO.__outputNumber(1), 23, Colors.Green)
        sparkbitO.rotateMotorDuration(sparkbitO.__outputNumber(2), 100, Directions.Clockwise)
    } else {
        sparkbitO.setLightModule(sparkbitO.__outputNumber(1), 23, Colors.Red)
        sparkbitO.stopMotor(sparkbitO.__outputNumber(2))
    }
})
```

# The Spark:bit

## Step 1

``|Download|`` the following program to the Spark:bit.

## Step 2

Test and observe the mechanism.