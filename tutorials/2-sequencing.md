### @explicitHints 1

# Sequencing

## Step 1

For each of the activities in the previous lesson, we placed a **statement block** inside an **event block** to complete some simple tasks.  

For more complex tasks, we can put multiple statement blocks inside an event block.

#### ~ tutorialhint

Event blocks will expand as necessary to hold more than one statement block.

```blocks
player.onChat("run", function () {
    player.say("Hello,")
    player.say("World!")
})
```

## Step 2

For the activities in this lesson, the agent needs to find its way to the lever and then interact with it.  

Use a chat command and code a solution with multiple blocks.  Be sure to put blocks in the correct sequence.

#### ~ tutorialhint

Order matters.  The last thing for the agent to do is to interact with the lever, so it wouldn't make much sense for the first block in the solution to be ``||agent:agent interact||``.

## Step 3

The ``||agent:agent turn||`` block makes the agent turn in the direction specified in the drop down menu.  Try using it in your solution to see how it works.

#### ~ tutorialhint

The agent can turn 90 degrees to the left or 90 degrees to the right.

## Step 4

There might be multiple solutions to get the agent from its starting point to the lever.  You might have the ``||agent:agent turn||`` or you might make the ``||agent:agent move||`` in different directions.

Also, the ``||agent:agent interact||`` block can open gates.

#### ~ tutorialhint
Although there is a suggested path for the agent to follow, you might be able to simplify your solution by having the agent not follow the path. 

```ghost
player.onChat("part3", function () {
    agent.move(RIGHT, 7)
    agent.move(FORWARD, 5)
    agent.interact(FORWARD)
})
player.onChat("part2", function () {
    agent.move(FORWARD, 5)
    agent.turn(LEFT_TURN)
    agent.move(FORWARD, 2)
    agent.interact(FORWARD)
})
player.onChat("part4", function () {
    agent.move(FORWARD, 7)
})
player.onChat("part1", function () {
    agent.move(FORWARD, 4)
    agent.interact(FORWARD)
})
player.say("Hello,")
```
