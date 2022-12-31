<h1 align="center">Notes to be taken from this project:</h1>
<h6 align="center">keep in mind that this project has been taken just in order to take notes from it.
 
npx create-react-app ghaith-clone-2


</h6>

this project especially the API part did not work, I analyzed the reason, and at the end, the database was not connecting so I merged two projects and two package.json files until it worked, it was an extreme experience to manipulate the two projects, and get out with one project even though a lot of errors faced me but I thrived on solving and make the project works, with learning what I was the face of code.


## nice assembly techniques : 
   - async func(Promise<void>) does both  await establishDatabaseConnection(), initializeExpress(); 
   - initializeExpress(){express,cor,json,urlencoded,}
   - use(addRespondToResponse())interface of RequestHandler{res.respond=(data):void{res.statur(200).send(data)}}
   - catchErrors takes a function of RequestHandler interface and return the latter.
   - not forgetting to put next for the middleware going to the next functions.
   - not putting the next() in middleware routes function, and putting the RouteNotFoundError after them in the main index.js,putting RouteNotFoundError in the next method, RouteNotFoundError as a class constructs {message,code,status,data={}}{extrend Error{{name;message;stack?:}
   - in a row thew handleError function comes with a type of ErrorRequestHandler
   - the authentication (Bearer authentication) (token authentication) process starts with req.get('Authorization') getting the header then the bearer and token
## backend basics reqs learning:
   - req.originalUrl retains the original request
   - installing the packages for typescripts because sometimes it is installed wrongly for javascripts.
   - express middleware concept
   - the next() funtiong and what it does
   - Cross-Origin Resource Sharing (CORS)(Resource Sharing policy, prevents accessing web          resources from sources other than the server the website is running        on for                      security      purposes.)
   - Origin is defined by the scheme (protocol), hostname (domain), and port
   - express.unencoded() is a method inbuilt in express to recognize the incoming Request Object as strings or arrays. This method is called app.use(express,urlencoded());
   - express.json() {it parses the incoming requests with JSON payloads and is based upon the bodyparser. This method returns the middleware that only parses JSON and only looks at the requests where the content-type header matches the type option.}
   - catching errors stratigy, putting the async func inside another one that does the (try:) in the errors.ts file 
   - the .use function and what function it takes, every thing that is implemented inside the      .use will be runing and adds a new middleware.
   - .all listens for all http methods
   - .route (chaining requests) and how to implement it in the middle ware file, and adjust it due to process.env(dev, test )
     to facilitate the testing process
   - in the middleware pathes putting * inside a the path url (for example user* thing) as in the place of * may come any thing else.
   - the middleware runs in sequence
   - TypeORM - Entity: it is an ORM(Object–relational mapping) used with TypeScript and JavaScript (ES5, ES6, ES7, ES8)
   - create QueryBuilder ways(DataSource, entity manager, repository)
   createQueryBuilder 
   - extending with the BaseEntity class
   getOneOrFail (single result), if no result throw an EntityNotFoundError), getOne(single result), getMany,"SUM(), AND, .andWhere, .orWhere, .having, .orderBy(,"DESC"/"ASC"), .addOrderBy{multiple order-by criteria}
   - classifying middleware, for example, running a function (auth(req,res,next)) before a .get app.get('/users', auth, (req, res) => {
   - basic responding techniques (res.json, res.redirect
   .send() {its own built-in headers natively}
   .status(){set a HTTP status code}
   .sendStatus() {adapt both the .status() and .send() methods}
   .redirect() {directing the client side to a different page}
   .render() method accepts an HTML file as an argument
   .sendFile{second argument is an options variable, sets an error handler as the third. it sends the files stored in the public directory to the client-side.
   .type() {res object it passes a file type as an argument
   .respond is set to a function as a responding action(created by namespace as interface)
## TypeORM:
  - important initializing params:(logging, synchronize, reconnectInterval, reconnectTries, entities:[], migrations:[], cli:[])
  - A migration is just a single file with sql queries to update a database schema and apply new changes to an existing database.
  - @entity
  - @column
## typescripts errors:
 - from tsconfig.json()comenting out the ("experimentaldecorators" : true)
## scripts to learn:
  - npm install --save @types/lodash (know how to install something for typescripts)
  - npm install --save-dev typescript @types/node @types/react @types/react-dom @types/jest @types/express -D (to install type scripts)
  - npm install --save-dev typescript @types/node @types/react @types/react-dom @types/jest
  - npm install --force
  - npm ci (uninstall and then install)
  - npm install -g ts-node(install as global)(is not recognized as an internal or external command)
  - npm ERR! code EJSONPARSE(npm install {ts-node --save-dev,typescript -g,typescript --save-dev })
  - npm install pg --save(to install postgresql)
## preparing for typescripts:
  -(npx tsc --init, touch src/app.ts{create new file})
  - in the scripts field inside the package.json(dev: ts-node-dev ts_file_name)
  - to rerun after save the ts file we add(dev: ts-node-dev --respawn --transpile-only ts_file_name)
    
  - <T>typescripts Generics declaration (any non-declared variable)
  - void (annotate the return type explicitly to void)(used if no data to return)
  - The static members of a class are accessed using the class name and dot notation
  - Type Assertion or casting(<>)
  - Namespaces (a TypeScript-specific way to organize code.) (.d.ts)
  - tcs (file_name)  
  - create config file (tsc --init)(npx tsc --init)(tsc-node-dev)
  - running script (tsc-node-dev ts_file_name)
  - Promise<void> nice to learn the promise but we put the void as it will not return any data
  - a class in type script after compiling how it would looks in javascript
  - type
## what i learned from this project:
- module-alias/register
- Written in modern React, only functional components with hooks
- the styling is not sorted well like using sass but in a new technique that i like and learned in details
- very tricky ways using styled-components has been learned(adv:1-track of which components and injects their styles 2-unique class names 3-every bit of styling is tied to a specific component)
- i read about ECMAScript to understand the errors like (Cannot use import statement outside a module) and differents between ECMAScript and the javascripts (CommonJS is a module formatting system). Succinctly, Node.js as a platform provides an environment outside of the traditional web browser for executing JavaScript code (It's important to note here that Node.js was created for building network applications using JavaScript). CommonJS is a module formatting system. It is a standard for structuring and organizing JavaScript code. CJS assists in the server-side development of apps and it’s format has heavily influenced NodeJS’s module management.
## useful libraries:
- Color from 'color' and how to use it (darken, tostring )
- styled-components(createGlobalStyle)
- <fragment> is used to wrap or group multiple elements without adding an extra node to the DOM.
## basics I learned:
 - A request header is an HTTP header, used in an HTTP request to provide information about the request context, so that the server can tailor the response.
 - instanceof operator is used to check the type of an object at the run time
 - console.error It prints to stderr with newline
 - express.urlencoded() It parses incoming requests with urlencoded payloads and is based on body-parser.
 - --save option instructed NPM to include the package inside of the dependencies section of your package.json(for npm 5.0.0and above, installed modules are added as a    dependency by default, so the --save option is no longer needed)
 - @alias tag (it causes JSDoc to treat all references to a member as if the member had a different name.){(alias) usage}
 - .urlencoded({extended: true}) precises that the req.body object will contain values of any type instead of just strings.
 - require('dotenv').config(){for the .env to works because i faced problems with it }
 - learning how to remove errors if the errors newly appear with no reason.(uninstalling amnd then installing the dependincies)
 - nodemon(automatically restarting the node application when file changes in the directory are detected.)(must installed globally)
  -(nodemon --watch)(nodemon.json{ignore,ext,watch,env,execMap})
 - package-lock.json (It stores an exact, versioned dependency tree)
 - SERVER TESTING: describe, test and expect (for testing){set env variable: NODE_OPTIONS=--experimental-vm-modules npx jest}
 - Async/await backend (await makes JavaScript wait)
 - how to add typescripts to your project by (npm install --save-dev typescript @types/node @types/react @types/react-dom @types/jest)
 - import without writing js
 - createRoot(the purpose is to Render an app fully built with React)
 - StrictMode (React Developer Tool)(highlighting potential problems in an application)
 - lodash functions(.pick(), )
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
 queryStringToObject,objectToQueryString,isNilOrEmptyString(undefined situations: null, undefined,''(string)),
 smooth way of functions exporting in createQueryParamModalHelpers.js
 handling the unreached data: (!data) return <PageLoader />;
 handling the error situation if (error) return <PageError />;
## javascripts basics:
 -The super keyword is used to call the constructor of its parent class to access the parent's properties and methods.
 - path.extname(), .includes(),path.parse(root, dir, base, ext, name), __filename, __dirname, parseInt()
  # different between ESmodules and commonjs practically:
 commonjs:(standards used to implement modules on JavaScript.)
 ESmodules:(standarize how JS modules work and implement this features in browsers (which didn't previously support modules).)
- module.exports={}, require (with commonjs)
- import {} export {} from (ESmodules) not to forget you must put the type:module in the package.json
 export default mod1Function => import dh from 
 export {dh} => import {dh} from 
## github basics:
- git remote -v(showing the origins)(if you have dev and master we can run git push dev master)
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
