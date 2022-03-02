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


## Blog ideas

GitHub repos that deal with major game brands or other game applications for new and unique article ideas:
- Haven't searched yet...

> Search issues and discussions tabs for article ideas.


## Header

Copy: https://www.dreamhustlecode.com/

Pages that are not linked to on the main site and the template files they are using:
- https://twoaveragegamers.com/about-two-average-gamers/ - page.php
- https://twoaveragegamers.com/about/ - page.php
- https://twoaveragegamers.com/read-new/ - page.php
- https://twoaveragegamers.com/read/ - page.php

Which Read page is/should be the main blog page. We need to get rid of one of them. Also for the duplicate about pages.

## Script code in head section

Here is a comment and there is no code above it:

```html
<!-- End Google Analytics opt-out snippet added by Site Kit -->
```

But lower down is this:

```html
<!-- Google Analytics snippet added by Site Kit -->
<script src='https://www.googletagmanager.com/gtag/js?id=UA-117911972-1' id='google_gtagjs-js' async></script>
<script id='google_gtagjs-js-after'>
window.dataLayer = window.dataLayer || [];function gtag(){dataLayer.push(arguments);}
gtag('set', 'linker', {"domains":["twoaveragegamers.com"]} );
gtag("js", new Date());
gtag("set", "developer_id.dZTNiMT", true);
gtag("config", "UA-117911972-1", {"anonymize_ip":true});
</script>

<!-- End Google Analytics snippet added by Site Kit -->
```

And even more Site Kit code:

```html
<!-- Google AdSense snippet added by Site Kit -->
<meta name="google-adsense-platform-account" content="ca-host-pub-2644536267352236">
<meta name="google-adsense-platform-domain" content="sitekit.withgoogle.com">
<!-- End Google AdSense snippet added by Site Kit -->

<!-- Google AdSense snippet added by Site Kit -->
<script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-2995836029247816" crossorigin="anonymous"></script>

<!-- End Google AdSense snippet added by Site Kit -->
```

Here is Analytics:

```html
<script id='google_gtagjs-js-after'>
window.dataLayer = window.dataLayer || [];function gtag(){dataLayer.push(arguments);}
gtag('set', 'linker', {"domains":["twoaveragegamers.com"]} );
gtag("js", new Date());
gtag("set", "developer_id.dZTNiMT", true);
gtag("config", "UA-117911972-1", {"anonymize_ip":true});
</script>
```

Here is google tag manager script:

```html
<script src="//www.googletagmanager.com/gtag/js?id=UA-117911972-1"  data-cfasync="false" data-wpfc-render="false" async></script>
```

Here is something else for Google:

```html
<script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-2995836029247816" crossorigin="anonymous"></script></head>
```

And here is the code I added to functions.php to property load Analytics though I changed the link to your link and the UA code for yours:

```php
// inline google analytics script via wp_print_scripts
function tower_google_print_scripts() { 
	
	?>
<!-- Global site tag (gtag.js) - Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=UA-117911972-1"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'UA-117911972-1');
</script>
	
	<?php
	
}
add_action('wp_print_scripts', 'tower_google_print_scripts');
```


I 
