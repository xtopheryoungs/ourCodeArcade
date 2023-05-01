### @explicitHints 1

# Repeat

## Step 1

A **compound statement block** is similar to a statement block in that it can attach to other blocks because of the indentation at the top and the tab at the bottom.  However, on its own, it doesn't do anything.  When combined with simple statement blocks, a compound statement block can show its usefulness.

#### ~ tutorialhint

This  ``||loops:repeat||`` block is a compound statement block.  By putting a simple statement inside it, we can perform an action such as saying "Hello, world!" multiple times while using only one ``||player:say||`` block.

```blocks
player.onChat("run", function () {
    for (let index = 0; index < 3; index++) {
        player.say("Hello, world!")
    }
})
```

## Step 2

Sometimes a solution involves performing the same actions over and over again.  Instead of writing the same lines of code multiple times, we can use a loop.  The ``||loops:repeat||`` block  is a type of loop that repeats a section of code a certain number of times.

#### ~ tutorialhint

The ``||loops:repeat||`` block expands as necessary to hold more blocks.  In this example, the ``||loops:repeat||`` loop makes the agent walk in a circle.

```blocks
player.onChat("run", function () {
    for (let index = 0; index < 4; index++) {
        agent.move(FORWARD, 1)
        agent.turn(LEFT_TURN)
    }
})
```

## Step 3

Recognizing patterns is a useful skill, as it can help determine when to use a ``||loops:repeat||`` block.  Try using ``||loops:repeat||`` blocks in conjunction with agent capabilities to complete the challenges.

#### ~ tutorialhint

The ``||agent:agent interact||`` block can do more than just make the agent activate levers.  It can also make the agent open and close gates. 

## Step 4

The ``||agent:agent destroy||`` block is another useful agent capability.  Like the ``||agent:agent interact||`` block, it has a drop-down menu to specify a direction in which the agent will try to destroy a block.  

#### ~ tutorialhint

The ``||agent:agent destroy||`` block can only target Minecraft blocks that are adjacent to the agent.  The agent can't destroy something that's two blocks away.

```ghost
player.onChat("part3", function () {
    for (let index = 0; index < 4; index++) {
        agent.move(FORWARD, 2)
        agent.move(UP, 1)
        agent.interact(DOWN)
    }
})
player.onChat("part2", function () {
    for (let index = 0; index < 7; index++) {
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
    }
    agent.interact(FORWARD)
})
player.onChat("part4", function () {
    for (let index = 0; index < 10; index++) {
        agent.interact(LEFT)
        agent.turn(LEFT_TURN)
        agent.turn(LEFT_TURN)
        agent.move(UP, 1)
    }
})
player.onChat("part1", function () {
    for (let index = 0; index < 4; index++) {
        agent.move(FORWARD, 2)
        agent.interact(FORWARD)
    }
})
```
