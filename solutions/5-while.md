# Lesson 5

## Step 1

The solutions for Lesson 5

```template
player.onChat("part1", function () {
    while (agent.inspect(AgentInspection.Block, DOWN) == OBSIDIAN) {
        agent.move(FORWARD, 1)
    }
    agent.interact(FORWARD)
})
player.onChat("part2", function () {
    while (agent.inspect(AgentInspection.Block, DOWN) == BRICKS) {
        if (agent.detect(AgentDetection.Block, FORWARD)) {
            agent.turn(LEFT_TURN)
        }
        agent.move(FORWARD, 1)
    }
})
player.onChat("part3", function () {
    while (agent.inspect(AgentInspection.Block, DOWN) != EMERALD_BLOCK) {
        if (agent.detect(AgentDetection.Block, FORWARD)) {
            agent.turn(LEFT_TURN)
        }
        agent.move(FORWARD, 1)
    }
    agent.move(FORWARD, 1)
    agent.interact(FORWARD)
})
player.onChat("part4", function () {
    while (agent.inspect(AgentInspection.Block, DOWN) != OBSIDIAN) {
        if (agent.detect(AgentDetection.Block, FORWARD)) {
            agent.turn(RIGHT_TURN)
        }
        agent.move(FORWARD, 1)
    }
    agent.interact(FORWARD)
})


```
