# Conditions and Actions If Else Statment

## Introdution 

The next step is to make the blinking LED only happen when a MakerBit touch sensor is touched. Another way of saying that would be, “Only blink the LED if the MakerBit touch sensor is touched.  If not, (“or else”), turn the LED off.” (If you need a hint you can simply click on the icon to the left!)

```blocks
basic.forever(function () {
makerbit.setDigitalPin(5, makerbit.level(PinLevel.High))
basic.pause(100)
makerbit.setDigitalPin(5, makerbit.level(PinLevel.Low))
basic.pause(100)
})
```
## Step 1

We can represent this in a block program by adding another Logic block.  Click on the Logic category, and choose the ``||Logic: if-else||`` block. Once this is in your work area, click on the top block (set digital pin) to drag the whole group of blocks into the “if” space of the if else block. Then drag the ``||Logic: if-else||`` block and attached blocks back into the forever block.

```blocks
basic.forever(function () {
    if (true) {
        makerbit.setDigitalPin(5, makerbit.level(PinLevel.High))
        basic.pause(100)
        makerbit.setDigitalPin(5, makerbit.level(PinLevel.Low))
        basic.pause(100)
    } else {
    }
})
```

## Step 2

Next we need to add a new block. Click on “MakerBit” and scroll down to the ``||MakerBit:touch sensor is touched||`` blocks. Now you can choose the MakerBit touch block, and place it into the “if” space of the if/else block.

```blocks
basic.forever(function () {
    if (makerbit.isTouched(makerbit.touchSensorIndex(5))) {
        makerbit.setDigitalPin(5, makerbit.level(PinLevel.High))
        basic.pause(100)
        makerbit.setDigitalPin(5, makerbit.level(PinLevel.Low))
        basic.pause(100)
    } else {
    	
    }
})
```

## Step 3 

Finally, if no touch sensor is being touched, you’ll want to turn off LED #5, so add one more set digital pin block from the micro:bit MakerBit Pins category (scroll back up), put it in the “else” space, and set pin 5 to low.

```blocks
basic.forever(function () {
    if (makerbit.isTouched(makerbit.touchSensorIndex(5))) {
        makerbit.setDigitalPin(5, makerbit.level(PinLevel.High))
        basic.pause(100)
        makerbit.setDigitalPin(5, makerbit.level(PinLevel.Low))
        basic.pause(100)
    } else {
        makerbit.setDigitalPin(5, makerbit.level(PinLevel.Low))
    }
})
```

##Step 4 

Lastly all you need to do is plug in your MakerBit and download the .hex file. Once it's downloaded drag it into your microBit.


