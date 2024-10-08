```package
Sparkbit=github:kidspark/pxt-sparkbit
```
# Pauses

## Step 1 @showdialog

Follow the step-by-step instructions in the curriculum packet for this lesson to assemble  the mechanism shown below. Then click the **Ok** button to proceed to the next step of the tutorial.

![1-3-pauses-1](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/1-3-pauses-1.png)

## Step 2

Open the ``||sparkbitO:Spark:bit Outputs||`` category and select the ``||sparkbitO:rotate motor module||`` block. Connect it to the ``||basic:forever||`` function. **Change output to 2**.

```blocks
basic.forever(function () {
    sparkbitO.rotateMotorModule(SparkbitOutPort.Output2, SparkbitDirection.Clockwise, 100)
})
```

## Step 3

Open the ``||basic:Basic||`` category and select the ``||basic:pause||`` block. Connect it to the bottom of the ``||sparkbitO:rotate motor module||`` block.

```blocks
basic.forever(function () {
    sparkbitO.rotateMotorModule(SparkbitOutPort.Output2, SparkbitDirection.Clockwise, 100)
    basic.pause(100)
})
```

## Step 4

Open the ``||sparkbitO:Spark:bit Outputs||`` category and select the ``||sparkbitO:stop motor module||`` block. Connect it to the bottom of the ``||basic:pause||`` block. **Change output to 2**.

```blocks
basic.forever(function () {
    sparkbitO.rotateMotorModule(SparkbitOutPort.Output2, SparkbitDirection.Clockwise, 100)
    basic.pause(100)
    sparkbitO.stopMotorModule(SparkbitOutPort.Output2)
})
```

## Step 5

Connect a ``||basic:pause||`` block to the bottom of the ``||sparkbitO:stop motor module||`` block.

```blocks
basic.forever(function () {
    sparkbitO.rotateMotorModule(SparkbitOutPort.Output2, SparkbitDirection.Clockwise, 100)
    basic.pause(100)
    sparkbitO.stopMotorModule(SparkbitOutPort.Output2)
    basic.pause(100)
})
```

## Step 6

``|Download|`` the program to the Spark:bit. Make sure the Spark:bit is powered on, then observe the mechanism.

## Step 7

Adjust both ``||basic:pause||`` times to **1000ms** (1 second). 

## Step 8

``|Download|`` the program to the Spark:bit. Make sure the Spark:bit is powered on, then observe the mechanism. [Click here](https://kidsparkeducation.org/media/2356) to see the mechanism in action.

## Step 9

Power off the Spark:bit, then click **Finish** and review the next section of the curriculum packet.
