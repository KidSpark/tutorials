```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

# Funcations

## Step 1

Defining ``||advanced:Advanced||`` and  ``||functions:functions||``

```blocks
function right () {
    sparkbitO.rotateMotorDuration(sparkbitO.__outputNumber(2), 100, Directions.Clockwise)
    basic.pause(1000)
}
function left () {
    sparkbitO.rotateMotorDuration(sparkbitO.__outputNumber(2), 100, Directions.Counterclockwise)
    basic.pause(1000)
}
function backward () {
    sparkbitO.rotateMotorDuration(sparkbitO.__outputNumber(1), 100, Directions.Counterclockwise)
    basic.pause(1000)
}
function forward () {
    sparkbitO.rotateMotorDuration(sparkbitO.__outputNumber(1), 100, Directions.Clockwise)
    basic.pause(1000)
}
right()
forward()
left()
right()
left()
right()
backward()
left()
right()
left()
```

