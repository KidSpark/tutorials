```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

# If Statements

## Step 1 @showdialog

Follow the step-by-step instructions in the curriculum packet for this lesson to assemble the mechanism shown below. Then click the **Ok** button to proceed to the next step of the tutorial.

![if-statements-1](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/2-2-if-statements-1.png)

##Step 2

Open the ``||logic:Logic||`` category, select the ``||logic:if||`` block, and connect it to the ``||basic:forever||`` function.

``` blocks
basic.forever(function () {
    if (true) {
    	
    }
})
```

## Step 3

Open the ``||sparkbitI:Spark:bit Inputs||`` category, select the ``||sparkbitI:bump sensor||`` block, and place it in the ``||logic:if||`` block by replacing **true**.

```blocks
basic.forever(function () {
    if (sparkbitI.bumpSensorIsPressed(SparkbitInPort.Input1)) {
    	
    }
})
```

## Step 4

Open the ``||sparkbitO:Spark:bit Outputs||`` category, select the ``||sparkbitO:rotate motor module||`` block, and place it in the middle of the ``||logic:if||`` block.

```blocks
basic.forever(function () {
    if (sparkbitI.bumpSensorIsPressed(SparkbitInPort.Input1)) {
        sparkbitO.rotateMotorModule(SparkbitOutPort.Output1, SparkbitDirection.Clockwise, 100)
    }
})
```

## Step 5

Follow the steps below to download and test the program:
* ``|Download|`` the program to the Spark:bit.
* Make sure the Spark:bit is powered on.
* Press the bump sensor and observe the mechanism.
* [Click here](https://youtu.be/29-e-DE9Xeg) to see a video of the mechanism in action.
* Power off the Spark:bit.

## Step 6

Click **Finish** and review the next section in the curriculum packet.