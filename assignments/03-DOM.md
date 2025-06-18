# DOM Challenges I

- **Due** June 20, 2025 by 10:00:00 AM EDT
- **Submitting** Fill out all of the appropriate information in the Google Sheet

## Goal

Demonstrate understanding of DOM traversal and DOM manipulation. Build familiarity with JS syntax. Look into: getElementById, querySelector, getElementsByClassName, querySelectorAll, the innerText property, classList.add, className, classList.remove, createElement, appendChild. Section off the code with comments based on the particular part of the prompt you are addressing.
Hint:
In a separate `script.js` file within the same repository (this repository holds `index.html` and `script.js`), include your answers like in the example below. Push this solo assignment in your bootcamp directory/repository on your GitHub.

```
// 1 - Select the section with an id of container without using querySelector.
document.getElementById("container");
```

## Direction

For this assignment, there is a starting point GitHub repo, which you can view [HERE](https://github.com/fterdal/DOM-1-StartingPoint). One person in your group should fork the repository and add the other members as collaborators (see the StartingPoint's README for details).

This is an exercise that will help get you acclimated to the DOM API. For each individual prompt, write out the code necessary to achieve the particular task at hand. Test it out, and then move forward. If you encounter a situation where you can use a previous prompt's solution for the one you are currently working on, feel free to keep it DRY (Do-Not-Repeat-Yourself) and leverage that reusable code. By the same token, if you encounter a situation where a previous prompt's solution is a blocker (gets in the way of what you are trying to achieve at the moment), then prioritize the current prompt. You can comment out the code that's blocking, test out the current code that you are working on, and after verifying that it works you can comment back in the previous code. In this way, you'll be treating each prompt as an individual, distinct task. The primary point is to become more familiar with the DOM methods that allow you to interact and manipulate the Document Object Model.

## Assignment

Complete and submit the following tasks based on the index.html file found in the StartingPoint repo.

Write the code necessary to do the following:

- [ ] Select the section with an id of container without using querySelector.
- [ ] Select the section with an id of container using querySelector.
- [ ] Select all of the list items with a class of "second".
- [ ] Select a list item with a class of third, but only the list item inside of the ol tag.
- [ ] Give the section with an id of container the text "Hello!".
- [ ] Add the class main to the div with a class of footer.
- [ ] Remove the class main on the div with a class of footer.
- [ ] Create a new li element.
- [ ] Give the li the text "four".
- [ ] Append the li to the ul element.
- [ ] Loop over all of the lis inside the ol tag and give them a background color of "green".
- [ ] Remove the div with a class of footer.

## BONUS

If you finish the above tasks early and want an extra challenge, do the following:

1. In the starting point repo, you'll find a bonus.html and bonus-script.js
2. The bonus.html only contains a div with an id of root
3. Note that when you view bonus.html in the browser, you see an h1 tag! This is because the bonus-script.js is adding that h1 tag _after the page loads_.

Your mission, should you choose to accept it, is to create an entire web page using only that bonus-script.js file. Add new elements, style them, add content. The website can be about anything you like. Make it look pretty ✨💅

As you'll see in bonus-script.js, `document.createElement()` and `document.appendChild()` are your best friends.
