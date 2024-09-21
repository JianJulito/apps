1. Form Layout:
Login and Signup Forms: There are two forms, one for login and one for signup. You can switch between the forms by clicking the "Login" or "Signup" buttons.
Login Form: Collects email and password.
Signup Form: Collects email, password, and password confirmation.
2. Form Switching:
By clicking on the "Login" or "Signup" labels, the forms slide left or right to show the corresponding form.
3. Signup Form Behavior:
When a user submits the signup form, it checks if:
The passwords match.
The email already exists in localStorage (saved users).
If valid, the new user is saved, and the form resets.
4. Login Form Behavior:
When a user submits the login form, it checks the credentials against users stored in localStorage.
If the email and password are correct, the user is logged in and redirected to "shopping-list.html".
5. LocalStorage:
User details (email and password) are stored in localStorage so that the app can remember the users across sessions.
In summary, the script handles basic login and signup functions with client-side user storage and validation using localStorage.
2. Add items: A form lets users input details like product name, brand, price, weight, quantity, store, category, and image.
View items: The added items are displayed in two columns (one column on small screens).
Edit items: A SweetAlert modal pops up for editing an item’s details.
Delete items: Users can delete items with a confirmation prompt.
Sidebar menu: Contains links to a shopping list and logout.
Responsive design: The layout adjusts for mobile devices.
The data is stored locally in the browser using localStorage.

3.. Top Bar & Sidebar:
Top Bar: Contains a settings icon (fa-cogs) that toggles the sidebar.
Sidebar: A collapsible sidebar that includes links for adding items, and logging out.
2. Main Container:
Cart Icon: Displays a cart icon with a badge to show the number of items in the cart.
Search Bar: Allows users to search for items based on name, brand, or store.
Sort and Filter Options:
Users can sort items by name, price, brand, or store using a dropdown menu.
Users can filter items by category (e.g., Coffee, Fruits, Vegetables, Soft Drinks, Snacks) using another dropdown.
3. Grocery List Display:
The list of grocery items is displayed as a grid of item cards. Each card contains:
Product image, name, brand, store, weight, category, and price.
A checkbox to toggle whether an item is selected.
An "Add to Cart" button, with a cart icon (fa-cart-plus).
4. JavaScript Functions:
Sidebar Toggle: Functions toggleSidebar and closeSidebar control the visibility of the sidebar by adjusting its left position.
Filter by Category: The filterByCategory function filters items based on the selected category.
Search Items: The searchItems function dynamically filters the displayed items as the user types in the search bar.
Sort Items: The sortItems function sorts the grocery items based on the selected criteria (name, price, brand, or store).
Create Item Card: The createItemCard function generates the HTML for each grocery item card and displays it.
Display Items: The displayItems function manages the logic for filtering, searching, and displaying items.
Checkbox Toggle: The toggleCheck function handles the checkbox state for selecting/unselecting items.
5. LocalStorage:
Items are loaded from localStorage with the key items. The items are expected to be an array of objects where each object contains details like productName, brand, store, category, weight, price, and productImage.
6. Search and Sort:
When the search input changes, the searchItems function filters the items by checking if the search query matches the product name, brand, or store.
When a sorting option is selected, the sortItems function sorts the list of items by the chosen criteria (name, price, brand, or store).
7. Category Filtering:
The filterByCategory function allows users to view items by category, such as Coffee, Fruits, Vegetables, etc.
This code combines interactive features like search, sort, and filtering to create a responsive grocery list application with stored data from localStorage.
