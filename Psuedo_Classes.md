
---

### **1. State-based Pseudo-classes**  
Apply styles based on user interaction or element state.

| Pseudo-class | Example | Description |
|-------------|---------|-------------|
| `:hover` | `a:hover { color: red; }` | Styles when mouse hovers over an element. |
| `:active` | `button:active { background: blue; }` | Styles while an element is being clicked. |
| `:focus` | `input:focus { border-color: green; }` | Styles when an element (like `<input>`) is focused. |
| `:visited` | `a:visited { color: purple; }` | Styles visited links. |
| `:link` | `a:link { color: blue; }` | Styles unvisited links. |
| `:checked` | `input[type="checkbox"]:checked { background: yellow; }` | Styles checked checkboxes/radio buttons. |
| `:disabled` | `input:disabled { opacity: 0.5; }` | Styles disabled form elements. |
| `:enabled` | `input:enabled { border: 1px solid black; }` | Styles enabled form elements. |
| `:required` | `input:required { border: 1px solid red; }` | Styles required form fields. |
| `:optional` | `input:optional { border: 1px solid gray; }` | Styles optional form fields. |
| `:valid` | `input:valid { border-color: green; }` | Styles inputs with valid content. |
| `:invalid` | `input:invalid { border-color: red; }` | Styles inputs with invalid content. |
| `:in-range` | `input[type="number"]:in-range { color: green; }` | Styles number inputs within range. |
| `:out-of-range` | `input[type="number"]:out-of-range { color: red; }` | Styles number inputs outside range. |

---

### **2. Structural Pseudo-classes**  
Target elements based on their position in the DOM.

| Pseudo-class | Example | Description |
|-------------|---------|-------------|
| `:first-child` | `li:first-child { font-weight: bold; }` | Styles the **first child** of a parent. |
| `:last-child` | `li:last-child { color: red; }` | Styles the **last child** of a parent. |
| `:nth-child(n)` | `li:nth-child(2) { background: yellow; }` | Styles the **nth child** (e.g., 2nd `<li>`). |
| `:nth-last-child(n)` | `li:nth-last-child(2) { background: pink; }` | Styles the **nth child from the end**. |
| `:first-of-type` | `p:first-of-type { font-size: 1.2em; }` | Styles the **first element of its type**. |
| `:last-of-type` | `p:last-of-type { color: blue; }` | Styles the **last element of its type**. |
| `:nth-of-type(n)` | `p:nth-of-type(odd) { background: #f0f0f0; }` | Styles **every odd/even/nth element of its type**. |
| `:nth-last-of-type(n)` | `p:nth-last-of-type(2) { border: 1px solid red; }` | Styles the **nth element from the end of its type**. |
| `:only-child` | `div:only-child { color: purple; }` | Styles an element if it’s the **only child** of its parent. |
| `:only-of-type` | `span:only-of-type { font-style: italic; }` | Styles an element if it’s the **only one of its type** in its parent. |
| `:empty` | `div:empty { display: none; }` | Styles elements with **no children** (including text nodes). |

---

### **3. Form & Input Pseudo-classes**  
Specific to form elements.

| Pseudo-class | Example | Description |
|-------------|---------|-------------|
| `:default` | `input[type="submit"]:default { opacity: 0.8; }` | Styles the **default submit button** in a form. |
| `:indeterminate` | `input[type="checkbox"]:indeterminate { background: gray; }` | Styles checkboxes in an **indeterminate state**. |
| `:placeholder-shown` | `input:placeholder-shown { border: 1px dashed gray; }` | Styles an input while its **placeholder text is visible**. |

---

### **4. Link & Navigation Pseudo-classes**  
Used for URL-based styling.

| Pseudo-class | Example | Description |
|-------------|---------|-------------|
| `:target` | `#section1:target { background: yellow; }` | Styles an element when its ID matches the URL hash (e.g., `#section1`). |
| `:any-link` | `a:any-link { text-decoration: none; }` | Styles **all links** (visited or unvisited). |

---

### **5. Logical Pseudo-classes**  
For conditional styling.

| Pseudo-class | Example | Description |
|-------------|---------|-------------|
| `:not(selector)` | `li:not(.special) { color: gray; }` | Styles elements that **do not match** the selector. |
| `:is(selector)` | `:is(h1, h2, h3) { font-family: sans-serif; }` | Styles elements that match **any** of the selectors. |
| `:where(selector)` | `:where(h1, h2, h3) { margin: 0; }` | Similar to `:is()`, but with **lower specificity**. |
| `:has(selector)` | `div:has(p) { border: 1px solid red; }` | Styles a parent if it **contains** a matching child (e.g., a `<div>` with a `<p>` inside). *(New in CSS4, limited browser support.)* |

---

### **6. Language & Direction Pseudo-classes**  
For multilingual or RTL (right-to-left) support.

| Pseudo-class | Example | Description |
|-------------|---------|-------------|
| `:lang(en)` | `p:lang(en) { quotes: '"' '"'; }` | Styles elements with a **specific language** (e.g., English). |
| `:dir(rtl)` | `p:dir(rtl) { text-align: right; }` | Styles elements with **right-to-left** text direction. |

---

### **7. User Action Pseudo-classes**  
For interactive elements.

| Pseudo-class | Example | Description |
|-------------|---------|-------------|
| `:fullscreen` | `div:fullscreen { background: black; }` | Styles an element when in **fullscreen mode**. |
| `:modal` | `dialog:modal { border: 2px solid red; }` | Styles **modal dialogs** (like `<dialog>`). |

---

### **Summary Table of Most Common Pseudo-classes**
| Type | Pseudo-classes |
|------|---------------|
| **State-based** | `:hover`, `:active`, `:focus`, `:visited`, `:checked` |
| **Structural** | `:first-child`, `:nth-child(n)`, `:not(selector)` |
| **Forms** | `:disabled`, `:valid`, `:placeholder-shown` |
| **Links/URLs** | `:target`, `:any-link` |
| **Logical** | `:is()`, `:has()` *(CSS4)* |

---

### **When to Use Which?**
- Use `:hover`/`:active` for **interactive effects** (buttons, links).  
- Use `:nth-child()` for **styling tables/lists** (e.g., zebra stripes).  
- Use `:checked` for **custom checkboxes/toggle switches**.  
- Use `:not()` to **exclude certain elements**.  
- Use `:target` for **single-page app (SPA) effects**.  
