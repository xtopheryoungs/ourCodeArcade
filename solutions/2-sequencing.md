# Lesson 2

## Step 1

The solutions for Lesson 2

```template
player.onChat("part1", function () {
    agent.move(FORWARD, 4)
    agent.interact(FORWARD)
})
player.onChat("part2", function () {
    agent.move(FORWARD, 5)
    agent.move(LEFT, 2)
    agent.interact(LEFT)
})
player.onChat("part3", function () {
    agent.move(RIGHT, 7)
    agent.move(FORWARD, 5)
    agent.interact(FORWARD)
})
player.onChat("part4", function () {
    agent.move(RIGHT, 2)
    agent.move(FORWARD, 3)
    agent.interact(FORWARD)
    agent.move(FORWARD, 3)
    agent.move(LEFT, 2)
    agent.interact(FORWARD)
})
```
