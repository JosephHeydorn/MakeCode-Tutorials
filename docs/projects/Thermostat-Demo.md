# Thermostat Demo

## Introduction 

This is a big project, so we are going to work in 3 sections. This will help keep everything nice and organized. We are starting from top to bottom. With that being said, let's get to it! (If you need a hint you can simply click on the icon to the left!)

## Step 1

For the first section let's grab an ``||Logic: if-else||`` block from the logic tab and place it in the forever block. 

```blocks 
basic.forever(function () {
    if (true) {
    	
    } else {
    	
    }
})
```

## Step 2

Up next we want to grab two ``||Pins: digital write pin||`` blocks from the advanced tab. Let's place one below the IF, and one below the ELSE. Let's set each pin to P5. Then let's change the top ``||Pins: digital write pin||`` block value to 1 by clicking on the "0" and sliding the value over to "1".

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

Next let's grab a less than or equal too comparison block from the logic tab and place an ``||Pins: analog read pin||`` block in the left bubble. Then let's change the value of the other bubble to 600. It should be "Analog 0 ≤ 600". Lastly we just need to place it at the very top of the where it says "true". That ends the first section. 

```blocks
basic.forever(function () {
    if (pins.analogReadPin(AnalogPin.P0) <= 600) {
        pins.digitalWritePin(DigitalPin.P5, 1)
    } else {
        pins.digitalWritePin(DigitalPin.P5, 0)
    }
})
```

## Step 4 

Now let's grab a second ``||Logic: if-else||`` block. Then we can essentially leave the the digital write blocks inside of the ``||Logic: if-else||`` block just like we placed them in the first section. The only thing we need to do is change the pin value to P6. 

```blocks 
basic.forever(function () {
    if (true) {
        pins.digitalWritePin(DigitalPin.P6, 1)
    } else {
        pins.digitalWritePin(DigitalPin.P6, 0)
    }
})
```

## Step 5

Now let's grab one ``||Logic: and||`` block, one ``||Logic: ≥||`` block, and one ``||Logic: ≤||`` block each from the logic tab. Place the ``||Logic: ≥||`` block to the left of the and block and place the ``||Logic: ≤||`` to the right of the and block. Then we can place that whole block where it says "true".

```blocks
basic.forever(function () {
    if (0 >= 0 && 0 <= 0) {
        pins.digitalWritePin(DigitalPin.P6, 1)
    } else {
        pins.digitalWritePin(DigitalPin.P6, 0)
    }
})
```

## Step 6 

Let's grab two analog pin read blocks and place them to the left of each block. Then let's set the two values, for the ≥ let's set it to 600, and for the ≤ let's set it to 625. That concludes the second section

```blocks
basic.forever(function () {
    if (pins.analogReadPin(AnalogPin.P0) >= 600 && pins.analogReadPin(AnalogPin.P0) <= 625) {
        pins.digitalWritePin(DigitalPin.P6, 1)
    } else {
        pins.digitalWritePin(DigitalPin.P6, 0)
    }
})
```

## Step 7 

The current look of the code should be this!

```blocks
basic.forever(function () {
    if (pins.analogReadPin(AnalogPin.P0) <= 600) {
        pins.digitalWritePin(DigitalPin.P5, 1)
    } else {
        pins.digitalWritePin(DigitalPin.P5, 0)
    }
    if (pins.analogReadPin(AnalogPin.P0) >= 600 && pins.analogReadPin(AnalogPin.P0) <= 625) {
        pins.digitalWritePin(DigitalPin.P6, 1)
    } else {
        pins.digitalWritePin(DigitalPin.P6, 0)
    }
})
```

## Step 8 

Now let's finish this up with the last part! This one should be easier than the second part and very similar to the first. 

```blocks 
basic.forever(function () {
    if (true) {
    	
    } else {
    	
    }
})
```

## Step 9

Up next we want to grab two ``||Pins: digital write pin||`` blocks. Let's place one below the IF, and one below the ELSE. Let's set each pin to P7 and then and then change the value of the top one to 1.

```blocks
basic.forever(function () {
    if (true) {
        pins.digitalWritePin(DigitalPin.P7, 1)
    } else {
        pins.digitalWritePin(DigitalPin.P7, 0)
    }
})
```

## Step 10
Next let's grab a greater than comparison and place an analog read in the left bubble. Then let's change the value of the other bubble to 600. It should be "Analog 0 ≥ 625" This will help us detect if it is picking up light or not and if there is no light, it will turn on the LED. Lastly we just need to place it at the very top of the where it says "true".

```blocks
basic.forever(function () {
    if (pins.analogReadPin(AnalogPin.P0) >= 625) {
        pins.digitalWritePin(DigitalPin.P7, 1)
    } else {
        pins.digitalWritePin(DigitalPin.P7, 0)
    }
})
```

## Step 11

That's it! We have completed the code! The finished project should look like this! 

```blocks
basic.forever(function () {
    if (pins.analogReadPin(AnalogPin.P0) <= 600) {
        pins.digitalWritePin(DigitalPin.P5, 1)
    } else {
        pins.digitalWritePin(DigitalPin.P5, 0)
    }
    if (pins.analogReadPin(AnalogPin.P0) >= 600 && pins.analogReadPin(AnalogPin.P0) <= 625) {
        pins.digitalWritePin(DigitalPin.P6, 1)
    } else {
        pins.digitalWritePin(DigitalPin.P6, 0)
    }
    if (pins.analogReadPin(AnalogPin.P0) >= 626) {
        pins.digitalWritePin(DigitalPin.P7, 1)
    } else {
        pins.digitalWritePin(DigitalPin.P7, 0)
    }
})
```