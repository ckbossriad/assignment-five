1. What is the difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll?

**ans:**
getElementById

This one is the simplest.Give it an id and it gives back that one element. IDs are supposed to be unique, so you’ll only ever get one thing.
Think of it like calling someone by their exact name:
"Hey, Rahim!" -> only one Rahim will answer.

2. How do you create and insert a new element into the DOM?

**ans:**
To create and insert a new element into the DOM:
Create the element (make it in memory).
Add content/attributes to it (like text, class, id).
Insert it into the page (using append, prepend, before, or after).

3. What is Event Bubbling and how does it work?

**ans:**
Event bubbling means when I click on an element, the event doesn’t just stay there. It first happens on that element, then it slowly moves up to its parent, then the parent’s parent, and so on until it reaches the top of the page.

It’s like the click starts small and then bubbles upward through all the containers.

So basically → click child -> parent -> grandparent-> document.
4. What is Event Delegation in JavaScript? Why is it useful?

**ans:**
Event delegation is when instead of adding event listeners to a bunch of child elements one by one, I just put the event listener on their parent. Because of event bubbling, the event will still “bubble up” to the parent, and I can check which child was actually clicked.

It’s useful because:

I don’t need to attach listeners to every single element.

It saves memory and makes the code cleaner.

It also works for elements that are added later (dynamically), since the parent is still listening.

5. What is the difference between preventDefault() and stopPropagation() methods?

**ans:**
preventDefault() and stopPropagation() are not the same thing.

preventDefault() -> This is used when I want to stop the browser’s default action. For example, clicking a link normally takes me to another page — if I call preventDefault(), it won’t go anywhere. Same for form submission, right-click menu, etc.

stopPropagation() -> This is used to stop the event from bubbling up to parent elements. Like if I click a button inside a div, normally the click goes to the button and then the div. But if I call stopPropagation(), it will stop right there at the button.