# Opensource.com with PatternFly Elements

This is a proof of concept site of using [PatternFly Elements](https://patternflyelements.org) as the base for [opensource.com](https://opensource.com).

The PatternFly Elements components and CSS are loaded from [unpkg.com/](https://unpkg.com/). This is *NOT* the recommended way to use PatternFly Elements on a site. The recommended way is to load PatternFly Elements from a local node_modules directory.

## Getting started

### Install the dev dependencies
```
npm install
```

### Run the server
```
npm start
```

## Things to note

### Load only what you need
The index.html file and the blog.html file are loading only the JavaScript that's needed for the page.

### Theming
In the index.html file, there are CSS variables for the overall theme and few component overrides for customization.
```css
:root {
  --pfe-theme--color--ui-accent: #0098C3;
  --pfe-theme--color--surface--accent: #005172; 
}

pfe-navigation {
  --pfe-navigation--BackgroundColor: #005172;
  --pfe-theme--color--feedback--default: #ccc;
}

pfe-cta[priority="primary"] {
  --pfe-cta--BackgroundColor: #69BE28;
  --pfe-cta--BorderColor: #69BE28;
}
```

### Lighthouse scores
After starting the web server with `npm start`, run a Lighthouse audit to see how the page performs. Both desktop and mobile scores are pretty high.