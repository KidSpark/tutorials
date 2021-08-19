```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

```template
basic.forever(function () {
    if (sparkbitI.bumpSensor(1)) {
        sparkbitO.setLightModule(1, 23, Colors.Green)
        sparkbitO.rotateMotorDuration(2, 100, Directions.Clockwise)
    } else {
        sparkbitO.setLightModule(1, 23, Colors.Red)
        sparkbitO.stopMotor(2)
    }
})
```

# The Spark:bit

## Step 1 @showdialog

Follow the step-by-step instructions in the curriculum packet for this lesson to assemble the mechanism shown below. Then click **OK** to proceed to the next step of the tutorial.

![MakeCode screen](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/1-1-sparkbit.png)

## Step 2

``|Download|`` the following program to the Spark:bit (program already completed).

## Step 3 

Make sure the Spark:bit is powered on, then press the Bump Sensor and observe the mechanism. [Click here](https://youtu.be/LGxoURbz980) to see the mechanism in action.

## Step 4

Click **Finish** and review the next section of the curriculum packet.