```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

# Introduction to MakeCode

## Step 1 @showdialog

Welcome to MakeCode for Spark:bit. Inside the Spark:bit is a microcontroller called the micro:bit that has buttons, sensors, LEDs, and wireless capabilites, in addition to all the inputs and outputs that connect to the Spark:bit. MakeCode includes programming blocks that enable you to write software programs using all of the inputs and outputs to the Spark:bit.

There are four main parts of the MakeCode editor:
* **Toolbox** - holds all of the coding blocks and is organized into categories
* **Workspace** - is where you will drag the coding blocks and build your program
* **micro:bit Simulator** - enables you to run some of your code on a virtual micro:bit. However, it does not simulate the Spark:bit inputs and outputs.
* **Download Button** - is how you will download your program to run on the Spark:bit

![MakeCode screen](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/1-2-makecode-screen-labeled.png)

```blocks
basic.forever(function () {
})
```
## Step 2 @showdialog

By clicking on each of the categories in the toolbox, a list of coding blocks will appear for that category.

![sparkbitO menu](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/1-2-makecode-sparkbitO.png)

```blocks
basic.forever(function () {
})
```

## Step 3 @showdialog

There are additional catories available by selecing ``||advanced:Advanced||`` at the bottom of the toolbox. This is where the ``||serial:Serial||`` category is located.

![Advanced categories](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/1-2-makecode-toolbox-advanced.png)

```blocks
basic.forever(function () {
})
```

## Step 4 @showdialog

The workspace is the large area on the right-hand side of the screen. This is where you will drag your coding blocks and connect them together to build your program. It doesn't matter where your coding blocks are located in the workspace. And there are controls at the bottom of the screen to zoom in and zoom out if you need to change the size of the workspace.

When you start a new program, usually the ``||basic:on start||`` and ``||basic:forever||`` blocks are already in the workspace. They are also located in the ``||basic:Basic||`` category.

![MakeCode screen](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/1-2-makecode-whole-screen.png)

```blocks
basic.forever(function () {
})
```

## Step 5 @showdialog

MakeCode has a built-in simulator for the micro:bit inside of the Spark:bit, but it does not include all of the input sensors and output modules for the Spark:bit. You can interact with the simulator by selecting the buttons and viewing the LEDs. Some micro:bit sensors can also be controlled from the simulator to test your program before downloading it to the Spark:bit. There are additional controls under the simulator to stop and restart the simulator, or mute the simulator audio on your computer.  

When you use coding blocks from the ``||serial:Serial||`` category, a **Show console Simulator** will appear below the simulator. This allows you to see additional information about the serial communications of the Spark:bit.

![micro:bit simulator](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/1-2-makecode-show-console.png)

