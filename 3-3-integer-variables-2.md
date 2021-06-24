```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

```template
let count = 0
serial.writeLine("" + (count))
basic.forever(function () {
    if (sparkbitI.bumpSensor(sparkbitI.__inputNumber(1))) {
        count += 1
        serial.writeLine("" + (count))
        basic.pause(500)
    }
})
```

# Integer Variables

## Step 1

