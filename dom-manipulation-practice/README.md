# DOM Manipulation Practice

This module demonstrates the step-by-step evolution of handling user click events, managing state, and animating elements.

## Progression Roadmap

### [1. Smooth CSS Transitions](./index1-animation.html)
* **Core Concept:** Moving inline JavaScript into a function and applying `transition` properties.
* **Key Learning:** Learned how `linear` timing ensures uniform animation speed compared to `ease`.

### [2. Reset Functionality](./index2-reset.html)
* **Core Concept:** Managing element states by adding a secondary control action.
* **Key Learning:** Clearing inline styles by assigning an empty string (`''`), forcing the element to efficiently inherit default CSS stylesheet rules.

### [3. Targeting Multiple Elements](./index3-multiple.html)
* **Core Concept:** Transitioning from specific target IDs to shared component classes.
* **Key Learning:** Utilizing `document.querySelectorAll()` to gather a NodeList collection, and applying style changes sequentially via a `.forEach()` loop.
### [4. DOM Selectors](./index4-selectors.html)
* **Core Concept:** Finding element nodes using specific unique IDs versus flexible CSS selector queries.
* **Key Learning:** Differentiated between `getElementById` (single element), `querySelector` (first match using CSS syntax), and `querySelectorAll` (NodeList collection target).

### [5. Text & Content Injection](./index5-text-content.html)
* **Core Concept:** Extracting and injecting layout text versus operational HTML markup.
* **Key Learning:** Mastered the CSS awareness distinction between `innerText` and `textContent`, and analyzed the Cross-Site Scripting (XSS) vulnerability risks of using `innerHTML`.

### [6. Dynamic Styling via Class Lists](./index6-classes.html)
* **Core Concept:** Managing visual states through structural CSS classes instead of inline adjustments.
* **Key Learning:** Mastered the `classList` API methods (`add`, `remove`, `toggle`) and used `.contains()` for precise programmatic state verification.





