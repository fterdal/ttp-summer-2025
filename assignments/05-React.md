# React I

- **Due** June 24, 2025 by 10:00:00 AM EDT
- **Submitting** Fill out all of the appropriate information in the Cohort Spreadsheet

## Goal

This is another exercise to deepen your understanding of HTML, CSS, JS, DOM manipulation, and now handling user events with React.

## Direction

This assignment has a Starting Point repo, which can be found [HERE](https://github.com/fterdal/React-Mini-StartingPoint). One person in your group should fork this repository and add the other members of the group as collaborators. Each member of the group should take an active role in committing and pushing to this forked repository.

You'll be re-doing part of the functionality of the DOM Challenges III (grid/row/column/color) assignment, but with React this time around. Instead of directly using the DOM API, you'll be managing state (hint: the currently selected color and the grid), writing methods within React components instead of standalone functions, and passing down event handlers to be fired off in the children components that have event listeners on them. The MVP (minimum viable product) features can be achieved with four components: App.jsx, Table.jsx, TableCell.jsx, TableRow.jsx.

The MVP features are: a user can add a row, a user can add a column, and a user can select a color to change a single cell via click. As a user, I can add a row, add a column, select a color from a dropdown menu of colors, and click on individual cells to color in the cell.

Stretch and optional features will be: recreating the entirety (clear the grid, fill the grid, fill uncolored cells, etc) of DOM Challenges III, but in React.

**Use this time to also do two things:**

1. Navigate to this extension for Google Chrome and install it: https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi?hl=en. This shows you the root React components that were rendered on the page, as well as the subcomponents that they ended up rendering. By selecting one of the components in the tree, you can inspect and edit its current props and state in the panel on the right. In the breadcrumbs you can inspect the selected component, the component that created it, the component that created that one, and so on. If you inspect a React element on the page using the regular Elements tab, then switch over to the React tab, that element will be automatically selected in the React tree.

2. Deploy this to GitHub Pages. Please refer to this link for guidance on this: https://codeburst.io/deploy-react-to-github-pages-to-create-an-amazing-website-42d8b09cd4d
   (debug as necessary)

## More Direction/Suggestions

- Remember to separate each component into it's own file and export that component. It will look something like this:

In `./src/components/table.jsx`:

```
const Table => () {...}
export default Table
```

In `./src/app.jsx`:

```
import Table from ./components/table
...
```

- app.jsx could maintain the state of the grid as well as the state of the selected color (stateful, class component)
- app.jsx could have methods (bound event handler functions) on the class which will be passed down to children components via props (the children components, will have event listeners that fire off the event handler functions
- app.jsx could render the dropdown menu as well as the Table Component
- Table.jsx could be the parent of TableRow.jsx
- TableRow.jsx could be the parent of TableCell.jsx

**The above are merely suggestions. Follow your intuitions and feel free to experiment.**

## Assignment

Complete the following user stories (bold denotes an MVP/mandatory feature, whereas italics denotes a stretch/optional feature):
As a user, I can:

- [ ] **add rows to the grid**
- [ ] **add columns to the grid**
- [ ] remove rows from the grid
- [ ] remove columns from the grid
- [ ] **select a color from a dropdown menu of colors**
- [ ] **click on a single cell, changing its color to the currently selected color**
- [ ] fill all uncolored cells with the currently selected color
- [ ] fill all cells with the currently selected color
- [ ] clear all cells/restore all cells to their original/initial color
- [ ] click and hold (mouseover) from a single cell (start) to a different cell (end) such that all affected/hovered-over cells from start to end change to the currently selected color
