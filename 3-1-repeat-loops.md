```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

```template
basic.forever(function () {
    if (sparkbitI.bumpSensor(sparkbitI.__inputNumber(1))) {
    	
    }
})
```

# Repeat Loops

## Step 1

Open the ``||loops:Loops||`` container, select the ``||loops:repeat||`` block, and connect it below ``||logic:then||``. Change the value to **3**.

```blocks
basic.forever(function () {
    if (sparkbitI.bumpSensor(sparkbitI.__inputNumber(1))) {
        for (let index = 0; index < 3; index++) {
        	
        }
    }
})
```

## Step 2

Add a ``||sparkbitO:rotate motor module||`` and a ``||basic:pause||`` block inside the ``||loops:repeat||`` loop. Change the pause to **1 second**.

```blocks
basic.forever(function () {
    if (sparkbitI.bumpSensor(sparkbitI.__inputNumber(1))) {
        for (let index = 0; index < 3; index++) {
            sparkbitO.rotateMotorDuration(sparkbitO.__outputNumber(1), 100, Directions.Clockwise)
            basic.pause(1000)
        }
    }
})
```

## Step 3