```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

```template
basic.forever(function () {
    sparkbitO.rotateMotorDuration(sparkbitO.__outputNumber(2), 100, Directions.Clockwise)
    basic.pause(1000)
    sparkbitO.stopMotor(sparkbitO.__outputNumber(2))
    basic.pause(1000)
})
```

# Pauses

## Step 1

Open the ``||sparkbitO:Spark:bit Outputs||`` container and select the ``||sparkbitO:set light module||`` block. Connect it to the bottom of the ``||sparkbitO:rotate motor module||`` block.

```blocks
basic.forever(function () {
    sparkbitO.rotateMotorDuration(sparkbitO.__outputNumber(2), 100, Directions.Clockwise)
    sparkbitO.setLightModule(sparkbitO.__outputNumber(1), 100, Colors.Green)
    basic.pause(1000)
    sparkbitO.stopMotor(sparkbitO.__outputNumber(2))
    basic.pause(1000)
})
```
## Step 2

Select another ``||sparkbitO:set light module||`` block and connect it to the bottom of the ``||sparkbitO:stop motor module||`` block.

```blocks
basic.forever(function () {
    sparkbitO.rotateMotorDuration(sparkbitO.__outputNumber(2), 100, Directions.Clockwise)
    sparkbitO.setLightModule(sparkbitO.__outputNumber(1), 100, Colors.Green)
    basic.pause(1000)
    sparkbitO.stopMotor(sparkbitO.__outputNumber(2))
    sparkbitO.setLightModule(sparkbitO.__outputNumber(1), 100, Colors.Red)
    basic.pause(1000)
})
```
## Step 3

``|Download|`` the program to the Spark:bit and observe the mechanism.

## Step 4

Adjust the ``||basic:pause||`` times. ``|Download|`` the program to the Spark:bit and observe the mechanism.