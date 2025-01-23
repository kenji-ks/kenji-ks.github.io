---
layout: project
type: project
image: img/computer-mouse-152249_1280.png
title: "MouseBot"
date: 2022
published: true
labels:
  - Java
  - Programming
  - Game Development
summary: "I developed a bot that controls a mouse while it tries to collect as much cheese as it can before running out of stamina."
---

The bots in the MouseBot project were made to traverse a maze while trying to collect as much cheese as possible. The dimensions of the labyrinth changed on every run, and so did the walls, which prevented them from running the same code repeatedly. Every bot had a stamina bar, which got lower as the mouse moved. If a mouse runs out of stamina, it dies, so the project's goal was to collect as much cheese as possible before that happens. The more cheese the mouse has on it, the more stamina it takes to move.

The mice also had charging pads, which allowed them to recharge and stay alive. When programming my MouseBot, I tried to add code that made it recognize where the closest charging pad was and when it was safe to walk over to it. I also added code that allowed my MouseBot to drop cheese when necessary. This allowed my MouseBot to stay alive for the longest while being the most efficient.

Here is some code that illustrates how I did this:

```java
public class Miu2 extends MouseBot
{

    public Miu2()
    {
        setName("Miu2");
        this.setPreferredColor(Color.YELLOW);
    }

    public int chooseAction()
    {
        //Go towards first destination if materials are met...
        if (this.getListOfVisibleDestinations().size() > 0){
            if(this.getListOfVisibleDestinations().get(0).areRequirementsMet(this.getMyMaterialList())){
                return this.getDirectionTowards(getListOfVisibleDestinations().get(0));
            }
        }
  }
```
