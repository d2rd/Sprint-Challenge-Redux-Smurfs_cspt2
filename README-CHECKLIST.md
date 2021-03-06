// PR - https://github.com/LambdaSchool/Sprint-Challenge-Redux-Smurfs/pull/560

## [x] Start by forking and cloning this repository.

## Questions - Self Study - You can exercise your Google-Fu for this and any other _Sprint Challenge_ in the future.

1. [x]  Name 3 JavaScript Array/Object Methods that do not produce side-effects? Which method do we use to create a new object while extending the properties of another object?
2. [x]  Describe `actions`, `reducers` and the `store` and their role in Redux. What does each piece do? Why is the store known as a 'single source of truth' in a redux application?
3. [x]  What is the difference between Application state and Component state? When would be a good time to use one over the other?
4. [x]  What is middleware?
5. [x]  Describe `redux-thunk`, what does it allow us to do? How does it change our `action-creators`?
6. [x]  Which `react-redux` method links up our `components` with our `redux store`?

## Initializing Project - READ THIS CAREFULLY, you have two apps here. A server, and a client.

* [x]   `cd` into the forked copy of this repo.
* [x]   **RUN** `yarn` or `npm install` to retrieve all `server-side` the dependencies.
* [x] **LOOK** at all the files you've been given for this project. One important file to note is `server.js`. This file contains an **API** that you are going to be interfacing with. Below is documentation on how to interact with the **API**.
* [x] **RUN** `yarn start` or `npm start` to get your API up and running on `http://localhost:3333`. This is the **URL** you're going to need to use within your React app in order to make AJAX requests for data.
* [x] After your API is up and running, you can open chrome and type in `http://localhost:3333/smurfs`. You should see an empty Array `[]` returned to you. This is an array that your **API** will be using to store our Smurf Data.
* [x] **LOOK** at your `smurfs` directory and notice it's just a plain ol' React App that we've built using `create-react-app`.


* [x] **Open** `src/index.js` to make sure that your app is ready to roll with the proper middleware.
* [x] **cd** into `smurfs` and run `yarn` or `npm install` to retrieve the client side dependencies.
* [x] **RUN** `yarn start` or `npm start` to fire up your React application. There ought to be a pretty little message awaiting you welcoming you to the app. `Follow` the prompting.


## API Design

### GET '/smurfs'

* [x] To retrieve an array all the smurfs in the Smurf DB simply write a get to the endpoint `'/smurfs'`.
* [x] Because `Redux-Thunk` is wired up as a middleware for this project. Be sure to utilize thunks when appropriate.

* [] Your response from the server should be an array of smurfs.

### POST '/smurfs'

* [] To add a smurf to the Smurf DB you'll need all three fields. `name`, `age`, and `height`.

* [] If a smurf is created correctly, you should see a response that is an array of smurfs with uniqe id's assigned to each smurf.
* []  Initially Brainey will be in the array, but it takes more than one smurf to make the village. Be sure to add a few smurfs to populate our smurf village.
* **HINT** if you are going to be working on Stretch Problem, you'll need to use that unique `id`.
    
## STRETCH PROBLEM

* The following two endpoints are here for you if you'd like to push yourselves a little further.

###  [] PUT '/smurfs/123', where 123 is the Id of the smurf you want to modify

* []  For this endpoint to work, you'll need an `id` added to the URL, and at least one field to update on the Smurf object. `name` `age` `height`.
    

###  [] DELETE '/smurfs/123', where 123 is the Id of the smurf you want to remove

* For this endpoint to work, all you need is an id sent up as part of the request url.

* If your delete worked, you'll get a an array back with all of the smurfs but with your requested smurf removed.
* You don't need any input beyond the url parameter of the smurf, so if we send up a delete request to `/smurfs/123` then you'll remove the smurf by that id.

