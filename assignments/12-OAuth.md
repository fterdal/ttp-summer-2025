# 🤝 OAuth

- **Due** July 9, 2025 by 10:00:00 AM EDT
- **Submitting** Fill out all of the appropriate information in the Cohort Spreadsheet

## Goals:

- Understand the basic OAuth flow
- Practice setting up an Auth0 account
- Use OAuth access tokens to act on the user's behalf

## Direction

This assignment has two starting point repos, one for the [Backend](https://github.com/fterdal/OAuth-Backend-Starter) and one for the [Frontend](https://github.com/fterdal/OAuth-Frontend-Starter). You should take some time reviewing the changes made to these repos compared with the previous assignment.

In particular, our React app has functionality for sending user account credentials for a traditional login process. But it also allows users to authenticate with an Auth0 provider.

```
const App = () => {
  return (
    <Auth0Provider {...auth0Config}>
      <Router>
        <AppContent />
      </Router>
    </Auth0Provider>
  );
};
```

If you run the app as-is, it will not work. That's because it's expecting a `.env` file with several environment variables in it.
You can look at `.env.example` for an example of what those values should look like. You'll need to create an Auth0 account to find the appropriate values.

When you are creating your account, you'll want to go to the Marketplace tab, add GitHub, and then add it to your new project. You'll be asked what kind of access you'll need for the user's GitHub: you should at least have their email address. Look at the various scopes and see what they enable. (HINT: You'll probably want access to the repo scope.)

<img width="978" alt="Screenshot 2025-07-08 at 12 17 29 AM" src="https://github.com/user-attachments/assets/25d1f13e-e022-4957-84c5-8f0a750f1418" />

You'll know you have it set up when you can click "Login with Auth0" and be redirected to an Auth0 page where you can successfully connect with Google or GitHub.

## Deployment

For this assignment, don't worry about deployment. Each member of your team should be able to run the application locally, and should have their own individual Auth0 account and distinct .env file.

## Assignment

Your goal should be to play around with your new GitHub OAuth credentials. You can even branch out and add additional OAuth providers, such as Spotify. You should be looking through the GitHub API documentation (e.g. [how to retrieve commits](https://docs.github.com/en/rest/commits/commits?apiVersion=2022-11-28))

Complete the following.

- [ ] **Users should be able to sign up with their GitHub account**
- [ ] **After they log in, they are greeted with their basic GitHub information: full name, photo**
- [ ] **Users can log out securely**
- [ ] **Users can view a list of their GitHub repos**
- [ ] **Users can click on a GitHub repo and see a list of the commits on that repo (e.g. timestamp, committer, message)**
