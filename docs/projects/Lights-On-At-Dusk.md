# Lights On At Dusk

## Introduction 

In this project, we want to create a way for the LED to turn on and off based on the amount of light that is hitting the light sensor. (If you need a hint you can simply click on the icon to the left!)

## Step 1

Let's start by getting an ``||Logic: if-else||`` block from the basic tab and dragging it in the forever block. 

```blocks 
basic.forever(function () {
    if (true) {
    	
    } else {
    	
    }
})
```

## Step 2

Up next we want to grab two ``||Pins: digital write pin||`` blocks from the advanced tab. Let's place one below the IF, and one below the ELSE. Let's set each pin to P5 and then and then change the value of the top one to 1.

```blocks
basic.forever(function () {
    if (true) {
        pins.digitalWritePin(DigitalPin.P5, 1)
    } else {
        pins.digitalWritePin(DigitalPin.P5, 0)
    }
})
```

## Step 3
Next let's grab a ``||Logic: >||`` comparison from the logic tab and place an ``||Pins: analog read pin||`` block in the left bubble. Then let's change the value of the other bubble to 600. It should be "analog read pin 0 > 600" This will help us detect if it is picking up light or not and if there is no light, it will turn on the LED. Lastly we just need to place it at the very top of the where it says "true".

```blocks
basic.forever(function () {
    if (pins.analogReadPin(AnalogPin.P0) > 600) {
        pins.digitalWritePin(DigitalPin.P5, 1)
    } else {
        pins.digitalWritePin(DigitalPin.P5, 0)
    }
})
```

## Step 4 

Lastly all you need to do is plug in your MakerBit and download the .hex file. Once it's downloaded drag it into your microBit.
