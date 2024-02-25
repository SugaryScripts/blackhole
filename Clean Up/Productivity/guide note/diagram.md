## Pie Chart
``` mermaid
pie title usage
"Mobile":25
"Web":120
```

## Graph 
### Direction
to Top to Bottom `graph TB`
to Bottom to Top `graph BT`
to Left to Right `graph LR`
to Right to Left `graph RL`

``` mermaid
graph TB
A-->B
```

### Shapes
1. Normal Box
``` mermaid
graph TD
boxa[Normal Box with text]
```
2. Pill Shaped Box
``` mermaid
graph TD
boxa([Normal Box with text])
```
3. Box with Rounded edges
``` mermaid
graph TD
boxa(Normal Box with text)
```
4. Subroutine shaped Box
``` mermaid
graph TD
boxa[[Normal Box with text]]
```
5. Cylindrical Shape
``` mermaid
graph LR
boxa[(Normal Box with text)] --> boxb[(Database B)]
```
6. Circle
``` mermaid
graph TD
boxa((Normal Box with text))
```
7. Asymmetric Shape
``` mermaid
graph TD
boxa>Normal Box with text]
```
8. Rhombus
``` mermaid
graph TD
boxa{Normal Box with text}
```
9. Hexagon
``` mermaid
graph TD
boxa{{A}}
```
10. Parallelogram
``` mermaid
graph TD
boxa[/Normal Box with text/]
```
11. Parallelogram Alt
``` mermaid
graph TD
boxa[\Normal Box with text\]
```
12. Trapezoid
``` mermaid
graph TD
boxa[/Normal Box with text\]
```
13. Trapezoid Alt
``` mermaid
graph TD
boxa[\Normal Box with text/]
```

### Links
1. Arrow Head
``` mermaid
graph LR
A --> B
```
2. Open Link
``` mermaid
graph LR
A --- B
```
3. Text on Link
``` mermaid
graph LR
A --Text--> B
```
4. Dotted Link
``` mermaid
graph LR
A -.-> B
```
5. Dotted Link with Text
``` mermaid
graph LR
A -.Text.-> B
```
6. Thick Link
``` mermaid
graph LR
A ==> B
```


## State Diagram
```mermaid
stateDiagram-v2
Push --> Move
Move --> Stop
```
```mermaid
stateDiagram-v2
[*] --> s1
s1 --> [*]
```






