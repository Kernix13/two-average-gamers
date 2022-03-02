# Website Redesign

1. Create and edit template files.
1. Create cusom CSS for each page template
1. Add custom functions to `functions.php`: 1) enqueue Google scripts, 2) Other...

## Astra Child Theme

Add the correct template files and then change the PHP and CSS for custome designs. 

## Images

Two 2 redesigns for main logo:
- TAG-logo-redesign1.png: text center aligned
- TAG-logo-redesign2.png: text left-aligned

Consider changing the text to website custom colors, and maybe even as linear-gradients. IF kept black, change the text from #000 to #333.


## Template files

A list of the current template files used for each page:
- `archive.php`
- `page.php`
- `search.php`
- `single.php`

A list of template files that are missing from the parent theme:
- `category.php` for the category archive pages (Copied archive.php)
- `front-page.php` for the Home page (Copied page.php)
- `home.php` for the main blog page (Copied index.php)
- `author.php` for the author pages (Copied archive.php)
- `comments.php` for the comments section - copied my comments.php and changed the textdomain but what about `$tower_`? Consider asking in Astra's forum what they recommend as the source code.

### Home page

- URL: https://twoaveragegamers.com/
- Current Template: `page.php`
- Home should be `front-page.php`

### Raad page (main blog page)

- URL: https://twoaveragegamers.com/read-new/
- Current Template: `page.php`
- The main blog page should be `home.php`

### Simple post pages

- URL example: https://twoaveragegamers.com/the-best-valorant-agents-to-play-right-now/
- Current Template: `single.php`(CORRECT)

### Category pages

- URL example: https://twoaveragegamers.com/category/nintendo/
- Current Template: `archive.php`
- Categories pages should be `category.php`
- Category pages: Nintendo, PC, Playstation, XBOX, Tabletop, TAG (TAG roundup, TAG guides, TAG Mount Rushmore, TAG Previews, TAG REviews)

### Author pages

- URL example: https://twoaveragegamers.com/author/yoshyaes/
- Current Template: `archive.php`
- Author pages should be `author.php`

### Search pages

- URL example: NA
- Current Template: `search.php`(CORRECT)

### All other pages

- URL: https://twoaveragegamers.com/read-new/
- Current Template: `page.php` (CORRECT)

### Comments

- No template?





