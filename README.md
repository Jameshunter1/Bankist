# Bankist — Minimalist Banking Website

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript_ES6%2B-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![No frameworks](https://img.shields.io/badge/Dependencies-none-2ea44f?style=flat-square)

A polished marketing site for a fictional bank, built in **vanilla JavaScript** — no frameworks, no libraries. The point of the project is modern DOM techniques: event delegation, the Intersection Observer API, and performance patterns like lazy loading.

**🔗 Live demo:** [jameshunter1.github.io/Bankist](https://jameshunter1.github.io/Bankist/)

<!-- To add a screenshot: save one as img/screenshot.png and uncomment the next line -->
<!-- ![Bankist screenshot](img/screenshot.png) -->

## Features

| Feature | How it's built |
| --- | --- |
| Modal window | Class toggling; closes on button, overlay click, or `Escape` |
| Smooth scrolling | `scrollIntoView({ behavior: 'smooth' })` |
| Page navigation | Single delegated listener on the nav — one handler for every link |
| Tabbed component | Event delegation + `closest()` + `data-tab` attributes |
| Nav hover fade | `mouseover`/`mouseout` with `bind()` to pass opacity values |
| Sticky navigation | Intersection Observer on the header with a `rootMargin` offset |
| Section reveal on scroll | Intersection Observer at 15% threshold, unobserved after first reveal |
| Lazy image loading | Low-res placeholders swapped via `data-src` 200px before entering view |
| Slider / carousel | `translateX` transforms, dot indicators, arrow-key support |

## Why No Framework?

Every one of these features is standard portfolio fare *with* a framework. Doing them with raw DOM APIs shows the underlying mechanics: how event delegation replaces per-element listeners, how Intersection Observer replaces scroll-event polling (and why that matters for performance), and how CSS transforms make animation cheap.

## Run Locally

No build step, no dependencies:

```bash
git clone https://github.com/Jameshunter1/Bankist.git
cd Bankist
# open index.html in a browser, or serve it:
npx serve .
```

## Project Structure

```
.
├── index.html
├── style.css
├── script.js      # ~280 lines of feature code
├── img/
└── .prettierrc
```

## Credit

Built as part of [Jonas Schmedtmann's JavaScript course](https://www.udemy.com/course/the-complete-javascript-course/) — design and concept are his; the implementation here is my own work from the course.
