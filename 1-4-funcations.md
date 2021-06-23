```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

# Funcations

## Step 1

Observe how the ball maze can tilt in four directions: left, right, forward, and backward. In order for the ball to move through the maze, the maze must tilt in each direction multiple times.

## Step 2

Expand the ``||advanced:Advanced||`` section, open the ``||functions:Functions||`` container and select **Make a Function**. Change **doSomething** to **left** and click ``||game:Done||``. Functions are used when the same task needs to be performed multiple times in a program.

```blocks
function left () {
}
```

## Step 3

Look at the maze and observe how the motor module that is connected to output 2 on the Spark:bit needs to rotate conterclockwise in order to tilt the maze left. Open the ``||sparkbitO:Spark:bit Outputs||`` container, select the ``||sparkbitO:rotate motor module||`` block and connect to the ``||functions:function left||`` block. Change the output to **2** and the direction to **counterclockwise**.

```blocks
function left () {
    sparkbitO.rotateMotorDuration(sparkbitO.__outputNumber(2), 100, Directions.Counterclockwise)
}
```

## Step 4

Open the ``||basic:Basic||`` container, select the ``||basic:pause||``, and connect it to the bottom of the ``||sparkbitO:rotate motor module||`` block. Change the pause to **1 second** (1000 ms).

```blocks
function left () {
    sparkbitO.rotateMotorDuration(sparkbitO.__outputNumber(2), 100, Directions.Counterclockwise)
    basic.pause(1000)
}
```

## Step 5

Look at the maze and observe how the motor module that is connected to output 2 on the Spark:bit needs to rotate clockwise in order to tilt the maze right. Crate a new ``||functions:Function||`` called **right**. Make sure to include a **1 second** pause.

```blocks
function left () {
    sparkbitO.rotateMotorDuration(sparkbitO.__outputNumber(2), 100, Directions.Counterclockwise)
    basic.pause(1000)
}
function right () {
    sparkbitO.rotateMotorDuration(sparkbitO.__outputNumber(2), 100, Directions.Clockwise)
    basic.pause(1000)
}
```

## Step 6

Create two new ``||functions:Functions||`` called **forward** and **backward**. Make sure the correct output and direction are selected on the ``||sparkbitO:rotate motor module||`` block.

```blocks
function left () {
    sparkbitO.rotateMotorDuration(sparkbitO.__outputNumber(2), 100, Directions.Counterclockwise)
    basic.pause(1000)
}
function right () {
    sparkbitO.rotateMotorDuration(sparkbitO.__outputNumber(2), 100, Directions.Clockwise)
    basic.pause(1000)
}
function forward () {
    sparkbitO.rotateMotorDuration(sparkbitO.__outputNumber(1), 100, Directions.Clockwise)
    basic.pause(1000)
}
function backward () {
    sparkbitO.rotateMotorDuration(sparkbitO.__outputNumber(1), 100, Directions.Counterclockwise)
    basic.pause(1000)
}
```
