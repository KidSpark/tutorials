```package
Sparkbit=github:kidspark/pxt-sparkbit
```

# Introduction to MakeCode

## Step 1 @showdialog

Follow the step-by-step instructions in the curriculum packet for this lesson to assemble the mechanism shown below. Then click the **Ok** button to proceed to the next step of the turorial.

![1-2-makecode-2](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/1-2-makecode-2.png)

## Step 2
Open the ``||sparkbitO:Spark:bit Outputs||`` category and select a ``||sparkbitO:rotate motor module||`` block. Drag the block to the workspace and connect it to the ``||basic:forever||`` function. **Change the output to 2**.

```blocks
basic.forever(function () {
    sparkbitO.rotateMotorModule(SparkbitOutPort.Output2, SparkbitDirection.Clockwise, 100)
})
```

## Step 3

``|Download|`` the program to the Spark:bit. Make sure the Spark:bit is powered on, then observe the mechanism. [Click here](https://kidsparkeducation.org/media/2354) to see the mechanism in action.

## Step 4

Adjust the direction and speed of the ``||sparkbitO:rotate motor module||`` block. 

## Step 5 

``|Download|`` the program to the Spark:bit. Make sure the Spark:bit is powered on, then observe the mechanism.

## Step 6

Power off the Spark:bit, then click **Finish** and review the next section in the curriculum packet.
