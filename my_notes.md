.
├── \_config.yml              # Site configuration
├── \_posts/                  # Blog posts (Markdown files named YYYY-MM-DD-title.md)
├── \_layouts/                # HTML layouts using Liquid
├── \_includes/               # Reusable HTML snippets
├── \_sass/                   # Sass partials
├── assets/                 # CSS, JS, images, etc.
│   └── css/
│       └── style.scss
├── index.md                 # Home page (can also be .html)
├── \_pages/                 # all the pages, not default, added in config file with includes
├── \_projects/                 # not default, added in config file as a collection
├── \_site/                   # Generated output (auto-created, do not edit)
└── Gemfile / Gemfile.lock   # Ruby dependencies (like the theme)


post, page and home inherit from base
home inherits from post
page inherits from home

include.path can be changed in the config file

page.property is written in each .md file at the top, front matter

assets/css/style.scss is the main sass file, has front matter, import statements can be added here

using bootstrap4 because bootstrap 5 is not compatible with jekyll-sass-reader since it uses an old sass engine called LibSass
One can stop Jekyll from processing sass and use an external engine (installed using npm) for that, but that is overkill 
`npm install boostrap`

After adding something to hte GemFile you need to do `bundle install`

<!-- You can also put regular text between your rows of images, even citations {% cite einstein1950meaning %}. -->

Third-party libraries and external libraries are added in the head.html

Three types of objects in HTML: block, inline and inline-block.

When inserting a figure usig figure.liquid, you can either change the image or the figure. It is prefferable to change the figure, not just the image.

Schema.org is a standard vocabulary (maintained by Google, Bing, etc.) for marking up HTML with structured data — metadata that helps search engines understand what your page is about. Exmaple: `itemtype="http://schema.org/BlogPosting"` `itemprop="headline"`
Microformats are an older, HTML-class-based way to do the same thing: embed metadata directly into class names. Instead of `itemprop`, you use class names like: `h-entry`, `p-name`, `e-content`, `u-url`, `p-author`, etc.

jekyll-tagging is added to the config file as jekyll/tagging otherwise it does not work