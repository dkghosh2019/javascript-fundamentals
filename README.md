# JavaScript Fundamentals

A comprehensive, structured repository documenting my journey through core JavaScript programming, DOM manipulation, and problem-solving concepts. This archive serves as both a learning log and a practical technical interview preparation toolkit.

## Repository Architecture

Each directory is a self-contained module focused on a specific core concept, featuring step-by-step code files and dedicated documentation.

* **[DOM Manipulation Practice](./dom-manipulation-practice)** — Covers event handling, element styling, node iteration (`querySelectorAll`/`forEach`), state resets, and CSS transition integration.

## Interview Cheat Sheets & Takeaways
* **Operator Precedence:** Be cautious with inline HTML attribute scripts; operators like `&&` evaluate expressions logically rather than executing separate assignments sequentially. Always default to semi-colons `;` or standalone functions.
* **Batch Operations:** DOM lists fetched via `querySelectorAll` are returned as a non-live NodeList. Iteration via methods like `.forEach()` is required to update individual element nodes.
* **Inline Style Resets:** Assigning an empty string (`element.style.property = ''`) deletes the inline style declaration, triggering an efficient fallback to standard external stylesheet rules.
