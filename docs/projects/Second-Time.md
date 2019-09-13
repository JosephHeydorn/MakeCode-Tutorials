# Title 

## Introduction 

In this tutorial we will create a seconds timer on the MakerBit LCD display. 

## Step 1

To begin we want to create a variable named "NumberOfSeconds" then lets set the variable to 0 and drag it to the ``||Basic:on start||`` block.

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

Next lets lets have something display on the LCD display. What we want to do is have "MakerBit Timer" appear on screen. So lets grab our "Show LCD String" block and set it from P0 - P15.

```blocks
let NumberOfSeconds = 0
makerbit.connectLcd(39)
makerbit.clearLcd()
makerbit.showStringOnLcd("MakerBit Timer", makerbit.position(LcdPosition.P0), makerbit.position(LcdPosition.P15))
```

## Step 5

Lastly for this step, lets have the word seconds display on the screen. We are going to do exactly the same thing as last time except change the text to "Seconds: " and set it to P0 - P24

```blocks
let NumberOfSeconds = 0
makerbit.connectLcd(39)
makerbit.clearLcd()
makerbit.showStringOnLcd("MakerBit Timer", makerbit.position(LcdPosition.P0), makerbit.position(LcdPosition.P15))
makerbit.showStringOnLcd("Seconds: ", makerbit.position(LcdPosition.P0), makerbit.position(LcdPosition.P24))
```

##Step 6 



## Delete Later 

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
