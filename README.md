I use winscp app to copy the file from local to remote AWS EC2 instance.

I use method 1 to run app continuously

Below documentation source: https://www.geeksforgeeks.org/how-to-run-a-node-js-application-permanently/

How to run a node.js application permanently ?
Read
Discuss
Courses
NodeJS is a runtime environment on a V8 engine for executing JavaScript code with some additional functionality that allows the development of fast and scalable web applications but we can’t run the Node.js application locally after closing the terminal or Application, to run the nodeJS application permanently. We use  NPM modules such as forever or PM2 to ensure that a given script runs continuously. NPM is a Default Package manager for Node.js Which enables us to access a lot of packages or modules that make things a lot easier for developing a web application.

Method 1: 

Using PM2 module:

Installing module in project Directory:
npm install pm2 -g
Start Your Node.js Application by pm2.
pm2 start [Your fileName]
All processes listed up which are registered with pm2.
pm2 list
Console output:

We can also stop any process runs by pm2 stop command:
 pm2 stop all                  
 pm2 stop [id number]       
Method 2: 

Using forever module

Installing module in your project Directory:
npm install forever -g
Start Your Node.js Application by forever module. 
forever start [Your FileName]
All processes listed up which are registered with forever
forever list
Console output:

 We can also remove or stop any processes that are registered with forever using index (such as 0 in this case)              
forever stopall
forever stop [index]
So now your Application will be running permanently even after exiting the terminal or Application.
