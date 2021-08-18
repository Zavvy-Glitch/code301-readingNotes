# Readings 03

## Lists and Keys

- What does .map() return?
  - It will return a new array.
  
- If I want to loop through an array and display each value in JSX, how do I do that in React?
  - by using a pair of curly braces inbetween an <li> or <ul>
  
- Each list item needs a unique ____.
  - KEY
  
- What is the purpose of a key?
  - To help React identify which items have changed, are added, or are removed.
  
  ## Spread Operator
  
- What is the spread operator?
  - It will "spread" the array into different/separate arguments
  
- List 4 things that the spread operator can do.
  - Copy an Array
  - Use Math Functions
  - Add an item to a list
  - Converting NodeList to an Array
  
- Give an example of using the spread operator to combine two arrays.
  - (Example from https://medium.com/coding-at-dawn/how-to-use-the-spread-operator-in-javascript-b9e4a8b06fab)
  - [...["😋😛😜🤪😝"]] // Array [ "😋😛😜🤪😝" ]
  - [..."🙂🙃😉😊😇🥰😍🤩!"] // Array(9) [ "🙂", "🙃", "😉", "😊", "😇", "🥰", "😍", "🤩", "!" ]

  - const hello = {hello: "😋😛😜🤪😝"}
  - const world = {world: "🙂🙃😉😊😇🥰😍🤩!"}

  - const helloWorld = {...hello,...world} <<<<< the arrays of hello and world are combined [HERE]
  - console.log(helloWorld) // Object { hello: "😋😛😜🤪😝", world: "🙂🙃😉😊😇🥰😍🤩!" } 
  
- Give an example of using the spread operator to add a new item to an array.
  - (Example from https://medium.com/coding-at-dawn/how-to-use-the-spread-operator-in-javascript-b9e4a8b06fab)
  - const fruits = ['🍏','🍊','🍌','🍉','🍍']
  - const moreFruits = [...fruits];
  - console.log(moreFruits) // Array(5) [ "🍏", "🍊", "🍌", "🍉", "🍍" ]
  - fruits[0] = '🍑' <<<<<<<<<<< the peach got added [HERE]
  - console.log(...[...fruits,'...',...moreFruits]) //  🍑 🍊 🍌 🍉 🍍 ... 🍏 🍊 🍌 🍉 🍍
  
- Give an example of using the spread operator to combine two objects into one.
  - (Example from https://medium.com/coding-at-dawn/how-to-use-the-spread-operator-in-javascript-b9e4a8b06fab)
  - const myArray = [`🤪`,`🐻`,`🎌`]
  - const yourArray = [`🙂`,`🤗`,`🤩`]
  - const ourArray = [...myArray,...yourArray] <<<<<<<<<<<<<<<<<< Arrays being combined into one [HERE]
  - console.log(...ourArray) // 🤪 🐻 🎌 🙂 🤗 🤩
  
 ## Passing Functions between Components
 
- In the video, what is the first step that the developer does to pass functions between components?
  - The function is created where the state is living.

- In your own words, what does the increment function do?
  - Increment is intended add a value to the original set value provided within the state.
  
- How can you pass a method from a parent component into a child component?
  - It can be passed just like a prop in the parent to the child. 
  
- How does the child component invoke a method that was passed to it from a parent component?
  - It will be invoked as a this.props in the child component as part of the new function to call back to the parent.
  
