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
    return React.createElement('div',{},React.createElement('h1',{}, 'Welcome to react'))
}

App();
```
> Now, even if we call this function still it will not work because here we just create an react element for us, in order to run this we need to some more work.


###