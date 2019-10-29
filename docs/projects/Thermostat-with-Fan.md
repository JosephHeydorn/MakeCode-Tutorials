# Thermostat with Fan

## Introduction 

In this tutorial we are going to be creating a fan that turns on based on the reading of the thermostat. If the room gets too warm, we want to turn on the fan! (If you need a hint you can simply click on the icon to the left!)

## Step 1 

Let's start by getting an ``||Logic: if-else||`` block from the logic tab and dragging it in the forever block. 

```blocks
basic.forever(function () {
    if (true) {
    	
    } else {
    	
    }
})
```

## Step 2 

Now we want to grab two ``||Pins: digital write pin||`` blocks from the Pins tab. To access the Pins tab we need to press the advanced drop down menu. Then let's place one below the if, and one below the else statement. Let's set each one to P10. Then let's change the top ``||Pins: digital write pin||`` block value to 1 by clicking on the "0" and sliding the value over to "1".

```blocks
basic.forever(function () {
    if (true) {
        pins.digitalWritePin(DigitalPin.P10, 1)
    } else {
        pins.digitalWritePin(DigitalPin.P10, 0)
    }
})
```

## Step 3 

Now we want to grab a ``||Logic: ≤||`` block and place it at the very top of the ``||Logic: if-else||`` block. Then let's grab an ``||Pins: analog read pin||`` block from the Pins tab and set it to P0. Let's place that block on the left of the ≤ symbol. Now let's set the value to the right of the ≤ symbol to "620". 

```blocks
basic.forever(function () {
    if (pins.analogReadPin(AnalogPin.P0) <= 620) {
        pins.digitalWritePin(DigitalPin.P10, 1)
    } else {
        pins.digitalWritePin(DigitalPin.P10, 0)
    }
})
```

## Step 4 

Lastly all you need to do is plug in your MakerBit and download the .hex file. Once it's downloaded drag it into your microBit.