### What is React Element ?

* It is a lightweight description of a piece of UI.
* In simple terms, a react element is simple js object which describe what properties an actual DOM node should contain.

>NOTE- BY JUST CREATING A REACT ELEMENT, IT WON'T AUTOMATICALLY RENDER IN DOM.

```javascript
    type : 'button',
    props: {
        className : 'btn-btn-primary',
        children: 'submit'
    }
```
<!-- this is an example of a react element which look like as an JavaScript object -->

```html
<button class = "btn btn-primary">
    submit
</button>
```
<!-- The above React element is equavalent to this above html code -->


### How to create this element ?

* by using the `createElement` function and to use this function we need  to include the `React CDN`

example : `React.createElement(type,property,...children)`;

<!-- Let's see this in action  -->

```js
<script>
const App = ()=>{
    return React.createElement('div',{},React.createElement('h1',{}, 'Welcome to react')) // it will not automatically render in the DOM.
}

App();
```
> Now, even if we call this function still it will not work because here we just create an react element for us, in order to run this we need to some more work.


###  React DOM ?

* So, DOM is a tree and every tree has a root node. so, we need to define a root node.

>how to create root node ?
* So, we create a element which act as a root node.

```js
<div id = "root"></div>
const rootNode = document.getElementById("root");
const root = reactDom.createRoot(rootNode);
```

> if we still run still we are not going to see anytthing because we just created a root node not rendered it.

* In order to run we run.

    `root.render(App());`

### Babel

* Now, above we can see if we need to write this much js, why we dont write just plain js ?

```js 
<script type="text/babel">
const App = () =>{ 
    return (<div><h1> Welcome</h1></div>); // Now, this is a React Component
    }
    const rootNode = document.getElementById('root');
    const root = ReactDOM.createRoot(rootNode);
    root.render(<App/>); // now this is a self closing html tag 
</script>

```

* We, can write like this in `JSX` format, but it will not run if we want too, because the javascript does not know this html syntax. So, we need to convert it, and there is something called `tranpiler`

* `transpiler` is a soure - to - source converter, there is a transpiler called `babel`.

* jsut add babel script  and `<script type="text/babel">` run it.
