# Assignment 6.1 — Box Model Inspection

## Files
- `index.html` — Main inspection page with three example boxes and an interactive sizing toggle.
- `css/style.css` — External CSS showing different padding, border, margin, and box-sizing values.
- `js/script.js` — Lets you switch between `content-box` and `border-box`.
- `screenshots/box-model-annotated.png` — Annotated diagram for content, padding, border, and margin.

## Run the project
1. Extract the ZIP file.
2. Open this folder in VS Code.
3. Open `index.html` with Live Server or in Chrome.
4. Use the buttons to switch between `content-box` and `border-box`.

## Chrome DevTools screenshot task
1. Open the page in Chrome.
2. Right-click one of the three cards and select **Inspect**.
3. In DevTools, select the card element and open the **Computed** tab.
4. Find the Box Model diagram. Hover each section to see it highlighted on the page.
5. Take a screenshot using the operating system screenshot tool. Keep the element and Box Model diagram visible.
6. Add labels or arrows for Content, Padding, Border, and Margin if your teacher specifically requires a screenshot from DevTools.

## Explanation
The CSS box model describes the space used by an HTML element. Content is the text or other material inside the element. Padding is the space between content and the border. The border surrounds the padding and content. Margin is the outer space that separates the element from other elements. With `content-box`, the declared width applies only to content; with `border-box`, the declared width includes content, padding, and border.

## Important note
The included annotated image is a labelled educational diagram. It is not a screenshot captured from Chrome DevTools. Capture your own DevTools screenshot using the steps above if your instructor requires an actual browser screenshot.
