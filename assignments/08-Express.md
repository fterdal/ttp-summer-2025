# REST & Express

- **Due** June 27, 2025 by 10:00:00 AM EDT
- **Submitting** Fill out all of the appropriate information in the Cohort Spreadsheet

## Goal

Learn the basics of Express.js, how to create API routes, and connect it to a React app.

## Direction

This assignment has TWO Starting Point repos, one for the [Backend (Express)](https://github.com/fterdal/Express-Intro-StartingPoint), and another for the [Frontend (React)](https://github.com/fterdal/Express-Intro-Frontend).

One person in your group should fork these repositories and add the other members of the group as collaborators to both of them.

You'll be implementing a simple task management app. Users should be able to view tasks, create new tasks, mark them as complete or incomplete, and delete tasks.

The frontend is already built out for you! You'll see React components for listing the tasks, filtering out by complete or incomplete, and creating new tasks. Go spend some time reviewing the frontend code as a team, and make sure you understand the API routes that the frontend requires. Unfortunately, the components are making requests to endpoints that _do not yet exist_. That's where you come in!

You should be able to complete all of the basic functionality without editing the frontend at all. If you want to go for some of the stretch goals, you're welcome to modify the frontent to your heart's content.

We'll need routes for retrieving all the tasks, deleting a task based on its id, creating a new task, and editing a task (e/g/ toggling the "complete" status).

## Deployment

You can deploy the frontend to GitHub Pages, just as we've been doing. As always, ask a TA if you need help with that.

For the backend, GitHub Pages isn't gonna cut it. Fortuntely, there's a hosting platform called Vercel that has a fairly generous Free plan. The starting point for the Backend repo already has a vercel.json configuration file, so you should be able to create a Vercel account, connect your GitHub, and add the GitHub repo as a project on Vercel. From then on, every time you push a new commit to main, your deployed app will re-deploy!

Vercel will assign you a random (really long) public URL. If you want your frontend on GitHub Pages to make requyests to that API instead of whatever is on http://localhost:8080, you may need to change the URLs in your React code.

## More Direction/Suggestions

The Express starting point already has a structure set up for you, including several types of Express middleware (e.g. cors, static file serving middleware, logging). Take a look at `app.js` to see more details.

You will also want to look at `api/tasks.js`, which would be a great place to add some new API routes.

Finally, take a look at `dummy-database.js`. We're not working with a real database just yet (that's coming soon!). In the meantime, we're gonna fake it. Since this isn't a real database, all of the data we add or modify will be reset every time our Express app restarts (which will happen every time we save a file). In other words, our data is not _persistent_. Nevertheless, review the dummy database and see if there are some methods that may come in handy (e.g. `Task.findAll()`).

Use [Postman](https://www.postman.com/)! It's a great way to send custom data to your API endpoints. This is especially true if you plan to implement some advanced features that don't yet have any corresponding frontend functionality built yet.

## Assignment

Complete the following user stories.

As a user, I can:

- [ ] **view the list of tasks**
- [ ] **submit the AddTask form and see the new task appear in the list**
- [ ] **Click the trash can icon on a task and confirm that it's deleted**
- [ ] **Toggle a task's completed status by clicking on the ✅ or 🔄**

</br>

### BONUS

These are just endpoints that don't have any UI built out for them yet. It's a great chance to use Postman to confirm functionality! If you're feeling _extra ambitious_, you can also go modify the frontend code and create that functinoality.

- [ ] GET /api/tasks/:id -> get the task with id
- [ ] GET /api/users/:id/tasks -> get all the tasks assigned to the user with id
- [ ] POST /api/users -> create a new user
- [ ] DELETE /api/users/:id -> delete the user with id and then also delete all of their tasks
- [ ] PATCH /api/users/:id -> modify the user with id
