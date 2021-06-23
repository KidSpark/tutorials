```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```
# Pauses

## Step 1

Open the ``||sparkbitO:Spark:bit Outputs||`` container and select the ``||sparkbitO:rotate motor module||`` block. Connect it to the ``||basic:forever||`` function.

```blocks
basic.forever(function () {
    sparkbitO.rotateMotorDuration(sparkbitO.__outputNumber(2), 100, Directions.Clockwise)
})
```

## Step 2

Open the ``||basic:basic||`` container and select the ``||basic:pause||`` block. Connect it to the bottom of the ``||sparkbitO:rotate motor module||`` block.

```blocks
basic.forever(function () {
    sparkbitO.rotateMotorDuration(sparkbitO.__outputNumber(2), 100, Directions.Clockwise)
    basic.pause(1000)
})
```

## Step 3

Open the ``||sparkbitO:Spark:bit Outputs||`` container and select the ``||sparkbitO:stop motor module||`` block. Connect it to the bottom of the ``||basic:pause||`` block.

```blocks
basic.forever(function () {
    sparkbitO.rotateMotorDuration(sparkbitO.__outputNumber(2), 100, Directions.Clockwise)
    basic.pause(1000)
    sparkbitO.stopMotor(sparkbitO.__outputNumber(2))
})
```

## Step 4

Connect a ``||basic:pause||`` block to the bottom of the ``||sparkbitO:stop motor module||`` block.

```blocks
basic.forever(function () {
    sparkbitO.rotateMotorDuration(sparkbitO.__outputNumber(2), 100, Directions.Clockwise)
    basic.pause(1000)
    sparkbitO.stopMotor(sparkbitO.__outputNumber(2))
    basic.pause(1000)
})
```

## Step 5

``|Download|`` the program to the Spark:bit and observe the mechanism.

## Step 6

Adjust the ``||basic:pause||`` times. ``|Download|`` the program to the Spark:bit and observe the mechanism.