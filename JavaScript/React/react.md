# React

- [Qiita blog](http://qiita.com/kimagure/items)
- [**9 things every React beginner should know**](https://camjackson.net/post/9-things-every-reactjs-beginner-should-know)
- [**React and ES6 - Part 1**](http://egorsmirnov.me/2015/05/22/react-and-es6-part1.html)
- [React Cheat Sheet](http://reactcheatsheet.com/)
- [**RAW React!**](http://jamesknelson.com/learn-raw-react-no-jsx-flux-es6-webpack/)
- [**React Inspire - Curated sites built with React.js**](http://reactinspire.com/)
- [**https://github.com/sindresorhus/awesome**](https://github.com/sindresorhus/awesome)
- [**React Primer**](https://github.com/mikechau/react-primer-draft)
- [**Essential JavaScript links**](https://github.com/ericelliott/essential-javascript-links#essential-javascript-links)
- [**Nice survey tutorial**](http://www.browniesblog.com/A55CBC/blog.nsf/dx/reactjs_tutorial.html)
- [**Navigating the React ecosystem**](http://www.toptal.com/react/navigating-the-react-ecosystem)
- [ReactConf 2015 notes](http://chantastic.io/2015-reactjs-conf/)
- [React Cheatsheet](http://ricostacruz.com/cheatsheets/react.html)
- [**React Kung Fu**](http://reactkungfu.com/)
- [**Easy React Book**](http://easyreactbook.com/book/intro)
- [Setting up Vim for React.js](https://jaxbot.me/articles/setting-up-vim-for-react-js-jsx-02-03-2015)
- [Comprehensive list of React resources](http://www.gajotres.net/a-comprehensive-list-of-reactjs-resources/)
- [Learn React in 8 mins](https://blog.skcript.com/learn-react-js-in-7-min-92a1ef023003)
- [Coding with React like a Game Developer](https://medium.com/@PhilPlckthun/coding-with-react-like-a-game-developer-e39ffaed1643)
- [**React.js Best Practices and Tips**](http://www.toptal.com/react/tips-and-practices)
- [Angular is easy, React is hard?](https://medium.com/@ericclemmons/angular-is-easy-react-is-hard-6f55e360482c#.xpvodmu4u)
- [Why and how to bind methods](http://reactkungfu.com/2015/07/why-and-how-to-bind-methods-in-your-react-component-classes/)

> React is truly only for UI. Put your business logic elsewhere in plain JavaScript objects.

* [Setting up Vim for React.js](https://jaxbot.me/articles/setting-up-vim-for-react-js-jsx-02-03-2015)
* [Problem with Backbone rendering view](http://ianstormtaylor.com/rendering-views-in-backbonejs-isnt-always-simple/)

> The value of DI is that we can depend on abstract ideas instead of concrete implementations.

Why SPA? Imagine using Facebook where every like and every comment made you refresh the page.

Web Application has 3 parts

1. Listen for user events
2. Handle network events (XHR, WebSocket)
3. Manipulate the DOM (Rendering)

> Simplicity is prerequisite for reliability

KVO is built around Observables and Computed Properties.

https://github.com/reactjs/react-future/blob/master/09%20-%20Reduce%20State/01%20-%20Declarative%20Component%20Module.js

After a while, you will see the "cascading updates" problem, where a ListView will trigger a side drawer for input and once done, hide the drawer, update the ListView and update the counter, present a new dialog based on the newly added list, etc.

* [NativeScript??](https://www.nativescript.org/blog/answering-nativescript-beta-webinar-questions)

## Context

* [Context in React and Dependency Injection](http://jaysoo.ca/2015/06/09/react-contexts-and-dependency-injection/)
* [The land of the undocumented: The Context](https://medium.com/@skwee357/the-land-of-undocumented-react-js-the-context-99b3f931ff73)
* [Issue #2112 - Switch the Context to use the parent tree instead of the owner tree](https://github.com/facebook/react/issues/2112)

```js
const Text = (props, context) =>
  <p style={context}>{props.children}</p>;

Text.contextTypes = {
  fontFamily: React.PropTypes.string
};

class App extends React.Component {
  static childContextTypes = {
    fontFamily: React.PropTypes.string
  }
  getChildContext() {
    return {
      fontFamily: 'Helvetica Neue'
    };
  }
  render() {
    return <Text>Hello World</Text>;
  }
}
```

## Real-time

* [Create a character voting app with Socket.IO](http://sahatyalkabov.com/create-a-character-voting-app-using-react-nodejs-mongodb-and-socketio/)
* [React and Socket.IO chat app](http://danialk.github.io/blog/2013/06/16/reactjs-and-socket-dot-io-chat-application/)

## Examples to Learn

* [react-baby-steps](https://github.com/RisingStack/react-baby-steps)
* [Percolate Studio's router](https://github.com/percolatestudio/percolatestudio.com/blob/master/app/components/Routes.jsx)
* [JWT router example](https://github.com/auth0/react-flux-jwt-authentication-sample/blob/gh-pages/src/app.jsx#L11-L29)
* [cosmos.js](https://github.com/skidding/cosmos)
* [react-flux-jwt-authentication-sample](https://github.com/auth0/react-flux-jwt-authentication-sample)
* [fixed-data-table](https://github.com/facebook/fixed-data-table)
* [React router auth flow example](https://github.com/rackt/react-router/blob/master/examples/auth-flow/app.js)
* [Authenticated route example from Ryan Florence](https://gist.github.com/ryanflorence/c1fe013af753456c1ca9)
* [Avatar.js](https://gist.github.com/ryanflorence/bded2eadf8094704d0ab)
* [react-textarea-autosize](https://github.com/andreypopp/react-textarea-autosize)
* [Date Picker](http://react.rocks/tag/DatePicker)
* [`<ReactFitText>`](https://github.com/gianu/react-fittext/blob/master/lib/ReactFitText.js)
* [react-ui-builder](https://www.npmjs.com/package/react-ui-builder/)
* [Sample mobile application with React](http://coenraets.org/blog/2014/12/sample-mobile-application-with-react-and-cordova/)
* [react-new-way](https://github.com/KamilLelonek/react-new-way)
* [react-es6](https://github.com/topheman/react-es6)
* [Atomic](http://thenextweb.com/creativity/2015/02/19/meet-atomic-missing-tool-interface-design-thats-entirely-browser/)
* [Idiomatic React](https://github.com/netgusto/IdiomaticReact)
* [Web publishing platform](https://github.com/vesparny/morpheus)
* [sprintly-kanban](https://github.com/sprintly/sprintly-kanban)
* [reddit-mobile](https://github.com/reddit/reddit-mobile)
* [Tchaik](https://github.com/tchaik/tchaik)
* [Creating a real-time photo experience with Socket.io](http://ditrospecta.com/javascript/react/es6/socketio/nodejs/realtime/2015/08/21/creating-real-time-instagram-socketio-react.html)
* [Trader desktop](http://coenraets.org/blog/2015/03/real-time-trader-desktop-with-react-node-js-and-socket-io/)

### File Structure Examples

* [From mrtnbroder](https://gist.github.com/mrtnbroder/4a4a00d6e158df82611e)
* [From Ryan Florence](https://gist.github.com/ryanflorence/110d4538bf98694538de)
* [From Ryan Florence... again](https://gist.github.com/ryanflorence/daafb1e3cb8ad740b346)

## Style Guides

* [**JSX style guide from Airbnb**](https://github.com/airbnb/javascript/tree/master/react)
* [react-pacomo](https://github.com/unicorn-standard/react-pacomo)
* [Khan Academy's style guide](https://github.com/Khan/style-guides/blob/master/style/react.md)
* [React-starter kit style guide](https://github.com/kriasoft/react-starter-kit/blob/master/docs/react-style-guide.md)
* [React tips and best practices](http://aeflash.com/2015-02/react-tips-and-best-practices.html)
* Think in Elements. Think about the `<img>` element. It has `src`, `width`, `height` properties. It dispatches `load` event when it is fully loaded.
* Domain-specific components are "containers" and atomic components are "components"
* [**CSS Modules**](http://glenmaddern.com/articles/css-modules)

```js
{ this.state.show && 'This is Shown' }
{ this.state.on ? 'On' :  Off }
```
	
Move complex JSX out of `render`

```js
// Notice the parentheses here.
var complexHtml = (
  <Section>
    <InnerSection />
    <InnerSection />
  </Section>
);

return (
  <div>
    { complexHtml }
  </div>
);
```

```js
import React, { Component } from 'react';

class Builder extends Component {
  willTransitionTo(transition) {
    // Check authentication
  }

  componentDidMount() {
    this.databaseRef = new Firebase();
    this.databaseRef.on('dataFetched', function() {
      this.setState(...);
    });
  }

  render() {
    return ();
  }
}
```

## Browser Support

If you need IE8 support, you need to include [es5-shim](https://github.com/kriskowal/es5-shim) yourself to make use of several `Array` and `Date` functions.

You are need to include [html5shiv](https://github.com/aFarkas/html5shiv) for IE8.

## Fastclick

* [react-tap-event-plugin](https://github.com/zilverline/react-tap-event-plugin)
* [react-tappable](https://github.com/JedWatson/react-tappable)
* [react-hammerjs](https://github.com/JedWatson/react-hammerjs)
* [IE 10 touch events](https://github.com/facebook/react/issues/499)

```js
React.initializeTouchEvents(true); // But put where??
```

## People

* [Christopher Chedeau](http://blog.vjeux.com/), [@Vjeux](https://twitter.com/Vjeux)
* [Tom Occhino](https://twitter.com/tomocchino)
* [Michael Johnston](Creator of React Canvas)
* [Ben Anderson](http://www.banderson.me/)
* [Kevin Dangoor - Adobe Brackets](http://www.kevindangoor.com/blog/)
* [Ian Obermiller](http://ianobermiller.com/blog/)
* [David Nolen](http://swannodette.github.io/)
* [Huey Petersen](http://hueypetersen.com/)

> "Given the extremely tight coupling between the template and it's context (a controller/component), the concerns are the same, and splitting the DOM into a template is an arbitrary separation of technologies rather than a legit separation of concerns." - Hence in React, everything is a component. There is no template. Just define a `render` function.

---
> "The React alternative is programming like you are throwing away your entire component and re-rendering it every time because it is simpler and easier to reason about. Event-based and data binding approaches frequently run into timing problems keeping track of which callback gets called first as well as make it difficult to understand how a small change in state will affect performance."

http://facebook.github.io/react/index.html

---
> Mutable state and 2-way bindings made it hard to reason about.

**React replaces an imperative mutating API with a declarative one that favors immutability.**

Declarative -> Predictable -> Confidence -> Reliability

* Components rather than templates
* State is hard to manage
* DOM insertion is painful!
* No controller in React
* No template in React
* The single source of truth is all at the Component
* All the stuffs that live on the Ember controller live in React component
* Developed by Facebook
* Predictable Web Framework
* Expressive and modular
* Just the "V"
* Component ownership pattern (iOS-like?) - Top-level components, higher hierarchy tell children how they should render.
* Components can be stateful
* Encouraged 1-way data flow
* Highly performant
* Good practices of creating very very small components
* Re-render everything on every change
* Model states, not transitions
* Declarative programming
* Immediate mode rendering

React don't like 2-way data binding and template. It like one-way data flow and no template.

```
f(d) = v
f(d`) = v`
diff(v, v`) = changes
diff(v`, v) = undo # Go back in time, getting undo for free

d = data
v = virtual DOM
```

`renderComponentToString() // Isomorphic applications`

The initial HTML can be generated on the server. React handles the "view" but not with templates in the usual sense. React views are not dumb, they are "virtual DOM".

Using a [difference algorithm](http://calendar.perfplanet.com/2013/diff/) to calculate the fewest number of steps required to render each state.

Render (and re-render) a view hierarchy to any sort of backend you want. It is DOM agnostic.

What makes UI so hard? State changing over time is evil.
Model your UI as pure function.

* [**A small open-source app made with React and Rails-api**](http://jamesknelson.com/introducing-memamug-a-small-open-source-app-made-with-react-and-rails-api/)
* [**Build with React**](http://buildwithreact.com/)
* [**Nice tutorial to start**](http://blog.risingstack.com/the-react-way-getting-started-tutorial/)
* [**$19 book**](http://swizec.com/reactd3js)
* [**Master React - Another book**](http://ludovf.net/reactbook/)
* [**React Primer**](https://github.com/mikechau/react-primer-draft)
* [Why React? (2013 articles)](http://facebook.github.io/react/blog/2013/06/05/why-react.html)
* [React Conf roundup](http://facebook.github.io/react/blog/2015/02/18/react-conf-roundup-2015.html)
* [**A comprehensive guide to building apps with React**](http://tylermcginnis.com/reactjs-tutorial-a-comprehensive-guide-to-building-apps-with-react/)
* [**Why React is awesome**](http://jlongster.com/Removing-User-Interface-Complexity,-or-Why-React-is-Awesome)
* [**Awesome React**](https://github.com/enaqx/awesome-react)
* [60fps mobile web](http://engineering.flipboard.com/2015/02/mobile-web/)
* [**Fixed Data Table**](https://github.com/facebook/fixed-data-table)
* [What's so great about React](http://www.reddit.com/r/javascript/comments/2uvz0x/whats_so_great_about_reactjs/)
* [React.js and ES6 classes](http://www.reactbook.org/blog/reactjs-es6-classes.html)
* [Takeaways from React.js Conf 2015](http://kevinold.com/2015/01/31/takeaways-from-reactjs-conf-2015.html)
* [Tweet on Michael Jackson's react](https://twitter.com/mjackson/status/466286956989542400)
* [Why React Native matters](http://joshaber.github.io/2015/01/30/why-react-native-matters/)
* [**React Future??**](https://github.com/reactjs/react-future)
* [**React Components - Searchable database**](http://react-components.com/)
* [**Presenting the most over-engineered blog ever - Pretty insightful**](http://jlongster.com/Presenting-The-Most-Over-Engineered-Blog-Ever)
* [**React.js UI framework for hybrid mobile apps**](http://touchstonejs.io/)
* [Pete Hunt: High performance functional programming with React and Meteor](http://www.youtube.com/watch?v=qqVbr_LaCIo)
* [**React: RESTful UI Rendering**](https://www.youtube.com/watch?v=IVvHPPcl2TM)
* [**Reactive UI**](http://blog.percolatestudio.com/engineering/reactive-user-interfaces/)
* [Building robust web apps with React](http://maketea.co.uk/2014/03/05/building-robust-web-apps-with-react-part-1.html)
* [Using react with browserify](https://medium.com/publish-what-you-learn/a1ea2dd606b)
* [Example](https://github.com/aslansky/react-stack-playground)
* [Gulpfile example for reactify](https://github.com/callum/tool-test/blob/master/gulpfile.js)
* [Client side layout engines: React vs FruitMachine](http://labs.ft.com/2013/10/client-side-layout-engines-react-vs-fruitmachine/)
* [React vs Angular](http://stackoverflow.com/questions/21111217/react-vs-angular)
* [The question of having DOM in JavaScript](https://twitter.com/jo_liss/status/459101670656708608)
* [Faster AngularJS rendering with ReactJS](http://www.williambrownstreet.net/blog/2014/04/faster-angularjs-rendering-angularjs-and-reactjs/)
* [Improving AngularJS long list rendering performance using ReactJS](http://mono.software/posts/Improving-AngularJS-long-list-rendering-performance-using-ReactJS/)
* [Quickcoin nice React programming](http://quickcoin.co/tech/responsive-design-and-multi-platform-live-coding/)
* [Why you might not need MVC with React.js](http://www.code-experience.com/why-you-might-not-need-mvc-with-reactjs/)
* [Introduction to React.js](https://vimeo.com/106261417)
* [Goya](https://github.com/jackschaedler/goya)
* [Rendering React Components on the server](http://www.crmarsh.com/react-ssr/)
* [Om - too mind blow!](https://github.com/swannodette/om)
* [Facebook's Immutable.js](https://github.com/facebook/immutable-js)
* [React.js and how does it fit in with everything else?](http://www.funnyant.com/reactjs-what-is-it/)
* [Pete Hunt response to side-by-side AngularJS comparison](http://www.quora.com/Pete-Hunt/Posts/Facebooks-React-vs-AngularJS-A-Closer-Look)
* [Reactive Rails](http://www.inspire.nl/blog/2015/5/19/reactive-rails-all-you-have-to-know-about-reactjs-library)
* [React for stupid people](http://blog.andrewray.me/reactjs-for-stupid-people/)
* [Do it myself or callback](https://gist.github.com/jamesgpearce/53a6fc57677870f93248)
* [React.rb using Opal](https://github.com/zetachang/react.rb)
* [Some useful React utils](https://github.com/facebook/react/tree/master/src/utils)
* [Fresh on our radar: React Native](http://www.railslove.com/stories/fresh-on-our-radar-react-native)
* [Container components](https://medium.com/@learnreact/container-components-c0e67432e005)
* [Glimmer in React](https://github.com/facebook/react/issues/3226)
* [React: Create maintainable, high-performance UI components - IBM developerWorks](http://www.ibm.com/developerworks/library/wa-react-intro/index.html)
* [React tutorial and guide to the gotchas](https://zapier.com/engineering/react-js-tutorial-guide-gotchas/)
* [Implementing React.js in Swift?](http://blog.scottlogic.com/2015/03/05/reactjs-in-swift.html)
* [React is a terrible idea](https://www.pandastrike.com/posts/20150311-react-bad-idea)
* [Component interop with React and Custom Element](http://addyosmani.com/blog/component-interop-with-react-and-custom-elements/)
* [Mozilla and Web Component](https://hacks.mozilla.org/2014/12/mozilla-and-web-components/)
* [Real-time offline-ready web apps](http://swarmjs.github.io/articles/todomvc/)
* [Exploring hotkeys and focus](http://chrispearce.co/exploring-hotkeys-and-focus-in-react/)
* [Best practices for building large React applications](http://blog.siftscience.com/blog/2015/best-practices-for-building-large-react-applications)
* [How I learned to stop worrying and love React](http://firstdoit.com/react-1/)
* [2 weird tricks that fix React](https://medium.com/@dan_abramov/two-weird-tricks-that-fix-react-7cf9bbdef375)
* [Why React will force you to leave that comfort zone](https://medium.com/@sharifsbeat/why-react-will-force-you-to-leave-that-comfort-zone-e298d3db48bc)
* [React 0.13 and Autobinding](https://medium.com/@goatslacker/react-0-13-x-and-autobinding-b4906189425d)
* [Baby's first reaction](https://medium.com/javascript-scene/baby-s-first-reaction-2103348eccdd)
* [**React, Part I: Building Reactive, Component-based UIs**](http://www.banderson.me/2014/11/01/react-series-intro/)
* [React from scratch](http://ryanfunduk.com/articles/react-from-scratch/)
* [**Introduction to React.js diff algorithm**](http://www.schibsted.pl/2015/06/react-internals-introduction-to-react-js-diff-algorithm/)
* [Ask HN: React - Do you use it? Do you like it?](https://news.ycombinator.com/item?id=9751539)
* [**Making performant React application**](http://greweb.me/2015/08/making-performant-react-applications/)

```
var gulp = require('gulp');
var browserify = require('gulp-browserify]');
var concat = require('gulp-concat');

gulp.task('scripts', function() {
  gulp.src(['./src/main.js'])
      .pipe(browserify({
        transform: ['reactify']
      }))
      .pipe(concat('main.js'))
      .pipe(gulp.dest('./build'));
});
```

## Component - ReactElement

* [React Component, Elements and Instances](https://medium.com/@dan_abramov/react-components-elements-and-instances-90800811f8ca#.bq8rgq5i1)
* [ReactNode, ReactElement, ReactFragment, ReactComponent](https://facebook.github.io/react/docs/glossary.html)
* [Understanding the difference between React Elements and Components](https://quickleft.com/blog/understanding-the-difference-between-react-elements-and-components/)
* [React (Virtual) DOM Terminology](https://gist.github.com/sebmarkbage/fcb1b6ab493b0c77d589#file-react-terminology-md)

> While its true that `React.createElement` is an instruction in a way, all it does is return a plain object (i.e. a `ReactElement`). Passing that `ReactElement` to `ReactDOM.render` is what actually creates the `ReactComponent`. So, you can think of the `ReactElement` as the instruction which is passed to `ReactDOM.render`.

In v0.12, you no longer call it as React Component, but rather call it as ReactElement.

React is functional. Components are just like functions. [They take in `props` and `state` and render HTML](http://facebook.github.io/react/docs/displaying-data.html#components-are-just-like-functions).

```js
f(state, props) = UI Fragment

React.createElement('a', {href: 'http://host'}, 'Hello!')

// In JSX
<a href="http://host">Hello!</a>

// More examples
var MyComponent = React.createClass({
  render() {}
});

var element = React.createElement(MyComponent);

// MyComponent is ReactComponent and you don't normally instantiate it
var component = new MyComponent(props); // never do this
```

Well-written components don't even need state, so:

`f(props) = UI Fragment`

This introduces the concept of idempotency and immutability.

```js
React.renderComponent();   // Deprecated
React.render();            // Use this

React.isValidComponent();  // Deprecated
React.isValidElement();    // Use this

React.PropTypes.component  // Deprecated
React.PropTypes.element    // Use this

React.PropTypes.renderable // Deprecated
React.PropTypes.node       // Use this
```

Components are hierarchical. Without this you won't be able to represent HTML. To access the children:

`this.props.children`

Components are state machines. They have properties (determined by their parent) and state (which they can change themselves, perhaps based on user actions).

## Component Events

```
// Enable touch events for mobile devices
React.initializeTouchEvents(true);
```

## JSX

* [Change and Its Detection in JavaScript Frameworks](http://teropa.info/blog/2015/03/02/change-and-its-detection-in-javascript-frameworks.html)
* [Face-off - Virtual DOM vs Incremental DOM vs Glimmer](https://auth0.com/blog/2015/11/20/face-off-virtual-dom-vs-incremental-dom-vs-glimmer/)
* [**JSX: The other side of the coin**](https://medium.com/@housecor/react-s-jsx-the-other-side-of-the-coin-2ace7ab62b98)
* [A case for JSX](https://medium.com/@thinkfunctional/a-case-for-jsx-73763ee9aa03)
* [WTF is JSX](https://gist.github.com/developit/da77a4d3bbf365908c8c)
* [Static and Dynamic element](https://github.com/facebook/react/issues/3226)
* [Incremental DOM: What is it and why I should care?](https://auth0.com/blog/2015/10/23/incremental-dom/)

> Angular, Ember and Knockout put "JS" in your HTML.
React puts "HTML" in your JS.

JSX is the key to React and it's purpose is to build composable tree/hierarchical UI.

**Scale by composition** - Build it small, compose it and scale it big.

Note: In v0.12, no more `/** @jsx React.DOM */`

```js
<Component /> === React.createElement(Component)

const h = React.createElement;

h('ul', null, [
  h('li', null, 'Foo'),
  h('li', null, 'Bar'),
]);

const ul = React.createFactory('ul');
const li = React.createFactory('li');

ul(null, [
  li(null, 'Foo')
  li(null, 'Bar')
]);
```

Solved cross-site scripting?

Allow to create composite component. Component is the proper separation of concern for us. Not the 3-legged stool of HTML, CSS and JavaScript. But a single JavaScript all the way. More composable?

* [Live JSX compiler for testing](https://facebook.github.io/react/jsx-compiler.html)
* [JSX: E4X The Good Parts](http://blog.vjeux.com/2013/javascript/jsx-e4x-the-good-parts.html)
* [Draft: JSX Specification](http://facebook.github.io/jsx/)

```js
class HelloMessage extends React.Component {
  tick() {
    this.setState({count: this.state.count + 1});  }
  
  render() {
    // No autowinding for tick() in v0.13.0
    return <div onClick={this.tick.bind(this)}>Hello {this.props.name}</div>;  }}
	
React.render(<HelloMessage name="mech" />, mountNode);

// Equivalent to this old ES3 module pattern?
function HellMessage(initialProps) {
  return {
    state: { value: initialProps.initialValue },
    render: function() {
      return <div>Hello {this.state.value}</div>;    }  };}
```

If you use JSX, `displayName` is generated for you.

## Props and States

* [Demystifying React Components State](http://www.sitepoint.com/demystifying-react-components-state/)
* [**Props vs States**](https://github.com/uberVU/react-guide/blob/master/props-vs-state.md)
* [Pending state updates may be confusing #122](https://github.com/facebook/react/issues/122)

`getDefaultProps` only ever called once for "all" instances. Do not do anything like `Date.new` inside `getDefaultProps`.

In Backbone, you are coding imperatively to specify when something changes, certain things should happen through it various view events setup.

In React, things are more declarative. You specify how your UI should look like at the `render()` and through `props` and `states` changes, the UI will change.

Declarative style require developer to think through at the start how the whole component UI look like and how they will interact.

```
---------     ---------
| Props |     | State |
---------     ---------
     +           +
      ----------
      | Render |
      ----------
           |
        -------   
        | DOM |
        -------
```

* Props - Constant and immutable. Likely fixed from the on-set. Supplies as component attributes like `<Hello name="mech" />`. Try to use `props` as the source of truth where possible.
* States - Can change. Mutable. You should design your component to not use state as much as possible. Try to keep as many of your components as possible stateless. Use state when you need to respond to user input, a server request or the passage of time. State should contain data that a component's event handlers may change to trigger a UI update (such as JSON request). Think of the UI as a state machine. By thinking of a UI as being in various states and rendering those states, it's easy to keep your UI consistent.

Props and states collectively represent the Model.

The final rendered DOM can have events. And once the events are triggered, the state can change which trigger another render.

If a component need to change and the cause of the change is the component's parent, then the parent can simply change the child's props and re-render.

If a component need to change due to some other component, then it need to use state.

Avoid states as much as possible. Instead push the event handling and state management up toward the top of your component hierarchy.

Note: Spread operator `{...}` deprecate `this.transferPropsTo`
	
* [JSX Spread Attributes](https://gist.github.com/sebmarkbage/07bbe37bc42b6d4aef81)

> A common pattern is to create several stateless components that just render data, and have a stateful component above them in the hierarchy that passes its state to its children via props. The stateful component encapsulates all of the interaction logic, while the stateless components take care of rendering data in a declarative way.

## Refs

* [How should refs work?](https://github.com/facebook/react/issues/3234)

```
handleClick: function() {
  // Wanting to focus is a very example of when to use refs
  // Unique only in this component the refs `nameInput`
  this.refs.nameInput.getDOMNode().focus();},

render: function() {
  return(
    <div>
      <input type="text" ref="nameInput" />
      <button onClick={this.handleClick}>Focus</button>
    </div>
  );}
```

Before using `ref`, exhaust your options of using the reactive data flow approach. `ref` is a way to talk to the "backing instance" of the real DOM element.

Refs are a great way to send a message to a particular child instance in a way that would be inconvenient to do via streaming Reactive `props` and `state`. They should, however, not be your go-to abstraction for flowing data through your application. By default, use the Reactive data flow and save `refs` for use cases that are inherently non-reactive.

Refs are automatically destroyed for you. No worrying about memory leaking unless you do something crazy to retain a reference.

Take a moment and think more critically about where `state` should be owned in the component hierarchy.

## Composition (Composable)

Combine *simple* functions to build more *complicated* ones. One way to manage complexity.

Just build simple interfaces. Makes it easier to predict what will happen.

How React enable nested component? By having a clear Input (properties) and Output (render() callback function), nested components is a very common outcome.

## Idempotence

Certain operations that can be applied multiple times without changing the result beyond the initial application.

Easy to predict output for a given input. Immutability gets you idempotence for free.

## Virtual DOM

You would use `requestIdleCallback` to make DOM changes on document fragment, but you would *apply* the DOM patches in the next `requestAnimationFrame` callback, not the idle callback.

Dirty-checking model can be slow. Virtual DOM is using tree, as we all know, tree can be fast.

DOM operation is very expensive! Because modifying the DOM will also apply and calculate CSS styles, layouts, etc.

* [React-less Virtual DOM with Snabbdom](https://medium.com/@yelouafi/react-less-virtual-dom-with-snabbdom-functions-everywhere-53b672cb2fe3#.q046lbm2b)
* [Snabbdom](https://github.com/paldepind/snabbdom)
* [virtual-dom](https://github.com/Matt-Esch/virtual-dom)
* [Virtual DOM Benchmark](http://vdom-benchmark.github.io/vdom-benchmark/)
* [A Virtual DOM and diffing algorithm](https://github.com/Matt-Esch/virtual-dom)
* [Issues/3](https://github.com/Matt-Esch/virtual-dom/issues/3)
* [Virtual DOM and diffing algorithm](https://gist.github.com/Raynos/8414846)
* [Getting started with Virtual DOM](https://www.youtube.com/watch?v=lXJGTtHlf9U)

## Re-render

Re-render the entire application on every change.

* No observers
* No magical data binding
* No model dirty checking
* No `$apply()` or `$digest()`

BUT: You can't just throw out the DOM and rebuild on every update? Lose form state, lost scroll position?

## Director

* [Router for React](https://github.com/flatiron/director)
* [Example of router](https://github.com/andreypopp/react-router-component)

## Mithril

* [Mithril - with Virtual DOM diff](http://lhorie.github.io/mithril/)

## Mixins

* [react-mixin](https://github.com/brigand/react-mixin)
* [Mixins are dead. Long live composition](https://medium.com/@dan_abramov/mixins-are-dead-long-live-higher-order-components-94a0d2f9e750)

Cross-cutting concern like Logger, Subscribing? Just mix in methods.

## Examples

* [react-flux-puzzle](https://github.com/weslleyaraujo/react-flux-puzzle)
* [**Mattermost**](https://github.com/mattermost/platform/tree/release-1.1.0/web/react/components)
* [Ryan Florence HYPE](https://github.com/ryanflorence/reactconf-2015-HYPE)
* [React tutorial](https://github.com/phaedryx/react-tutorial)
* [5 practical examples for learning React](http://tutorialzine.com/2014/07/5-practical-examples-for-learning-facebooks-react-framework/)
* [Firebase Vulcan - A chrome extension tool](https://github.com/firebase/vulcan)
* [Using TDD with React](https://reactjsnews.com/using-tdd-with-reactjs/)
* [Hacker News App](https://github.com/reapp/hacker-news-app)
* [React Magician](https://github.com/SanderSpies/react-magician)
* [Great.dj](https://github.com/ruiramos/greatdj)
* [Building a multi-step registration form](http://viget.com/extend/building-a-multi-step-registration-form-with-react)
* [AirBnb](https://github.com/airbnb/airpal)
* [Cosmos](https://github.com/skidding/cosmos)
* [Pivotal CF](http://styleguide.cfapps.io/react_beta.html)
* [**pivotal-ui-react**](https://github.com/pivotal-cf/pivotal-ui-react/tree/master/src/media)
* [react-calendar](https://github.com/erikthedeveloper/react-calendar)
* [react-tween-state](https://github.com/chenglou/react-tween-state)
* [Creating Chrome extensions with React](http://brandontilley.com/2014/02/24/creating-chrome-extensions-with-react.html)
* [Trying out React.js with the Marvel API](http://ryanlanciaux.github.io/blog/2014/05/26/trying-out-reactjs-with-the-marvel-api/)
* [Implementing the board game Go](http://cjlarose.com/2014/01/09/react-board-game-tutorial.html)
* [react-phonecat](http://jgebhardt.github.io/blog/react-phonecat/)
* [React and Adobe Brackets](http://www.kevindangoor.com/2014/05/simplifying-code-with-react/)
* [Building a board game with React.js](http://jjt.io/2014/07/30/building-a-board-game-with-react-js/)
* [Some example working with jQuery dialog](http://sterling.ghost.io/working-with-jqueryui-and-reactjs-components/)
* [Integrate with jQuery](http://winterbe.com/posts/2015/08/24/integrate-reactjs-into-jquery-webapps/)

## GitHub Issues

* [Optimizing Compiler: Reuse Constant Value Types like ReactElement](https://github.com/facebook/react/issues/3226)
* [JSX optimization in babel.js](https://twitter.com/sebmck/status/582191152356458497)
* [Implement Sideways Data Loading](https://github.com/facebook/react/issues/3398)
* [React/Flow/Type optimizations](https://github.com/babel/babel/issues/653)

## Companies using React

* [Real life at Codecademy](http://www.infoq.com/articles/reactjs-codecademy)
* [Netflix likes React](http://techblog.netflix.com/2015/01/netflix-likes-react.html)
* [Atlassian - Rebuild HipChat with React](https://developer.atlassian.com/blog/2015/02/rebuilding-hipchat-with-react/)

## TDD

* [Jest preprocessor](https://github.com/RisingStack/react-way-getting-started/blob/master/tools/preprocessor.js)

## Books

* [React books](http://survivejs.com/blog/react-books/)

## Blog to follow

* [Sift Science](http://blog.siftscience.com/)
* [Simple Studios](http://simblestudios.com/blog)
* [Futurice](http://futurice.com/blog/)
* [Little Blimp Dev Blog](http://blog.littleblimp.com/)
* [James K Nelson](http://jamesknelson.com/)

## Videos

* [Pete Hunt - React vs The World](https://www.youtube.com/watch?v=MC376f3QWYw)
* [Pete Hunt - Rethinking Best Practices](https://www.youtube.com/watch?v=x7cQ3mrcKaY)
* [Pete Hunt - Rethinking Best Practices (updated) 2013](https://www.youtube.com/watch?v=DgVS-zXgMTk)
* [Functional Web Development](https://www.youtube.com/watch?v=Elr_RNt2R5Q)
* [Secret of the Virtual DOM](https://www.youtube.com/watch?v=1h2G20A-AvY)
* [Alt.Net Jan 2015](http://youtu.be/kNVatRjnU7U)
* [Thinking in Components: Building Powerful UIs in React.js](https://www.youtube.com/watch?v=xSGuffp0o6E)
* [Learn React, Flux, and Flow - Seattle.js](https://www.youtube.com/watch?v=Pd6Ub7Ju2RM)
* [London React meetup - ES6 Modules and React with SystemJS](https://www.youtube.com/watch?t=20&v=NpMnRifyGyw)
* [E4E Developer Conf 2014 - Reactive, Component-based UIs with React](https://www.youtube.com/watch?v=uwnjDXtJufs)
* [All you need to know to get started with React](https://www.youtube.com/watch?v=gzl80JozIZE)
* [Learn React, Flux, and Flow](https://www.youtube.com/watch?v=Pd6Ub7Ju2RM)
* [**Netflix JavaScript Talks**](https://www.youtube.com/watch?feature=youtu.be&list=PLfXiENmg6yyU5kEHyo1kYkq7HEzBOoiTT&v=FAZJsxcykPs&app=desktop)

## Twitter

* [@jingc](https://twitter.com/jingc)
* [@Vjeux](https://twitter.com/Vjeux)
* [@sebmarkbage](https://twitter.com/sebmarkbage)
* [@jordwalke](https://twitter.com/jordwalke)
* [@ryanflorence](https://twitter.com/ryanflorence)
* [@browserify](https://twitter.com/browserify)
* [@geteslint](https://twitter.com/geteslint)