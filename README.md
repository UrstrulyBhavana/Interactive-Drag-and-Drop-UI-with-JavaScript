# 🖱️ Drag & Drop Using JavaScript

A dynamic **drag and drop** interface built with JavaScript, HTML, and CSS. This project enables users to drag list items between two containers, showcasing the power of event handling in JavaScript.

---

## 🚀 Features
- 🖱️ **Drag and Drop Functionality:** Move items seamlessly between two containers.
- 🎨 **Modern Design:** Features a sleek and interactive interface with vibrant colors.
- 🖥️ **Responsive Layout:** Works flawlessly across all devices.
- ✨ **Interactive Events:** Handles drag and drop events with precision for a smooth user experience.

---

## 🛠️ Technologies Used
- 🎨 **HTML:** Provides the structure for the containers and list items.
- 🎨 **CSS:** Styles the containers and list items with a modern, responsive design.
- ✨ **JavaScript:** Implements drag and drop functionality using event listeners.

---

## 🔧 How to Use
1. **Drag Items:**
   - Click and hold any list item from the **left container**.
   - Drag the item to the **right container**.

2. **Drop Items:**
   - Release the dragged item inside the target container to drop it.

3. **Reposition Items:**
   - Drag and drop items between the containers to reorganize as needed.

---

## 🔑 Key Features (Code)

### **Drag and Drop Implementation**
This snippet enables the drag and drop functionality:
```javascript
let lists = document.getElementsByClassName("list");
let rightBox = document.getElementById("right");
let leftBox = document.getElementById("left");

for (list of lists) {
    list.addEventListener("dragstart", function (e) {
        let selected = e.target;

        rightBox.addEventListener("dragover", function (e) {
            e.preventDefault();
        });
        rightBox.addEventListener("drop", function (e) {
            rightBox.appendChild(selected);
            selected = null;
        });

        leftBox.addEventListener("dragover", function (e) {
            e.preventDefault();
        });
        leftBox.addEventListener("drop", function (e) {
            leftBox.appendChild(selected);
            selected = null;
        });
    });
}
```
## Demo.gif
