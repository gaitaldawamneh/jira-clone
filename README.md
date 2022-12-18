<h1 align="center">Notes to be taken from this project:</h1>
<h6 align="center">keep in mind that this project has been taken just in order to take notes from it.
 
npx create-react-app ghaith-clone-2
npm install --save-dev typescript @types/node @types/react @types/react-dom @types/jest
 
</h6>
## backend bsics requirments:
    - express middleware concept
    - the next() funtiong and what it does
    - the .use function and what function it takes, every thing that is implemented inside the .use will be runing and adds a new middleware.
    - .all for all http methods
    - the miiddleware runs in sequence
    - classifying middleware, for example, running a function (auth(req,res,next)) before a .get app.get('/users', auth, (req, res) => {

## preparing for typescripts:
   #scripts: 
    - tcs (file_name)  
    - create config file (tsc --init)(npx tsc --init)(tsc-node-dev)
    - running script (tsc-node-dev ts_file_name)
   

## what i learned from this project:

- Written in modern React, only functional components with hooks
- the styling is not sorted well like using sass but in a new technique that i like and learned in details
- very tricky ways using styled-components has been learned(adv:1-track of which components and injects their styles 2-unique class names 3-every bit of styling is tied to a specific component)
- i read about ECMAScript to understand the errors like (Cannot use import statement outside a module) and differents between ECMAScript and the javascripts (CommonJS is a module formatting system). Succinctly, Node.js as a platform provides an environment outside of the traditional web browser for executing JavaScript code (It's important to note here that Node.js was created for building network applications using JavaScript). CommonJS is a module formatting system. It is a standard for structuring and organizing JavaScript code. CJS assists in the server-side development of apps and it’s format has heavily influenced NodeJS’s module management.
## useful libraries:
- Color from 'color' and how to use it (darken, tostring )
- styled-components(createGlobalStyle)
- <fragment> is used to wrap or group multiple elements without adding an extra node to the DOM.
## basics I learned:

 - Async/await backend (await makes JavaScript wait)
 - how to add typescripts to your project by (npm install --save-dev typescript @types/node @types/react @types/react-dom @types/jest)
 - import without writing js
 - createRoot(the purpose is to Render an app fully built with React)
 - StrictMode (React Developer Tool)(highlighting potential problems in an application)
## techniques I learned:
 - useRef in api 
 - dealing with history thing history.location.search.path
 - publish/subscribe pattern
 - A transition component
 - The toast is in the app file so must be alwaysshown in during surfing the routes
## functions I learned:
 - setTimeout, uniqueId, queryString.parse, omit,stringify,querystring.stringify(produce an URL query string),useRouteMatch()
 - history.(functions)
## functions created I learned:
 queryStringToObject,objectToQueryString
 smooth way of functions exporting in createQueryParamModalHelpers.js
 handling the unreached data: (!data) return <PageLoader />;
 handling the error situation if (error) return <PageError />;
## scripts i used:
 npm install --save-dev typescript @types/node @types/react @types/react-dom @types/jest (to install type scripts)
 
  # different between ESmodules and commonjs practically:
 commonjs:(standards used to implement modules on JavaScript.)
 ESmodules:(standarize how JS modules work and implement this features in browsers (which didn't previously support modules).)
- module.exports={}, require (with commonjs)
- import {} export {} from (ESmodules) not to forget you must put the type:module in the package.json
 export default mod1Function => import dh from 
 export {dh} => import {dh} from 
<h1 align="center">A simplified Jira clone built with React and Node</h1>

<div align="center">Auto formatted with Prettier, tested with Cypress 🎗</div>

<h3 align="center">
  <a href="https://jira.ivorreic.com/">Visit the live app</a> |
  <a href="https://github.com/oldboyxx/jira_clone/tree/master/client">View client</a> |
  <a href="https://github.com/oldboyxx/jira_clone/tree/master/api">View API</a>
</h3>

![Tech logos](https://i.ibb.co/DVFj8PL/tech-icons.jpg)

![App screenshot](https://i.ibb.co/W3qVvCn/jira-optimized.jpg)

## What is this and who is it for 🤷‍♀️

I do React consulting and this is a showcase product I've built in my spare time. It's a very good example of modern, real-world React codebase.

There are many showcase/example React projects out there but most of them are way too simple. I like to think that this codebase contains enough complexity to offer valuable insights to React developers of all skill levels while still being _relatively_ easy to understand.

## Features

- Proven, scalable, and easy to understand project structure
- Written in modern React, only functional components with hooks
- A variety of custom light-weight UI components such as datepicker, modal, various form elements etc
- Simple local React state management, without redux, mobx, or similar
- Custom webpack setup, without create-react-app or similar
- Client written in Babel powered JavaScript
- API written in TypeScript and using TypeORM

## Setting up development environment 🛠

- Install [postgreSQL](https://www.postgresql.org/) if you don't have it already and create a database named `jira_development`.
- `git clone https://github.com/oldboyxx/jira_clone.git`
- Create an empty `.env` file in `/api`, copy `/api/.env.example` contents into it, and fill in your database username and password.
- `npm run install-dependencies`
- `cd api && npm start`
- `cd client && npm start` in another terminal tab
- App should now be running on `http://localhost:8080/`

## Running cypress end-to-end tests 🚥

- Set up development environment
- Create a database named `jira_test` and start the api with `cd api && npm run start:test`
- `cd client && npm run test:cypress`

## What's missing?

There are features missing from this showcase product which should exist in a real product:

### Migrations 🗄

We're currently using TypeORM's `synchronize` feature which auto creates the database schema on every application launch. It's fine to do this in a showcase product or during early development while the product is not used by anyone, but before going live with a real product, we should [introduce migrations](https://github.com/typeorm/typeorm/blob/master/docs/migrations.md).

### Proper authentication system 🔐

We currently auto create an auth token and seed a project with issues and users for anyone who visits the API without valid credentials. In a real product we'd want to implement a proper [email and password authentication system](https://www.google.com/search?q=email+and+password+authentication+node+js&oq=email+and+password+authentication+node+js).

### Accessibility ♿

Not all components have properly defined [aria attributes](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA), visual focus indicators etc. Most early stage companies tend to ignore this aspect of their product but in many cases they shouldn't, especially once their userbase starts growing.

### Unit/Integration tests 🧪

Both Client and API are currently tested through [end-to-end Cypress tests](https://github.com/oldboyxx/jira_clone/tree/master/client/cypress/integration). That's good enough for a relatively simple application such as this, even if it was a real product. However, as the app grows in complexity, it might be wise to start writing additional unit/integration tests.

## Contributing

I will not be accepting PR's on this repository. Feel free to fork and maintain your own version.

## License

[MIT](https://opensource.org/licenses/MIT)

<hr>

<h3>
  <a href="https://jira.ivorreic.com/">Visit the live app</a> |
  <a href="https://github.com/oldboyxx/jira_clone/tree/master/client">View client</a> |
  <a href="https://github.com/oldboyxx/jira_clone/tree/master/api">View API</a>
</h3>
