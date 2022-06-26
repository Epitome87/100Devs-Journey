# Class 04 - Style With CSS

## Agenda

- Review: Client Server Model
- Review: Progressive Enhancement
- Learn - CSS Fundamentals
- Learn - Parent / Child Selectors
- Hint At: Classes and IDs
- Learn - Specificity
- Lab - Style a Simple Site

### CSS Fundamentals

**Where does CSS go?**

- Inline?
- In the head?
- In a separate file?

Although all three are possibilities, in a separate file is ideal. Remember, separation of concerns.

**Exception for inline styles?**

- Emails! They don't have access to internal stylesheets.
- Style in the head element, when you work at a company like Amazon who super-optimizes. They use `critical path CSS` -- CSS you absolutely need to render above the fold.

**Use a separate CSS file**

It is best practice to put CSS in its own file and link to it from the head:

```css
<link rel="stylesheet" href="css/style.css">
```

**CSS Syntax**

Syntax is the spelling and grammar rules.

- Selector
- Property
- Property value
- Declaration

```css
p {
  color: red;
}
```

In the above code, the "p" is the `selector`, "color" is the `property`, "red" is the `property value` (or just `value`), and "color: red" is the `declaration`, the content within "{}" is the `declaration block`. The entire thing is a `rule`

1. _Selector_ specifies what parts of the HTML document should be styled by teh declaration.

**CSS Cascade**

CSS is read top to bottom. What comes below, can override what came above. This is called the **Cascade**.

**CSS Color**

Four main ways to specify colors:

- Word
  - Very limited selection
  - Very minor overheard due to automatic conversion into Hex, so FAANG type companies steer clear
- Hex
  - Hexidecimal (#FF00BB)
- RGBa
  - Red, Green, Blue, alpha (opacity)
- HSLa
  - Hue, Saturation, Lightness

Good designers will give colors.

**CSS Font-Family**

```html
<head>
  <link href="someCDN" rel="stylesheet" />
</head>
```

```css
p {
  font-family: 'Poppins', 'Times New Roman', sans-serif;
}
```

Always specify `fallback fonts`, which will load if the other choices are not found.

**Selecting By Relationship**

To select an element that is the `direct descendent` of another element, use: `parent > child`. This ">" in this context is called the `child combinator`.

```html
<section>
  <p>Hello, World!</p>
</section>
```

```css
section > p {
  color: red;
}
```

To select an element that is inside of another element without being directly descended, use: `parent child`. This " " in this context is called the `descendant combinator`

```html
<section>
  <article>
    <p>Hello, World!</p>
  </article>
</section>
```

```css
// This WILL NOT color the paragraph tag above! It's not a direct descendent
section > p {
  color: red;
}
```

To select an element that is the next sibling, use: `previous sibling + next sibling`

```html
<section>
  <p>Hello, Twitch!</p>
  <p>Hello, Youtube!</p>
</section>
```

```css
// This will color the second paragraph, but not the first
p + p {
  color: red;
}
```

**IDs**

IDs are a used for selecting distinct elements.
Only one ID with the same name per document!

`#idName`

```html
<section>
  <p>Hello, Twitch!</p>
  <p id="zebra">Hello, Youtube!</p>
</section>
```

```css
#zebra {
  color: red;
}
```

**Classes**

Classes are for selecting multiple ements.
Multiple with same value allowed per document.
`.className`

```html
<p class="robot">Hello!</p>
```

```css
.robot {
  color: red;
}
```

**Specificity**

There is a point system that determines what will override what.

- !important, inline style: 1000 points
- IDs: 100 points
- Classes: 10 points
- Tags: 1 point

### Questions / Possible Ankis

Q1. What is the Internet?

- A wire, how we connect different devices (clients and servers)

Q2. What is the Golden Rule?

- Separation of concerns between HTML (Content / Structure), CSS (Style), and JavaScript (Behavior / Interaction)

- Brings organization to our code

Q3. What is Progress Enhancement?

- Idea that content is king, thin layer of CSS and JS
- Accessibility reasons -- people without high-speed internet

Q4. Breakdown CSS into 6 parts.

Q. What is the fact that what comes below can override what came above called in CSS?

- The Cascade.

Q. Why might we want to link to a separate CSS file?

- Organization, separation of concerns

Q. What are the different ways to represent color in CSS? Can you describe them?

- Word ("red", "green", etc)
  - Overheard to convert to Hex that top companies that rely on performance will want to avoid
- Hex (#FF00BB)
- RGBa (Red, Green, Blue, alpha)
- HSLa (Hue, Saturation, Lightness, alpha)

Q. In CSS, why does the link to a font need to come before the link to a CSS file?

- For the CSS file to have access to that font, the font needs to first be loaded and available.

Q. What are the 4 Basic Selectors? And their syntax? And what does each target?

- Universal selector: "\*"
- Type selector: "element" ("p", for instance)
- Class selector: ".className"
- ID selector: "#idName"

Q. What are some of the Combinator selectors? And their syntax? And what does each target?

- Child: "parent child"
- Descendent: "parent > child"
- Adjacent Sibling: "sibling + sibling"
- General Sibling: "sibling ~ sibling"

Q. In CSS, what are two ways we can we target a specific element, without targeting its type? What are the differences between these two methods?

- The ID and Class selectors.
- We can only provide an ID to one element in our markup, while classes can have multiple.

Q. In CSS, list the specificity of the different selector types.

- Tags: 1 point
- Classes: 10 points
- IDs: 100 points
- !important, inline styles: 1000 points

Q. List a few reasons why using inline styles is not ideal.

- Due to their 1000 point specificity, they will most likely override every other styling applied to them.
- For organization purposes (The Golden Rule), we should avoid inline and put CSS in its own file
