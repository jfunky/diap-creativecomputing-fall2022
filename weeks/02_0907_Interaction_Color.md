## Subversion & Surveillance

#### Notes

- Culture jamming: 1950/60s avant garde methods for inverting power dynamics, ironic re-appropriation of pop culture semiotics to critique traditional structures of value, mass media, consumerism, governance; see also: agitprop, guerilla communication, détournement
- Early techno-utopian vision of the internet as democratic, accessible, global (obviating borders)
  - Early social networks and community discussion boards
- 90's & 00's in this realm demystified the internet, how hyperlinks work, explored global information networks
- Also: progressively more tools for government & corporate survellance and re: the internet, the consolidation of search, media, news into fewer companies
- "The War on Terror" and subsequent revelations of the states' expanded surveillance powers has broadened the discource around data privacy rights, which is now a major area of focus among artists, activists, journalists, legislators

#### Art

- [Astro Noise](https://www.artsy.net/show/whitney-museum-of-american-art-1-laura-poitras-astro-noise?sort=partner_show_position), Laura Poitras
- [net.flag](https://www.guggenheim.org/artwork/10703), Mark Napier
- [Glyphiti](http://artcontext.net/glyphiti/docs/about.html), andy deck'
- [MILKproject](https://www.polakvanbekkum.com/done/major-gps-projects/milk-project/), Esther Polak, Ieva Auzina, Marcus The
- [Zoom Escaper](https://lav.io/projects/zoom-escaper/), Sam Lavigne

## Animation

- Recall: the draw loop runs continuously at a default rate of 60x per second
- You can animate movement or color

#### Variable Review & Part 2

- Variables can vary in value
- Declaring variables: sets aside a space in memory to store data
  - Use [let](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let) rather than the [var](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let) keyword
  - You can also use [const](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var) in cases where the variable value will not vary
  - let & const are "block scoped"
- Initializing variables: assigning a value

#### Some Math

- Addition +
- Subtraction -
- Multiplication \*
- Division /
- Assignment =
- Javascript follows PEMDAS order
- Shorthand
  - x++ (equivalent to x=x+1)
  - x-- (equivalent to x=x-1)
  - x+=10 (equivalent to x=x+10)
  - x-=10 (equivalent to x=x-10)
- random()

#### [Color functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var)

- color() creates colors as color data type to store in variables
- lerpColor() blends two colors for a third in-between color
- colorMode() changes the way p5 interprets color values allowing you to use HSB or HSL instead of default RGB

#### [Mouse & Keyboard interaction](https://p5js.org/reference/#group-Events)

- mouseIsPressed boolean variable versus mousePressed() function
- keyIsPressed boolean variable versus KeyPressed() function

## Resources

- P5.js reference:
  - [Interactivity](https://p5js.org/learn/interactivity.html)
  - [Color](https://p5js.org/learn/color.html)
  - [Debugging](https://p5js.org/learn/debugging.html)
- Getting Started with P5.js ch.4
- The Coding Train tutorials:
  - [Varibles Part 1](https://www.youtube.com/watch?v=RnS0YNuLfQQ)
  - [Variables Part 2](https://www.youtube.com/watch?v=Bn_B3T_Vbxs)
  - [Boolean Variables](https://www.youtube.com/watch?v=Rk-_syQluvc)
- Learning Processing, ch.3-4
- [Git & Github for Poets](https://www.youtube.com/playlist?list=PLRqwX-V7Uu6ZF9C0YMKuns9sLDzK6zoiV)

## Assignment

- Create a new sketch or build on your sketch from last week, where there is a change in the color, animation, or design based on mouse or keyboard input.
- Stretch goal: Incorporate at least one random element that changes over time, with user input, or when the sketch loads.
- Add a link to the [homework wiki](https://github.com/jfunky/diap-creativecomputing-fall2022/wiki/Homework).
- Read: [A short history of color theory](https://programmingdesignsystems.com/color/a-short-history-of-color-theory/index.html) & [Color models and color space](https://programmingdesignsystems.com/color/color-models-and-color-spaces/index.html) by Rune Madsen
