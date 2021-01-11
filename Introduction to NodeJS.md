## What is NodeJS? :innocent:

It is a JS runtime environment which allows you as a developer to write a pure JS can be running on both **client** and **server** to create a scalable and optimized web apps. 


## The benefits of using NodeJS in the server side :dango:
1. Has a great performance especially node is designed to optimize the **throughput** and **scalability** of our web app. It is an ideal solution when it comes to design a real-time web apps.

2. It is based on one language (JS) so the syntax stills pure JS therefore no need to learn a new programming language and it's syntax.

3. It is a cross platform environment means it can be installing and working with almost any type of OS such as Windows, Linux, MAC OS, ..etc.

4. Has a NPM which stands for **"Node Package Manager"** to enable us install any package or library used in the area of web apps.

## How to install a package in NodeJS? :heavy_check_mark:
There are multiple ways to install packages in NodeJS:
* Install the package locally and save it's name inside a `package.json` file:

        npm install express --save 


* Install it as a dev dependency means you'll only need it in the development not for production:

       npm install -D nodemon
 
  Or:

        npm install nodemon --save-dev

       
* Install the package globally with the flag -g:

        npm i -g nodemon


## Get started with NodeJS: :rocket:
To get start with NodeJS, all you need to install NodeJS so you can download it from **[here](https://nodejs.org/en/)**. After that open your CMD or Terminal and type the following command: 
        
    node --version 
    
---
## Write your first *hello world* program with NodeJS :computer:

1. Open your project directory with your preferable text editor, for example: **VSCode** :credit_card: and then open your VSCode terminal and type the following command:

       npm init -y
       
This is to create a new `package.json` file which contains all the details about your app such as: The main JS file which will be as the root file to your app, Author, Scripts to be running, the package name and so on.

2. Create a file named `index.js` then copy ans paste the following code snippet below:

    ```javascript
    // Load the http module
    const http = require("http")
    // Use a port
    const port = 5000;
    
    // Create a HTTP Server
    const server = http.createServer((request, response) => {
        response.end("<h1>Hello World</h1>");
    })
    
    // Make the server listen to your port
    server.listen(port, () => console.log(`Server is running on the port: ${port}`));
    ```

3. Open your terminal again and type the following command to run your NodeJs program:

        node index
        
 
An you can see below that your response now is printed on your browser:

![First Program](https://raw.githubusercontent.com/asattar30/NodeJS/main/Screenshots/FirstProgram.jpg)


## How NodeJS handles the request? :heartpulse:

NodeJS uses asynchronous programming means it has a single thread contains of all the tasks or requests which we need them to be running on our server. The goal here is never wait or block the next request when you have sent the first or previous request (Non-Blocking Process), so send the next request and get the response of the previous one rather than waiting a specific request to be running. This lead us to a high performance and memory efficient.
