# Using Variables in a Loop 

## Introduction 

Wouldn’t it be good if we could create the program so as to use a place-holder for the touch sensor and LED pin number, and then change that place-holder value from 5 to 16 in a loop? With “variables”, that’s exactly what you can do.  You can create a loop with a variable that will count from 5 to 16, and then other blocks will check if the sensor number that corresponds to that point in the counting loop is being touched.

## Step 1 

First lets start off by creating a variable named index. Then lets drag the variable into the for "index" from 0 to 5. We need to change it to 5 and 16. 

```blocks
basic.forever(function () {
    loops.forLoop(5, 16, function (index) {
    	
    })
})
```

## Step 2

Next we want to add an empty if-else statement block inside of our for loop. 

```blocks
basic.forever(function () {
    loops.forLoop(5, 16, function (index) {
        if (true) {
        	
        } else {
        	
        }
    })
})
```

## Step 3 

Next we want to add the "touch sensor 5 is touched" under the touch section of the MakerBit drop down menu. 

```blocks
basic.forever(function () {
    loops.forLoop(5, 16, function (index) {
        if (makerbit.isTouched(makerbit.touchSensorIndex(5))) {
        	
        } else {
        	
        }
    })
})
``` 

## Step 4 

We now want to add two blocks a set digital pin high and low. We want to place the high block in the if statement, then we want to place the low block in the else statement.

```blocks
basic.forever(function () {
    loops.forLoop(5, 16, function (index) {
        if (makerbit.isTouched(makerbit.touchSensorIndex(5))) {
            makerbit.setDigitalPin(5, makerbit.level(PinLevel.High))
        } else {
            makerbit.setDigitalPin(5, makerbit.level(PinLevel.Low))
        }
    })
})
```
## Step 5 

Lastly all we need to do is add index to any place that represents a pin. This includes the touch sensor block, and also the two set digital pin slots.  

```blocks
basic.forever(function () {
    loops.forLoop(5, 16, function (index) {
        if (makerbit.isTouched(index)) {
            makerbit.setDigitalPin(index, makerbit.level(PinLevel.High))
        } else {
            makerbit.setDigitalPin(index, makerbit.level(PinLevel.Low))
        }
    })
})
```

## Final Step @tutorialCompleted

Lastly all you need to do is plug in your MakerBit and download the .hex file. Once it's downloaded drag it into your microBit.


