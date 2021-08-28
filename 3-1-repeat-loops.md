```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

```template
basic.forever(function () {
    if (sparkbitI.bumpSensorIsPressed(SparkbitInPort.Input1)) {
    	
    }
})
```

# Repeat Loops

## Step 1 @showdialog

Follow the step-by-step instructions in the curriculum packet for this lesson to assemble the mechanism shown below. Then click the **Ok** button to proceed to the next step of the tutorial.

![repear-loops](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/3-1-repeat-loops.png)

## Step 2

Open the ``||loops:Loops||`` category, select the ``||loops:repeat||`` block, and connect it below ``||logic:then||``. Change the value to **3**.

```blocks
basic.forever(function () {
    if (sparkbitI.bumpSensorIsPressed(SparkbitInPort.Input1)) {
        for (let index = 0; index < 3; index++) {
        	
        }
    }
})
```

## Step 3

Add a ``||sparkbitO:rotate motor module||`` and a ``||basic:pause||`` block inside the ``||loops:repeat||`` loop. Change the pause to **1 second**.

```blocks
basic.forever(function () {
    if (sparkbitI.bumpSensorIsPressed(SparkbitInPort.Input1)) {
        for (let index = 0; index < 3; index++) {
            sparkbitO.rotateMotorModule(SparkbitOutPort.Output1, SparkbitDirection.Clockwise, 100)
            basic.pause(1000)
        }
    }
})
```

## Step 4

Add a ``||sparkbitO:stop motor module||`` and a ``||basic:pause||`` block to the ``||loops:repeat||`` loop. Change the pause to **1 second**.

```blocks
basic.forever(function () {
    if (sparkbitI.bumpSensorIsPressed(SparkbitInPort.Input1)) {
        for (let index = 0; index < 3; index++) {
            sparkbitO.rotateMotorModule(SparkbitOutPort.Output1, SparkbitDirection.Clockwise, 100)
            basic.pause(1000)
            sparkbitO.stopMotorModule(SparkbitOutPort.Output1)
            basic.pause(1000)
        }
    }
})
```

## Step 5

Follow the steps below to download and test the program:
* ``|Download|`` the program to the Spark:bit.
* Make sure the Spark:bit is powered on.
* Press the bump sensor and observe the mechanism.
* [Click here](https://youtu.be/d6GwBTKQqAs) to see a video of the mechanism in action.

## Step 6

Experiment by changing the number of times you want the commands to repeat. ``|Download|`` the program and observe the mechanism.

## Step 7

Power off the Spark:bit, then click **Finish** and review the next section in the curriculum packet.