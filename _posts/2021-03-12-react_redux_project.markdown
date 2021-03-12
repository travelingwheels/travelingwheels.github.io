---
layout: post
title:      "React/Redux Project"
date:       2021-03-12 06:30:44 +0000
permalink:  react_redux_project
---


For my React project I choose to build an app that I wish I had back when I was driving truck.  The company I worked for was small and they would hand write each drivers schedule on paper and then you would have to go to the office and check it out. I hated going to the office and wished for something online.

I started out using the  `npx create-react-app Load_Board_Frontend`  command in the terminal. This creates the main structure of the application. I decided to put all of the state in redux. Redux is a JavaScript library for managing application state, it makes state accessable globally instead of in each individual component.  One advantage of this is not having to pass data from a grandparent to grandchild component relationships. The connect function provided by redux does exactly that, it connects a react component to the redux store, and the store is where the state is stored. Now here is where things get tricky to read state from the store you use the mapStateToProps function passed in as the first argument to the connect function. The second argument that can be passed in to the connect function is mapDispatchToProps, this function writes data to the store. Here is an example:

```
function mapStateToProps(state) {
  return { todos: state.todos }
}

function mapDispatchToProps(dispatch) {
  return { addTodo: bindActionCreators(addTodo, dispatch) }
}

export default connect(mapStateToProps, mapDispatchToProps)(Todos);
```

You can also use the shorthand object syntax for mapDispatchToProps which in this example would be { addTodo }.

```
export default connect(mapStateToProps, { addTodo })(Todos);
```

The basic flow of a react/redux app is this: an event happens in a component, then it is passed to an action creator, from there the data is set to an action and a payload(data), where it is passed to a reducer that will update the store and the store tells the components that something has changed and they should re-render. I found it confusing at first but after repeating the process many times it starts to sink in. I made this project bigger than what was required, not because I felt I had to, but rather I kept thinking of things to add. Honestly I still have alot I can add to the project.
