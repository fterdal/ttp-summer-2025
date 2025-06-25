# React II: Forms

- **Due** June 26, 2025 by 10:00:00 AM EDT
- **Submitting** Fill out all of the appropriate information in the Cohort Spreadsheet

## Goal

This is another exercise to deepen your understanding of React. We'll be exploring forms!

## Direction

This assignment has a Starting Point repo, which can be found [HERE](https://github.com/fterdal/React-2-Forms). One person in your group should fork this repository and add the other members of the group as collaborators. Each member of the group should take an active role in committing and pushing to this forked repository.

You'll be implementing a book reviewing app, similar to Goodreads or StoryGraph. The basic functionality will include creating a new book, and viewing a list of the books that have been created, all on the same page. Optionally, you may want to add a search bar, to filter the book list in various ways.

Each book should have the following fields:

A book should have the following fields:

- title (required)
- author (required)
- image (optional, url)
- publishedDate (optional, datetime)
- description (optional, text)
- rating (number, 1-5)
- category (optional, dropdown with options: fiction, non-fiction, poetry, drama, biography, history, science, technology, art, music, travel, cooking, gardening, etc.)
- isRead (boolean, default false)
- isFavorite (boolean, default false)

As the user is filling out the NewBook form, they should not be able to submit the form unless the required fields are filled in, and the validations are met (e.g. the rating is valid).

If they successfully submit the NewBook form, they should see their new book appear in the book list immediately

**Don't forget to deploy to GitHub Pages!**

## More Direction/Suggestions

The starting point has a few blank components already: AddBook, BookCard, BookList. You don't have to use these components, but you should at least think about how you want to break your project up into components.

Consider where you want to keep the books state. You'll need to update the books state from AddBook. And BookList will need to receive any changes to the books state.

If you want to test out your book list component before you're finished with the AddBook, consider adding in some dummy data.

There are a lot of fields on each book. Start small, make a form that only takes in title, and make sure that it works. Then start adding in additional fields to ramp up complexity.

**The above are merely suggestions. Follow your intuitions and feel free to experiment.**

## Assignment

Complete the following user stories.

As a user, I can:

- [ ] **view the list of books**
- [ ] **submit the AddBook form and see the new book appear in the list**
- [ ] **not submit the form if there are validation errors**
- [ ] **see that each book has the correct fields (see above)**

</br>

### BONUS

- [ ] see the validation errors that prevent form submission
- [ ] use a search bar to filter books in various ways (e.g. category, isRead, author)
