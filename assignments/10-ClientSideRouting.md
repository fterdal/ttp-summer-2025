# Client-side Routing

## Goals:

- Describe the difference between server-side and client-side routing
- Set up React Router to enable common browser behavior
- Understand built in React Router components / hooks (Route, Router, Link, useNavigation, useParams)

## Direction

This assignment will be a continuation of the previous React assignment. Last time, we had a simple todo front-end with a navbar at the top that didn't actually interact with the address bar. Today's task is to fix that, and make our application more usable with intuitive navigation options. You can even go further by

This assignment has two starting points: one for the [Front-end (React / React-Router)](https://github.com/fterdal/ClientSideRouting-Frontend) and another for the [Back-end (Express / Sequelize)](https://github.com/fterdal/ClientSideRouting-Backend). We won't be touching the Back-end one today. If you have a finished copy of the Backend from the previous exercise (Sequelize), you're welcome to use that one instead.

As always, one person in your group should fork or clone the starting point repositories and add the other members of the group as collaborators.

## Deployment

Today, we're graduating from using GitHub Pages! We've been using Vercel to deploy our backend code, and Vercel is also a great way to deploy front-end code. The starting point for the front-end already has a Vercel configuration that should make it seemless to deploy.

One advantage of deploying to Vercel is that it offers support for environment variables. This means we could create an environment varialbe called API_URL. When we're running the application locally, API_URL is equal to `http://localhost:8080`, and when it is deployed to Vercel, it's equal to whatever backend URL we get back from our backend deployment. You should be prompted to enter in an environment variable when you deploy your Reach application, and you can always configure it later.

## Assignment

Complete the following.

- [ ] **When clicking on the navbar links, the user is brought to the appropriate page, and the address bar changes accordingly.**
- [ ] **If the user is on a page besides / and they refresh, they are still on the same page.**
- [ ] **When the user successfully submits the Add Task form, they are brought back to the homepage.**
- [ ] **The user can click on a task title, and is brought to a tasks/:id page, where they see only that task, including the name of the user assigned to it.**
- [ ] **The user can navigate the page without reloading the page (check the Network tab to confirm).**

### BONUS

- [ ] Add a new /users page (and corresponding navbar option) to view all users.
- [ ] Clicking on an individual user shows a /users/:id page that lists all their tasks.
