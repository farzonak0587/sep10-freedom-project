# Entry 5: Learning Flexbox: 
Farzona Khabibova 
##### 4/21/25

## Tool: Flexbox

## Content

###  What I Learned

Over the past few weeks, I’ve been learning all about **Flexbox**, and honestly, it’s been really cool seeing how much easier it makes web design. At first, I didn’t really get what it was for, but now I understand that Flexbox helps you control how things are laid out on a webpage—especially when the screen size changes.

Here are some of the main things I learned:

- `display: flex;` changes how elements are arranged—without it, everything just stacks.
- `flex-direction` lets you switch between rows and columns.
- `justify-content` and `align-items` help space out stuff on the main and cross axis.
- `flex-wrap` lets items wrap to a new row if they don’t fit.
- `flex-grow`, `flex-shrink`, and `flex-basis` control how items change size.
- You can even change the order of items using the `order` property.
- And finally, `gap` is a super simple way to add space between items without using margins.

---

### How I Learned

I used a bunch of websites to help me figure it out:

- [W3Schools - Flexbox Guide](https://www.w3schools.com/css/css3_flexbox.asp)
- [MDN Web Docs - Flexbox](https://developer.mozilla.org/en-US/docs/Web/CSS/flex)
- [CSS-Tricks: A Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- YouTube: Searched things like “Flexbox in 5 minutes” and watched short, focused videos

I also wrote down notes and tried out the properties in live code editors like CodePen.

---

### What I Tried / Changed / Made
I didn’t just read or watch stuff—I actually tried things out too! Here are some examples:

🔹 Basic Flexbox Layout
I made a simple box layout with 3 items in a row using:


``` css 
.container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
```

Before Flexbox, everything was stacked. After I added display: flex, the items lined up in a row and spaced out perfectly.

🔹 **Switching Directions**

Then I tried flex-direction: column, and it stacked the items vertically instead. Super easy to change the whole layout with just one line.

🔹 **Wrapping Items**

I made a box of 8 items and used flex-wrap: wrap; to make it look better on smaller screens. Without it, everything just squished together.

🔹 **Grow and Shrink**

I tested flex-grow: 1 on one item and flex-grow: 2 on another, and I could actually see how the second one grew more than the first when there was extra space.

🔹** Order and Align Self**

I also changed the order of items using the order property, which was kinda fun. And I used align-self: flex-end on one item to move it to the bottom by itself.

**Screenshots + Examples:**

**Without** `display: flex;`

![image](https://github.com/user-attachments/assets/3ca86c7b-22ff-472d-9bfd-72fd0cc4ab29)


**With** `display: flex;`

![image](https://github.com/user-attachments/assets/5b76931a-bb80-4bf6-9993-7540de9c3610)

**Another Example of flex-direction:**
``` css 
.parent {
  display: flex;
  flex-direction: column;
}
```

## Skills 



[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
