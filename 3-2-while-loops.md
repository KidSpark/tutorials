```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

```template
basic.forever(function () {
    if (sparkbitI.bumpSensorIsPressed(SparkbitInPort.Input1)) {
    	
    }
})
```

# While Loops

## Step 1 @showdialog

Follow the step-by-step instructions in the curriculum packet for this lesson to assemble the mechanism shown below. Then click the **Ok** button to proceed to the next step of the tutorial.

![if-statements-1](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/3-2-while-loops.png)

## Step 2

Open the ``||loops:Loops||`` category, select the ``||loops:while||`` block, and connect it below ``||logic:then||``.

```blocks
basic.forever(function () {
    if (sparkbitI.bumpSensorIsPressed(SparkbitInPort.Input1)) {
        while (false) {
        	
        }
    }
})
```

## Step 3

* Add a ``||logic:<not>||`` block to the ``||loops:while||`` loop.
* Add a ``||sparkbitI:bump sensor||`` block inside the ``||logic:<not>||`` block, and change to **input 2**.

```blocks
basic.forever(function () {
    if (sparkbitI.bumpSensorIsPressed(SparkbitInPort.Input1)) {
        while (!(sparkbitI.bumpSensorIsPressed(SparkbitInPort.Input2))) {
        	
        }
    }
})
```

## Step 4

Add a ``||sparkbitO:set light module||`` block inside the ``||loops:while||`` loop, and change the color to **red**.

```blocks
basic.forever(function () {
    if (sparkbitI.bumpSensorIsPressed(SparkbitInPort.Input1)) {
        while (!(sparkbitI.bumpSensorIsPressed(SparkbitInPort.Input2))) {
            sparkbitO.setLightModule(SparkbitOutPort.Output1, SparkbitColor.Red, 100)
        }
        
    }
})
```

## Step 5

Add a ``||sparkbitO:turn off light module||`` block outside the ``||loops:while||`` loop but inside the ``||logic:if||`` statement.

```blocks
basic.forever(function () {
    if (sparkbitI.bumpSensorIsPressed(SparkbitInPort.Input1)) {
        while (!(sparkbitI.bumpSensorIsPressed(SparkbitInPort.Input2))) {
            sparkbitO.setLightModule(SparkbitOutPort.Output1, SparkbitColor.Red, 100)
        }
        sparkbitO.stopLightModule(SparkbitOutPort.Output1)
    }
})
```

## Step 6

Follow the steps below to download and test the program:
* ``|Download|`` the program to the Spark:bit.
* Make sure the Spark:bit is powered on.
* Press the bump sensor and observe the mechanism.
* [Click here](https://kidsparkeducation.org/media/2368) to see a video of the mechanism in action.
* Power off the Spark:bit.

## Step 7

Click **Finish** and review the next section in the curriculum packet.