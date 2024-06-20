# Simon Demo
A simon project for CS260, focused on learning HTML, CSS, Javascript, and React. By the end, I gained an understanding of the MERN web stack from the ground up, including other useful technologies such as Websockets, AWS EC2 instances and Route56, Caddy, and more. This README.md is intended to catalog some of my observations about the simon project as it evolves. At the time of writing, you can find the complete site at this link (but I may take it down to save money): [https://simon.harrison260site.click](url)

_2/8/23 HTML Simon Project_
- Button elements can have SVG or IMG children, which gives the button an interesting design
- tr and td elements are table row and column elements, which give more control when using tables
- hr and br are useful tools for adding horizontal line divisions and line breaks respectively
- Text spacing is based on width, not on line breaks in VS code

_2/21/23 CSS Simon Project_
- Absolute positioning with a translation of sorts can help center an element
- Overriding bootstrap qualities may be important as shown in the menu for this project
- Flex with different values: proportion then minimum (calculations also viable here see main)
- display types to override normal ways html is shown
- mess with border radius for shapes
- min-width or height takes priority over normally set width or height to be responsive

_3/4/23 JS Simon Project_
- we can access local storage to save things about our website on a particular browser so that the facts are remembered, and access it later (keys values)
- document marks the top of our html DOM tree, from which we can select and manipulate elements
- this keyword returns the actual item, which in Simon tends to be an element of the DOM to manipulate
- await keyword which delays something before running it
- JSON is an important way to store data in local storage but removes functions

_3/22/23 Simon Service_
- Node.js steps: create project directory, npm init -y, add node-modules to gitignore, install packages, use require in JS code for appropriate functions, run with node index.js service
- Express is a "wrapper" which mediates numerous middlewares to interpret http requests. we use express() constructor express.Router() mostly
- Those request and response objects have data values and member functions, which can be sent to users - see sequence diagrams if needed. It is of the form (req, res, next)
- That service can also listen on a particular port to perform its functions effectively

_3/25/23 Simon DB_
- Environment variables must be changed in the development and production environment. Use sudo in production, and advanced setting in windows
- Various databases exist online that can be used for a website, tailored to different needs
- All databases support a kind of object based querires. In Mongo they are of the form database.collection.find(*regex or other method*)
- export in js signifies a public function required elsewhere
- We must get and update database data asyncronously

_3/27/23 Simon Login_
- A login takes an email, password, and other necessary information and returns a cookie with an authorization token
- Different endpoints for different HTTP requests to do different authentication functions
- We must encrypt whatever passwords of users we have using a package like bcrypt

_3/29/23 Simon WebSocket_
- For communication to happen between users, websockets can allot a server for multiple users to communicate with (an upgraded http connection of sorts)
- ping/pong every once and awhile to see if a connection is still alive
- in messaging, WebSockets can use connection, message, and close pattern to forward messages appropriately: connection adds to list of connections where messages are forwarded until closed

_4/19/23 Simon React_
- It is important in testing for you to have your node.js for index.js in services running as well as your npm build in the main directory. The idea is that 3001 is the app that interfaces with port 3000 for services
- React changes our code to be handled in three rather than two parts: public, service, and src
- use npx create-react-app in order to create a template react for you to move code into before copying it back (apparently plays into better feedback as well)
- The power of react is such that it can use states with set functions (useState()) and effects when things render (useEffect()), allowing an application to be one page
- Ideally, web programming starts with react rather than being ported from it
- Kind of a pain in the behind to port over

-----

![simonPic](https://github.com/harrydcole2/simon-game-demo/assets/63384355/b8581bc1-4803-4e9b-a099-fcc070584f66)
