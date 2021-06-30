```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

```template
basic.forever(function () {
    if (sparkbitI.bumpSensor(1)) {
    	
    }
})
```

# While Loops

## Step 1

Open the ``||loops:Loops||`` container, select the ``||loops:while||`` block, and connect it below ``||logic:then||``.

```blocks
basic.forever(function () {
    if (sparkbitI.bumpSensor(1)) {
        while (true) {
        	
        }
    }
})
```

## Step 2

Add a ``||logic:not||`` block to the ``||loops:while||`` loop.

```blocks
basic.forever(function () {
    if (sparkbitI.bumpSensor(1)) {
        while (!(false)) {
        	
        }
    }
})
```

## Step 3

Add a ``||sparkbitI:bump sensor||`` block inside the ``||logic:not||`` block, and change to **input 2**.

```blocks
basic.forever(function () {
    if (sparkbitI.bumpSensor(1)) {
        while (!(sparkbitI.bumpSensor(2))) {
        	
        }
    }
})
```

## Step 4

Add a ``||sparkbitO:set light module||`` block inside the ``||loops:while||`` loop, and change the color to **red**. Add a ``||sparkbitO:turn off light module||`` block outside the ``||loops:while||`` loop but inside the ``||logic:if-then||`` statement.

```blocks
basic.forever(function () {
    if (sparkbitI.bumpSensor(1)) {
        while (!(sparkbitI.bumpSensor(2))) {
            sparkbitO.setLightModule(1, 100, Colors.Red)
        }
        sparkbitO.stopLight(1)
    }
})
```

## Step 5

``|Download|`` the program to the Spark:bit, press the bump sensors, and observe the mechanism.