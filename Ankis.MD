# Anki

Here I will write out questions after each lecture or study assignment, as a way to actively recall what I just learned. Some of these will also be added to my Anki collection!

## Week 01

### Class 01

**Assignment #01**: Watch video on Active Recall `https://www.youtube.com/watch?v=ukLnPbIffxE`

Q1. What are some common revision techniques student use and think are effective, but are actually not?

- Re-reading
- Highlighting
- Summarizing / Note-making

Q2. What are two names for the most effective revision technique?

- Active Recall
- Active Retrieval

Q3. What does Active Recall involve?

- As the name suggest, simply recalling the study material shortly after it was introduced. The more effort something requires to retrieve it, and the more often, the stronger the neural connections will be.

Q4. Research has shown which to be more effective -- active recalling once, or re-reading material four times?

- Active recalling just a single time was shown to be more effective than re-reading four times!

Q5. What are some things or tools you could use to promote active recall?

- Flash cards (with an app such as Anki)
- Writing down as much as you remember after a study session
- A practice test right after learning new material
- Writing notes in the form of questions

**Assignment #02**: Watch video on Active Recall `https://www.youtube.com/watch?v=Z-zNHHpXoMM`

Q1. After Active Recall, what is the second important technique proven to help with studying? (The opposite of cramming)

- Spaced repetition

Q2. In general, what does spaced repetition involve?

- Spacing when you _actively recalling_ information. Spacing actions such as re-reading does not count!

Q3. Is spaced repetition useful only after completing a study session for the day?

- No; spaced repetition also has tremendous value when used _within_ a single study session.

Q4. What is the name of the curve that determines how we retain information over time?

- Forgetful Curve

Q5. What is the growth of the Forgetful Curve?

- It is an exponential decline over time

Q6. How can we "flatten" the Forgetful Curve?

- By actively recalling information in spaced repetitions. Each time we actively recall information, we improve the amount of information we will remember and how long it will take to forget. Eventually the curve is flat; the information is part of our long-term memory.

Q7. What is "The Magical Spreadsheet"?

- It is Ali's personal technique for implementing spaced repetition. It involves using a spreadsheet and writing the name of broad subjects as different sheets, and in those sheets writing down a comprehensive list of topics (scoped appropriately). Every time you actively recall information from that topic, put the current date in a column beside it. Color code each cell to represent how well / easily you actively recalled. Focus on new information first, and information you perform poorly on. Take a quantity over quality approach -- attempting to visit many topics on a general level rather than the fine details of a single topic.

Q8. What is "Interleaving Practice"?

- It is the concept of working on something and _just_ before mastery, moving onto a new concept.

**Assignment #03**: Do full Coursera course of "Learning how to Learn".

### Class 02 - Become a Software Engineer

**Assignment - Read Shay Hoe article**

Q. Can inline elements wrap block level elements? Can block level wrap inline level? What are the exceptions?

A. No, inline elements cannot wrap block-level elements, although HTML was updated to allow anchor tags to do so. Block-level elements can wrap inline elements, as well as other block-level.

Q. What are the two most common types of links? What types of paths do each have?

- Links to _other pages_ of the same website and links to _other websites_
- Links to other pages of the same websites use relative links (no need to include domain), while links to other websites use absolute paths (include the full domain).

Q. How do we link to a part of the same page?

```html
<body id="top">
  <a href="#elementID">Go to Top</a>
</body>
```

Q. What is the syntax to link to an email address, when using an anchor tag? What about when including a subject and body?

```html
<a href="mailto:matthew@gmail.com">Email Me</a>
```

With subject and body:

```html
<a href="mailto:matthew@gmail.com?subject=Hello&body=How%20are%20you">Email Me</a>
```

Q. What is the syntax for opening a link in a new window?

- `<a href="https://somesite.com" target="_blank">Go Here</a>`
- To trigger the action of opening a link in a new window, use the target attribute with a value of \_blank. The target attribute determines exactly where the link will be displayed, and the \_blank value specifies a new window.

Q: When selectors are combined, what direction should they be read in? And what is the farthest right selector called?

- They should be read from right-to-left. The farthest right selector is known as the _key selector_ -- it identifies exactly which element the styles will be applied to. Any selector to the left of this serves as a prequalifier.

Q. In CSS, what are the two form length values can come in? Can you give examples of each?

- Relative lengths, and Absolute lengths.
- Some examples of absolute lengths include px, in (inch), mm (millimeters)
- Some examples of relative lengths include: % (percentage), em, rem, ch, vh, vw

Q. When specifying an absolute length of pixels in CSS, how many inches is a pixel equal to?

- A px is 1/9th of an inch. So 96 pixels can fit into an inch.
- The exact measurement of a pixel, however, may vary slightly between high-density and low-density devices.

Q. What will the width and height properties on an inline element do?

A. Nothing; inline elements do not accept width and height properties or any values tied to them. Block and inline-block elements will, however.

### Class 03 - Review / Hands on Keyboard

### Class 04 - Style With CSS

### Class 05 - CSS Layout

## Class 06 - Relationship, Specificity, Box Model, Responsiveness

## Class 07 - Responsive CSS

## Class 08 - Layouts & Unleash Your Inner Baddie

## Class 09 - Live Networking

## Class 10 - Trough of Sorrow
