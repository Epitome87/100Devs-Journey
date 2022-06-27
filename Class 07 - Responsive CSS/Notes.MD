# Class 07 - Responsive CSS

## Agenda

- Learn: How to Network (Part 1)
- Review: CSS Fundamentals
- Review: Box Model
- Review: Float
- Review: Three Simple Layouts
- Learn: Responsive Basics
- Learn: Flexbox
- Homework: Flexbox Froggy + Movie

## Networking

Stranger > Acquaintance > Friend > Referral > Coworker

It's important to get referrals:

- Application might get put higher in stack
- Skip first round interview
- Skip right to technical interview
- Companies are paying engineers for referrals (so easier to receive one)

Don't make it all about you; take the time to get to know the person, form a connection.

- More likely to be replied to
- More likely to receive a meaningful referral

**How to make friends**

- Read "How to Win Friends and Influence People"
- Practice!

**How to meet people**

1. Events

- Start on Meetup and then find local boards. You'll soon keep encountering the same people. Greet them with their name and a hello!
- Find local boards
- Find the closest city with the most jobs. Focus your virtual meetups there.

2. Conferences

- People mostly show up here in hopes of networking
- Find via Google search of "Interest + Conference Type" or #100devs-events
- If not free, find a way to email them and ask if there's a way to get discount for new learner / hardship
  - Some allow you to do a small volunteer task, and then let you free the rest of the conference
  - The volunteering is also a great way to network!
- "Don't ever eat alone"

3. Community Groups

- Text channels, Discord, Slack, IRC
- Easier if you struggle face-to-face
- Local community groups, either text or face-to-face

4. Apps

- Lunchclub
- Bumble Bizz
- Be careful using these, though!

5. Friends & Family

- Talk to them, let them know you're a software engineer

Networking is easier if you bring a buddy!

Provide value to those you talk to; don't make it all about you
End a coffee chat by asking who else you can talk to; this may lead to your next coffee chat!

**Normal follow up**

Meet > Email > LinkedIn > Twitter

- Meet someone
- Next day, send them an email. Provide value to show you were engaged in the conversation
- On day 3, add them on LinkedIn, with a message reminding them where you met, thank for their time
- On day 6, add them on Twitter
- Essentially, we're making them perform spaced repetition into remembering who we are, and hopefully become an acquaintance

From now on, never add someone on LinkedIn without also including a message!

**Want a Coffee Chat?**

Having a deeper conversation with someone one-on-one. 15-20 minutes of their time. If you're meeting in person for an actual coffee chat, arrive early, order a small coffee, when the person comes in announce you have your coffee and tell them to feel free to join. Preferable with someone who's in a position you want to eventually be in, so you can gain insight.

Email follow up #1 > Email follow up #2 > Last email

- Initial email requests if they can find 15 minutes of their time to have a chat with you
- After 1 week, send initial follow-up email
- After 2 weeks, send a 2nd follow-up email
- Final email at 1 month

**Use the Sheet**

- An excel sheet to keep track of your networking. Keep track of each person you network with; the event, name, company, spark (something you remember about them), email, follow-up, next steps, etc.
- Also a potential "Hit List"

**Pro Moves**

Alerts! Set up custom alerts on Google.
`https://www.google.com/alerts`

Someone mention Pokemon once? Set an alert for it, which will be tied to that person.

## Responsive Websites

With the introduction and popularity of the mobile phone, we have to ensure our sites look good on smaller sizes. Sites can no longer be _fixed_ -- they must be **responsive**.

**What makes a site responsive?**

- Fluid
- Elastic
- Content decisions

**Fluid**

Everything as a percentage or can respond natively

**Elastic**

Using EMs & REMs.
Font size of the parent, in the case of typographical properties like font-size, and font size of the element itself, in teh case of other properties like with.

```css
html {
  font-size: 62.5%;
}
section {
  font-size: 10px;
}
/* Not this way! EMs can grow unpredictably  */
p {
  font-size: 1em;
}

/* This way! */
p {
  font-size: 1rem;
}
```

Note that it is not too uncommon to find people setting the font-size of the html to 62.5%, so they can do the conversions from px to em/rem easier (as this gives us 10px instead of the default browser choice of 16px).

**Content Decisions**

What content to show on what screen sizes.

How do we make content decisions? Media queries!

**Media Queries**

Mobile-first: Start with mobile view, add as screen gets bigger
Desktop-first: Start large and add media queries whenever shrinking stops looking good

```css
/* Between 0 and 600px */
@media screen and (max-width: 600px) {
  h1 {
    color: red;
  }
}

/* Between 601px and 900px */
@media (min-width: 601px) and (max-width: 900px) {
  h1 {
    color: green;
  }
}
```

Whenever we see `screen`, that essentially means 0. "Between 0 pixels and 600px, do this"

**Important Addition to the Template**

In order for responsive design to work, we need the following in our head in the HTML:

```html
<meta name="viewport" content="width=device-width, initial-scale=1" />
```

This tells the browser to figure out the width of the screen. Initial scale is the initial zoom level. Never set user-scalable to no, it won't allow pinching and zooming!


