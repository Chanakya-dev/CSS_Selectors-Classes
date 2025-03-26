### **1. Core Pseudo-Elements**
| Pseudo-Element | Example | Description |
|---------------|---------|-------------|
| `::before` | `p::before { content: "→ "; }` | Inserts content **before** an element. |
| `::after` | `p::after { content: " ←"; }` | Inserts content **after** an element. |
| `::first-letter` | `p::first-letter { font-size: 2em; }` | Styles the **first letter** of a block-level element. |
| `::first-line` | `p::first-line { font-weight: bold; }` | Styles the **first line** of a block-level element. |
| `::selection` | `::selection { background: yellow; }` | Styles text **highlighted by the user**. |

---

### **2. Typography & Content Pseudo-Elements**
| Pseudo-Element | Example | Description |
|---------------|---------|-------------|
| `::marker` | `li::marker { color: red; }` | Styles list bullets/numbers. |
| `::placeholder` | `input::placeholder { opacity: 0.5; }` | Styles placeholder text in inputs. |

---

### **3. Advanced/Experimental Pseudo-Elements**
| Pseudo-Element | Example | Description |
|---------------|---------|-------------|
| `::backdrop` | `dialog::backdrop { background: rgba(0,0,0,0.5); }` | Styles the **background behind modals/dialogs**. |
| `::file-selector-button` | `input[type="file"]::file-selector-button { background: #eee; }` | Styles the **button** in file inputs. |
| `::grammar-error` | `::grammar-error { text-decoration: red wavy underline; }` | (Experimental) Styles grammar errors. |
| `::spelling-error` | `::spelling-error { text-decoration: blue wavy underline; }` | (Experimental) Styles spelling errors. |

---


---

### **5. Deprecated Pseudo-Elements**
❌ Avoid these (modern CSS uses double colons `::`):
- `:before` → Use `::before`
- `:after` → Use `::after`
- `:first-letter` → Use `::first-letter`
- `:first-line` → Use `::first-line`

---

### **Key Differences: Pseudo-Classes vs. Pseudo-Elements**
| Feature | Pseudo-Class (e.g., `:hover`) | Pseudo-Element (e.g., `::before`) |
|---------|-------------------------------|-----------------------------------|
| **Purpose** | Targets element **states** | Targets **specific parts** of an element |
| **Syntax** | Single colon (`:`) | Double colon (`::`) (modern) |
| **Example** | `a:hover { color: red; }` | `p::first-line { font-weight: bold; }` |

---

### **Practical Examples**
#### 1. Add Icons with `::before`
```css
a::before {
  content: "🔗 ";
}
```

#### 2. Custom List Bullets with `::marker`
```css
li::marker {
  content: "✓ ";
  color: green;
}
```

#### 3. Highlight First Line with `::first-line`
```css
p::first-line {
  font-variant: small-caps;
}
```

#### 4. Style Input Placeholders
```css
input::placeholder {
  font-style: italic;
  color: #999;
}
```

---

### **Browser Support**
Most pseudo-elements work in modern browsers, but:
- `::grammar-error`/`::spelling-error` are experimental.
- `::part()`/`::slotted()` require Shadow DOM (web components).

---

### **Summary Table**
| Type | Pseudo-Elements |
|------|-----------------|
| **Content** | `::before`, `::after`, `::marker` |
| **Typography** | `::first-letter`, `::first-line`, `::selection` |
| **Forms** | `::placeholder`, `::file-selector-button` |
