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


## How it works

1. Create a **GoKu**. (**GoKu** is the character who can perform **kamehameha** with great power. "Kamehameha" is hard to spell. "Goku" should be more human-friendly.)

	```js
	var options = {
		watch: function (next) {}
		,shouldTrigger: function (event) {}
		,onHold: function (event) {}
		,onEmit: function (event) {}
		,restingSeconds: (number)
	}
	var goku = new Goku(options);
	```

2. Decide a watching target (**options.watch**). By default, he watches on window *scroll* event

3. Decide a triggering condition (**options.shouldTrigger**). By default, he tirggers the action while page reaches bottom

4. Decide a callback to perform ajax requesting (**options.onHold**).

	```js
	// load 10 images from http://lorempixel.com/
	```

5. Decide a callback to perform data rendering (**options.onEmit**).

	```js
	// for each loaded image 	
	$container.append($(<img>).attr('src', url));
	```
6. Decide how long to take a rest (**options.restingSeconds**)

7. Ask **Goku** to study what you teach and start to work

	```js
	goku.study();
	```


## Kamehameha in action

![kamehameha](./demo.gif)