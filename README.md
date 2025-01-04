# Fruits Array Project

A beginner-friendly project to practice basic HTML, CSS, and JavaScript. This interactive web app allows users to manage a list of fruits by adding or removing them dynamically.

## Features

- **View Fruits**: Displays an initial list of fruits.
- **Add a Fruit**: Users can type a fruit name and add it to the list.
- **Remove a Fruit**: Clicking on a fruit removes it from the list.

## Technologies Used

- **HTML**: Structure of the webpage.
- **CSS**: Minimal styling (optional, not included in the base project).
- **JavaScript**: Dynamic functionality like adding/removing fruits and updating the list.

## How to Use

1. Open `index.html` in any modern web browser.
2. **To Add a Fruit**:
   - Type the name of the fruit in the input field.
   - Click the "Add Fruit" button.
3. **To Remove a Fruit**:
   - Click on any fruit in the list to remove it.

## Code Overview

### HTML
- The structure includes:
  - A heading (`<h1>`) for the title.
  - An unordered list (`<ul>`) to display fruits.
  - An input box and button to add new fruits.

### JavaScript
- **Fruits Array**: Stores the list of fruits.
- **Functions**:
  - `renderFruits()`: Updates the fruit list on the page.
  - Event listeners handle adding and removing fruits dynamically.

### Example Code
Here’s a snippet to give you an idea:

```javascript
const fruits = ['Apple', 'Banana', 'Cherry', 'Date'];

function renderFruits() {
    const fruitList = document.getElementById('fruitList');
    fruitList.innerHTML = '';

    fruits.forEach((fruit, index) => {
        const li = document.createElement('li');
        li.textContent = fruit;

        li.addEventListener('click', function() {
            fruits.splice(index, 1);
            renderFruits();
        });

        fruitList.appendChild(li);
    });
}

