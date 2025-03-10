# Tool Learning Log

## Tool: **Flexbox**



### 3/6/25:
### `display: flex;`

**Without** `display: flex;`

![image](https://github.com/user-attachments/assets/bd7e2f41-a7b2-4c1e-80f3-c5b82220630f)


**With** `display: flex;`  

![image](https://github.com/user-attachments/assets/0cdbebbe-7ace-4d70-ad7d-a398c2472e0b)


When you add `display: flex;`, it allows you to use various flex properties to design a webpage that adjusts smoothly across different screen sizes. It went from being vertically to horizontally

---

#### Example on a Webpage:

**Without** `display: flex;`

![image](https://github.com/user-attachments/assets/3ca86c7b-22ff-472d-9bfd-72fd0cc4ab29)


**With** `display: flex;`

![image](https://github.com/user-attachments/assets/5b76931a-bb80-4bf6-9993-7540de9c3610)

#### Sources 
* https://www.freecodecamp.org/learn/responsive-web-design/css-flexbox

---


### 3/7/25:
### `display: direction;`

The `flex-direction` property is used to define the direction in which the flex container's child elements (flex items) are laid out.

#### Values

- **`row`** (default): Aligns the children horizontally, from left to right.
- **`column`**: Aligns the children vertically, from top to bottom.
- **`row-reverse`**: Aligns the children horizontally, but in reverse order (right to left).
- **`column-reverse`**: Aligns the children vertically, but in reverse order (bottom to top).

#### Example

```css
.parent {
  display: flex;
  flex-direction: row; /* or column, row-reverse, column-reverse */
}
```
---

### 3/8/25:
### `justify-content` Property

When you’re using Flexbox, sometimes the items inside the container don’t fill up all the space. You probably want to align and space out the items in a certain way, right? Well, the `justify-content` property helps you do just that!

#### Important Stuff to Know First

Before jumping into how `justify-content` works, you need to know a couple of things:

- **Main Axis**: This is the direction your items are laid out in. 
  - If you set the container to `row`, the main axis is **horizontal** (left to right).
  - If you set it to `column`, the main axis is **vertical** (top to bottom).

Now that we know that, the `justify-content` property will control how the items are spaced out along the main axis.

#### The Different Ways You Can Use `justify-content`

Here are the most common values for `justify-content`:

- **`flex-start`**: This lines up your items at the start of the container.
  - For a `row`, this means your items will be on the left side.
  - For a `column`, this pushes your items to the top.
  - This is the default if you don’t set anything for `justify-content`.

- **`flex-end`**: This lines up your items at the end of the container.
  - For a `row`, your items will be pushed to the right.
  - For a `column`, they’ll be pushed to the bottom.

- **`center`**: This lines up your items right in the center of the container.

- **`space-between`**: This spreads the items out along the main axis, with space between them.
  - The first and last items will be pushed to the edges of the container.
  - For a `row`, the first item will be on the left, the last on the right, and the others will have even space between them.

- **`space-around`**: This is kinda like `space-between`, but with a little space on both ends of the container too.
  - The space between each item is even, but there’s also half the space on the edges of the container.

- **`space-evenly`**: This makes the space between all the items completely equal, including the space at the edges of the container.

#### Example

```css
.container {
  display: flex;
  justify-content: center; /* Or flex-start, flex-end, space-between, space-around, space-evenly */
}
```
<!--
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
