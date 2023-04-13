# HappyTrak

This app aims to asses employee satisfaction, engament and well-being by collecting data on various aspects of the work environment. This is done by giving surveys every week and track this data. 

This app is created with the employees in mind. Surveys are sent every week for employees to respond and submit and therefore, gauge their satisfaction accross multiple aspects of their work envrionment. This helps the employer track happinees in the workplace and it may provide valuable feedback to organizations, which may help them identify areas of improvement, implement changes, and create a more positive and supportive work envrionmentfor their employees.  

Technology used for this app includes, React, React Router, Hooks, node,js, postgreSQL, and mongodb. 

React was used in this project to build reusable UI components. Which allowed us to create a dynamic and interactive user interface by composing components, managing state and props, and efficiently updating the DOM. React, provides a virtual DOM, which optimizes performance by minimizing actual DOM updates, which result in a faster rendering and better user experience. 

React Router handled client side routing. Also react router prevents triggering a full page reload. It allowed for define routes routes for different paths in this React application.    

Hooks are a new feature introduced in React 16.8. This new featured allowed us to use state and create functional components. Hooks provided an alternative to manage state, use UseState, useEffect which managed component state, and handling side-effect and therefore, mades our code more modular.

Node.js was used in order to use javascript in the backend. It was used in the server so we could use javascript in the front end and back end and therefore be string line. Node.js provided a path to install and create a dependency file that future developers can utilize to start working in the project immediately. 

PostgreSQL was used for our data storage and management. It provided a realiable and efficient way to store and manage structured data. 

MongoDB was used to store user information such as name and password. MongoDB was used to create user authentication and session control. Mongoose was used as a tool framework to make changes to the database as needed.


# Installation and Running the App

1. Fork and clone the repo. This creates a repo in your Github account
2. Go to the forked version of this repo on your Github account. Click the green "<> Code" button and copy the github url.
3. In your terminal, type `git clone <paste copied url here>`
4. Install dependencies by running `npm install` in your terminal.
5. To view the app in your browser and see live changes, run `npm run dev` in your terminal.

# How to Use

To use this project, the developer must have knowledge of Javascript for modyfiying the backend and the front end, as the frameworks and technologies behind this project run on this language. 

The front end makes requests to an api point that has been isolated in its own router, making the server files modular allowing the developer to easily modify routes to without compromising other components. The front end 

Authentication and session control uses a no SQL database and the employee information uses a SQL database. The developer must create their own databases and add the respective URI's to the `/server/models/dataModel` and `/server/models/employerModel` files


# Credits

### Idea and original creation of the app:

Christina
* Github: CElizOwens

Giovana
* Github: giovanacdlc

Iris
* Github: wiris316

Rachel
* Github: rachelk585

### Iteration update

Alejandro
* Github: AlejandroFlorez

Jon
* Github: Jrcrz

Kasey
* Github: kaseywolff

Matteo
* Github: MatteoDiter


# File Connections

## Backend

### Database
PostgreSQL database -> dataModel.js -> employeeController.js
MongoDB -> employerModel.js -> employerController.js

### Server
server.js -> employeeController.js -> dataModel.js
* Upon request (in server), go to controller, grab data from Postgres db (via path described above), back to controller, respond to client

server.js -> employerController.js -> employerModel.js
* Upon request (in server), go to controller, grab data from Postgres db (via path described above), back to controller, respond to client

## Routes
* Entry point for application is ./src/index.js
    * Browser Router is used in entry point when root is rendered
    * index.html and index.js are connected by id="root"
    * Within index.js, root is rendered using the Browser Router listed above
    * Browser Router wraps the App component
* App component contains Routes to other components, using paths defined in the server
    * path='/'
        * get request in server.js to '/' -> populate Dashboard.jsx component and render to web browser page

## Frontend
Each React component is currently housed within the App.jsx component. Currently, none of the other component .jsx files are connected, other than to the App component. Each component is rendered individually/ separate from one another depending on the route taken/ the route provided to the server.


  