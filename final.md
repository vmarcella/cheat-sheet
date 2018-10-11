# BEW 1.1
## October 11th, 2018

1. Bootstrap components
	* container - create fixed width containers and container fluid creates 100% 
	* row is a responsive container for columns
	* col-*-* creates a response grid for the screen size and column length
	* default font size is 14 px
2. http verbs and status codes
	* GET - get me a resource
	* POST - create a new resource
	* PUT - update a resource
	* DELETE - delete a resource
	* status codes
		* 100 - informational
		* 200 - OKAY
		* 300 - redirects
		* 400 - client side error
		* 500 - server side error
3. Label all parts of a URL
	* https://www.google.com?query=hi&message=sup
		* https:// - The uniform resource loader (protocol)
		* www - sub domain
		* google - domain name
		* .com - top level domain
		* ?query - query parameter
		* & - adding another query
4. Define and describe the characteristics of Node.js
	* Node.js is a js runtime
	* async I/O
	* event driven
	* allows javascript code to be ran inside the command line
	* very small std lib, allowing users to create all the resources needed for bootstrapping a project 
5. Conventional environment strategy
	* Development
		* PATH variable correctly setup
		* set on one text editor and it's customized to your liking
		* secret keys in .env files
	* Staging
		* C/I that automates testing before being pushed to production
	* Production
		* ENV variables configured
		* Proper server configurations
	* Model view controller architecture (not apart of this section, but still relevant)
		* Model - handles the creation, deletion, and manipulation of data
		* View - what the user physically sees and interacts with
		* Controllers - handles requests made by the user. interacts with both the model and view
		* The model NEVER interacts with the view.
		* separates the concerns of each component
6. Define and describe the characteristics of a web server
	* Stateless
	* REST archictecture
	* has resources that can be CRUDed
	* communicates to clients via a request response cycle
7. Define and describe the characteristics of a web framework
	* assists in creating a web server
	* Allows developers to create web servers very fast
	* good web frameworks are generally opionless about the software you attach to them
	* allows for middleware to be attached
8. Be able to list all of the resourceful routes
	* /photos
		* show - GET - /photos - show all photos
		* index - GET - /photos/:photoId - show a single photo
		* edit - GET - /photos/:photoId/edit - edit for for editing a single photo
		* update - PUT - /photos/:photoId - updated photo
		* new - GET - /photos/new - form for creating a new photo
		* create - POST - /photos - all photos or the single one you just created
		* destroy - DELETE - /photos/:photoId - all photos
9. Draw an ERD
	* ERD = entity relationship diagram
	* one to one relationship ->
	* one to many relationship => 
	* many to many relationship <=>
	* Make school
		* One instructor has many students (instructor => students)
		* One instructor has many classes to teach (instructor => classes)
		* many classes have many students (classes <=> students)
		* students have one instructor per class (students -> teacher)
10. List the characteristics, pros, and cons of a document based database
	* characteristics
		* NoSQL database, meaning that no sql has to be written at all
		* uses commands to do things within the database
	* pros
		* Javascript objects can be turned directly into documents through an ODM
		* Very easy to create Schemas
		* Very easy to get started
		* Uses BSON
	* cons
		* not good for normalizing data
		* Cannot join tables
		* queries aren't as powerful
11. Define automated testing
	* automated testing is the automation of tests that ensure your code runs properly
		* Mocha is a test runner, meaning that it runs through tests in folders named `tests` (at least by default)
		* Chai is a asseration framework for unit testing. Unit testing make sures specific parts of your code work rather than the entire thing
		* stubbing is the replacement of external data with data of your own to produce expected results (hopefully)
		* UI testing is testing if the ui works and performs what it should do
12. Diagram and interpret javascript errors
	* Common JS errors
		* Uncaught type error
			* Cannot read property
			* You tried accessing a property from an undefined object
		* TypeError
			* 'undefined' is not a object
			* Reading a property or calling a method of an undefined object
		* TypeError
			* null is not a object
			* Reading a property or calling a method of a null object
		* ReferenceError
			* var is not defined
			* You tried to reference a variable that wasn't defined
		* SyntaxError
			* Unexpected char at...
			* You messed up javascript syntax. Get good.
		* RangeError
			* you tried indexing a value out of range
			* You probably tried indexing a value in a array out of range.
13. Mongo vs mongoose commands
	* Mongo is a native client for interacting with mongoDB. Mongoose is an Object document mapper that assists in modeling javascript objects to documents
	* mongo commands
		* show db - show all of your databases
		* use databaseName - use a database with the name of databaseName
		* db.auth() - authenticate with mongoDB
		* db.logout() - logout
		* show collections - show the collections of the current database
	* mongoose functions
		* mongoose.connect() - connect to a database
		* mongoose.on() - attach an event listener for mongoose events
		* mongoose.model() - create a new model for your database
14. Define an ODM
	* Object document mapping is mapping data that you're going to be using and interacting with in your code to documents that can be read and write to in your data.
15. Define and describe the characteristics of the DOM
	* the dom is DOCUMENT OBJECT MODEL. It represents the entire web page and all of the elements that make it up in a tree like object.
	* The dom is useful for interacting with web pages
	* Allows you to add functionality and styling with javascript
16. User center agile development
	* agile is a methodology of developing products. Instead of developing one giant end result project, you create a tinier version of that product and add features along the way
	* The client comes in when creating these features. The client can chime in on what they like and don't like about your project during development to you and because of agile you can make these changes on the fly
	* heavily orientated around change
17. Explain how to protect hidden keys in dev and production
	* environment variables and dotenv
	* Both of the previously mentioned allows you to access variables that don't have to be defined in your project. This way, people can look at your code and see that it uses secrets without actually using exposing that secret
18. Tell the main epochs in js history
	* Born in 1995, the same year that netscape and sun teamed up to work on it
	* handed to ECMA in 1996
	* Eich and mozilla join ecma in 2005 and js flourishes
	* 2016 92% of websites use JS
19. Define and describe the characteristics of REST
	* client-server archictecture - 
	* statelessness - no client context is ever stored on the server
	* cachability - responses can be cached 
	* Layered system - the user shouldn't be able to tell whether they're communicating with an endpoint server or a server in between'
20. convention over configuration
	* Convention - a standard that is practiced by multiple people and organizations
	* configuration - a very specific preference that is configured for a single entity
	* convention applies to a broader range of people, making it easier to work together.
	* programming languages have conventions for how you interact with the languae
21. Benefits of a server oriented architecture vs monolithic servers
	* services can go down without your entire web server going down
	* no central point of failure
	* distributes work load for a web server
	* very scalable and in a way separates the concerns from other services
