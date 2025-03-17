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

---


### 3/7/25:
#### `flex-direction` Property

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
--- 

### 3/10/25
### `align-items` Property

The `align-items` property is used to align flex items along the **cross axis** (perpendicular to the main axis). It's similar to the `justify-content` property, but instead of affecting the main axis, it works on the cross axis.

#### Main Axis vs. Cross Axis

- **Main Axis**: The direction in which flex items are laid out.
  - For a `row` container: Horizontal (left to right).
  - For a `column` container: Vertical (top to bottom).

- **Cross Axis**: The opposite of the main axis.
  - For a `row` container: Vertical (top to bottom).
  - For a `column` container: Horizontal (left to right).

#### Purpose of `align-items`
Aligns items along the **cross axis**:

- For **rows**: Aligns items vertically (top to bottom).
- For **columns**: Aligns items horizontally (left to right).

#### Values for `align-items`

1. **`flex-start`**
   - Aligns items to the start of the container.
     - **Rows**: Aligns items to the top.
     - **Columns**: Aligns items to the left.

2. **`flex-end`**
   - Aligns items to the end of the container.
     - **Rows**: Aligns items to the bottom.
     - **Columns**: Aligns items to the right.

3. **`center`**
   - Aligns items to the center of the container.
     - **Rows**: Vertically centers items (equal space above and below).
     - **Columns**: Horizontally centers items (equal space to left and right).

4. **`stretch`**
   - Stretches items to fill the container (default value if no `align-items` is specified).
     - **Rows**: Stretches items top-to-bottom.
     - **Columns**: Stretches items left-to-right.

5. **`baseline`**
   - Aligns items based on their baselines (for text alignment).
     - Items align to the imaginary line where the text sits.

---
     
### 3/11/25:
### `flex-wrap` Property

The `flex-wrap` property in CSS allows you to split a flex container into multiple rows (or columns) when there are too many items to fit in a single line. By default, all flex items will fit together in one line, but using `flex-wrap`, you can create multiple rows or columns as necessary.

#### Direction of the Wrap
The direction of the wrapping depends on the container's layout (row or column), and the wrapping behavior is determined by the size of the items and the container.

#### Values for `flex-wrap`

1. **`nowrap`** (default)
   - This is the default setting and **does not wrap** items. All items will stay in one row or column, depending on the flex direction.

2. **`wrap`**
   - This wraps items onto multiple lines.
     - If the flex container is in **rows**, it wraps items **from top to bottom**.
     - If the flex container is in **columns**, it wraps items **from left to right**.

3. **`wrap-reverse`**
   - This wraps items onto multiple lines, but in the reverse direction.
     - If the flex container is in **rows**, it wraps items **from bottom to top**.
     - If the flex container is in **columns**, it wraps items **from right to left**.

---

  ### 3/12/25:
### `flex-shrink` Property

So far, all the Flexbox properties we've talked about apply to the **flex container** (the parent), but now we're going to talk about a property that applies to the **flex items** (the stuff inside the container).

The `flex-shrink` property lets a flex item shrink if the container is too small. This happens when the container is smaller than the total width of all the items inside it.

#### How It Works
If the flex container is too narrow (or too short), the items inside it will shrink to fit. The `flex-shrink` value decides **how much** an item will shrink compared to the others.

#### Values for `flex-shrink`

- **Default Value**: `1` – This just means the item can shrink if needed.
  
- **Higher numbers**: The bigger the number, the more the item will shrink. For example:
  - If one item has `flex-shrink: 1` and another has `flex-shrink: 3`, the item with `3` will shrink **3 times more** than the one with `1`.
  
---

### 3/12/25:
### `flex-grow` Property

The opposite of `flex-shrink` is the `flex-grow` property. While `flex-shrink` controls how much an item shrinks when the container gets smaller, `flex-grow` controls how much an item **grows** when the container gets bigger.

#### How It Works
When the flex container has extra space (like if the container gets larger), the `flex-grow` property decides how much each item will grow to take up that extra space.

Just like `flex-shrink`, the higher the number for `flex-grow`, the more that item will grow compared to the others.

---

### 3/13/25:
### `flex-basis` Property

The `flex-basis` property is all about setting the **initial size** of a flex item before any growing or shrinking happens with `flex-grow` or `flex-shrink`. It’s like telling CSS how big you want the item to be when it first appears in the container.

#### How It Works
- The value of `flex-basis` determines the starting size of the item.
- Once the container has extra space or is too small, `flex-grow` or `flex-shrink` will adjust the item, but `flex-basis` sets the starting point.
  
You can use the same units as other size properties (like `px`, `em`, `%`, etc.). If you use `auto`, CSS will size the item based on its content.

---

### 3/14/25:
### `flex` Property (Shortcut)

There’s a shortcut in CSS that lets you set the `flex-grow`, `flex-shrink`, and `flex-basis` properties all at once using the `flex` property. This makes it quicker to apply multiple flex properties without writing them separately.

#### How It Works
The `flex` property combines the following three properties into one:
- `flex-grow`
- `flex-shrink`
- `flex-basis`

The syntax is:
```css
flex: flex-grow flex-shrink flex-basis;
```
---

### 3/15/25:
### `order` Property

The `order` property allows you to control the **order** in which flex items appear inside a flex container. By default, the items will appear in the same order they are written in the HTML code, but with the `order` property, you can change that.

#### How It Works
The `order` property takes **numbers** as values. Items with a lower number will appear before items with a higher number. You can even use **negative numbers** to make items appear first.

#### Example

```css
.item1 {
  order: 2; /* This item will appear after items with order: 1 */
}


.item2 {
  order: 1; /* This item will appear first */
}

.item3 {
  order: -1; /* This item will appear first, even before order: 1 */
}
```
--- 

### 3/17/25:
### `align-self` Property

The `align-self` property is used to **adjust the alignment of individual flex items**. This is different from the `align-items` property, which sets the alignment for all items in the container. If you want to change the alignment of just one item without affecting the others, `align-self` is the way to go!

#### How It Works
`align-self` allows you to override the alignment set by `align-items` for a specific flex item. It works the same way as `align-items`, but it only affects the item it’s applied to, not the whole container.

---

### 3/18/2025
### Flexbox - `gap` Property

The `gap` property in Flexbox is used to control the space between items inside a flex container. It’s super simple and helps you avoid using margins on each individual item.

## What does it do?

- **`gap`** adds space between items in a flex container, making your layout cleaner and easier to manage than using margins on each item.

## Syntax:
```css
.container {
  display: flex;
  gap: 10px;  /* Adds 10px space between all items */
}
```


<!--

https://www.freecodecamp.org/learn/responsive-web-design/css-flexbox
https://www.youtube.com/watch?v=wsTv9y931o8



* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->


