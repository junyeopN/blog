# Blueprint

## How to open Level Blueprint

![blueprintforlevel](../../images/unreal8.png)

![unrealeventgraph](../../images/unrealeventgraph.pngz)

## BluePrint Glossary

| Term          | Definition                                              |
| ------------- | ------------------------------------------------------- |
| Event Graph   | The Canvas for our Blueprint                            |
| Node          | Premade functionality we can drop and use in Blueprint. |
| Event         | A "when" node                                           |
| Pins          | Socket we can connect up                                |
| Input Pin     | When to run this node (left pin)                        |
| Output Pin    | What to do (right pin)                                  |
| Connections   | Wires between pins                                      |
| Objects       | Collection of data and functionality                    |
| Actors        | Objects that can go in a level                          |
| Components    | Objects that can go on an actor                         |
| Data Pin      | Input or Output data of a node (blue pin)               |
| Execution Pin | When to run this node (white pin)                       |
| Return Pin    | Output of a node                                        |
| Spawn         | Creating an Object while playing                        |
| Transform     | Location, rotation and scale                            |

![unrealpin](../../images/unrealpins.png)

![unrealdatapin](../../images/unrealdatapin.png)

## Physics Implementation

- Physics option:

![unrealphysics1](../../images/unrealphysics1.png)

- Gravity option:

![unrealgravity](../../images/unrealgravity.png)

- Mass: calculated by default. Can check and enter custom value too.

![unrealmass](../../images/unrealmass.png)

- Data node pins: **ran when Unreal thinks they need to run, no specification.**

## Keyboard Events

- Triggered when a keyboard input is pressed.
- has pressed/released/key pins

![unrealkeyboardevent](../../images/unrealkeyboardevent.png)

## Impulse

- Moves mesh by certain vector direction

![impulse](../../images/impulse2.png)

- F = MA
- Impulse = Mass \* Velocity Change

ex) increase speed by 400 = 4m/s (since unreal uses cm default) : impulse needs to be **4 \* mass**

however, if we check vel change, **unreal automatically calculates impulse needed to change by given vector unit.**

![impulse2](../../images/impulse3.png)

## Blueprint Class

![blueprint class](../../images/unrealblueprintclass.png)

## Spawn Class

![blueprint spawn](../../images/unrealbpprojectile.png)

![blueprint spawn2](../../images/unrealbpprojectile2.png)

![blueprint spawn3](../../images/unrealbpprojectile3.png)

![blueprint spawn4](../../images/unrealbpprojectile4.png)

## Pawn

- While playing, hold F8 to spawn : **Physical representation of the player in the game**

![pawn](../../images/unrealpawn.png)

- Cannot find in scene - **spawned to "PlayerStart" Actor by default**

![playerstart](../../images/unrealplayerstart.png)

- Can get in blueprint by "Get Player Pawn"

![pawn](../../images/pawn.png)

- Pawn rotation doesn't change with the camera rotation by default - **Need control rotation.**

![controlrotation](../../images/pawncontrolrotation.png)

- You need to connect both data pin and execution pin with impulse

![impulse](../../images/unrealconnectdataandexec.png)

- forward vector to get the direction vector of facing direction

![forwardvector](../../images/unrealforwardvector.png)

- multiply node - convert to integer

![multiply](../../images/unrealmultiply)

## BSP (Binary Space Partitioning)

- Used to easily create custom objects

![placeactor](../../images/place_actor_panel.png)

![placeactor2](../../images/place_actor_panel2.png)

- For these shapes, **adjust the brush settings instead of the transform scale**

![placeactor3](../../images/place_actor_panel3.png)

- brush can also **subtract from brush that is already existent**

![subtractive](../../images/place_actor_panel4.png)

- save and set this map to default level

![defaultlevel2](../../images/defaultlevel2.png)

## Materials and Lights

- filter search to find only certain asset types:

![filter search](../../images/materialfiltersearch.png)

- directional light: rotate to change light direction

## Actor Component

- An actor that holds multiple actors - root and childs
- Drag a mesh to StaticMeshComponents

![comp](../../images/actorcomponents.png)

- Childs get relative location to the parent actor - because of this when we rotate/move/scale the parent, the child does the same.

![comp2](../../images/actorcomponents2.png)

## Collision Mesh

- Watch collision mesh view

![collision mesh](../../images/collisionview.png)

![collision mesh2](../../images/collisionview2.png)

- Open Static mesh editor by double clicking the static mesh

![collision mesh3](../../images/collisionview3.png)

- Remove collision and add Z simplified axis

![collision mesh4](../../images/collisionview4.png)

![collision mesh5](../../images/collisionview5.png)

- Come back to editor. Much more simpler mesh

![collision mesh6](../../images/collisionview6.png)

## Functions

- Collapse to function

![function](../../images/blueprintfunction.png)

![function2](../../images/blueprintfunction2.png)

- Input pin and output pin

![function3](../../images/blueprintfunction3.png)

![function4](../../images/blueprintfunction4.png)

- If function doesn't have side effects, check pure
- If pure is checked, the execution pin is gone, since pure function can be thought of a modification that can be done any time before the next pin, and doesn't need specific execution order.

![pure](../../images/blueprintfunction5.png)


## Member Function

* Double click a mesh to open its blueprint editor

* Add function = member function, can use self reference

![self](../../images/selfreference.png)

