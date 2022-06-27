# Class 06 - Relationship, Specificity, Box Model and Responsiveness

## Agenda

- Review: HTML Fundamentals
- Review: CSS Fundamentals
- Review: Box Model
- Review: Float 💩
- Review: Three Simple Layouts
- Learn: Responsive Basics
- Homework: Simple Responsive Site

## Reset

Gets rid of every single default styling. Start from scratch. H1 will look like span, etc.

## Normalize

Keep some of the default styling, but that default styling is consistent across every browser.

## Media Queries

**The mechanism that allows our sites to be responsive**. They are writing in a syntax like:

```css
@media screen and (min-width: 600px) {
  h1 {
    color: blue;
  }
}
```
