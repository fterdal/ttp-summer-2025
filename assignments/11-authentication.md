# 🔐 Authentication

## Goals:

- Understand cookies and JSON Web Tokens on the server-side
- Set up client-side authentication flows
- Explore the basics of web security

## Direction

You should start by reviewing a [Pull Request (PR) on the CRUD-Backend Starting Point](https://github.com/TTP-2025/CRUD-Backend/pull/13/files). This PR adds several features necessary for authenticating users, for example:

- Adds a User model, with username and password
- Adds methods to create passwords and check passwords for users
- Adds Express middleware to parse cookies
- Adds a custom `authenticateJWT` middleware which protects routes from non-logged-in users
- Adds a `GET /auth/me` route which clients can use to confirm that they are logged in
- Adds a `POST /auth/signup` route for creating new user accounts
- Adds a `POST /auth/login` route for logging in to an existing user account
- Adds a `POST /auth/logout` route for logging out and deleting cookies
- Configures CORS with environment variables to accept requests from specific domains

You should begin by reviewing this PR carefully with your team. You should already be familiar with the CRUD-Backend starting point repo from your time working on the CRUD assignment. Reading PRs is an essential skill: pay attention to where things are defined, and then how they are used. Ask questions. Take notes.

You and your team will be using this backend to create an authentication flow on the frontend. You can eiher:

1. Pull these changes down and work from the starting point:

```
git clone https://github.com/TTP-2025/CRUD-Backend
git checkout add-auth
```

1. Integrate these changes into a finished CRUD app.

```
git remote add upstream https://github.com/TTP-2025/CRUD-Backend
git checkout -b add-auth
git merge upstream add-auth
```

If you're working off of a finished CRUD project, please make your commits on the `add-auth` branch, not the `main` branch.

Deployment is not a requirement of this assignment (though feel free if you are so inclined).

If you chose to work from a finished CRUD app, use the CRUD-Frontend repo for the frontend. Otherwise, you can use the CRUD-Frontend starting point repo:

```
git clone https://github.com/TTP-2025/CRUD-Backend
git checkout add-auth
```

## Assignment

Complete the following.

- [ ] **For unauthenticated users, the navbar shows Login and Signup Buttons**
- [ ] **For authenticated users, the navbar shows a Logout Button**
- [ ] **Users are able to fill out the Signup Form to create a new user account**
- [ ] **Users are able to fill out their username and password login to an existing user account**
- [ ] **Users are able to log out of their account by clicking the Logout button**
- [ ] **Unauthenticated users are not able to create new campuses or students**
- [ ] **Unauthenticated users are not able to delete campuses or students**
- [ ] **The Signup and Login forms show validation errors where appropriate**

### BONUS

- [ ] Add an association between users and campuses, where a user has many campuses, and a campus belongs to a user
- [ ] When a user creates a new campus, that campus is automatically associated with the user
- [ ] Only users that are associated with a campus can delete it, otherwise they receive an informative error
- [ ] Users can only view students from campuses that they are associated with – unauthenticated users cannot view any students
