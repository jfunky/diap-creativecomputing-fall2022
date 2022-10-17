## Web Audio

#### Brief History

- [bgsound](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/bgsound) html element (deprecated)
- [embed](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/embed) html element for multimedia
- Adobe Flash Player [(deprecated)](https://www.adobe.com/products/flashplayer/end-of-life-alternative.html) allowed for more precise manipulation of sound
- [audio](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/audio) html tag provides native support for audio playback in all modern browsers (with limitations around precise timing, real-time effects, sound analysis)
- [Web Audio API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API) allows for loading & manipulating sound files without using plugins, as well as more complex sound processing

#### References

- [Awesome web audio](https://github.com/notthetup/awesome-webaudio) github
- [Interactive audio for the web](https://vispo.com/misc/ia.htm) list of projects
- [Awesome live coding music](https://github.com/pjagielski/awesome-live-coding-music)

## Functions

#### You've been using functions this whole time
- A functions is a block of code that is executed when something "calls" it
- They take some input and provide some output
- Calling a function will execute the procedure defined with any indicated parameters, then continue to execute the next piece of code
- Callback functions are passed into another function as an argument

#### Defining your own functions
- Useful once you want to execute the same code more than once
- By abstracting re-used areas of code, you can make your code more modular
- Parameters provide flexibility, based on where you want to add variation in your function
- Parameters are variables created when the function runs
- You can use functions to return a value to the main program
- Like with variables, function names should be unique (not a name already in use by another function) and descriptive

#### Loading & Playing Sound
- [loadSound()](https://p5js.org/reference/#/p5/loadSound)
- filesize limited in the p5.js web editor is 5MB
- Javascript is asynchronous. A lot of the code we've run so far has been synchronous, which means it executes in order. However, in some cases javascript will continue executing code that follows, even when code earlier in the program hasn't completed executing yet. You might notice this when you are loading images, video, sound files, or data files. To make sure the media/files have loaded by the time you use them, you can load them in the preload function rather than in setup.
- Another way to handle asynchronicity is by using a callback function. The function passed through as a parameter is not executed right away. Instead, it is called once some work is done or a relevant event happens.

## Resources
- [Class examples](https://editor.p5js.org/jfunky/collections/lOc5D2DXq)
- Getting Started With p5.js, ch.9, ch.7 (Media)
- The Coding Train 
    - [Functions](https://www.youtube.com/playlist?list=PLRqwX-V7Uu6ajGB2OI3hl5DZsD1Fw1WzR) tutorials
    - [Uploading Media Files](https://www.youtube.com/watch?v=rO6M5hj0V-o)
    - [Loading and Playing Sound](https://www.youtube.com/watch?v=Pn1g1wjxl_0&list=PLRqwX-V7Uu6aFcVjlDAkkGIixw70s7jpW)

## Assignment
- Pick one:
    - Refactor a previous assignment using the abstraction & modularity methods we've been covering (variables, loops, functions).
    - Define at least one function and use it in a loop. Use iterations in the loop to vary the arguments to your function.
- Add a link to the [homework wiki](https://github.com/jfunky/diap-creativecomputing-fall2022/wiki/Homework).
