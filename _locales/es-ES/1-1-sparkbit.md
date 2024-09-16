```package
Sparkbit=github:kidspark/pxt-sparkbit
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

# El Spark:bit

## Paso 1

``|Download|`` el siguiente programa para el Spark:bit.

## Paso 2

Pruebe y observe el mecanismo.
