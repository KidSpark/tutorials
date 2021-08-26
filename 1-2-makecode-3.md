```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

```template
basic.forever(function () {
    sparkbitO.rotateMotorModule(2, SparkbitDirection.Clockwise, 100)
})
```

# Introduction to MakeCode

## Step 1 @showdialog

Follow the step-by-step instructions in the curriculum packet for this lesson to assemble the mechanism shown below. Then click the **Ok** button to proceed to the next step of the tutorial.

![1-2-makecode-2](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/1-2-makecode-2.png)

## Step 2

Open the ``||sparkbitO:Spark:bit Outputs||`` container and select the ``||sparkbitO:set light module||`` block and connect it to the bottom of the ``||sparkbitO:rotate motor module||`` block.

```blocks
basic.forever(function () {
    sparkbitO.rotateMotorModule(2, SparkbitDirection.Clockwise, 100)
    sparkbitO.setLightModule(1, SparkbitColor.Green, 100)
})
```

## Step 3

``|Download|`` the program to the Spark:bit. Make sure the Spark:bit is powered on, then observe the mechanism. [Click here](https://youtu.be/ZduFrq8SoWE) to see the mechanism in action.

## Step 4

Adjust the color and brightness values of the ``||sparkbitO:set light module||`` block.

## Step 5

``|Download|`` the program to the Spark:bit. Make sure the Spark:bit is powered on, then observe the mechanism.

## Step 6

Click **Finish** and review the next section in the curriculum packet.