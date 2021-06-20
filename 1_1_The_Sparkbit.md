```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

```template
basic.forever(function () {
    if (SparkbitI.Bump_Sensor(SparkbitI.__inputNumber(1))) {
        SparkbitO.setLightModule(SparkbitO.__outputNumber(1), 23, Colors.Green)
        SparkbitO.rotateMotorDuration(SparkbitO.__outputNumber(2), 100, Directions.Clockwise)
    } else {
        SparkbitO.setLightModule(SparkbitO.__outputNumber(1), 23, Colors.Red)
        SparkbitO.stopMotor(SparkbitO.__outputNumber(2))
    }
})
```

# Introduction to MakeCode

## Step 1

``|Download|`` the following program to the Spark:bit.

## Step 2

Test and observe the mechanism.