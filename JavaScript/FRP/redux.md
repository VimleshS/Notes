# Redux

Short overview of Redux:

1. You spend time to write your reducers to do the work of converting state to new state. You can have multiple reducers that ultimately will need to be -->
2. `combineReducers`
3. At your new main new page component (it can be your route component), you need to setup the store: `const store = createStore(reducer)`
4. If something happen, you just `store.dispatch(ACTION)` away.
5. Rest assure all your 'connected' or subscribed React components will `store.getState()` and re-render.

---

* [**State of React - How Redux came to be**](http://jamesknelson.com/state-react-2-inception-redux/)
* [**Good video series**](http://remzolotykh.net/category/react-and-redux)
* [**Learning Redux with Reducks**](http://www.aaron-powell.com/posts/2016-06-06-learning-redux-with-reducks-intro.html)
* [3 simple steps to improve your React Redux code](https://www.ckl.io/blog/3-simple-steps-to-improve-react-redux-code/)
* [**Why does the Elm Architecture matter to Redux developers?**](http://salsita.github.io/redux-elm/)
* [Getting Started with React, Redux and Immutable: a Test-Driven Tutorial](http://www.theodo.fr/blog/2016/03/getting-started-with-react-redux-and-immutable-a-test-driven-tutorial-part-1/)
* [**The Anatomy Of A React Redux App**](https://medium.com/@rajaraodv/the-anatomy-of-a-react-redux-app-759282368c5a#.gptl457nd)
* [Has Redux lost it the API design?](https://youtu.be/lk4M6FoRNgI)
* [**React without undue complications**](https://medium.com/@davidvlsea/react-without-undue-complications-f3490403fdc0#.f8z1106i1)
* [Step by step guide to building Redux apps](https://medium.com/@rajaraodv/step-by-step-guide-to-building-react-redux-apps-using-mocks-48ca0f47f9a#.6nk2flafc)
* [**Middlewares and Redux Lifecycle**](https://medium.com/@rajaraodv/using-middlewares-in-react-redux-apps-f7c9652610c6#.u1xzqeqm3)
* [React Redux Best Practices](http://nalwaya.com/javascript/2016/05/02/react-js-best-practices.html)

> React is not reactive because it does not observe the data

If you don't have synchronization problem and don't really need single source of truth, you don't need Redux. Local component is perfectly fine for other cases.

Redux is where interaction happens like `onClick`, `onMouseOver`, etc.

To give a bit of perspective on complex front-end application, let's consider Google Docs. Every time a user presses a key, a number of things need to happen (doing them all before returning to the event queue would be a recipe for an unresponsive app):

* the new character has to be displayed on the screen
* the caret has to be moved
* the action has to be pushed to the local undo history
* spell-check may have to run
* word count and page count may need to be updated

We want to use **distributed events**, where a single incident can trigger reactions throughout our application. Event emitter is how you can distribute events.

> Data dominates. Data Structures, not algorithms, are central to programming - Rob Pike

Flux == Unidirectional data flow with changes described as plain objects.

Just like Docker, but for React data. Immutable snapshot of state.

Falcor as solving data fetching problem and Redux as predictable state management library.

```js
(state, action) => state

// Some usage example:

const store = createStore(counter);

<Counter
  value={store.getState()}
  onIncrement={() => store.dispatch({ type: 'INC' })}
  onDecrement={() => store.dispatch({ type: 'DEC' })} />
```

Data lives outside of React view hierarchy. I can easily reason about my view layer. How I want to also easily reason about my data. And that is where Redux with single state tree comes in.

* [redux-auth](https://github.com/lynndylanhurley/redux-auth)
* [The difference between Redux and Rx](http://qiita.com/kimagure/items/a534d149cd9176d34cc1)
* [Levelling up with React: Redux](https://css-tricks.com/learning-react-redux/)
* [Server-side rendering with Redux and React-Router](https://www.codementor.io/reactjs/tutorial/redux-server-rendering-react-router-universal-web-app)
* [Step by step guide to building React Redux apps](https://medium.com/@rajaraodv/step-by-step-guide-to-building-react-redux-apps-using-mocks-48ca0f47f9a#.1mzij69r2)
* [fully-reactive-react-example](https://github.com/belfz/fully-reactive-react-example)
* [**React has no networking/Ajax features**](http://andrewhfarmer.com/react-ajax-best-practices/)
* [Why I'm tired of using and teaching flux](https://gist.github.com/justinwoo/08f9f8fcdcf865025f18)
* [A simple way to route with Redux](http://jlongster.com/A-Simple-Way-to-Route-with-Redux)
* [**Nothing new in React and Flux**](http://staltz.com/nothing-new-in-react-and-flux-except-one-thing.html)
* [**Why React/Redux is an inferior paradigm**](http://staltz.com/why-react-redux-is-an-inferior-paradigm.html)
* [**Why we use Om, and why we're excited for Om Next**](http://blog.circleci.com/why-we-use-om-and-why-were-excited-for-om-next/)
* [**Awesome Redux Course Note**](https://github.com/tayiorbeii/egghead.io_redux_course_notes)
* [**Flux vs Single State Tree**](http://www.christianalfoni.com/articles/2015_11_16_Flux-vs-Single-State-Tree)
* [Interview with Dan Abramov](http://softwareengineeringdaily.com/2015/09/18/flux-redux-and-react-hot-loader-with-dan-abramov/)
* [**Full-stack Redux tutorial**](http://teropa.info/blog/2015/09/10/full-stack-redux-tutorial.html)
* [**A cartoon guide to Redux**](https://code-cartoons.com/a-cartoon-intro-to-redux-3afb775501a6#.isxvwd9em)
* [**Understanding Redux (how I fell in love with a state container)**](http://www.youhavetolearncomputers.com/blog/2015/9/15/a-conceptual-overview-of-redux-or-how-i-fell-in-love-with-a-javascript-state-container)
* [**James Long's Redux Blog**](http://jlongster.com/The-Seasonal-Blog-Redux)
* [awesome-redux](https://github.com/xgrommx/awesome-redux)
* [Redux isomorphic example](https://github.com/coodoo/react-redux-isomorphic-example)
* [Simplest redux + react example](https://github.com/jackielii/simplest-redux-example)
* [Issue#20](https://github.com/gaearon/react-redux/issues/20#issuecomment-127168519)
* [Universal infinite scrolling stars Redux](http://react.rocks/blog/post/roundup-2015-Aug-09/)
* [What the Flux?! Let's Redux](https://blog.andyet.com/2015/08/06/what-the-flux-lets-redux)
* [Handcrafting an isomorphic Redux application](https://medium.com/@bananaoomarang/handcrafting-an-isomorphic-redux-application-with-love-40ada4468af4)
* [redux-devtools](https://github.com/gaearon/redux-devtools)
* [react-redux-starter-kit](https://github.com/davezuko/react-redux-starter-kit)
* [redux-requests - Manages in-flight requests](https://github.com/idolize/redux-requests)
* [**redux-blog-example**](https://github.com/GetExpert/redux-blog-example)
* [react-reversi](https://github.com/jhewlett/react-reversi)
* [**State Management with Redux**](http://konkle.us/state-management-with-redux/)
* [redux-store-visualizer](https://github.com/romseguy/redux-store-visualizer)
* [redux-undo](https://github.com/omnidan/redux-undo)
* [Redux interview by Survive.js](http://survivejs.com/blog/redux-interview/)
* [redux-tutorial](https://github.com/happypoulp/redux-tutorial)
* [Redux best practices](https://medium.com/lexical-labs-engineering/redux-best-practices-64d59775802e#.g7ayoa8i6)
* [redux-thunk - Middleware](https://github.com/gaearon/redux-thunk)
* [Is Redux too much?](https://medium.com/@davidvlsea/react-without-undue-complications-f3490403fdc0#.qncruotht)
* [Tracker 2.0: The evolution of Tracker and solutions to its core problem](https://medium.com/@faceyspacey/the-evolution-of-tracker-solutions-to-its-core-problems-4b9cb90d479a#.x3o7lt78t)
* [Issue#155 - Redux's relation to cursors](https://github.com/rackt/redux/issues/155)

**Starter Kits**

* [**react-pure-component-starter**](https://github.com/ericelliott/react-pure-component-starter)
* [MERN](http://mern.io/)
* [**react-ultimate**](https://github.com/Paqmind/react-ultimate)
* [**thisless-react**](https://github.com/jas-chen/thisless-react)
* [**Shasta - Simple opinionated toolkit for building applications on top of React, Redux, and immutable.js**](https://github.com/shastajs/shasta)
* [react-slingshot](https://github.com/coryhouse/react-slingshot)
* [react-starter-kit](https://github.com/kriasoft/react-starter-kit)
* [react-router-redux](https://github.com/rackt/react-router-redux)
* [redux-easy-boilerplate](https://github.com/anorudes/redux-easy-boilerplate)
* [react-redux-starter-kit](https://github.com/davezuko/react-redux-starter-kit)
* [react-redux-universal-hot-example](https://github.com/erikras/react-redux-universal-hot-example)

## Architectural Discussion

* [Reuse complex components implemented in React + Redux](https://github.com/reactjs/react-redux/issues/278)
* [DDD in Redux?](https://github.com/reactjs/redux/issues/1315#issuecomment-179164091)
* [`connect` could be used with a custom `store.subscribe()`](https://github.com/reactjs/react-redux/issues/269)
* [Performance issues with a tree structure and shouldComponentUpdate in React / Redux](http://stackoverflow.com/questions/34981924/performance-issues-with-a-tree-structure-and-shouldcomponentupdate-in-react-re)
* [Top-down vs bottom-up](https://github.com/cyclejs/core/issues/191#issuecomment-162320830)
* [redux-react-local](https://github.com/threepointone/redux-react-local)
* [redux-architecture](https://github.com/jarvisaoieong/redux-architecture)

`connect()` does a ton of trickery to be very optimized. Always re-rendering from the top means you're doing a bunch of unnecessary reconciliation.

> A widget is an autonomous component that has its own reducer, use something like "connect" to get the state of that reducer. The widget only re-renders when its state changes. I try to make the widget only receive its own state, to make it really independent but it is really a mater of taste and many don't adopt a similar approach and assume the widget should have a global knowledge of the global appstate to select the state it needs to use.

## Libraries

* [react-router-redux](https://github.com/rackt/react-router-redux)
* [normalizr](https://github.com/gaearon/normalizr)

## Do you need Redux in the first place

* [How to choose between Redux's store and React's state?](https://github.com/reactjs/redux/issues/1287)

If the state of a component doesn't matter to anyone else, just keep that state internal to the component itself.

Redux is primarily intended for "application state".

* UI state - React local state
* Controlled inputs - React local state as it need fast update time
* Application state - Redux single state tree

> The way I think about it, if you create an app with Redux, embrace the single state tree. Put UI state there as well. However if it gets tedious and frustrating don’t be afraid to put state into the components. My point is that use single state tree unless it is awkward, and only do this when it simplifies things for you rather than complicates them. That’s the only guideline.

Flux is about application states, using Flux for component states is an anti-pattern!

> One problem we suffered from when we first started using Redux was an over-eagerness to extract state into our Redux store. In some cases, this led to using Redux in places where component state was a better fit.
>
> Problems can arise when a component unmounts but its "state" is left over inside the store, or when two different components are attempting to read and modify the same slice of state. It also involves splitting logic over multiple files. By contrast, component state has the enormous benefit of being confined to a single component. Redux works best for concerns that are more global — or app level — in nature.
> 
> Once we realized our error, we found it was harder to refactor Redux reducers back to normal component state than it would have been to refactor component state into a Redux reducer.
> Now, our approach is to implement features using component state first, and only move things into Redux once it becomes necessary.

## Redux and Forms

* [Using debounce to save state upstream?](https://gist.github.com/markerikson/554cab15d83fd994dfab)
* [redux-form](https://github.com/erikras/redux-form)

## Single Store Tree (Root Store?) - Single Source of Truth - Single State Atom

That’s what your Store really is: a function telling the initial state and how the subsequent actions transform it. There is no reason for the Store to actually own that state. It might be held in a single big tree, for example, but it would be an implementation detail of the dispatcher. You don’t have to use the cursors. You can keep the “stores” and “subscriptions” mentality if that’s what you like, because it is easy to understand and feels natural to use. - [First article on Redux](https://medium.com/@dan_abramov/the-evolution-of-flux-frameworks-6c16ad26bb31#.8du8rosdi)

> We don't intend Redux to be used for all state. Just whatever seems significant to the app. I would argue inputs and animation state should be handled by React (or another ephemeral state abstraction). Redux works better for things like fetched data and locally modified models.

---

> You should do your best to keep the state serializable. Don't put anything inside it that you can't easily turn into JSON.

* [CircleCI - Local State, Global Concerns](https://circleci.com/blog/local-state-global-concerns/)
* [Issue#140 - Rename store to reducer](https://github.com/rackt/redux/pull/140)
* [Issue#1385 - What are the disadvantages of storing all your state in a single immutable atom?](https://github.com/reactjs/redux/issues/1385)
* [**Umbrella: Externalize the State Tree (or alternatives)**](https://github.com/facebook/react/issues/4595)

> Om Now was one of the early influencers for the single atom app state idea. The only difference is that, instead of using cursors, Redux uses Flux-style actions for mutations.

You App need to hold states. Where should you "store" it? Redux and Flux both has the "Store" concept where states are resided.

> Redux is basically event-sourcing where there is a single projection to consume.
	
Redux has single state tree.

State === Model


See Om Next approach on changing a state tree to a graph one, sort of like GraphQL and Falcor.

> The tree is really a graph

A single state tree (i.e. Baobab) can be easily navigated by a cursor. However, visited different branch of a tree prove tedious.

With graph, you can sort of visit anywhere you like! Query let you navigate the graph of your data in all sorts of directions.

Your data is a graph, but what your UI sees is a tree.

### Shape of your application state (State Shape)

It's a good idea to think of its shape of your data. Typically we need to store data as well as UI state.

## Actions

* [FSA - Flux Standard Action](https://github.com/acdlite/flux-standard-action)

Actions mutate states.

Action is just plain JS object:

```js
{ type: 'TAKE_LEAVES', leaves: [{}, {}] }
```

Actions are like newspaper, reporting on something has happened in the world.

The component itself do not know how to deal with the action. For example, the component event handler do not ever take upon itself to process business or application logic. For example, a very simple act of paging through a list can be described by this action:

```js
{ type: 'SET_PAGE_NUMBER', page_number: 12}
```

So `page_number` here is a state, and the only way to change this read-only state is to dispatch an action.

Actions are the change in your app. Actions represent mutations of your app state. Explicit, easy to find the places that could trigger a particular action, I can search for it.

In Cycle, it is `intent()` which interpret DOM events as user's intended actions:

```js
// intent() is Cycle.js's way of Action
// It's input is the DOM source where the UI world is at
// It has 2 observables here that interpret 2 DOM events
function intent(DOM) {
  return {
    changeWeight$: DOM.select('#weight').events('input').map(ev => ev.target.value),
    changeHeight$: DOM.select('#height').events('input').map(ev => ev.target.value)
  };
}
```

Action don't do anything. It don't mutate states. It only describe something has happen and ask Reducer to go deal with it.

### Action Creators (Where async can happen)

Action creators are just function that create action.

```js
// This is a simple synchronous dispatch. The UI will render immediately!!
store.dispatch({
  type: ADD_ITEM,
  status: 'start',
  name: 'James'
})

// This is a asynchronous dispatch.
function addItem(name) {
  return dispatch => {
    dispatch({
      type: ADD_ITEM,
      status: 'start',
      name: name
    });

    setTimeout(() => { // Just a fake XHR request
      dispatch({
        type: ADD_ITEM,
        status: 'finish',
        name: name
      });
    }, 100);
  }
}

// Or using some other promise middleware
const { PROMISE } = require('<promise-middleware>');

function addItem(name) {
  return {
    type: ADD_ITEM,
    name: name,
    [PROMISE]: api.addItem(name)
  }
}
```

**More examples of Action Creators**

```js
function addTodo(text) {
  const trimmedText = text.trim();
  return {
    type: 'ADD_TODO',
    text: trimmedText
  };
}

<button onClick={ dispatch(addTodo('Call Mom')) }>Add Todo</button>

// Or directly use XHR
export function addTodo(todo) {
  return (dispatch) => {
    dispatch({type: 'SAVING_TODO'}); // spinner?
    
    ajax.post('/todos', todo)
      .then(() => {
        dispatch({type: 'SAVED_TODO'}); // stop spinner?
        dispatch({
          type: 'ADD_TODO',
          todo: todo
        });
      });
  };
};
```

```js
export function login(email, password) {
  return ({fetch}) => ({
    types: [LOGIN, LOGIN_SUCCESS, LOGIN_ERROR],
    payload: {
      promise: fetch('auth/login', {
        body: JSON.stringify({email, password})
      })
    }
  })
};
```

## Reducer

Do the grunt work of your data flow. Taking information from action and produce a brand new state.

```js
// A mutable noop reducer
const reducer = (state, action) => state;

// A immutable noop reducer
const reducer = (state, action) => {...state};
const reducer = (state, action) => Object.assign({}, state, {});
```

> Reducers return Objects. Combine reducers adds up these Objects. Provider gives this Combined Object to all Components.

---

> Normally we suggest you to only run a single reducer on any state slice.
>
> In general multiple branches with the same state shape but managed by different reducers is an anti-pattern.

```
   Source ------> Handler ------> Sink
(don't care)                  (don't care)
```

Reducers are synchronous! Data logic is 100% separated from view logic.

Redux manages state by separating it into different reducers. Each reducer managing a little piece of a different branch of the global state tree.

* [Issue#328 - Cost of immutability](https://github.com/rackt/redux/issues/328)
* [Issue#758 - Why can't state be mutated?](https://github.com/rackt/redux/issues/758)

Where the action happen. Where the mutation occurs. In Flux, it is called the STORE. In Redux, it is just a pure function called REDUCER.

Redux assumes you never mutate your data. Since it is JavaScript, it can only assume. With Elm, it is enforced!

> Finally, nothing per se prevents you from mutating your Redux state tree. It is actively discouraged, and you will lose a lot of debugging benefits if you mutate your data, but for performance critical pieces you can write impure reducers that mutate the state in place. (Only do that if you're sure that's where the lag comes from—not likely to be an issue in real apps.)

Each reducer computes a separate piece of state, which is then all composed together to form the whole application.

**Things not to do in reducer:**

* Don't perform side effects like API calls and routing transitions. These should happen before an action is dispatched. (middleware??)
* Calling non-pure functions like `Date.now()` or `Math.random()`
* No surprises. No side effects. No API calls. No mutations. Just calculation.

**Reducer Composition to split your logics**

Depending on your state tree shape, you can have different reducer working on one part of the state for example.

```js
// This is your single state tree
{
  todos: [],
  visibilityFilter: 'SHOW_ALL'
}

// You can have 2 reducers, one for todos management and the
// other to take care of visibility filter logic

const todoApp = (state = {}, action) => {  
  return {
    todos: todos(state.todos, action),
    visibilityFilter: visibilityFilter(state.visibilityFilter, action)
  }
}

// Or use combineReducers
const todoApp = combineReducers({ todos, visibilityFilter })

const todos = (state = [], action) => {
  // This is a one part of the reducer that take care of the todos management.
  // Notice that it's state is an array
}

const visibilityFilter = (state = 'SHOW_ALL', action) => {
  // This is another part of the reducer that deal with filtering.
  // Notice that its default state is a string
}
```

**More examples**

We always get ready a brand `newState`. We also want to retain the old `state` by putting it through the `Object.assign` with any new state.

```js
const reducer = (state, action) => {
  switch (action.type) {
    case SET_SEARCH_TERM:
      const newState = {}
      Object.assign(newState, state, { searchTerm: action.value })
      return newState
    default:
      return state
  }
}
```

## Reducer Enhancer

* [multireducer](https://github.com/erikras/multireducer)
* [redux-delegator](https://github.com/lapanoid/redux-delegator)
* [redux-multiplex](https://github.com/reducks/redux-multiplex)
* [redux-batched-subscribe???](https://github.com/tappleby/redux-batched-subscribe)
* [redux-ignore](https://github.com/omnidan/redux-ignore)

## Transducer

* [Transducer Protocol](https://github.com/cognitect-labs/transducers-js)
* [Issue#176 - Transducers in Redux](https://github.com/rackt/redux/issues/176)
* [Issue#569 - Proposal: API for explicit side effects](https://github.com/rackt/redux/pull/569)

## Middleware

* [Understanding Redux middleware](https://medium.com/@meagle/understanding-87566abcfb7a#.pv692to4s)

Intercept action. Middleware transforms async actions before they reach the reducer. This is so that reducer will not have to deal with non-pure functional operations.

## Selector and Memoization

* [A brief history of Reselect](http://blog.startifact.com/posts/a-brief-history-of-reselect.html)
* [Issue#47 - Handling derived data](https://github.com/rackt/redux/issues/47)

## I/O, Effects, Async

* [**Redux-Elm: The problem with Redux and how to fix it**](http://blog.javascripting.com/2016/05/21/the-problem-with-redux-and-how-to-fix-it/)
* [Issue 1528 - Reducer Composition with Effects in JavaScript](https://github.com/reactjs/redux/issues/1528#issuecomment-198352851)
* [redux-saga, redux-effects, redux-side-effects, redux-loop](https://twitter.com/dan_abramov/status/689639582120415232)
* [Why do we need middleware for async flow in Redux?](http://stackoverflow.com/questions/34570758/why-do-we-need-middleware-for-async-flow-in-redux/34623840#34623840)
* [Reducer Composition with Effects in JavaScript???](https://github.com/reactjs/redux/issues/1528)

Async action creators are suboptimal.

Sync state transition??

## Sagas

* [**Confusion about Saga pattern**](https://medium.com/@roman01la/confusion-about-saga-pattern-bbaac56e622#.biu0lp9iy)
* [Handling async in Redux with Sagas](http://wecodetheweb.com/2016/01/23/handling-async-in-redux-with-sagas/)
* [Master complex Redux Workflows with Sagas](http://konkle.us/master-complex-redux-workflows-with-sagas/)
* [From actions creators to sagas](http://riadbenguella.com/from-actions-creators-to-sagas-redux-upgraded/)
* [Issue#1139 - An alternative side effect model based on Generators and Sagas](https://github.com/rackt/redux/issues/1139)
* [Alternatives Async/side effect models](https://github.com/paldepind/functional-frontend-architecture/issues/20)


## Thunk

* [Callback + Continuable](https://gist.github.com/creationix/b9557dd1dceba7aa90b5)
* [Thoughts on Thunks](http://blog.getify.com/thoughts-on-thunks)
* [How to dispatch a Redux action with a timeout?](http://stackoverflow.com/questions/35411423/how-to-dispatch-a-redux-action-with-a-timeout/35415559#35415559)

## Router

* [Redial - Route lifecycle management??](https://github.com/markdalgleish/redial)
* [#637 - Usage with React Router](https://github.com/rackt/redux/issues/637)
* [Issue#1362 - RFC: syncHistoryWithStore()](https://github.com/rackt/redux/pull/1362)

Angular 2 Router exposes route change as an Observable which you can leverage to keep route state synchronized with your Redux Store.

> Dispatching an action instead of using directly `history.pushState()` is really important. The action will go through the chain of middlewares, meaning (for example) automatic analytics, etc.
> 
> About `browserHistory` singleton, singletons and server side = bad idea. Actions and middleware are giving me an easy way to use history without propagating it through context/props on client side.

```js
// You listen for browser change event and dispatch an action to handle it
// browserHistory is a singleton??
import { browserHistory } from 'react-router';
browserHistory.subscribe(location => store.dispatch({ type: 'NAVIGATE', location }));
```

Provide ability to change URL location within an action creator. This is very useful because it's not uncommon to have a workflow in an action creator that is something like "authenticate user -> if successful, redirect to /admin".

## React Component Integration

After the action, the reducer will give you a new state. You can get back the new state using `store.getState()`. You use this new state to re-render your component using `component.setState(newState)`.

Only top-level components of your app (such as route handler) are aware of Redux. The rest are Presentational Components and receive all data via props.

Presentational components don't know WHERE the data comes from, or HOW to change it. They only render what's given to them.

### Context and Provider

* [**React, Automatic Redux Providers, and Replicators**](https://medium.com/@timbur/react-automatic-redux-providers-and-replicators-c4e35a39f1#.4au3tepxt)
* [react-redux-provide](https://github.com/loggur/react-redux-provide)

> Learning all this React environment and Redux is dragging me down. The connects and mapState make no sense to me and you have to do it for every container?

Convention over configuration is lost JavaScript's obsession with composability.

```js
import { createStore } from 'redux';
import { Provider } from 'react-redux';
import todoApp from './reducers';

let store = createStore(todoApp);

ReactDOM.render(
  <Provider store={store}>
    <App />
  </Provider>,
  document.getElementById('#app')
);


// App.jsx
import { connect } from 'react-redux';

const App = ({dispatch, state}) => {
  return (
    <button onClick={ dispatch(addTodo('Buy Milk')) }>Add Todo</button>
  );
};

export default connect(App);
```

### Connect

* [Implementation - connect.js](https://github.com/reactjs/react-redux/blob/master/src/components/connect.js)

Sort of like subscription. You wrap the component. When you do the wrapping, you need to "connect" the single state tree to props for your component to consume, thus `connect(stateToProps)`.

Or just do your own `store.subscribe()`.

* [redux-connected-proptypes](https://github.com/conorhastings/redux-connected-proptypes)

`connect()` from Redux React does a ton of trickery to be very optimized. It tries hard to be fast whereas functional components don't try at all.

When you always render from the top you are coupling parent components too hard to what child components need to render. You're essentially passing many props that are only required by children, and changing them can involve painful refactoring.

Instead as soon as you see that component passes props down without using it, we suggest generating a "container" component using `connect()`.

The benefit of using `connect(state, dispatch)` is that it takes care of subscribe (responding to state changes) and dispatch for you without having to hook into the React component lifecycle yourself.

```js
// connect() API?
export default PropTypes.shape({
  subscribe: PropTypes.func.isRequired,
  dispatch: PropTypes.func.isRequired,
  getState: PropTypes.func.isRequired
})
```

## `mapStateToProps`

* [Issue#291 - Should mapStateToProps be called every time an action is dispatched?](https://github.com/reactjs/react-redux/issues/291)

## Relay Style?

> That's what I’d do. (But I'm pretty sure one can take Redux + Normalizr and build something more Relay-like around it.)

## Redux and RxJS

* [redux-rx](https://github.com/acdlite/redux-rx)

## Videos

* [Redux, a journey from OOP to functional](https://www.youtube.com/watch?v=IdcIbDKar2U)