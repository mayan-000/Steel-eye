Question 1:
  This simple list shows items passed in as props from parent.
  With each ListItem as a object of structure (items = [{text: string}]).
  Another thing is, when any of list item is clicked the color of clicked item changes to green, otherwise it will remain red.
  And if items prop is changed at any point, no listItem is considered selected.

Question 2: 

  a.) In Single List Item, 
      1.) onClick directly calls the Click Handler function, whereas reference of Click Handler is required.
      Due to direct call, onClick does not update selectedItem.

  b.) In List Component,
      1.) items props is by default null, so we need to check before creating a loop on items array. Due to no check, app breaks.
      2.) When looping items props, SingleListItem is called, while passing isSelected prop, one needs to pass bool, but integer is being passed. So we need to pass bool, to check whether the selectedIndex is equal to index of the item.
  c.) In List Component Prop Types,
      1.) It's not PropTypes.array, instead it needs to be PropTypes.arrayOf.
      2.) It's not PropTypes.shapeOf, instead it needs to be PropsTypes.shape.


Question 3:
  I have modified the code to work properly.
  Bugs have been removed.
  Updated file is persent in List.js file. 