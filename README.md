# simon
Simon project for cs260

2/8/23 HTML Simon Project
- Button elements can have SVG or IMG children, which gives the button an interesting design
- tr and td elements are table row and column elements, which give more control when using tables
- hr and br are useful tools for adding horizontal line divisions and line breaks respectively
- Text spacing is based on width, not on line breaks in VS code

2/21/23 CSS Simon Project
- Absolute positioning with a translation of sorts can help center an element
- Overriding bootstrap qualities may be important as shown in the menu for this project
- Flex with different values: proportion then minimum (calculations also viable here see main)
- display types to override normal ways html is shown
- mess with border radius for shapes
- min-width or height takes priority over normally set width or height to be responsive

3/4/23 JS Simon Project
- we can access local storage to save things about our website on a particular browser so that the facts are remembered, and access it later (keys values)
- document marks the top of our html DOM tree, from which we can select and manipulate elements
- this keyword returns the actual item, which in Simon tends to be an element of the DOM to manipulate
- await keyword which delays something before running it
- JSON is an important way to store data in local storage but removes functions

3/22/23 Simon Service
- Node.js steps: create project directory, npm init -y, add node-modules to gitignore, install packages, use require in JS code for appropriate functions, run with node index.js service
- Express is a "wrapper" which mediates numerous middlewares to interpret http requests. we use express() constructor express.Router() mostly
- Those request and response objects have data values and member functions, which can be sent to users - see sequence diagrams if needed. It is of the form (req, res, next)
- That service can also listen on a particular port to perform its functions effectively

3/25/23 Simon DB
- Environment variables must be changed in the development and production environment. Use sudo in production, and advanced setting in windows
- Various databases exist online that can be used for a website, tailored to different needs
- All databases support a kind of object based querires. In Mongo they are of the form database.collection.find(*regex or other method*)
- export in js signifies a public function required elsewhere
- We must get and update database data asyncronously

3/27/23 Simon Login
- A login takes an email, password, and other necessary information and returns a cookie with an authorization token
- Different endpoints for different HTTP requests to do different authentication functions
- We must encrypt whatever passwords of users we have using a package like bcrypt

3/29/23 Simon WebSocket
- For communication to happen between users, websockets can allot a server for multiple users to communicate with (an upgraded http connection of sorts)
- ping/pong every once and awhile to see if a connection is still alive
- in messaging, WebSockets can use connection, message, and close pattern to forward messages appropriately: connection adds to list of connections where messages are forwarded until closed