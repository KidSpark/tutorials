```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

```template
basic.forever(function () {
    if (sparkbitI.bumpSensor(1)) {
        sparkbitO.setLightModule(1, 23, Colors.Green)
        sparkbitO.rotateMotorDuration(2, 100, Directions.Clockwise)
    } else {
        sparkbitO.setLightModule(1, 23, Colors.Red)
        sparkbitO.stopMotor(2)
    }
})
```

# The Spark:bit

## Step 1

``|Download|`` the following program to the Spark:bit.

## Step 2

Test and observe the mechanism.