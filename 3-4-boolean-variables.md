```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

```template
basic.forever(function () {
    if (sparkbitI.bumpSensor(sparkbitI.__inputNumber(1))) {
        if (true) {
            sparkbitO.setLightModule(sparkbitO.__outputNumber(1), 100, Colors.Red)
        } else {
            sparkbitO.setLightModule(sparkbitO.__outputNumber(1), 100, Colors.Green)
        }
        basic.pause(500)
    }
})
```

# Boolean Variables

## Step 1




```blocks
let toggle = false
serial.writeLine("" + (toggle))
basic.forever(function () {
    if (sparkbitI.bumpSensor(sparkbitI.__inputNumber(1))) {
        if (toggle) {
            sparkbitO.setLightModule(sparkbitO.__outputNumber(1), 100, Colors.Red)
            toggle = false
        } else {
            sparkbitO.setLightModule(sparkbitO.__outputNumber(1), 100, Colors.Green)
            toggle = true
        }
        basic.pause(500)
        serial.writeLine("" + (toggle))
    }
})
```