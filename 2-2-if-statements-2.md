```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

```template
basic.forever(function () {
    serial.writeLine("" + (sparkbitI.readAngleSensorDeg(DegreePercent.Degree, sparkbitI.__inputNumber(1))))
    if (true) {
    	
    }
    if (true) {
    	
    }
})
```

# If Statements

## Step 1

Open the ``||sparkbitI:Spark:bit Inputs||`` container, select the ``||sparkbitI:angle sensor||`` block with the equal sign and degrees, and place it in the top ``||logic:if-then||`` block by replacing **true**. Change the equal sign (=) to greater than (>) and adjust the degrees to 200.

``` blocks
basic.forever(function () {
    serial.writeLine("" + (sparkbitI.readAngleSensorDeg(DegreePercent.Degree, sparkbitI.__inputNumber(1))))
    if (sparkbitI.testAngleSensorDeg(sparkbitI.__inputNumber(1), LogicCompare.LogicCompareGT, 200)) {
    	
    }
    if (true) {
    	
    }
})
```

## Step 2

Open the ``||sparkbitO:Spark:bit Outputs||`` container, select the ``||sparkbitO:rotate motor module||`` block, and place it in the middle of the top ``||logic:if-then||`` block.

```blocks
basic.forever(function () {
    serial.writeLine("" + (sparkbitI.readAngleSensorDeg(DegreePercent.Degree, sparkbitI.__inputNumber(1))))
    if (sparkbitI.testAngleSensorDeg(sparkbitI.__inputNumber(1), LogicCompare.LogicCompareGT, 200)) {
        sparkbitO.rotateMotorDuration(sparkbitO.__outputNumber(1), 100, Directions.Clockwise)
    }
    if (true) {
    	
    }
})
```

## Step 3

Open the ``||sparkbitI:Spark:bit Inputs||`` container, select the ``||sparkbitI:angle sensor||`` block with the equal sign and degrees, and place it in the bottom ``||logic:if-then||`` block by replacing **true**. Change the equal sign (=) to less than (<) and adjust the degrees to 200.

```blocks
basic.forever(function () {
    serial.writeLine("" + (sparkbitI.readAngleSensorDeg(DegreePercent.Degree, sparkbitI.__inputNumber(1))))
    if (sparkbitI.testAngleSensorDeg(sparkbitI.__inputNumber(1), LogicCompare.LogicCompareGT, 200)) {
        sparkbitO.rotateMotorDuration(sparkbitO.__outputNumber(1), 100, Directions.Clockwise)
    }
    if (sparkbitI.testAngleSensorDeg(sparkbitI.__inputNumber(1), LogicCompare.LogicCompareLT, 200)) {
    	
    }
})
```

## Step 4

Open the ``||sparkbitO:Spark:bit Outputs||`` container, select the ``||sparkbitO:stop motor module||`` block, and place it in the middle of the bottom ``||logic:if-then||`` block.

```blocks
basic.forever(function () {
    serial.writeLine("" + (sparkbitI.readAngleSensorDeg(DegreePercent.Degree, sparkbitI.__inputNumber(1))))
    if (sparkbitI.testAngleSensorDeg(sparkbitI.__inputNumber(1), LogicCompare.LogicCompareGT, 200)) {
        sparkbitO.rotateMotorDuration(sparkbitO.__outputNumber(1), 100, Directions.Clockwise)
    }
    if (sparkbitI.testAngleSensorDeg(sparkbitI.__inputNumber(1), LogicCompare.LogicCompareLT, 200)) {
        sparkbitO.stopMotor(sparkbitO.__outputNumber(1))
    }
})
```

## Step 5

``|Download|`` the program to the Spark:bit and open the **Show console Simulator**. Rotate the angle sensor and observe the mechanism and the serial monitor/plotter.
