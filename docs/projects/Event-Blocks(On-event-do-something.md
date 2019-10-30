# Event Blocks 

## Introduction

In this tutorial we will create code that on an event or action it does something. (If you need a hint you can simply click on the icon to the left!)     

## Step 1 @fullscreen

Let's start by adding one touch sensor and setting it to ANY and RELEASED.

```blocks
makerbit.onTouch(TouchSensor.Any, TouchAction.Released, function () {   
})
```

## Step 2 @fullscreen

Up next let's do the same thing except this time just place it below the first one except this time instead of setting it to released you need to set it to TOUCHED.

```blocks
makerbit.onTouch(TouchSensor.Any, TouchAction.Released, function () {   
})
makerbit.onTouch(TouchSensor.Any, TouchAction.Touched, function () {   
})
```
## Step 3 @fullscreen

Once you have both of the blocks in place, we want to add the set digital pin and place it in our first block. Then let's set it to high and add the ``||MakerBit:touch sensor||`` sensor block right where you see the number 0 written. If you get stuck, check out the hint, as this is a very important step! 

```blocks
makerbit.onTouch(TouchSensor.Any, TouchAction.Released, function () { 
    makerbit.setDigitalPin(makerbit.touchSensor(), makerbit.level(PinLevel.High))  
})
makerbit.onTouch(TouchSensor.Any, TouchAction.Touched, function () {   
})
```

## Step 4 @fullscreen

Next let's do the same except thing on the lower block except this time we are going to be setting it to 
low. 

```blocks
makerbit.onTouch(TouchSensor.Any, TouchAction.Released, function () { 
    makerbit.setDigitalPin(makerbit.touchSensor(), makerbit.level(PinLevel.High))  
})
makerbit.onTouch(TouchSensor.Any, TouchAction.Touched, function () {   
    makerbit.setDigitalPin(makerbit.touchSensor(), makerbit.level(PinLevel.Low))
})
```

## Final Step @tutorialCompleted

Lastly all you need to do is plug in your MakerBit and download the .hex file. Once it's downloaded drag it into your microBit.