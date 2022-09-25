### Conceptual Exercise

Answer the following questions below:

- What are some ways of managing asynchronous code in JavaScript?

	> Callbacks, Promises and Async/Await

- What is a Promise?

	> I a object tha represents the eventual completion (or failure) of an asynchronous operation and its resulting value.

	 > #### Promise has 3 States
	 > 

     > - pending: initial state, neither fulfilled nor rejected.

	 >  - fulfilled: meaning that the operation was completed successfully.

     > - rejected: meaning that the operation failed.


- What are the differences between an async function and a regular function?

 >	#### The async and await keywords enable asynchronous, promise-based behavior to be written in a cleaner style, avoiding the need to explicitly configure promise chains.

- What is the difference between Node.js and Express.js?

	>ExpressJS is a web application framework for NodeJS.
	 > ### And

	>NodeJS is open-source, cross-platform JavaScript code that runs on servers.

- What is the error-first callback pattern?

	> Is a function which either returns an error object or any successful data returned by the function.

- What is middleware?

	> Is a functions than run between request and response cycles.

- What does the `next` function do?

	> Is a function in the Express router which, when invoked, executes the middleware succeeding the current middleware.

- What are some issues with the following code? (consider all aspects: performance, structure, naming, etc)

```js
async function getUsers() {
  const elie = await $.getJSON('https://api.github.com/users/elie');
  const joel = await $.getJSON('https://api.github.com/users/joelburton');
  const matt = await $.getJSON('https://api.github.com/users/mmmaaatttttt');

  return [elie, matt, joel];
}
```

   > - getUsers() reads more like get all users and is only getting 3 users.	 
> - Is making 3 requests instead of one request to get all the users  

> - There is no try and catch (error handeling) so if one fails they all fail 

> - There is no description is not clear what the function do 