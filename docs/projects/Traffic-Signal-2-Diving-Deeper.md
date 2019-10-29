# Traffic Signal 2 Diving Deeper

## Introduction 

This is a continuation of the Traffic Signal project. We are going to be creating the code for the second traffic light. To do so all we are going to do is add a few more blocks of code and thats it! (If you need a hint you can simply click on the icon to the left!)

## Step 1 

Once again let's look at the code as if it is in three sections. Each section ends at the ``||Basic: pause (ms)||`` block. With that being said let's do this in three parts once again!

```blocks
basic.forever(function () {
    pins.digitalWritePin(DigitalPin.P5, 1)
    pins.digitalWritePin(DigitalPin.P6, 0)
    pins.digitalWritePin(DigitalPin.P7, 0)
    basic.pause(4000)
    pins.digitalWritePin(DigitalPin.P5, 0)
    pins.digitalWritePin(DigitalPin.P6, 0)
    pins.digitalWritePin(DigitalPin.P7, 1)
    basic.pause(4000)
    pins.digitalWritePin(DigitalPin.P5, 0)
    pins.digitalWritePin(DigitalPin.P6, 1)
    pins.digitalWritePin(DigitalPin.P7, 0)
    basic.pause(1000)
})

```

## Step 2

Let's start by adding three more ``||Pins: digital write pin||`` blocks. We are going to place them right above the first ``||Basic: pause (ms)||`` block.

```blocks
basic.forever(function () {
    pins.digitalWritePin(DigitalPin.P5, 1)
    pins.digitalWritePin(DigitalPin.P6, 0)
    pins.digitalWritePin(DigitalPin.P7, 0)
    pins.digitalWritePin(DigitalPin.P0, 0)
    pins.digitalWritePin(DigitalPin.P0, 0)
    pins.digitalWritePin(DigitalPin.P0, 0)
    basic.pause(4000)
    pins.digitalWritePin(DigitalPin.P5, 0)
    pins.digitalWritePin(DigitalPin.P6, 0)
    pins.digitalWritePin(DigitalPin.P7, 1)
    basic.pause(4000)
    pins.digitalWritePin(DigitalPin.P5, 0)
    pins.digitalWritePin(DigitalPin.P6, 1)
    pins.digitalWritePin(DigitalPin.P7, 0)
    basic.pause(1000)
})
```

## Step 3 

Now let's change those value once again. This only include the new blocks we just added. Starting from top to bottom let's set the values to P8, P9, and P10. Then let's change the value of P10 to 1. This will turn one light green and turn one light red. 

```blocks
basic.forever(function () {
    pins.digitalWritePin(DigitalPin.P5, 1)
    pins.digitalWritePin(DigitalPin.P6, 0)
    pins.digitalWritePin(DigitalPin.P7, 0)
    pins.digitalWritePin(DigitalPin.P8, 0)
    pins.digitalWritePin(DigitalPin.P9, 0)
    pins.digitalWritePin(DigitalPin.P10, 1)
    basic.pause(4000)
    pins.digitalWritePin(DigitalPin.P5, 0)
    pins.digitalWritePin(DigitalPin.P6, 0)
    pins.digitalWritePin(DigitalPin.P7, 1)
    basic.pause(4000)
    pins.digitalWritePin(DigitalPin.P5, 0)
    pins.digitalWritePin(DigitalPin.P6, 1)
    pins.digitalWritePin(DigitalPin.P7, 0)
    basic.pause(1000)
})
```

## Step 4 

Once again let's copy those three blocks we jsut created. We want to place those copies on top of the 2nd ``||Basic: pause (ms)||`` block. Now let's change P10's value to 0 and P8's value to 1. 

```blocks
basic.forever(function () {
    pins.digitalWritePin(DigitalPin.P5, 1)
    pins.digitalWritePin(DigitalPin.P6, 0)
    pins.digitalWritePin(DigitalPin.P7, 0)
    pins.digitalWritePin(DigitalPin.P8, 0)
    pins.digitalWritePin(DigitalPin.P9, 0)
    pins.digitalWritePin(DigitalPin.P10, 1)
    basic.pause(4000)
    pins.digitalWritePin(DigitalPin.P5, 0)
    pins.digitalWritePin(DigitalPin.P6, 0)
    pins.digitalWritePin(DigitalPin.P7, 1)
    pins.digitalWritePin(DigitalPin.P8, 1)
    pins.digitalWritePin(DigitalPin.P9, 0)
    pins.digitalWritePin(DigitalPin.P10, 0)
    basic.pause(4000)
    pins.digitalWritePin(DigitalPin.P5, 0)
    pins.digitalWritePin(DigitalPin.P6, 1)
    pins.digitalWritePin(DigitalPin.P7, 0)
    basic.pause(1000)
})
```

## Step 5

Lastly for our final part we want to copy the three blocks again. Placing them above the last ``||Basic: pause (ms)||`` block. Now let's change P8's value to 0 and P1's value to 1. This will turn the light yellow!

## Step 6 

Lastly all you need to do is plug in your MakerBit and download the .hex file. Once it's downloaded drag it into your microBit.





