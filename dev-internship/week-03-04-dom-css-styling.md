# Week 3-4: DOM, CSS & Modern Styling

> [!IMPORTANT]
> **DO NOT** use AI tools to write code for you. You come here to **LEARN**, the goal of this program is to build
> your programming skills through **hands-on** practice. AI assistants can help explain
> concepts or debug issues, but writing the code yourself is **essential** for learning.

---

|                 |                                                                                                                        |
| :-------------- | :--------------------------------------------------------------------------------------------------------------------- |
| Learning Topics | DOM fundamentals, DOM manipulation, Event handling, CSS fundamentals, Flexbox, CSS Grid, Responsive design, TailwindCSS |
| Objectives      | Master DOM manipulation, Complete CSS games, Build interactive FreshCart clone with TailwindCSS and vanilla JavaScript |

## DOM Fundamentals (Days 1-4)

### Understanding the DOM
- Read [MDN: Introduction to the DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction)
- What is the DOM and how browsers create it
- DOM tree structure: nodes, elements, and text
- The document object and window object

### DOM Selection Methods
```javascript
// Element selection methods
document.getElementById('myId')
document.getElementsByClassName('myClass')
document.getElementsByTagName('div')
document.querySelector('.myClass')  // Returns first match
document.querySelectorAll('.myClass')  // Returns all matches

// Traversing the DOM
element.parentElement
element.children
element.firstElementChild
element.lastElementChild
element.nextElementSibling
element.previousElementSibling
```

### DOM Manipulation
```javascript
// Creating elements
const newDiv = document.createElement('div')
newDiv.textContent = 'Hello World'
newDiv.className = 'my-class'
newDiv.id = 'my-id'

// Adding/removing elements
parent.appendChild(newDiv)
parent.insertBefore(newDiv, referenceNode)
parent.removeChild(childNode)
element.remove()  // Modern approach

// Modifying attributes
element.setAttribute('data-id', '123')
element.getAttribute('data-id')
element.removeAttribute('data-id')

// Modifying styles
element.style.color = 'red'
element.style.backgroundColor = 'blue'
element.classList.add('active')
element.classList.remove('active')
element.classList.toggle('active')
element.classList.contains('active')
```

### Event Handling
```javascript
// Adding event listeners
button.addEventListener('click', function(event) {
  console.log('Button clicked!')
})

// Common events
// Mouse: click, dblclick, mouseenter, mouseleave, mousemove
// Keyboard: keydown, keyup, keypress
// Form: submit, change, input, focus, blur
// Window: load, resize, scroll

// Event object
element.addEventListener('click', function(event) {
  event.preventDefault()  // Prevent default behavior
  event.stopPropagation()  // Stop event bubbling
  console.log(event.target)  // Element that triggered the event
  console.log(event.currentTarget)  // Element with the listener
})

// Event delegation
document.getElementById('parent').addEventListener('click', function(event) {
  if (event.target.matches('.child-button')) {
    console.log('Child button clicked!')
  }
})
```

## Assignment 1: DOM Manipulation

Build an Interactive Todo List using vanilla JavaScript (no CSS needed):

- [ ] Add new todos with input field and button
- [ ] Mark todos as complete (strike-through styling)
- [ ] Delete todos with confirmation
- [ ] Filter todos (all, active, completed)
- [ ] Save todos to localStorage
- [ ] Count of remaining todos
- [ ] Deploy to GitHub Pages


## CSS Fundamentals (Days 5-7)

> [!NOTE]
> If you're already familiar with CSS basics, feel free to skip this section and jump straight to Flexbox & Grid.

1. Complete the [W3Schools CSS Tutorial](https://www.w3schools.com/css/default.asp) — covers all the basics from selectors to layout
2. Key topics to focus on:
   - Selectors & Specificity
   - The Box Model (`content`, `padding`, `border`, `margin`, `box-sizing`)
   - Display & Positioning (`block`, `inline`, `inline-block`, `static`, `relative`, `absolute`, `fixed`, `sticky`)
   - Colors, Typography & Units (`px`, `em`, `rem`, `%`, `vw`/`vh`)
   - Responsive design basics (media queries)
3. Complete all levels at [CSS Diner](https://flukeout.github.io/) — interactive CSS selectors practice

### Additional Resources
- [web.dev Learn CSS](https://web.dev/learn/css) — structured learning path by Google
- [MDN CSS First Steps](https://developer.mozilla.org/en-US/docs/Learn/CSS/First_steps) — in-depth reference

## Flexbox & Grid
1. Complete all levels at [Flexbox Froggy](https://flexboxfroggy.com/)
2. Complete all levels at [Grid Garden](https://codepip.com/games/grid-garden/)

## TailwindCSS

1. Learn [TailwindCSS](https://tailwindcss.com/docs). (Read through all **Core Concepts** to understand the framework)
2. Set up TailwindCSS in a project
3. Learn utility classes:
   - Layout & Spacing
   - Colors & Typography
   - Flexbox & Grid utilities

## Assignment 2: FreshCart Site

Build [FreshCart Site](https://freshcart-template.codescandy.com/) with interactivity:
- [ ] Build fully responsive design with TailwindCSS
- [ ] Deploy to GitHub Pages

---

[← Back to Overview](./README.md) | [Previous: Week 1-2](./week-01-02-javascript-typescript.md) | [Next: Week 5-6 →](./week-05-06-build-tools.md)
