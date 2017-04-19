# optimization-project
optimizing the critical rendering path

To Run The Application
1.open the app in the browser.
2.It is a pizza application where you can choose a pizza of your choice.
3.Menu,ingredients used,location and contact has also been provided.
4.Also you can select the size of pizza required

Optimization done in index.html
1. The css was inlined.
2. Media attribute was added to print.css as it should not block rendering.
3. Async was used with scripts which were not performing dom manipulations as they should also not block rendering.
4. All the images were compressed,The images were of very large size so they were compressed.

Optimization done in main.js
1. InchangePizzaSizes function code was modified to remove forced synchronous layout problem.code was refactored so that jankiness was removed while changing 
the size of the pizza.


2. In updatePositions function the operations on dom were done outside the loop so as to reduce rendering time.Also in
document.addEventListener('DOMContentLoaded') function number of iterations were reduced.as number of sliding pizza's were too many and this was also calling the dom 
again and again.

