```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

```template
basic.forever(function () {
    sparkbitO.rotateMotorDuration(2, Directions.Clockwise, 100)
    basic.pause(1000)
    sparkbitO.stopMotor(2)
    basic.pause(1000)
})
```

# Pauses

## Step 1 @showdialog

Follow the step-by-step instructions in the curriculum packet for this lesson to assemble the mechanism shown below. Then click the **Ok** button to proceed to the next step of the tutorial.

![1-3-pauses-1](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/1-3-pauses-1.png)

## Step 2

Open the ``||sparkbitO:Spark:bit Outputs||`` container and select the ``||sparkbitO:set light module||`` block. Connect it to the bottom of the ``||sparkbitO:rotate motor module||`` block.

```blocks
basic.forever(function () {
    sparkbitO.rotateMotorDuration(2, Directions.Clockwise, 100)
    sparkbitO.setLightModule(1, Colors.Green, 100)
    basic.pause(1000)
    sparkbitO.stopMotor(2)
    basic.pause(1000)
})
```
## Step 3

Select another ``||sparkbitO:set light module||`` block and connect it to the bottom of the ``||sparkbitO:stop motor module||`` block. Change color to **red**.

```blocks
basic.forever(function () {
    sparkbitO.rotateMotorDuration(2, Directions.Clockwise, 100)
    sparkbitO.setLightModule(1, Colors.Green, 100)
    basic.pause(1000)
    sparkbitO.stopMotor(2)
    sparkbitO.setLightModule(1, Colors.Red, 100)
    basic.pause(1000)
})
```
## Step 4

``|Download|`` the program to the Spark:bit. Make sure the Spark:bit is powered on, then observe the mechanism. [Click here](https://youtu.be/rxfwJP0eej0) to see the mechanism in action.

## Step 5

Adjust the ``||basic:pause||`` times.

## Step 6

``|Download|`` the program to the Spark:bit and observe the mechanism.

## Step 7

Click **Finish** and review the next section in the curriculum packet.