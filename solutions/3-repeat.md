# Lesson 3

## Step 1

The solutions for Lesson 3

```template
player.onChat("part1", function () {
    for (let index = 0; index < 4; index++) {
        agent.move(FORWARD, 2)
        agent.interact(FORWARD)
    }
})
player.onChat("part2", function () {
    for (let index = 0; index < 7; index++) {
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
    }
    agent.interact(FORWARD)
})
player.onChat("part3", function () {
    for (let index = 0; index < 4; index++) {
        agent.move(FORWARD, 2)
        agent.move(UP, 1)
        agent.interact(DOWN)
    }
})
player.onChat("part4", function () {
    for (let index = 0; index < 10; index++) {
        agent.interact(LEFT)
        agent.turn(LEFT_TURN)
        agent.turn(LEFT_TURN)
        agent.move(UP, 1)
    }
})
```
