# A 2 player 2D shooter game in pygame

## Installing Dependencies
```bash

pip install -r requirements.txt

```
## Basic usage

 The followig code creates an env and takes random actions

```python
from env import env
run = True
    env = env(display_dimension=(600,600), fps=60)
    env.create()
    
    while run:
        for event in pygame.event.get():
            if(event.type == pygame.QUIT):
                run = False
        actions = env.randomAction()
        data = env.Step(actions)

        if(data[-1]):
            env.reset()  

```
