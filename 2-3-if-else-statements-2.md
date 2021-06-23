```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

```template
basic.forever(function () {
    serial.writeLine("" + (sparkbitI.readAngleSensorDeg(DegreePercent.Percent, sparkbitI.__inputNumber(1))))
    if (true) {
        sparkbitO.setLightModule(sparkbitO.__outputNumber(1), 100, Colors.Red)
    } else {
        sparkbitO.stopLight(sparkbitO.__outputNumber(1))
    }
})
```

# If/Else Statements

## Step 1

Open the ``||sparkbitI:Spark:bit Inputs||`` container, select the ``||sparkbitI:angle sensor||`` block with the equal sign and percent (%), and place it after ``||logic:if||`` replacing **true**. Change the equal sign (=) to greater than (>) and adjust the percent to 70.

```blocks
basic.forever(function () {
    serial.writeLine("" + (sparkbitI.readAngleSensorDeg(DegreePercent.Percent, sparkbitI.__inputNumber(1))))
    if (sparkbitI.testAngleSensorPercent(sparkbitI.__inputNumber(1), LogicCompare.LogicCompareGT, 70)) {
        sparkbitO.setLightModule(sparkbitO.__outputNumber(1), 100, Colors.Red)
    } else {
        sparkbitO.stopLight(sparkbitO.__outputNumber(1))
    }
})
```

## Step 2

``|Download|`` the program to the Spark:bit and select **Show console Simulator**. Rotate the angle sensor and observe the light module and the serial monitor.