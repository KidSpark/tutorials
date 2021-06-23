```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

# Analog vs. Digital Sensors

## Step 1

Expand the ``||advanced:Advanced||`` section, open the ``||serial:Serial||`` container, select the ``||serial:serial write line||`` block, and connect it to the ``||basic:forever||`` function.

```blocks
basic.forever(function () {
    serial.writeLine("")
})
```
## Step 2

Open the ``||sparkbitI:Spark:bit Inputs||`` container, select the ``||sparkbitI:angle sensor||`` block, and place it in the ``||serial:serial write line||`` block.

```blocks
basic.forever(function () {
    serial.writeLine("" + (sparkbitI.readAngleSensorDeg(DegreePercent.Percent, sparkbitI.__inputNumber(1))))
})
```

## Step 3

Open the ``||sparkbitO:Spark:bit Outputs||`` container, select the ``||sparkbitO:rotate motor module||`` block, and connect to the bottom of the ``||serial:serial write line||`` block.

``` blocks
basic.forever(function () {
    serial.writeLine("" + (sparkbitI.readAngleSensorDeg(DegreePercent.Percent, sparkbitI.__inputNumber(1))))
    sparkbitO.rotateMotorDuration(sparkbitO.__outputNumber(1), 100, Directions.Clockwise)
})
```

## Step 4

Open the ``||sparkbitI:Spark:bit Inputs||`` container, select the ``||sparkbitI:angle sensor||`` block, and place it in the speed portion of the ``||sparkbitO:rotate motor module||`` block. Change **degrees (°)** to **percent (%)**.

```blocks
basic.forever(function () {
    serial.writeLine("" + (sparkbitI.readAngleSensorDeg(DegreePercent.Percent, sparkbitI.__inputNumber(1))))
    sparkbitO.rotateMotorDuration(sparkbitO.__outputNumber(1), sparkbitI.readAngleSensorDeg(DegreePercent.Percent, sparkbitI.__inputNumber(1)), Directions.Clockwise)
})
```

## Step 5

``|Download|`` the program to the Spark:bit. Select ``|Show console Simulator|`` located under the micro:bit simulator and observe the serial monitor and plotter. Rotate the angle sensor and ovserve the speed of the motor, as well as, the serial monitor and plotter.

