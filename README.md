## Youtube Adventure Mapper

Youtube used to allow annotations, clickable links that overlay a video, so some resourceful people created some choose-your-own-adventure games using videos and annotations which link to other videos.

One example is [The Dark Room](https://www.youtube.com/watch?v=OqozGZXYb1Y) by Australian comedian John Robertson.

This tool allows you to map these adventure games.

## Usage

> `node youtube-adventure-mapper.js <options> [url]`

There is, at the moment, only one option:

> `-o <filename> : sets the base output filename`

The url must be a valid youtube video url. Or one of the following example values:

> `escape` - a short youtube adventure involving nerf guns

> `darkroom` - the Dark Room by John Robertson.

So, just for clarity here are some examples of usage:

> `node youtube-adventure-mapper.js -o graph https://www.youtube.com/watch?v=Jm-Kmw8pKXw`

Or

> `node youtube-adventure-mapper.js -o graph darkroom`

This will create four output files:

- graph.json
- graph.dot
- graph.svg
- graph.png

## Output

The output consists of four files named 'output' with an appropiate extension by default:

- output.json - a JSON representation of the videos and their annotation links to other videos.

- output.dot - can be plotted as a graph using the [Graphviz](https://www.graphviz.org/) visualization software.

- output.svg - a vector graphics plot created using the [viz.js](https://www.npmjs.com/package/viz.js) module.

- output.png - a png conversion of the svg file created using [svg2img](https://www.npmjs.com/package/svg2img).

## Examples

The repository contains examples of maps generated from these three youtube games:

- [The Dark Room (2016)](https://www.youtube.com/watch?v=Jm-Kmw8pKXw)
- [Choose Your Adventure](https://www.youtube.com/watch?v=OqozGZXYb1Y)
- [Youtube Street Fighter](https://wwhttps://www.youtube.com/watch?v=LPQ1XrllZmA)

An example of the two output files and an svg graph are below

### The Dark Room

![alttext](darkroom.svg)

### Choose Your Adventure

![alttext](choose_your_adventure.svg)

### Street Fighter

This didnt turn out very well for some reason.

Note that the dot file for this was modified to increase the vertical node spacing and make it more readable.

```
digraph {
  graph [pad="0.5", nodesep="0", ranksep="3"];
  node[shape = circle]
  ...
```

![alttext](street-fighter.svg)
