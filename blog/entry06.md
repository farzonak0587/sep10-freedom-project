# Entry 6: Creating an MVP

Farzona Khabibova 

##### 05/12/25

## Content

For my Freedom Project, I’ve been working on creating a biology-themed website, and it’s been such a cool experience! I’ve learned a lot about the process, from the idea stage to wireframes, and using all the stuff I’ve learned, like Flexbox, Bootstrap, and more. Here’s a breakdown of how I went from thinking about the project to actually building it.

### What's an MVP?

So, MVP stands for Minimum Viable Product, which is basically the simplest version of a product that still works. It’s like building a foundation before you add all the extra stuff. For my website, my MVP was just a basic site with all the content on it, and the website had to be working. There is also a Beyond MVP, which is where you could add more stuff to the website to make it look better or add more content. 

### Making the Wireframes

Before I dove into coding, I needed a game plan. That’s where wireframes came in. I used wireframes to sketch out how my website would look, and it helped me figure out where everything should go. I kept it pretty simple with three main sections: Software, Hardware, and Future Innovations. The project was going to have a navbar, accordions, a carousel, and more.

I used [wireframe.cc](https://wireframe.cc/) to make the wireframes, which gave me a solid layout to follow when I started building. It was kind of like a guide that kept me on track during the whole development process.

### Research & Gathering Content

I knew from the start what kind of content I wanted to put on my website. Earlier this year, I did a ton of research about biology and technology, focusing on things like educational apps, medical devices, and the cool stuff that’s coming in the future. That research gave me a clear idea of what my website needed, and I could break it down into the different sections easily.

By getting all the research done first, I didn’t have to stress about what content to include while building the site. I already knew exactly what I needed.

### Using Bootstrap and Making Design Choices

To make my site look nice and professional, I used Bootstrap, which is a CSS framework that has pre-made components. I added a navigation bar at the top, used grid systems for the layout, and added the Bootstrap carousel to showcase the future innovations.

For fonts, I used [Google Fonts](https://fonts.google.com/) to keep it looking modern. I picked ‘Roboto’ for the body text because it’s clean and easy to read, and ‘Poppins’ for the headers because it gives a little extra personality to the design.

As for colors, I went with **soft blues, greys, and whites**. They fit the biology theme really well and give the site a calm, professional vibe.

### Using Flexbox in My Project

Flexbox was probably one of the most helpful things I learned. It made aligning elements and making the layout responsive way easier. I used Flexbox to organize the sections and boxes, making sure everything looked good on both desktop and mobile.

I used Flexbox throughout my whole project; for example, this is when I used it for the software part of my website. 

``` css

.software-box {

  display: flex;

  flex-direction: column;

  justify-content: flex-end;

```

### Parts of the Website:

#### Navigation Bar:

I used Bootstrap’s built-in `avbar` component for the navigation bar. It’s fixed at the top with links that scroll to different sections of the page. For responsiveness, I made it turn into a hamburger icon for mobile devices.

#### ** Home Page:**

The home page has a full-screen background image with centered text. I used `lexbox` to center the content both vertically and horizontally. A dark overlay is added on top of the image to make the text stand out better.

#### **Software Section:**

This section showcases different biology apps. I created individual boxes for each app, with titles, descriptions, and links. I made them look nice with `padding`, `margins`, and `shadows` to give the content some space and depth.

#### **Hardware Section:**

The hardware section follows a similar layout to the software section but includes images of medical devices. Each device has a description with the same box style for consistency.

#### **Future Innovations Section:**

For the future innovations, I used a collapsible`ccordion` design. This way, users can click to reveal more information, which is perfect for showcasing future tech or biotechnological ideas.

#### Image Carousel:

I added a Bootstrap carousel component to display multiple images in a slideshow style. This allows for a neat way of showcasing multiple medical images without taking up too much space on the page.

#### **Conclusion Section:**

I wrapped up with a simple conclusion that restates the importance of the topic. This section uses basic styling to match the rest of the content and ends the page on a clean note.

## Challenges

1. **Navbar Responsiveness:**

At first, my navbar wasn't playing nice on smaller screens. The mobile hamburger menu wasn’t working right, and the`avbar` items were either overflowing or not resizing correctly on mobile.

**Solution:**

I used Bootstrap’s built-in classes to make the `avbar` responsive. Specifically, I used `navbar-toggler`, `collapse`, and `navbar-expand-lg` to get the navbar to behave correctly on different screen sizes. The issue was that I didn't add the right classes and script to manage the collapse/expand stuff on smaller screens.

``` HTML

<nav class="navbar navbar-expand-lg navbar-dark bg-dark">

  <div class="container-fluid">

    <a class="navbar-brand mb-0 h1" href="#">Biology + Tech</a>

    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" 

            aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">

      <span class="navbar-toggler-icon"></span>

    </button>

```

**2. Using media queries:**

I ran into trouble with the carousel images not resizing right. They were either stretched out or not filling the entire width, especially on mobile. Also, in sections like "Software" and "Hardware," I had a ton of text that looked all over the place, especially on mobile. It was either too cluttered or overflowing.

**Solution for Both:**

I used media queries to make it responsive. This made it look so much better for people who use mobile, and they could see all the text instead of reading only half of it. The layout is so much better too because the website looks so much neater. 

**Example: **

``` CSS

@media (max-width: 768px) {

  .carousel-item img {

    height: 300px; /* Adjust the height for mobile as needed */

    object-fit: cover; /* Keeps the image covering the container */

  }

}

```

## Takeaways

- **Planning helps a ton.**

  Making wireframes before I even started coding saved me a lot of time. I already knew what the layout was going to look like, so I didn’t have to make it up as I went.

- **Bootstrap is super useful.**

  It made things like the navbar, carousel, and accordion way easier to build. I didn’t have to write everything from scratch, and it helped my site look more professional.

- **Flexbox = layout lifesaver**

  Flexbox helped me make sure all the sections and content stayed neat and responsive, especially on mobile screens.

- **Mobile-first matters.**

  At first, my site looked kind of messy on phones. Once I added media queries and used Bootstrap’s responsive classes, it looked way better and easier to use.

- **Small bugs can be big problems.**

  The navbar wasn’t working at first, and it was just because I forgot to add the right classes and scripts. Debugging took time, but it taught me to slow down and double-check my code.

- **Content first makes design easier.**

  Since I already had all my biology research ready, I didn’t have to pause during coding to figure out what to write. It made everything flow better.

## Engineering Design Process

Right now, I think I'm in the "improve as needed" part. I already came up with the idea, planned everything out, did research, made wireframes, and built my first working version (the MVP). I’ve tested it a bunch of times and fixed stuff like the navbar not working or images looking weird. Now I’m just making little changes to improve it — like cleaning up the layout more, maybe adding cooler stuff with JavaScript, and making sure everything looks good on phones and laptops. After that, I’ll probably share it and see what people think.

## Skills 

- **Time Management**

  I had to stay on track and manage my time so I didn’t fall behind. Breaking the project into small tasks really helped.

- **Communication**

  I got better at explaining my ideas clearly, especially when I had to share my progress or talk about what I was building.

- **Problem Solving**

  Whenever something broke or didn’t look right, I had to figure out why and fix it — sometimes that meant trying different solutions until it worked.

- **Planning & Organization**

  Creating wireframes and outlining content before coding helped keep everything organized and made the process smoother.

- **Creativity**

  I had fun picking colors, fonts, and images. It taught me how to make something both educational and nice to look at.

- **Patience**

  Things didn’t always go right the first time, so I learned to be patient and keep working through the tough parts.

- **Adaptability**

  Sometimes I had to change my original plans based on what worked and what didn’t. Being flexible really helped.

- **Independence**

  I built most of this on my own, so I learned how to research, figure stuff out, and keep going without needing help every time.

[Next](entry07.md)

[Home](../README.md)

