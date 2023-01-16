## Making a plan in React

1. Make a drawing of your app. Simple "wireframes"
1. Component Tree
   1. Look at the drawing and break it down into Components. Label these Components explicitly (i.e., DogList, etc)
   1. Draw a hierarchy (or tree) of components, describing which components are parents and which are children
   1. Looking at the drawing, make a list of your app's features. What should a user "be able to do" with this app?
   1. Now look at your component tree: which components "go with" which features? Draw lines and make these connections explicitly.
1. State
   1. Look back at the drawing and your list of features and imagine using the app. What _state_ do you need to track?
   1. For each piece of state, ask: "When does it change?" If the answer is, "never", then it is not state.
   1. Similarly, find all the 'events' (user clicks, form submit, on load etc) in your app. Ask one by one, "What state changes?" for each of these events. (This should feel like the the inverse of the previous step.)
   1. Think about how to validate each of your state changes. How will I know if state changed in response to this event? (Hint: react dev tools or console.log usually helps here.)
1. Data flow
   1. Look at your hierarchy and ask: which components need access to which state? Another way to ask this is: for each component, what does this component need to "do its job?". This list becomes the "props" of the component.
   1. If a child needs state from a parent, you will need to pass props. What will you name these props?
   1. Notice especially if two siblings need the same state: if so, you need a callback (i.e., debit card).
1. Pick one feature from your list and build it out. Start with its parentmost component, and work down the component chain. Do not build another feature until this one is finished (and you can prove that it is finished by validating state change).
