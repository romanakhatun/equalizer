# 📦 CSS `box-sizing: border-box`
  
## 🔹 Introduction
Normally in css, when you set an element's width or height that number only applies to the `content box`. The padding and border get added on top of that size, making the element larger than you expected.

Example (default ``box-sizing: content-box``):
 ```js
div {
  width: 200px;   /* content only */
  padding: 20px;  /* adds 40px total (20px each side) */
  border: 10px;   /* adds 20px total (10px each side) */
}
```
👉 Total Width = **200 + 40 + 20 = 260px**


## 🔹 Using ``border-box``
Now, if you use `box-sizing: border-box;`, the width and height include the **content + padding + border** together.

So the box never grows larger than what you set.

Example (``box-sizing: border-box``):
```js
div {
  width: 200px;   /* includes content + padding + border */
  padding: 20px;
  border: 10px;
}
```
👉 The total width = exactly **200px**, not 260px.

## 🔹 Why Use It?
- Makes layouts predictable
- Easier to control sizes
- Avoids unexpected overflow issues

## 🔹 Best Practice
Apply it to all elements for consistent behavior:
```js
* {
  box-sizing: border-box;
}
```
