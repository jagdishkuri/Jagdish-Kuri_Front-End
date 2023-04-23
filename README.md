# Jagdish-Kuri_Front-End
The List component is a simple list that renders an array of items, each represented as a SingleListItem. The SingleListItem component takes in index, isSelected, onClickHandler, and text props and returns a li element with a background color of either green or red depending on whether it is selected or not.
There are a few problems and warnings in the code that need to be addressed:

In the WrappedSingleListItem component, the onClickHandler function is called immediately instead of being passed as a callback function. This will cause the function to be executed every time the component is rendered, which is not the intended behavior. To fix this, the onClickHandler function should be passed as a callback function as follows:
onClick={() => onClickHandler(index)}

In the WrappedListComponent component, the isSelected prop is being set to the selectedIndex state value. However, selectedIndex is a number that is initialized to undefined, which is not a valid prop value for the isSelected prop of the WrappedSingleListItem component. Instead, the isSelected prop should be set to a boolean value indicating whether the current item is selected or not. To fix this, the isSelected prop should be set as follows:
isSelected={selectedIndex === index}

The PropTypes.shapeOf() method used in the propTypes declaration for the items prop is invalid. The correct method name is PropTypes.shape(). The corrected propTypes declaration should look like this:
items: PropTypes.arrayOf(
  PropTypes.shape({
    text: PropTypes.string.isRequired,
  })
)
