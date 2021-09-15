```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

# Functions

## Step 1 @showdialog

Follow the step-by-step instructions in the curriculum packet for this lesson to assemble the maze show below. Then click the **Ok** button to proceed to the next step of the tutorial. 

![1-4-functions](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/1-4-functions.png)

## Step 2 @showdialog

Observe how the ball maze can tilt in four directions: left, right, forward, and backward. In order for the ball to move through the maze, the maze must tilt in each direction multiple times.

![1-4-maze-directions](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/1-4-maze-directions.png)

## Step 3

Expand the **Advanced** section, open the ``||functions:Functions||`` category, and select **Make a Function**. Change **doSomething** to **left** and click **Done**.

A function is a named section of a program that performs a specific task. Functions are used when the same task needs to be performed multiple times in a program.

```blocks
function left () {
}
```

## Step 4 @showdialog

Look at the maze and observe how the motor module that is connected to output 2 on the Spark:bit needs to rotate conterclockwise in order to tilt the maze left.

![1-4-maze-left](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/1-4-maze-left.png)

## Step 5

Open the ``||sparkbitO:Spark:bit Outputs||`` category, select the ``||sparkbitO:rotate motor module||`` block and connect to the ``||functions:function left||`` block. Change the output to **2** and the direction to **counterclockwise**.

```blocks
function left () {
    sparkbitO.rotateMotorModule(SparkbitOutPort.Output2, SparkbitDirection.Counterclockwise, 100)
}
```

## Step 6

Open the ``||basic:Basic||`` category, select the ``||basic:pause||`` block, and connect it to the bottom of the ``||sparkbitO:rotate motor module||`` block. Change the pause to **1 second** (1000 ms).

```blocks
function left () {
    sparkbitO.rotateMotorModule(SparkbitOutPort.Output2, SparkbitDirection.Counterclockwise, 100)
    basic.pause(1000)
}
```

## Step 7

Open the ``||sparkbitO:Spark:bit Outputs||`` category, select the ``||sparkbitO:stop motor module||`` block, and connect it to the bottom of the ``||basic:pause||`` block. Change the output to **2** 

```blocks
function left () {
    sparkbitO.rotateMotorModule(SparkbitOutPort.Output2, SparkbitDirection.Counterclockwise, 100)
    basic.pause(1000)
    sparkbitO.stopMotorModule(SparkbitOutPort.Output2)
}
```

## Step 8 @showdialog

Look at the maze and observe how the motor module that is connected to output 2 on the Spark:bit needs to rotate clockwise in order to tilt the maze right. 

![1-4-maze-right](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/1-4-maze-right.png)

## Step 9

Create a new ``||functions:Function||`` called **right**. Make sure to include a **1 second** pause.

```blocks
function left () {
    sparkbitO.rotateMotorModule(SparkbitOutPort.Output2, SparkbitDirection.Counterclockwise, 100)
    basic.pause(1000)
    sparkbitO.stopMotorModule(SparkbitOutPort.Output2)
}
function right () {
    sparkbitO.rotateMotorModule(SparkbitOutPort.Output2, SparkbitDirection.Clockwise, 100)
    basic.pause(1000)
    sparkbitO.stopMotorModule(SparkbitOutPort.Output2)
}
```

## Step 10

Create two new ``||functions:Functions||`` called **forward** and **backward**. Make sure the correct output and direction are selected on the ``||sparkbitO:rotate motor module||`` blocks.

```blocks
function left () {
    sparkbitO.rotateMotorModule(SparkbitOutPort.Output2, SparkbitDirection.Counterclockwise, 100)
    basic.pause(1000)
    sparkbitO.stopMotorModule(SparkbitOutPort.Output2)
}
function right () {
    sparkbitO.rotateMotorModule(SparkbitOutPort.Output2, SparkbitDirection.Clockwise, 100)
    basic.pause(1000)
    sparkbitO.stopMotorModule(SparkbitOutPort.Output2)
}
function forward () {
    sparkbitO.rotateMotorModule(SparkbitOutPort.Output1, SparkbitDirection.Clockwise, 100)
    basic.pause(1000)
    sparkbitO.stopMotorModule(SparkbitOutPort.Output1)
}
function backward () {
    sparkbitO.rotateMotorModule(SparkbitOutPort.Output1, SparkbitDirection.Counterclockwise, 100)
    basic.pause(1000)
    sparkbitO.stopMotorModule(SparkbitOutPort.Output1)
}
```

## Step 11 @showdialog

Look at the maze and observe how the maze needs to tilt right in order for the ball to start rolling in the correct direction. 

![1-4-maze-ball-rolling-right](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/1-4-maze-ball-rolling-right.png)

## Step 12

Open the ``||functions:Functions||`` category, select the ``||functions:call right||`` block, and connect to the ``||basic:on start||`` function.

![call right](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/1-4-call-right.png)

## Step 13

Determine which directions the maze must tilt in order for the ball to continue rolling through the maze. Select the correct ``||functions:call function||`` blocks by placing them in the correct order in the ``||basic:on start||`` function block.

![call all](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/1-4-call-all.png)


## Step 14

Complete the steps to download and test the programming.
* Make sure the Spark:bit is powered on.
* ``|Download|`` the program to the Spark:bit and observe the maze.
* [Click here](https://kidsparkeducation.org/media/2358) to see the maze operating correctly.

## Step 15

Did your maze function correctly? If yes, proceed to the next step in the tutorial. If no, you may need to go back through your program and check a few things:
* Make sure the output number and direction are correct in the ``||sparkbitO:rotate motor module||`` blocks.
* Make sure the ``||functions:call function||`` blocks are in the correct order. 
* Make sure each direction ``||functions:function||`` includes a 1 second (1000 ms) ``||basic:pause||``.

Test out your revised program by downloading it to the Spark:bit.

## Step 16

Click **Finish** and review the next section in the curriculum packet.