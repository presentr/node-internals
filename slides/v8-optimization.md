##  v8 optimization

- "Hot" code is abstracted to "Hidden Classes"
- When a class changes members it has to deoptimize

```
    |<---------------------------------------------------------|                          
    |                                                          | deop
    |                         /---------------> [ Optimized ]--|
    |                        /                        |  
    |                       / "hot code"              | <- too many deops
JS -|->[ Unoptimized Code ]{                          | 
                            \                         |
             certain syntax  \-------------> [ Never optimized ]

```

note:
  - hot code is optimized
  - code is doptimzied when its members change
  - if the new shiz is "hot" it's re-optimized
  - too many opt/deopt flaps move it into 'unoptimized hell'
