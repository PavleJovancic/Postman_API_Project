# Postman_API_Project
This is project that demonstrates my knowledge for testing API using POSTMAN.
Project consists of dev enviroment with variable that holds basic url and one collection with 4 test groups.<br/>

Tests are categorized in the following groups:
- Auth tests: API calls for login, register, verify, reset password, refresh token
- City tests: API calls with and without token for cities data, filtering, creating new cities, editing and delete
- Profile tests: API calls for registering profile, login, get profile information with and without user token, editing profile, changing password
- User tests: API calls for creating user with admin token, login, get all users with and without admin token, filter users, edit user with admin/user token, deleting a user

## API features
- Multiple environment ready (development, production)
- Custom email/password user system with basic security
- HTTP request logger in development mode
- User roles
- User profile
- Users list for admin area
- Cities model
- Testing with mocha/chai for API endpoints
- Ability to refresh token
- JWT Tokens, make requests with a token after login with Authorization header with value Bearer yourToken where yourToken is the signed and encrypted token given in the response from the login process

## Requirements
- Node.js 16
- Postman
- Newman

## Running tests
- Download tested [API project](https://github.com/davellanedam/node-express-mongodb-jwt-rest-api-skeleton)
- In the root of this project you will find a file named .env.example
- Create a new file by copying and pasting the file and then renaming it to just .env
- Open terminal from the root of the project and run 3 commands: npm install, npm run fresh and npm run dev for running a server<br/>
  You will know server is running by checking the output of the command `npm run dev`
```bash
****************************
*    Starting Server
*    Port: 3000
*    NODE_ENV: development
*    Database: MongoDB
*    DB Connection: OK
****************************
```
### Postman documentation for this **API testing project** can be found [here](https://documenter.getpostman.com/view/30400758/2s9YXbAmJb).
- For running API calls and tests in Postman after running the server and visiting test documentation link, click on 'Run in Postman' button, import collection and you can see all tests in Tests tab for every request inside the collection and run them.

- For running tests from the command line, additionally, you need Newman installed and exported collection and environment json files from Postman.
  From directory with exported collection and environment, open another terminal and start tests with command `newman run exported_collection.json -e exported_environment.json` 