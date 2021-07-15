# Reading 4

## Forms

### What is a ‘Controlled Component’?

    - "We can combine the two by making the React state be the “single source of truth”. Then the React component that renders a form also controls what happens in that form on subsequent user input. An input form element whose value is controlled by React in this way is called a “controlled component”
    - HTML, each form element typically maintains its own state and is updated with user input.
    - Uses state props and setState()

### Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.
  
    - Depenedent upon how the code is written, if set with handleChange this updates with every keystroke in the React state. Therefore, the displayed value with update as the user types.

### How do we target what the user is entering if we have an event handler on an input field?

    - handleChange is used to update what the user is using as they type

## Ternary Operator

### Why would we use a ternary operator?

### Rewrite the following statement using a ternary statement

#### Notes Cited from
  
    - https://reactjs.org/docs/forms.html
    - https://codeburst.io/javascript-the-conditional-ternary-operator-explained-cac7218beeff
