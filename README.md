This multiplayer Tic-Tac-Toe is deployed in EC2 instance and use a A record for shrijandra.net map to public IP of EC2 instance.
Others:created A record for www.shrijandra.net map to shrijandra.net, www.saish.shrijandra.net map to shrijandra.net
When we Enter User1 it continuously search for next user to be log in.
copy all the file to /var/www/html/ of EC2 instance.
To run application install npm in EC2 instance
Then install dependencies: npm i express http nodemon socket.io
web socket enable instance data exchange between two player in real time.
socket.io library that enables realtime event based communication between client and server, index.js is backend http server
React on front end and Node js in backend.
The node js application is listening at port 3000, so we need to type www.shrijandra.net:3000, www.shrijandra.net only shows static page


![image](https://github.com/shrijandra/RealTimeTicTacToe/assets/108766166/59cfc1d9-dae7-4ee1-89f6-6881fdb83757)

when application is stop pm2 stop index
![image](https://github.com/shrijandra/RealTimeTicTacToe/assets/108766166/901420ff-0a92-44ce-8c8e-67a69470fe8b)

To start the application pm2 start index, nodemon index will also work but if disconnect the SSH connection the application will stop running, so we install pm2.
![image](https://github.com/shrijandra/RealTimeTicTacToe/assets/108766166/620d2dad-2f6d-4ff4-b090-c347df503be1)



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
