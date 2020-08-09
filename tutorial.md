# Countdown Timer

## Step 1
This program will count down from 9 to 0.

First up, get rid of the **start** and **forever** blocks, and create a
variable called **count**.

## Step 2
The countdown is going to start when you press the **A button** so drag
that in from the **Input** section, and inside that set the **count** variable
to 9.

```blocks
let count = 0
input.onButtonPressed(Button.A, function () {
    count = 9
})
```

## Step 3
Now take a **repeat** loop from the **Loops** section and put that under
your set block so that we can repeat a pattern. Change the number of times
the loop runs to **10**.

Any set of blocks you put in there will run in order 10 times, then move
to whatever is after the repeat block.

```blocks
let count = 0
input.onButtonPressed(Button.A, function () {
    count = 9
    for (let index = 0; index < 10; index++) {
    	
    }
})
```

## Step 4
Inside the **repeat** block, put a **show number** and **pause**
block from the **Basic** section.

Put your **count** variable into the **show number** block so that
it shows whatever value your variable currently has. Run your code - 
why doesn't it seem to do anything??

```blocks
let count = 0
input.onButtonPressed(Button.A, function () {
    count = 9
    for (let index = 0; index < 10; index++) {
        basic.showNumber(count)
        basic.pause(1000)
    }
})
```

## Step 5
Every time the loop runs, the variable should go down by 1.
Add a **change variable by** block after the pause, and set the amount
it changes by to **-1**.

Test your code again.

```blocks
let count = 0
input.onButtonPressed(Button.A, function () {
    count = 9
    for (let index = 0; index < 10; index++) {
        basic.showNumber(count)
        basic.pause(1000)
        count += -1
    }
})
```

## Step 6
This works well! But it's actually 10 seconds one second *after* the zero
appears on the screen, so let's use another **repeat** loop after the first
one to flash a symbol on the screen so you know it's really done.

Drag in another **repeat** loop and set the number of repetitions to **3**.

```blocks
let count = 0
input.onButtonPressed(Button.A, function () {
    count = 9
    for (let index = 0; index < 10; index++) {
        basic.showNumber(count)
        basic.pause(1000)
        count += -1
    }
    for (let index = 0; index < 3; index++) {
    	
    }
})
```

## Step 7
Inside the new loop, from the **Basic** section, drag in **show string**,
**pause**, **clear screen**, **pause** blocks.

Change the string to **!** and leave the pauses nice and short at **100ms**.

```blocks
let count = 0
input.onButtonPressed(Button.A, function () {
    count = 9
    for (let index = 0; index < 10; index++) {
        basic.showNumber(count)
        basic.pause(1000)
        count += -1
    }
    for (let index = 0; index < 3; index++) {
        basic.showString("!")
        basic.pause(100)
        basic.clearScreen()
        basic.pause(100)
    }
})
```

## Step 8
Test it out on a real Micro:bit, and compare how accurate it is against a
real stopwatch. If you change your **count** to 10 or more, does it keep its
accuracy? Why do you think that is? What could you do about it?

Save your program as **Countdown** into your Digital Technologies folder.
