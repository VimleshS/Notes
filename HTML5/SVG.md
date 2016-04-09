# SVG

HTML for graphics! SVG has a DOM structure and you can even use CSS3 and JavaScript!

JavaScript inside SVG is disabled for image-based SVG.

* [Delivering Octicons with SVG](https://github.com/blog/2112-delivering-octicons-with-svg)
* [**An Overview of SVG Sprite Creation Techniques**](https://24ways.org/2014/an-overview-of-svg-sprite-creation-techniques/)
* [**SVG-picture**](http://sarasoueidan.com/blog/svg-picture/)
* [**Pocket Guide to SVG**](http://svgpocketguide.com/book/)
* [**Awesome SVG**](https://github.com/willianjusten/awesome-svg)
* [Lots of SVG information](http://css-tricks.com/mega-list-svg-information/)
* [**SVG on the Web**](https://svgontheweb.com/)
* [**Incredible demo**](http://tympanus.net/codrops/2015/06/18/card-expansion-effect-svg-clippath/)
* [**Icon fonts vs SVG**](https://css-tricks.com/icon-fonts-vs-svg/)
* [Bulletproof Accessible Icon Fonts](https://www.filamentgroup.com/lab/bulletproof_icon_fonts.html)
* [Awesome light ray](http://ncase.github.io/sight-and-light/)
* [Control and filter settings using SVG and JavaScript](http://selfiecity.net/selfiexploratory/)
* [Lonely Planet's switch from icon font to SVG](http://ianfeather.co.uk/ten-reasons-we-switched-from-an-icon-font-to-svg/)
* [Chris Coyier's Using SVG](http://css-tricks.com/using-svg/)
* [Icon system with SVG sprites](http://css-tricks.com/svg-sprites-use-better-icon-fonts/)
* [Animated line drawing - Jake Archibald](http://jakearchibald.com/2013/animated-line-drawing-svg/)
* [Polygon PlayStation 4 and Xbox One review animation](http://product.voxmedia.com/2013/11/25/5426880/polygon-feature-design-svg-animations-for-fun-and-profit)
* [D3.js's gallery collection](https://github.com/mbostock/d3/wiki/Gallery#wiki-collections)
* [Nice icon animation](http://tympanus.net/Development/AnimatedSVGIcons/)
* [List animation](http://tympanus.net/Tutorials/ShapeHoverEffectSVG/index.html)
* [ICONIC](https://useiconic.com)
* [Adaptive SVG](http://w3.eleqtriq.com/2014/02/everything-is-relative-the-art-of-the-adaptive-image/)
* [Leaving pixels behind](https://docs.google.com/presentation/d/1CNQLbqC0krocy_fZrM5fZ-YmQ2JgEADRh3qR6RbOOGk/preview#slide=id.p)
* [Trianglify - SVG background](https://github.com/qrohlf/trianglify)
* [SVG workflow for designers](http://danielmall.com/articles/svg-workflow-for-designers/)
* [SVG4everybody](https://github.com/jonathantneal/svg4everybody)
* [export-svg](https://github.com/mtreik/export-svg)
* [Workflow to export SVG](http://hackingui.com/design/my-workflow-to-export-svgs-out-of-my-photoshop-design-files/)
* [SVG workflow](https://news.layervault.com/stories/28025-ask-dn-switching-from-icon-fonts-to-svg-whats-your-workflow)
* [Snippet expansion for Sublime Text](http://codepen.io/jorgeatgu/blog/svg-snippets)
* [High performance interactions using canvas](http://chairnerd.seatgeek.com/high-performance-map-interactions-using-html5-canvas/)
* [SVG Path](https://github.com/andreaferretti/paths-js)
* [Organized workflow for SVG](http://robots.thoughtbot.com/organized-workflow-for-svg)
* [Animate SVG icons with CSS and Snap.js](http://codyhouse.co/gem/animate-svg-icons-with-css-and-snap/)
* [Best of SVG icons in 2014](http://www.noupe.com/essentials/freebies-tools-templates/best-of-svg-2014-icons-tools-and-resources-86159.html)
* [Optimizing SVG for the web](http://calendar.perfplanet.com/2014/tips-for-optimising-svg-delivery-for-the-web/)
* [The SVG Canvas, Coordinate System, and Viewport](http://www.vanseodesign.com/web-design/svg-viewport/)
* [Write SVG is a PostCSS plugin](https://github.com/jonathantneal/postcss-write-svg)

```
<text>
<circle cx="" xy="">
<ellipse rx="" ry="" fill=""/>
<line>
<polygon fill="" points="350,75 379,161 ...">
<polyline>
<path d="M100,200 C100,100 250,100..."/>
<g fill="rgba(0,0,0,0.3)" transform="rotate()">
  <rect />
</g>
```


## SVG animation

The easiest way to animate SVG is using CSS animations or transitions, but does not work in IE (unless using `requestAnimationFrame`).

The act of "drawing" in an SVG is optical trick caused by manipulating 2 SVG `path` properties: `stroke-dasharray` and `stroke-dashoffset`.

Make the `stroke-dasharray` as long as the path to make it visually invisible. Then use `stroke-dashoffset` to gradually reveal it.

* [Snap.svg](http://snapsvg.io/)
* [Lazy line painter](http://lazylinepainter.info/)
* [**Animated SVGs: Custom easing and timing**](http://oak.is/thinking/animated-svgs/)
* [Not SVG, but related](http://coding.smashingmagazine.com/2013/03/04/animating-web-gonna-need-bigger-api/)
* [d3 and SVG](http://snips.net/blog/posts/2014/01-10-fast-interactive_prototyping_with_d3_js.html)
* [Animation path](http://blog.legomushroom.com/2014/03/defining-advanced-animation-path/)
* [Animating path](https://github.com/ConnorAtherton/walkway)
* [vivus.js - SVG animation](http://maxwellito.github.io/vivus/)

## d3.js

```
var svg = d3.select("body")
  .append("svg");

svg.append("circle")
  .attr("cx", 100)
  .attr("cy", 140)
  .attr("r", 10)
  .attr("fill", "#000000");

d3.selectAll("*").remove(); // If you mess it at console
```

### Selection

* [Section](http://bost.ocks.org/mike/selection/)

### Binding data/Joining data

```
// Data joins!
var dataset = [5, 10, 20, 15, 18];
var datasetObject = [{x: 5, y: 20, r: 10}, {x: 460, y: 90, r: 20}];

var svg = d3.select("body")
            .append("svg")
            .attr("width", w)
            .attr("height", h);

d3.select("svg").selectAll("circle") // `selectAll` return empty selection
  .data(dataset) 			// Enough rooms for 5
  .enter()					// Enter the data value
  .append("circle");
  
d3.selectAll("circle")
  .attr("r", function(d) {		// d is the data value, setup by d3
    return d
  });
  
// Benefits of binding data to elements
// 1. Lets you reference values later
// 2. Prevents need to redraw elements
```


## Examples

* [Nice activity graph using SVG and playback](http://well.blogs.nytimes.com/projects/2014/03/accelerometers.html)


## Tools

* [Grunticon - Search your SVG folder to generate CSS with PNG fallback](https://github.com/filamentgroup/grunticon)
* [Minify your SVG, don't trust Illustrator](https://github.com/sindresorhus/grunt-svgmin)
* [Raphael.js](http://raphaeljs.com/)
* [gRaphael](http://g.raphaeljs.com/)
* [Snap.svg](http://snapsvg.io/)
* [SVGO GUI](https://github.com/svg/svgo-gui)

## People

* [Sarah Drasner](http://sarahdrasnerdesign.com/)