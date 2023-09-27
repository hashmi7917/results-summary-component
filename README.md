# Frontend Mentor - Results summary component solution

This is a solution to the [Results summary component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/results-summary-component-CE_K6s0maV). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the interface depending on their device's screen size
- See hover and focus states for all interactive elements on the page
- **Bonus**: Use the local JSON data to dynamically populate the content

### Screenshot

#Mobile
![Screenshot 2023-09-27 at 3 22 31 PM](https://github.com/hashmi7917/results-summary-component/assets/38833326/77d046a7-4864-4b04-876c-048816cfa69c)

#Desktop
![](![Screenshot 2023-09-27 at 3 13 08 PM](![Screenshot 2023-09-27 at 3 41 45 PM](https://github.com/hashmi7917/results-summary-component/assets/38833326/c5d80546-8583-4b4b-9489-87e524c18a33)
))

Add a screenshot of your solution. The easiest way to do this is to use Firefox to view your project, right-click the page and select "Take a Screenshot". You can choose either a full-height screenshot or a cropped one based on how long the page is. If it's very long, it might be best to crop it.

Alternatively, you can use a tool like [FireShot](https://getfireshot.com/) to take the screenshot. FireShot has a free option, so you don't need to purchase it.

Then crop/optimize/edit your image however you like, add it to your project, and update the file path in the image above.

**Note: Delete this note and the paragraphs above when you add your screenshot. If you prefer not to add a screenshot, feel free to remove this entire section.**

### Links

- Solution URL: [Add solution URL here](https://github.com/hashmi7917/results-summary-component)
- Live Site URL: [Add live site URL here](https://results-summary-card-componnet.netlify.app/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- SCSS
- Mobile-first workflow

### What I learned

Flexbox, CSS Custom Properties, Layout, Block Sizes

To see how you can add code snippets, see below:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link
      rel="icon"
      type="image/png"
      sizes="32x32"
      href="./assets/images/favicon-32x32.png"
    />

    <link rel="stylesheet" href="style.css" />
    <title>Frontend Mentor | Results summary component</title>
  </head>
  <body>
    <section>
      <main class="container">
        <div class="results">
          <p>Your Result</p>
          <div class="circle">
            <h1>76</h1>
            <span>of 100</span>
          </div>
          <h4>Great</h4>
          <p class="resuslt-info">
            You scored higher than 65% of the people who have taken these tests.
          </p>
        </div>
        <div class="summary">
          <h4>Summary</h4>
          <div class="cards">
            <div class="cardDetail red">
              <div class="stats">
                <span
                  ><img src="./assets/images/icon-reaction.svg" alt="reaction"
                /></span>
                <h6>Reaction</h6>
              </div>
              <div class="score">
                <p>80 <span>/ 100</span></p>
              </div>
            </div>
            <div class="cardDetail yellow">
              <div class="stats">
                <span
                  ><img src="./assets/images/icon-memory.svg" alt="reaction"
                /></span>
                <h6>Memory</h6>
              </div>
              <div class="score">
                <p>92 <span>/ 100</span></p>
              </div>
            </div>
            <div class="cardDetail teal">
              <div class="stats">
                <span
                  ><img src="./assets/images/icon-verbal.svg" alt="reaction"
                /></span>
                <h6>Verbal</h6>
              </div>
              <div class="score">
                <p>61 <span>/ 100</span></p>
              </div>
            </div>
            <div class="cardDetail blue">
              <div class="stats">
                <span
                  ><img src="./assets/images/icon-visual.svg" alt="reaction"
                /></span>
                <h6>Visual</h6>
              </div>
              <div class="score">
                <p>72 <span>/ 100</span></p>
              </div>
            </div>
          </div>
          <div class="btnBox">
            <button class="btn">Continue</button>
          </div>
        </div>
      </main>
      <div class="attribution">
        Challenge by
        <a href="https://www.frontendmentor.io?ref=challenge" target="_blank"
          >Frontend Mentor</a
        >. Coded by
        <a href="https://www.frontendmentor.io/profile/hashmi7917">hashmi7917</a
        >.
      </div>
    </section>
  </body>
</html>
```

```css
@import url('https://fonts.googleapis.com/css2?family=Hanken+Grotesk:wght@400;700;800&display=swap');

:root {
  /* Primary */
  --light-red: hsl(0, 100%, 67%);
  --orange-yellow: hsl(39, 100%, 56%);
  --green-teal: hsl(166, 100%, 37%);
  --cobalt-blue: hsl(234, 85%, 45%);

  /* Gradients */
  --light-slate-blue-background: hsl(252, 100%, 67%);
  --light-royal-blue-background: hsl(241, 81%, 54%);
  --violet-blue-circle: hsla(256, 72%, 46%, 1);
  --persian-blue-circle: hsla(241, 72%, 46%, 0);

  /* Neutral */
  --white: hsl(0, 0%, 100%);
  --pale-blue: hsl(221, 100%, 96%);
  --light-lavender: hsl(241, 100%, 89%);
  --dark-grey-blue: hsl(224, 30%, 27%);
}

.red {
  background-color: hsla(0, 100%, 67%, 0.05);
  color: var(--light-red);
}
.yellow {
  background-color: hsla(39, 100%, 56%, 0.05);
  color: var(--orange-yellow);
}
.teal {
  background-color: hsla(166, 100%, 39%, 0.05);
  color: var(--green-teal);
}
.blue {
  background-color: hsla(234, 85%, 45%, 0.05);
  color: var(--cobalt-blue);
}

*,
::before,
::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Hanken Grotesk', sans-serif;
  font-size: 18px;
  /* - Weights: 500, 700, 800 */
  max-width: 375px;
  margin: 0 auto;
}

h1 {
  font-size: 56px;
  font-weight: 800;
}

p {
  color: var(--light-lavender);
}

/* 
- Mobile: 375px
- Desktop: 1440px
*/

.container {
  margin: 0 auto;
  width: 100%;
  max-width: 375px;
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: var(--white);
  box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
  border-radius: 32px;
}

.results {
  height: 350px;
  width: 100%;
  max-width: 375px;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  /* padding: 10px 0; */
  background: linear-gradient(
    var(--light-slate-blue-background),
    var(--light-royal-blue-background)
  );
  text-align: center;
  color: var(--white);
  border-radius: 0 0 32px 32px;
}

.results > h4 {
  font-size: 24px;
  color: var(--white);
  font-weight: 500;
}

.resuslt-info {
  width: 100%;
  max-width: 70%;
  align-self: center;
  font-size: 15px;
  line-height: 1.5;
  font-weight: 400;
}

.results:nth-child(1) {
  font-size: 18px;
  font-weight: 700;
}

.circle {
  width: 150px;
  height: 150px;
  background: linear-gradient(
    var(--violet-blue-circle),
    var(--persian-blue-circle)
  );
  align-self: center;
  border-radius: 50%;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.circle > span {
  color: hsla(252, 100%, 70%, 0.9);
  font-weight: 500;
  font-size: 15px;
}

.summary {
  height: 450px;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  padding-right: 10px;
}

.summary > h4 {
  font-size: 18px;
  font-weight: 600;
  color: var(--dark-grey-blue);
}

/* .cards {
  padding: 20px;
} */
.cards {
  height: 280px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  /* padding: 10px 20px; */
}

.cardDetail {
  width: 100%;
  min-width: 325px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 20px;
  border-radius: 8px;
}

.stats {
  display: flex;
  justify-content: space-around;
}

.stats img {
}

.stats > h6 {
  font-size: 15px;
  font-weight: lighter;
  padding-left: 12px;
}

.score p {
  font-size: 16px;
  color: var(--dark-grey-blue);
  font-weight: 800;
}

.score p span {
  color: var(--dark-grey-blue);
  font-weight: 100;
}

.btn {
  background-color: var(--dark-grey-blue);
  width: 100%;
  color: var(--white);
  padding: 20px 30px;
  border-radius: 32px;
  border-style: none;
  font-size: 16px;
  box-shadow: rgba(149, 157, 165, 0.2) 0px 8px 24px;
}

.btn:hover {
  transform: scale(1.01);
  transition: all 0.2s ease-in-out;
}

.btn:active {
  background-color: var(--violet-blue-circle);
}

.attribution {
  font-size: 10px;
  text-align: center;
  padding: 10px;
}

/* for large devices media queries*/
@media screen and (min-width: 750px) {
  body {
    margin: 0 auto;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .container {
    margin: 0 auto;
    width: 100%;
    min-width: 525px;
    height: 350px;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
  }

  .container:hover {
    box-shadow: rgba(17, 12, 46, 0.15) 0px 48px 100px 0px;
  }

  .results {
    max-width: 250px;
    border-radius: 32px;
  }

  .resuslt-info {
    font-size: 12px;
  }

  .results:first-child {
    font-size: 14px;
  }

  .circle:hover {
    background: linear-gradient(
      var(--light-slate-blue-background),
      var(--persian-blue-circle)
    );
  }

  .summary {
    height: 100%;
    /* max-width: 250px; */
    max-height: 320px;
    justify-content: space-around;
    align-items: center;
    padding-right: 25px;
  }

  .summary h4 {
    font-size: 15px;
    align-self: baseline;
  }

  .cards {
    max-height: 220px;
    justify-content: space-around;
    align-items: center;
  }
  .cardDetail {
    min-width: 220px;
    padding: 10px 6px;
    justify-content: space-between;
    border-radius: 8px;
  }

  .stats > h6 {
    font-size: 14px;
    font-weight: 500;
    padding-left: 12px;
  }

  .score p {
    font-size: 14px;
    color: var(--dark-grey-blue);
    font-weight: 800;
  }

  .btn {
    padding: 12px;
    font-size: 12px;
    font-weight: 400;
  }

  img:hover {
    transform: scale(1.1);
    transition: all 0.2s ease-in-out;
  }

  .btnBox {
    width: 100%;
    max-width: 245px;
    padding-top: 10px;
  }
}

@media screen and (max-width: 400px) {
  .container,
  .results,
  .cards,
  .cardDetail,
  .summary {
    min-width: 80%;
  }
}
```

### Continued development

Flexbox, Grids, Bootstrap, Styled Components

### Useful resources

- [Example resource 1](https://getcssscan.com/css-box-shadow-examples) - This helped me for BOX Shadow CSS. I really liked this pattern and will use it going forward.

## Author

- Website - [Muqtadeer](https://github.com/hashmi7917)
- Frontend Mentor - [@hahsmi7917](https://www.frontendmentor.io/profile/hashmi7917)
- Instagram - [@yourusername](https://www.instagram.com/hashmi.developer)

## Acknowledgments

Thanks To Frontend Mentor Community For Providing this Challenges
