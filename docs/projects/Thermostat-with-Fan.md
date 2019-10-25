# Thermostat with Fan

## Introduction 

In this tutorial we are going to be creating a fan that turns on based on the reading of the thermostat. If the room gets too warm, we want to turn on the fan! (If you need a hint you can simply click on the icon to the left!)

## Step 1 

Let's start by getting an If-Else statement from the basic tab and dragging it in the forever block. 

```blocks
basic.forever(function () {
    if (true) {
    	
    } else {
    	
    }
})
```

## Step 2 

Now we want to grab two "digital pin write" blocks. Then lets place one below the if, and one below the else statement. Let's set each one to P10. Then let's change the top one's value to 1.

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

Now we want to grab a ≤ block and place it at the very top of the If-Else statement. Then let's grab an "analog read pin" block and set it to P0. Let's place that block on the left of the ≤ symbol. Now let's set the value to the right of the ≤ symbol to 620. 

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