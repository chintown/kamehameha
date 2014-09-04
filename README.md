#Kamehameha — the way you perform infinite loading

## What is kamehameha?

![kamehameha](./kamehameha.gif)

> Kamehameha is a kind of energy attack in the [Dragon Ball](https://en.wikipedia.org/wiki/Dragon_Ball) series, and is [Goku](https://en.wikipedia.org/wiki/Goku)'s signature technique.

## How it goes with infinite loading

Let's simplify **kamehameha** and compare it with **infinite loading**:

| states  | action | kamehameha | infinite scrolling |
| --	 | -- | -- | -- |
| ready | ![1](./examples/img/ready.png) | watch on certain enemy | watch on scrolling event |
| triggering | ![2](./examples/img/trigger.png) | make a right pose | scroll the page to bottom |
| locked | ... | can't be interrupted until finish the action | can't issue next request until finish current request |
| holding | ![3](./examples/img/hold.png) | collect energy | request data through ajax | 
| emitting | ![4](./examples/img/emit.png) | booom!!! | redering the results |
| resting | ![5](./examples/img/rest.png) | take a rest | delay a short period (to avoid request burst) |
| unlocked | ... | go back to ready state | go back to ready state |

## Kamehameha in action

![kamehameha](./demo.gif)