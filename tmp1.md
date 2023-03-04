## uml: state diagram
1
```plantuml
SELECT  *
FROM  TMP
```
2

Regular **Markdown** here.

<div hidden>
```
@startuml firstDiagram

Alice -> Bob: Hello
Bob -> Alice: Hi!
		
@enduml
```
</div>

![](firstDiagram.svg)

Some more markdown.


```plantuml
@startuml
scale 600 width
skinparam backgroundColor #FFEBDC
[*] -> Begin
Begin -right-> Running : Succeeded
Begin --> [*] : Aborted
state Running {
  state "The game runneth" as long1
  long1 : Until you die
  long1 --> long1 : User interaction
  long1 --> keepGoing : stillAlive
  keepGoing --> long1
  long1 --> tooBadsoSad : killed
  tooBadsoSad --> Dead : failed
}
Dead --> [*] : Aborted
@enduml
```
