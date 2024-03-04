# Responsive design course on web.dev

## Folder structure
- pages in /src
- layouts in /_layouts
- includes in /_includes
- Json files in /_data
- Simple CSS in /assets/css
- images in /assets/images

## Page layout
- _layouts/base.liquid
- _includes/header.liquid
- _includes/footer.liquid

## Primary navigation
- add tags in frontmatter: primary

## Package.json scripts
- "start": "npx @11ty/eleventy --serve",
- "build": "eleventy",
- "debug": "DEBUG=* eleventy"

## Dependencies
- "@11ty/eleventy": "^2.0.1"

## eleventy.config.js
```
module.exports = function (eleventyConfig) {
    eleventyConfig.addPassthroughCopy("src/assets"); // Scss, JS, and images files
    return {
        dir: {
            input: "src", // Set the source for 11ty to the /src directory
            output: "_site", // This is the default
            includes: "_includes", // All UI partials
            layouts: "_layouts" // Base page layouts
        },
        templateFormats: ["html", "md", "liquid"]
    };
};
```

## Links to docs
- [Eleventy](https://www.11ty.dev/docs/)
- [LiquidJS](https://liquidjs.com/tutorials/intro-to-liquid.html)
- [Simple.css](https://simplecss.org/)
