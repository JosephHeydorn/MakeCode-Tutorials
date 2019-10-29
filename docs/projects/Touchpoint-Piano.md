# Touchpoint Piano

## Introduction 

In this tutorial we are going to be working on creating the code for a Touchpoint Piano. In this specific tutorial we are going to be making 4 different notes. After that you can work on adding as many more notes as you would like to. This will expand the range of your piano! (If you need a hint you can simply click on the icon to the left!)

## Step 1

To begin, let's grab 4 ``||Loops: while-do||`` blocks and place them inside the forever block. Make sure that they are stacked on top of one another and not placed inside of each other. 

```blocks
basic.forever(function () {
    while (true) {
    	
    }
    while (true) {
    	
    }
    while (true) {
    	
    }
    while (true) {
    	
    }
})
```

## Step 2

Next we want to grab 4 "touched sensor is touched" blocks. Then we want to place them inside of the while block. This block should be placed where it says "true". Then we want to number them from 5 to 8. 

```blocks
basic.forever(function () {
    while (makerbit.isTouched(makerbit.touchSensorIndex(TouchSensor.T5))) {
    	
    }
    while (makerbit.isTouched(makerbit.touchSensorIndex(TouchSensor.T6))) {
    	
    }
    while (makerbit.isTouched(makerbit.touchSensorIndex(TouchSensor.T7))) {
    	
    }
    while (makerbit.isTouched(makerbit.touchSensorIndex(TouchSensor.T8))) {
    	
    }
})

```

## Step 3 

For our second to last step we want to grab 4 "play tone" blocks. These blocks will be placed inside of the while block right next to where it says "do". Let's set each block to a different tone. Going from top to bottom its going to look like this. Middle A, Middle B, High C, High D.

```blocks
basic.forever(function () {
    while (makerbit.isTouched(makerbit.touchSensorIndex(TouchSensor.T5))) {
        music.playTone(440, music.beat(BeatFraction.Sixteenth))
    }
    while (makerbit.isTouched(makerbit.touchSensorIndex(TouchSensor.T6))) {
        music.playTone(494, music.beat(BeatFraction.Sixteenth))
    }
    while (makerbit.isTouched(makerbit.touchSensorIndex(TouchSensor.T7))) {
        music.playTone(523, music.beat(BeatFraction.Sixteenth))
    }
    while (makerbit.isTouched(makerbit.touchSensorIndex(TouchSensor.T8))) {
        music.playTone(587, music.beat(BeatFraction.Sixteenth))
    }
})
```

## Step 4 

Finally if you haven't already done so, let's change the beat of each block to 1/16th of a beat. This will give off a constant sound that wont drag on once we release our finger from the touch sensor. 

```blocks
basic.forever(function () {
    while (makerbit.isTouched(makerbit.touchSensorIndex(TouchSensor.T5))) {
        music.playTone(440, music.beat(BeatFraction.Sixteenth))
    }
    while (makerbit.isTouched(makerbit.touchSensorIndex(TouchSensor.T6))) {
        music.playTone(494, music.beat(BeatFraction.Sixteenth))
    }
    while (makerbit.isTouched(makerbit.touchSensorIndex(TouchSensor.T7))) {
        music.playTone(523, music.beat(BeatFraction.Sixteenth))
    }
    while (makerbit.isTouched(makerbit.touchSensorIndex(TouchSensor.T8))) {
        music.playTone(587, music.beat(BeatFraction.Sixteenth))
    }
})

```

## Step 5

Lastly all you need to do is plug in your MakerBit and download the .hex file. Once it's downloaded drag it into your microBit.


