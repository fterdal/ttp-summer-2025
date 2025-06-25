# React II

- **Due** June 26, 2025 by 10:00:00 AM EDT
- **Submitting** Fill out all of the appropriate information in the Cohort Spreadsheet

## Goal

This is another exercise to deepen your understanding of React. We'll be exploring client side routing, and form submission.

## Direction

This assignment has a Starting Point repo, which can be found [HERE](https://github.com/fterdal/React-Next-Starter). One person in your group should fork this repository and add the other members of the group as collaborators. Each member of the group should take an active role in committing and pushing to this forked repository.

You'll notice that this starting point has a lot more boilerplate than previous assignments. This starting point uses [Next.js](https://nextjs.org/), a popular React framework. For right now, all we care about is using Next.js for routing purposes.

You'll be implementing a book reviewing app, similar to Goodreads or StoryGraph. The basic functionality will include creating a new book, viewing a list of the books that have been created (just the titles), and viewing the details of a single book (all the fields about that book).

Each book should have the following fields:

- Title (required)
- Author (required)
- Rating (required, number between 0 and 5)
- Blurb (optional)
- Image (optional)

There should be at least four distinct routes:

- Homepage /
- BookList /books
- BookDetail /books/[id]
- NewBook /books/new

As the user is filling out the NewBook form, they should not be able to submit the form unless the required fields are filled in, and the validations are met (e.g. the rating is valid).

If they successfully submit the NewBook form, they should automatically be redirected to the BookList, where they should see their new book.

**NOTE:** At this point, you may notice that any new books you add are erased whenever you refresh the page. That's normal. We'll fix that tomorrow!

There should also be a navbar at the top of the screen with buttons including Home, Books, and NewBook

Stretch and optional features include: The user can add reviews on a book, which include a star rating and a brief comment

**Don't forget to deploy!**

Deploy this on Vercel. Deployment on Vercel ought to be even easier than on GitHub Pages Please refer to this link for guidance on this: https://vercel.com/new?utm_source=create-next-app&utm_medium=appdir-template&utm_campaign=create-next-app. Consult the documentation and reach out if you get stuck.

## More Direction/Suggestions

Note that the starting point already includes an example of routing for /posts. Each new route is a new folder, and each page within that folder is named page.js. **The names are important!** If you do not name your component "page.js" and put it in the correct folder, it will not be at the route you expect. Use the provided "posts" example as inspiration and go from there.

Also, pay attention to `app/layout.js`. Note that there is a Context provider for Posts. Layout is our root component, it's the parent of all our React components, and it can keep track of our application state (e.g. posts or books) even when the user navigates between different routes. Note that the PostDetail component is able to access this state with `useContext(PostsContext)`.

You may want to create your own Context provider, and pass it down to the new components you create. Feel free to copy this same pattern, and adjust as needed. For instance, yours may look like this:

```
<PostsContext.Provider value={{ posts, setPosts }}>
  <BooksContext.Provider value={{ books, setBooks }}>
    {children}
  </BooksContext.Provider>
</PostsContext.Provider>
```

If you want to test out the BookList page before you've written your form, I suggest creating some dummy data:

```
const dummyBooks = [{id: 1, title: 'The Hobbit', ...}, {id: 2, title: 'Emma', ...}, ...]
const [books, setBooks] = useState(dummyBooks)
```

**The above are merely suggestions. Follow your intuitions and feel free to experiment.**

## Assignment

Complete the following user stories.

As a user, I can:

- [ ] **visit /books to see a list of the books**
- [ ] **visit /books/1 to see a single book**
- [ ] **visit /books/new to see a CreateBook form**
- [ ] **use a navbar at the top with links to home, booklist, and new book**
- [ ] **view the application deployed on Vercel**
- [ ] **see that each book has these fields: title (required), author (required), blurb, rating (0-5)**
- [ ] **see validation errors on the CreateBook form**
- [ ] **submit the CreateBook form and be redirected to /books**
- [ ] **submit the CreateBook form which creates a new book**

</br>

### BONUS

- [ ] implement a search feature on the book list page
- [ ] on the book details page, see a list of reviews
- [ ] on the book details page, there's a form you can fill out that adds a new review
- [ ] instead of entering the rating for a book manually, the book's rating is calculated as the average of all review ratings
