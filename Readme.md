# CND Sample Events Web Application
## Step 1 - Starter Version
1. Getting started:  
   Using Google Cloud Shell  
   prerequisites: node and npm  
   these are available inside Google Cloud Shell.
    1. open two separate terminal sessions:
        * check that your **Project Id** is shown in yellow/gold in parentheses.
        * in one terminal **cd sample-master-2022/api-server**
        * in the other terminal **cd sample-master-2022/web-server**
    2. run **npm install** in each terminal
    3. run **nvm install 16** in each terminal
    4. run **nvm alias default 16** in each terminal
    5. run **npm start** in the *api-server* terminal
    6. run **npm start** in the *web-server* terminal
    7. click on the "preview" button of your Cloud Shell 
       * verify that it is pointing to port 8080.

1. The sample app  
   Uses nodejs with the express web server on both server and client microservices.  
   The api-server service receives REST requests on port 8082 and returns mock data.  
   The web-server service receives requests from the browser & unpacks json from  
   the internal service into a html template in the Views folder
   and returns it to the browser on port 8080.

1. Dependencies  
   The api-server and web-server both use the following npm packages:

    * express: a web server
        * https://www.npmjs.com/package/express
    * body-parser to convert json and form data in the request into parameters.
        * https://www.npmjs.com/package/body-parser
    * mocha, chai and supertest (for unit testing)
        * https://www.npmjs.com/package/mocha
        * https://www.npmjs.com/package/chai
        * https://www.npmjs.com/package/supertest
    * nyc for code coverage reporting
        *  https://www.npmjs.com/package/nyc

   The web-server service uses the following additional libraries:

    * express-handlebars ( a templating library)
        * https://github.com/ericf/express-handlebars
    * nock (for mocking the api call for unit tests)
        * https://www.npmjs.com/package/nock

