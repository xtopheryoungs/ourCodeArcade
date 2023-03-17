# Lesson 4

## Step 1

The solutions for Lesson 4

```template
player.onChat("part1", function () {
    agent.setItem(DIAMOND_BLOCK, 1, 1)
    agent.place(FORWARD)
})
player.onChat("part2", function () {
    for (let index = 0; index < 10; index++) {
        if (agent.detect(AgentDetection.Block, FORWARD)) {
            agent.destroy(FORWARD)
        }
        agent.move(FORWARD, 1)
    }
    agent.interact(FORWARD)
})
player.onChat("part3", function () {
    for (let index = 0; index < 20; index++) {
        agent.move(FORWARD, 1)
        if (agent.detect(AgentDetection.Block, LEFT)) {
            agent.setItem(SAND, 1, 1)
            agent.place(RIGHT)
        }
    }
    agent.interact(FORWARD)
})
player.onChat("part4", function () {
    for (let index = 0; index < 20; index++) {
        agent.move(FORWARD, 1)
        if (agent.detect(AgentDetection.Block, LEFT)) {
            agent.destroy(LEFT)
            agent.setItem(REDSTONE_TORCH, 1, 1)
            agent.place(LEFT)
        }
    }
    agent.interact(FORWARD)
})


```
