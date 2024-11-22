# MAST-FINAL-POE
https://youtube.com/shorts/quyXKOsaQ7c?si=IMohF6aJ5oR-Ohen
Change Log
Project: Menu Management App
Date: 22 November 24'
Features Added
1. Home Screen Displays Average Prices
Added functionality to calculate and display the average price of menu items for Starters, Mains, and Desserts in a row layout.
Styled the display for better readability using flexDirection: 'row'.
2. Separate Screen for Adding and Removing Menu Items
Moved the "Add Menu Items" feature to a new separate screen: AddMenuScreen.tsx.
Implemented functionality to remove menu items directly from AddMenuScreen.
Added a FlatList to display all menu items with "Remove" buttons next to each item.
Synced the menuItems state with HomeScreen to ensure changes persist.
3. Filter Menu Items
Created a new screen (FilterMenuScreen.tsx) to filter menu items by course (Starters, Mains, Desserts).
Added custom-styled filter buttons with:
Active state highlighting the selected filter.
A "Clear Filter" button to reset the filter.
Bugs Fixed
1. Menu Items Not Transferring Between Screens
Fixed an issue where menuItems was not transferring between AddMenuScreen and HomeScreen.
Used route.params to pass menuItems between screens and ensured state updates persist.
2. Duplicate Item Addition
Cleared route.params after adding an item to prevent duplicate entries when navigating between screens.
3. Empty List Display in AddMenuScreen
Resolved the issue where menu items were not displaying in AddMenuScreen.
Properly synced menuItems state with the data passed via navigation.
UI Enhancements
1. Picker Customization
Changed the text color and background styling for the Picker component in AddMenuScreen.
2. Button Colors for FilterMenu
Styled filter buttons with distinct colors:
Default filter buttons: Blue.
Active filter button: Green.
Clear filter button: Red.
Files Modified
1. AddMenuScreen.tsx
Added menuItems display and "Remove" functionality.
Updated navigation to sync menuItems with HomeScreen.
2. HomeScreen.tsx
Added logic to receive updated menuItems from AddMenuScreen.
Displayed average prices in a row layout.
3. FilterMenuScreen.tsx
Implemented filtering by course with a styled button interface.
4. App.tsx
Verified proper screen navigation and data passing between HomeScreen, AddMenuScreen, and FilterMenuScreen.
5. types.ts
Updated RootStackParamList to ensure proper type checking for menuItems across all screens.
Outstanding Work
Add persistent storage (e.g., using AsyncStorage) for menu items to ensure they remain available across app restarts.
Improve error handling for edge cases (e.g., invalid price inputs).
