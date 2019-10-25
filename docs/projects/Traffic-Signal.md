# Traffic Signal 

## Introduction

This is the first part of the traffic light porject is getting 1 traffic light working. (If you need a hint you can simply click on the icon to the left!)

## Step 1

To get a basic understanding of the project we are only going to use two very basic blocks. First is the "Digital Write Pin" block, the second is the "Pause" block. Lets tackle this in three main parts. 

```blocks
basic.pause(100)
pins.digitalWritePin(DigitalPin.P5, 1)
```

## Step 2 

For part 1 we are going to add the red light. To start lets grab 3 "Digital Write Pin" blocks from the advanced tab, and one "Pause" block from the basic tab. Stack the three digital blocks, then place the pause block under the three existing blocks. 

```blocks
basic.forever(function () {
    pins.digitalWritePin(DigitalPin.P0, 0)
    pins.digitalWritePin(DigitalPin.P0, 0)
    pins.digitalWritePin(DigitalPin.P0, 0)
    basic.pause(100)
})
```

## Step 3 

Next for part 1 lets change all the values. Lets set each pin going from top down here are the pin values. P5, P6, P7. Then lets change P5's value to 1. Lastly lets change the pause from 100 to 4000. 4000 being 4 seconds. 

```blocks
basic.forever(function () {
    pins.digitalWritePin(DigitalPin.P5, 1)
    pins.digitalWritePin(DigitalPin.P6, 0)
    pins.digitalWritePin(DigitalPin.P7, 0)
    basic.pause(4000)
})
```

## Step 4 

For part 2 all we need to do is copy exactly what we have done above, except we are going to change a few values. Lets set P5 to 0 and change P7 to 1. This is signifying that the light is turning green!

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
})
```

## Step 5

For part 3 lets add the yellow light. To do so, once again copy 3 "digital write pin" blocks from above and one "pause" block. Keep the values the same, except this time we want to set P7 to 0 and P6 to 1. Then lets change the pause blocks value to 1000.

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

## Step 6

Lastly all you need to do is plug in your MakerBit and download the .hex file. Once it's downloaded drag it into your microBit.






