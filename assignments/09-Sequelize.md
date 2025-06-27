# PostgreSQL & Sequelize

- **Due** June 30, 2025 by 10:00:00 AM EDT
- **Submitting** Fill out all of the appropriate information in the Cohort Spreadsheet

## Goal

Learn the basics of Sequelize, how to create a PostgreSQL schema, and connect it to an Express app.

## Direction

This assignment will be a continuation of the previous Express assignment. Instead of using a dummy database, you'll be using a real database!

This assignment has TWO Starting Point repos, one for the [Backend (Express/Sequelize)](https://github.com/fterdal/Sequelize-Intro-StartingPoint), and another for the [Frontend (React)](https://github.com/fterdal/Express-Intro-Frontend).

One person in your group should fork these repositories and add the other members of the group as collaborators to both of them. If you'd like to continue where you left off from the previous assignment, you're welcome to do so, though I recommend at least taking a look at the Sequelize Starting Point to see how the database connection is set up.

You'll finish implementing the task management app you started previously. Last time, whenever the server restarted, all the data was lost. Now, we'll introduce a database, which will allow us to persist that data.

The existing frontend has functionality that uses the following routes:

- GET /api/tasks
- POST /api/tasks
- PATCH /api/tasks/:id
- DELETE /api/tasks/:id

You are also encouraged to build:

- GET /api/tasks/:id

You can test that one pretty easily by pasting the URL in your browser

## Deployment

Just like last time, you can deploy the frontend to GitHub Pages, just as we've been doing. As always, ask a TA if you need help with that.

For the backend, we'll deploy to Vercel again. But since we're using a database now, we'll need to tell Vercel how to connect to that database. Vercel offers a connection to a free PostgreSQL server through a service called [Neon](https://vercel.com/marketplace/neon). You should be able to connect your deployed Express server to Neon PostgreSQL. I recommend trying this out early and reaching out for help if you get stuck.

Remember: Vercel will assign you a random (really long) public URL. If you want your frontend on GitHub Pages to make requests to that API instead of whatever is on http://localhost:8080, you may need to change the URLs in your React code.

## More Direction/Suggestions

The Sequelize starting point already has a structure set up for you, including a database connection file (`database/db.js`), and several files for defining your PostgreSQL tables and their relationships. There's also a seed file (`database/seed.js`), which you can run with `npm run seed`. As you build out the fields on your tables, you can re-run the seed file and confirm that the resulting data looks as expected.

Again, use [Postman](https://www.postman.com/)! It's a great way to send custom data to your API endpoints. This is especially true if you plan to implement some advanced features that don't yet have any corresponding frontend functionality built yet.

## Assignment

Complete the following.

- [ ] **Task has the appropriate fields (title, description, completed, user_id)**
- [ ] **POST /api/tasks creates a new task in the database**
- [ ] **PATCH /api/tasks/:id modifies an existing task in the database**
- [ ] **DELETE /api/tasks/:id deletes a task from the database**
- [ ] **GET /api/tasks retrieves all tasks from the database**
- [ ] **When invalid data is sent to the server, it responds with an informative status & message**

</br>

### BONUS

- [ ] POST /api/users creates a new user in the database
- [ ] GET /api/tasks/:id retrieves a single task from the database, including it's user
- [ ] GET /api/users/:id retrieves a single user from the database, including all it's tasks
- [ ] PATCH /api/users/:user_id/tasks/:task_id/assign assigns task with task_id to user with user_id
- [ ] PATCH /api/users/:user_id/tasks/:task_id/unassign unassigns task with task_id from user with user_id
- [ ] POST /api/tasks/bulk_complete accepts a request body with a list of task ids and marks them all complete
- [ ] Start editing the frontend repo, and just go nuts with it. With a working backend, you are unstoppable
