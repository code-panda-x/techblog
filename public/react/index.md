# All you need to know about React


### What is React
- A JavaScript library
- Use component-based approach
    1. All individual entities become completely reusable and independent of each other
    2. Rendering the application is easy and not dependent on other components of the UI
- 2011 developed by Facebok developer

Advantages:
- Easy for UI testing
- High readability
- Both client-side and server-side
- Easy understanding and boost efficiency 

Disadvantages:
- Writing code is compliciated
- Hard to cope its syntaxes and methods
- React is a simple library, not a complete framework, so it calls for dependency

### Angular vs React
![react-angular](/images/react-angular.png)

### Important feature of React
- React makes use of a single-direction data flow model
- It deals with complete server-side data processing and handling
- React uses Virtual DOM that has many advantages 

### What is DOM (Document object model)
When load HTML file, DOM is the representation of the same HTML document in a different format for Javascript access

Javascript looks at objects blow:
1. Element Node: head tag
2. Text Node: some text
3. Attribute Node: id = "div1"

### What is virtual DOM
A simple Javascript object that is the exact copy of the corresponding real DOM


### Difference between Virtual DOM and Real DOM
![dom.png](/images/dom.png)

### What is JSX?
Javascript XML that includes HTML and Javascript syntax

Browser **cannot** read JSX files directly, it can only read the objects provided by JavaScript

```
render(){
    return(
        <div>
        <h1> Hello what</h1>
        </div>
    );
}

```

### How rendering works
- Use render() function
- Once the function is called, it returns an element that represents a DOM component 

### Rendering slow, how to fix it?
1. React.memo(): prevent all of the unnecessary re-rendering
2. PureComponent: ensure the unnecessary re-rendering

### What are states
A source of data or objects that control aspects such as component behavior and rendering

States are used to create dynamic and interactive components

### What are props 
Props: properities

Props are read-only components that are **immutable** in nature

props is passed bown from parents to child components (single directional flow in data al all times)


### What is =>
It allows users to manually bind components easily

    <Myinput onChange={this.handleChange.bind(this)}/>
    <Myinput onChange={(e) => this.handleChange.bind(e)}/>

### create-react-app
CLI (Command line interface) to start a simple project

    Create-react-app my-app

Advantages:
- Support JSX
- Built with auto-prefixed CSS
- Scripts to handle JSS, CSS
- Fast interactive testing components

### Redux
Redux is used to store the state of the application in a single entity. This entity is a JavaScript object.

```
{
    first_name: 'Max'
    last_name: 'Turner'
    age: 21 
}
```
All of the data is retained by Redux (also called a store)

Advantages:
1. Code has to be organized, easy to work with
2. Test is easy beceause functions are small and isolated
3. Redux has a large community

#### Components of Redux
- Action: An object that describes the call
- Reducer: The state change storage unit
- Store: the state and object tree storage
- View: Displays data provided by the store


### Three phases of a component life cycle in react

1 Initial rendering -> 2 Update -> 3 Unmounting

1: Involves beginning of the journey of the component to the DOM

2: The component can be updated and rendered again

3: Involves the destruction of the component and its eventual removal from the DOM

### What are events
All the actions trigger events (Move mouse, press a key)

Events perform set activities as a response to these triggers

### How events are created
Onclick
```
class Display extends React.Component({
    show(evt){
        // code here
    },
    render(){
        // Render the div with an onclick prop
        return(
            <div onClick = {this.show}>Click here </div>
        );
    }
});
```

### Flux vs Redux 
![flux-vs-redux.png](/images/flux-vs-redux.png)

### Synthetic events
Synthetic events are objects that act as cross-browser wrappers, allowing for the use of native events

Ensure that a variety of browsers can run the API 

### Stateful components
Are entities that store the changes that happen and place them into the memory

The state can be changed, storing info as past, current, and future changes

### Controlled components
Components that have the ability to maintain their state

The data is completely controlled by the parent component

### Uncontrolled components
Data gets handled by DOM and not the React component

This is ususally done using refs in React

### Pure components
Singular entities that are written in React

Fast and simple to write, ensures performance is good


### Router
```
<switch>
    <route exact path='/' component={Home}/>
    <route path='/posts/:id' component={Newpost}/>
    <route path='/posts' component={Post}/>
</switch>
```

### Keys
Keys are used to check all items and to track changes actively

They are used to directly check if an item has been added or removed from a list

### Is there a way to avoid binding
1. Define the event handler as an inline arrow function =>
2. Use a function component along with hooks

### Hooks
Hooks are used to make use of state and other features without having to explicitly write a class

### Javascript append text
    <p id="test" name="hacker">Hi</p>
    document.getElementById("test").innerHTML += "Some text"


