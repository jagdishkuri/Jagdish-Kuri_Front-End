# Jagdish-Kuri_Front-End
The List component is a simple list that renders an array of items, each represented as a SingleListItem. The SingleListItem component takes in index, isSelected, onClickHandler, and text props and returns a li element with a background color of either green or red depending on whether it is selected or not.

One problem with the code is that setSelectedIndex should just be setSelectedIndex in the WrappedListComponent, as it is a function returned by the useState hook. Another issue is that isSelected in the WrappedSingleListItem should be a Boolean value but is instead a reference to the selectedIndex state variable.

Additionally, the items prop should have a default value of an empty array instead of null, and the array and shapeOf PropTypes should be PropTypes.arrayOf and PropTypes.shape, respectively.
