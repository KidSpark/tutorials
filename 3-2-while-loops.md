```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

```template
basic.forever(function () {
    if (sparkbitI.bumpSensor(sparkbitI.__inputNumber(1))) {
    	
    }
})
```

# While Loops

## Step 1

Open the ``||loops:Loops||`` container, select the ``||loops:while||`` block, and connect it below ``||logic:then||``.

```blocks
basic.forever(function () {
    if (sparkbitI.bumpSensor(sparkbitI.__inputNumber(1))) {
        while (true) {
        	
        }
    }
})
```

## Step 2

Add a ``||logic:not||`` block to the ``||loops:while||`` loop.

```blocks
basic.forever(function () {
    if (sparkbitI.bumpSensor(sparkbitI.__inputNumber(1))) {
        while (!(false)) {
        	
        }
    }
})
```

## Step 3





```blocks
basic.forever(function () {
    if (sparkbitI.bumpSensor(sparkbitI.__inputNumber(1))) {
        while (!(sparkbitI.bumpSensor(sparkbitI.__inputNumber(2)))) {
            sparkbitO.setLightModule(sparkbitO.__outputNumber(1), 100, Colors.Red)
        }
        sparkbitO.stopLight(sparkbitO.__outputNumber(1))
    }
})
```