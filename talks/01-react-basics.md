title: JavaScript Introduction

--

<center>
  <h1>React Basics</h1>
  <br />
  <small>
    <i>In react we trust</i>
  </small>
  <br />
  <br />
  <small>
    by [Vladimir Starkov](https://iamstarkov.com)
    <br>
    frontend engineer at [Nordnet Bank AB](https://www.nordnet.se/)
  </small>
</center>


---

### History

* html
* html + css
* DHTML / XMLHttpRequest
* Java / Flash
* JQuery
* Backbone/Ember/Angular/etc
* React


---

### React

* A JavaScript library for building user interfaces
* predictable user interfaces
* Declarative
* Component-Based
* Learn Once, Write Anywhere

---

### JQuery era

* write a form
* add event handlers
* write another form
* add more event handlers
* modify DOM manually all along
* end up in combinatoric explosion of your states and event handlers
* also not testable

---

### Backbone/Ember/Angular/etc aka JS frameworks era

* learn extensive API surface
* pick new framework
* learn extensive API surface again
* barely can use one with another
* learn ad-hoc DSL for HTML DSL
* yet to end up in combinatoric explosion of your states and event handlers
* but in more complex apps
* testable, but ohmy

---

### React era

* learn ~~extensive~~ small API surface
* learn concept once, write everywhere
* use with frameworks as you wish
* ~~learn ad-hoc DSL~~ just learn JS
* care about components—not DOM
* simple and predictable
* ~~yet to be~~ testable, as any other JS parts
* paradigm shift, 'cause you model your your UI around its state.

---

### JSX

```js
const element = <h1>Hello, world!</h1>;
```

* neither string nor HTML.
* not yet another Ad Hoc DSL
* isnt required
* doesnt violate ["Separation of concerns"](https://en.wikipedia.org/wiki/Separation_of_concerns)
* allows to build units of UI—react components

---

### interpolation in JSX

```js
const trainName = 'Trainy McTrainface';

const element = <h1>Train name is {trainName}!</h1>;
```

---

### React Component

* Either function or class or stateless and stateful, respectively
* Takes in `props`
* functional components can only rely on `props`
* class-based components can have its own state
* class-based components can have life-cycle methods
* special `children` props to nest components
* returns stuff to render

---

### Pure Function

## 𝑦﹦𝑓(𝑥)

> A pure function is a function that, given the same input, will always return the same output and does not have any observable side effect.  
> — ["Mostly adequate guide to FP"](https://drboolean.gitbooks.io/mostly-adequate-guide/content/ch3.html#oh-to-be-pure-again)

*same input = same output, in short.*  
<small>*also, no side effects please*</small>

---

### functional or stateless

```js
const Button = props => (
  const children = props.children;
  const onClick = props.onClick;
  return (
    <button onClick={onClick}>
      { children }
    </button>
  )
)
```

---

### functional or stateless v2

```js
const Button = ({ children, onClick }) => (
  <button onClick={onClick}>
    { children }
  </button>
)
```

---

### class-based or stateful

```js
class ClickCount extends React.Component {

  constructor(props) {
    super(props);

    this.state = { counter: 0 }

    this.incCounter = () => {
      this.setState({ counter: this.state + 1 });
    }

  }

  render() {
    const counter = this.state.counter;
    const incCounter = this.incCounter;

    return (
      <div>
        Number of clicks: { counter }.
        <br />
        <button onClick={incCounter}> Increment counter </button>
      </div>
    )
  }
}
```
---

### Composition vs Inheritance

Composition won.

* Containment: [via "children"](https://codepen.io/gaearon/pen/ozqNOV?editors=0010) or [via "props"](https://codepen.io/gaearon/pen/gwZOJp?editors=0010)
* Specialization: [deriving specific purpose component from generic one](https://codepen.io/gaearon/pen/kkEaOZ?editors=0010)

---

### Get Started


* [Documentation](https://reactjs.org/docs/)
* [Tutorial](https://reactjs.org/tutorial/tutorial.html)
* [Create react app](https://github.com/facebook/create-react-app/)


---

### Assignment

Simple React App

* Use "create-react-app"
* commit initial state
* create branch "feat/basic", work in it
* Page Component (enforces page layout)
* Header Component
* Content Component
* Footer Component
* create pull-request to master
* deploy to [Now](https://now.sh)

---

<center>
  <h1>React Basics</h1>
  <br />
  <small>
    <i>In react we trust</i>
  </small>
  <br />
  <br />
  <small>
    by [Vladimir Starkov](https://iamstarkov.com)
    <br>
    frontend engineer at [Nordnet Bank AB](https://www.nordnet.se/)
  </small>
</center>