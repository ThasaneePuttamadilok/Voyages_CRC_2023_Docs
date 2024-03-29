# getOptionsFlatObject

### Slice Configuration
```getOptionsFlatObject```: The getOptionsFlatObjSlice data includes information about different filter objects, such as the variable name, type, label, and flatable. This data is used to display the filter options in the top navigation bar, allowing users to search for specific information within the application. The filter options are also displayed in the menu bar and menu list.

```getOptionsFlatObjSlice```: The getOptionsFlatObjSlice is configured using the createSlice function from the @reduxjs/toolkit package. It defines the following properties:
- `name`: The name of the slice is set to "optionFlatMenu".
- `initialState`: The initial state of the slice includes one property:
    - `value` it calls jsonData from transatlantic_voyages_filter_menuTEST.json

`Actions`
The ggetOptionsFlatObject slice defines the following actions:

- `getOptionsFlatMenu`: Accepts a payload and updates the initialState property in the state with the provided value.

To use these actions, import them from `getOptionsFlatMenu` and dispatch them as needed to modify the state.

``Reducer``

The reducer function for getOptionsDataSlice is automatically generated by the createSlice function. It handles state updates based on the dispatched actions and returns the updated state.

## Usage
To use the getOptionsDataSlice in other parts of the application, follow these steps:

1) Import the necessary actions and the reducer function from getOptionsDataSlice.
2) Dispatch the actions (getOptionsFlatMenu) when needed, providing the appropriate payload values.

Example usage:


```jsx
import { getOptionsFlatMenu} from './path/to/getOptionsFlatObjSlice';
import { useDispatch, useSelector } from 'react-redux';

// Inside a component
const dispatch = useDispatch();

// Dispatching the actions
dispatch(getOptionsFlatMenu({...value}));

// Accessing the state
const menuOptionFlat: VoyagaesFilterMenu = useSelector((state: RootState) => state.optionFlatMenu.value);


```



## Additional Information
Ensure that you have the required dependencies installed and properly configured before using this code. This code is intended to be used in a Redux-based application for managing data list values. Refer to the Redux documentation for more details on incorporating this slice into your Redux store.

Feel free to modify the initial state, actions, and reducer based on your specific requirements.

Note: Make sure to adjust the import paths according to your project structure.
