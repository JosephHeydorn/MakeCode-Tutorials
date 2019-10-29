# Blinking LED

## Introdution 

In this tutorial we will be creating a blinking LED. (If you need a hint you can simply click on the icon to the left!)

## Step 1 

To turn on and off LEDs with the MakerBit, you will start with the MakerBit Pins category.  Drag the ``||Pins: digital write pin||`` block into the Forever loop block. To turn on LED #5, confirm that the block shows pin “P5” to “high”. For other pins, you would click on the “5” of the block to change it to “5”, and edit “high” to “low” if you wanted to turn an LED off.

```blocks
basic.forever(function () {
makerbit.setDigitalPin(5, makerbit.level(PinLevel.High))
})
```

	## Step 2

Look in the Basic category find the ``||Basic: pause (ms)||`` block, and drag it to place it under the ``||Pins: digital write pin||`` block.

```blocks
basic.forever(function () {
	    makerbit.setDigitalPin(5, makerbit.level(PinLevel.High))
	    basic.pause(100)
})
```

## Step 3

Then repeat to add two more blocks to complete the program. Add one ``||Pins: digital write pin||`` block and set the pin to P5 and the value to 1. Lastly let's add a ``||Basic: pause (ms)||`` block and set the value to 100ms (0.1 seconds). 

```blocks 
basic.forever(function () {
makerbit.setDigitalPin(5, makerbit.level(PinLevel.High))
basic.pause(100)
makerbit.setDigitalPin(5, makerbit.level(PinLevel.Low))
basic.pause(100)
})
```

## Step 4 

In digital circuits and programming, “high” is for “on”, and “low” is for “off”. Repeating this loop will make the LED blink on and off every 0.2 seconds.  That’s because 0.1 seconds in the “on” condition (pin 5 = high), and 0.1 seconds in the “off” condition, for a total of 0.2 seconds per complete cycle.

## Step 5

Lastly all you need to do is plug in your MakerBit and download the .hex file. Once it's downloaded drag it into your microBit.

