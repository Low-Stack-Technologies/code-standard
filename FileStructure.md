# File Structure Instructions

## Naming files
When naming files we always use camel case, this means that the there are no spaces, dashes or underscores and that the first word is not capitalized, but all others are. Here are some examples:
- GOOD: `requestIsAuthenticated.ts`
- BAD: `RequestIsAuthenticated.ts`
- BAD: `request_is_authenticated.ts`

We do not include the type of module in the file name, so a user service does not have `service` in the file name.
- GOOD: `src/services/user.ts`
- BAD: `src/services/userService.ts`

### TypeScript types
When naming a type file for TypeScript make sure to include the `.d.ts` at the end.

## Directory structure
### /src - Source directory
The source directory conaints all code necessary to build/compile the application. In this directory **only the main application file** should be located.

### /src/libs - Lib
Libs are modules that only contains one function. In these files it is important to (when possible) export the function as default and give it the same name as the file.

#### Examples:
- `/src/libs/expectError.ts` - *Expects an error to be thrown while running a function.*
- `/src/libs/pythagoreanTheorem.ts` - *Calculates the hypothenuse of a right-angle triangle.*
- `/src/libs/internalServerErrorResponse.ts` - *Handle internal server errors.*

### /src/middlewares - Middleware
This is most applicable to Express projects, but middleware are functions which are run during the processing of a request from another client/server. In these files it is important to (when possible) export the function as default and give it the same name as the file.

#### Examples:
- `/src/middlewares/validateAuthenticationToken.ts` - *Validate the authentication token provided in the request headers.*
- `/src/middlewares/authenticateRequest.ts` - *Decode the provided authentication token and store the authentication data in the request.*

### /src/routes - Routes
Routes are *[libs](#srclibs---lib)** but they are made to handle an incoming request to a specific route.

#### Examples:
- `/src/routes/getUser.ts` - *Gets data about a requested user and responds to the client with the data.*
- `/src/routes/updateOtp.ts` - *Handles a partial update to an Otp in the database.*

### /src/routers - Routers
Here a sub-directory can be used to specify the API version such as `/src/routers/v1`. The routers are modules which contain an Express router to handle a specific category of routes. The router provides the Http server on how to find the final routes.

#### Examples:
- `/src/routers/user.ts` - *Handles all user related requests.*
- `/src/routers/v2/user.ts` - *Handles user related requests where backwards-compatability is important.*

### /src/services - Services
A service is a module that has many functions which are all related to a single thing, this could be users, web sockets, express server and more. Services are used by other modules such as in routes and the main application file to accolplish something such as updating user data in the database or starting the Http server.

Examples:
- `/src/services/server.ts` - *Handles all functions of the Express server.*
- `/src/services/user.ts` - *Handles getting/changing/creating/deleting user accounts and user data.*

### /src/types - Types
When working with TypeScript custom types are not uncommon, these are stored in the types directory.

Examples:
- `/src/types/userChanges.d.ts` - *Defines the different changes that can be applied to a user account.*