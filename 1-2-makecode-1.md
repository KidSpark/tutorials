```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

# Introduction to MakeCode

## Step 1 @showdialog

Welcome to MakeCode for Spark:bit.  MakeCode is an online programming environment that can be used to create custom programs that can be uploaded to the Spark:bit. MakeCode makes it easy to write programs by using blocks of code.

There are four main parts of the MakeCode editor:
* **Toolbox** - holds all of the coding blocks and is organized into categories.
* **Workspace** - where you will drag the coding blocks to build your program.
* **micro:bit Simulator** - enables you to run some of your code on a virtual micro:bit. The micro:bit is a small computer inside the Spark:bit that has buttons, sensors, LEDs, and wireless capabilities.
* **Download Button** - how you will download your program to run on the Spark:bit.

Also, notice the toggle at the top to switch between blocks and text, but we'll stick to blocks for now.

![MakeCode screen](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/1-2-makecode-screen-labeled.png)

## Step 2 @showdialog

By clicking on each of the categories in the toolbox, a list of coding blocks will appear for that category.

![sparkbitO menu](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/1-2-makecode-sparkbitO.png)

## Step 3 @showdialog

There are additional categories that can be accessed by selecting **Advanced** at the bottom of the toolbox. This is where the ``||serial:Serial||`` category is located.

![Advanced categories](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/1-2-makecode-toolbox-advanced.png)

```blocks
serial.writeLine("")
```

## Step 4 @showdialog

The workspace is the large area on the right-hand side of the screen. This is where you will drag your coding blocks and connect them together to build your program. It doesn't matter where your coding blocks are located in the workspace. There are controls at the bottom of the screen to zoom in and zoom out if you need to change the size of the workspace.

There are two ways to delete a coding block from the workspace:
* Drag it back to the toolbox, or
* Right-click on the block and select **Delete Block**

When you start a new program, usually the ``||basic:on start||`` and ``||basic:forever||`` blocks are already in the workspace. They are also available in the ``||basic:Basic||`` category.

![MakeCode screen](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/1-2-makecode-whole-screen.png)

```blocks
basic.forever(function () {
	
})
```

## Step 5 @showdialog

MakeCode has a built-in simulator for the micro:bit inside of the Spark:bit, but it does not include all of the input sensors and output modules for the Spark:bit. You can interact with the simulator by selecting the buttons and viewing the LEDs. Some micro:bit sensors can also be controlled from the simulator to test your program before downloading it to the Spark:bit. There are additional controls under the simulator to stop and restart the simulator, or mute the simulator audio on your computer.  

When you use coding blocks from the ``||serial:Serial||`` category and the Spark:bit is connected to USB, a **Show console Device** will appear below the simulator. This allows you to see additional information about the serial communications of the Spark:bit.

![micro:bit simulator](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/1-2-makecode-show-console.png)

## Step 6 @showdialog

After you have created a program, you will need to download it to the Spark:bit. In order to do this, you will need to pair the Spark:bit to your computer using a USB connection.

* Step 1 - Connect the Spark:bit to a computer using a USB cable.
* Step 2 - In the MakeCode editor, select the select the three dots ``|download:•••|`` beside the ``|Download|`` button and select **Connect device**.
* Step 3 - Follow the onscreen instructions to pair the Spark:bit with the computer. Notice the icon on the ``|Download|`` button will change when the Spark:bit is successfully paired to your computer.

![USB pairing](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/1-2-makecode-webusb.png)

## Step 7

These are the main parts of MakeCode that you'll be using with Spark:bit. 

## Step 8

Click **Finish** and review the next section of the curriculum packet.