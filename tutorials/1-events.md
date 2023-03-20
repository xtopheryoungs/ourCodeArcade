### @explicitHints 1

# Events

## Step 1

An **event block** is what allows code to run.  On its own, an event block doesn’t do anything; it needs to have other code blocks inside it to make something happen. 

Event blocks have a distinct shape.  At the top and bottom, the edges are flat which means that event blocks cannot be placed inside other blocks.  On the interior of the event block are a tab and an indentation indicating that other code blocks with the correct shape can be placed inside.

#### ~ tutorialhint

In "Hello, World!" we used an ``||loops:on start||`` event block.

## Step 2

Event block names typically start with the word "on" and describe an action to perform in Minecraft.  Performing that action will cause the event block to run its code.

The ``||loops:on start||`` event runs when code is started by pressing the Play button.

#### ~ tutorialhint

Examples of some event blocks:

```blocks
player.onArrowShot(function () {
	
})
player.onChat("run", function () {
	
})
player.onItemInteracted(IRON_SHOVEL, function () {
	
})
```

## Step 3

The ``||player:on chat command||`` block is the event block we will focus on, since it is easy to control.  It does not have any requirements pertaining to the player's inventory or the Minecraft world and can be run multiple times after closing the CodeBuilder window.

The player simply needs to open the chat window in Minecraft and send the name of the chat command.

#### ~ tutorialhint

What "Hello, World!" may have looked like with an ``||player:on chat command||`` event:

```blocks
player.onChat("run", function () {
    player.say("Hello, World!")	
})
```

## Step 4

Another type of block is the **statement block**.  A simple statement block performs a single action.  

Statement blocks have a distinct shape.  At the top there's an indentation indicating that the block can be attached to another block that has a tab.

At the bottom there's a tab indicating that another block of appropriate shape can be attached.

#### ~ tutorialhint

The ``||player:say||`` block we used in "Hello, World" is a statement block.

```blocks
player.say("Hello, World!")
```
On their own, statement blocks are inactive.  They need to be placed inside an active event block.

## Step 5

``||agent:agent move||`` and ``||agent:agent interact||`` are statement blocks that make the agent perform certain actions.

See if you can complete the challenges by using  ``||player:on chat command||`` events in combination with ``||agent:agent move||`` to move the agent or ``||agent:agent interact||`` to activate a lever.

#### ~ tutorialhint

Identical event blocks can't coexist in the workspace.  Use different command names in order to have multiple ``||player:on chat command||`` blocks.

Use the drop-down menu to control the direction in which the agent moves or interacts.  The agent can float, so moving the agent up will cause it to hover in the air.

Also, adjust the number in the ``||agent:agent move||`` block to control how far the agent moves in the specified direction.

```ghost
player.onChat("part3", function () {
    agent.move(UP, 1)
})
player.onChat("part2", function () {
    agent.interact(FORWARD)
})
player.onChat("part4", function () {
    agent.move(FORWARD, 7)
})
player.onChat("part1", function () {
    agent.move(FORWARD, 1)
})
```
