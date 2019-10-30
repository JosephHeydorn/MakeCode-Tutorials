# Second-Timer 

## Introduction @unpluggeds

In this tutorial we will create a seconds timer on the MakerBit LCD display. (If you need a hint you can simply click on the icon to the left!)

## Step 1

To begin we want to create a variable named "NumberOfSeconds" then let's set the variable to 0 and drag it to the ``||Basic:on start||`` block.

```blocks 
let NumberOfSeconds = 0
```
## Step 2 

Next we want to initilize and connect the LCD. This block is going to be placed below the previous block. Now let's set the number of that block to 39.

```blocks
let NumberOfSeconds = 0
makerbit.connectLcd(39)
```

## Step 3

Now we want to clear what's on the LCD screen. We can simply do that by placing the next block below the previous block. 

```blocks
let NumberOfSeconds = 0
makerbit.connectLcd(39)
makerbit.clearLcd()
```

## Step 4

Next let's have something display on the LCD display. What we want to do is have "MakerBit Timer" appear on screen. So let's grab our "Show LCD String" block and set it from P0 - P15.

```blocks
let NumberOfSeconds = 0
makerbit.connectLcd(39)
makerbit.clearLcd()
makerbit.showStringOnLcd("MakerBit Timer", makerbit.position(LcdPosition.P0), makerbit.position(LcdPosition.P15))
```

## Step 5

Lastly for this step, let's have the word seconds display on the screen. We are going to do exactly the same thing as last time except change the text to "Seconds: " and set it to P0 - P24

```blocks
let NumberOfSeconds = 0
makerbit.connectLcd(39)
makerbit.clearLcd()
makerbit.showStringOnLcd("MakerBit Timer", makerbit.position(LcdPosition.P0), makerbit.position(LcdPosition.P15))
makerbit.showStringOnLcd("Seconds: ", makerbit.position(LcdPosition.P0), makerbit.position(LcdPosition.P24))
```

## Step 6 
 
 Next let's grab and place a forever block if it's not already on screen. This will help us loop a timer forever! We need to have a way that it wait's 1 second everytime before it adds on to the actual timer, so let's grab the ``||Basic: pause (ms)||`` and set it to 1000.

```blocks
 basic.forever(function () {
    basic.pause(1000)
})
```

## Step 7 

Then we are going to add to our variable every time our 1 second pause ends, this is so that our timer can update every second. 

```blocks
 basic.forever(function () {
    basic.pause(1000)
    NumberOfSeconds += 1
})
```

## Step 8 

For our last step before we test our code on our MakerBit and LCD screen, we want to show a number on the LCD in the space that is free to do so! That means we need to position it in the right place. Let's grab our "Show number on LCD", set it to 0 and set the two positions to P25 and P26. 

```blocks
basic.forever(function () {
    basic.pause(1000)
    NumberOfSeconds += 1
    makerbit.showNumberOnLcd(0, makerbit.position(LcdPosition.P25), makerbit.position(LcdPosition.P26))
})
```

## Final Step @tutorialCompleted 

Lastly all you need to do is plug in your MakerBit and download the .hex file. Once it's downloaded drag it into your microBit. Your final product should look exactly the same as whats in the hint box!

```blocks
let NumberOfSeconds = 0
makerbit.connectLcd(39)
makerbit.clearLcd()
makerbit.showStringOnLcd("MakerBit Timer", makerbit.position(LcdPosition.P0), makerbit.position(LcdPosition.P15))
makerbit.showStringOnLcd("Seconds: ", makerbit.position(LcdPosition.P0), makerbit.position(LcdPosition.P24))
basic.forever(function () {
    basic.pause(1000)
    NumberOfSeconds += 1
    makerbit.showNumberOnLcd(0, makerbit.position(LcdPosition.P25), makerbit.position(LcdPosition.P26))
})
```
