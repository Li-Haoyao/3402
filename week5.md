# Week 5

## Learning Activities & Resources

This week I focused on learning how to create and customise a WordPress child theme. I studied why child themes are used, how they connect to a parent theme, and how custom CSS and `functions.php` can be used to safely change the appearance of a WordPress website.

Resources used:

* WordPress Developer Documentation: Child Themes
  https://developer.wordpress.org/themes/advanced-topics/child-themes/

* WordPress Theme Handbook
  https://developer.wordpress.org/themes/

* WordPress documentation
  https://wordpress.org/documentation/

* CSS reference from MDN
  https://developer.mozilla.org/en-US/docs/Web/CSS

* Browser Developer Tools guide
  https://developer.chrome.com/docs/devtools/

During the practical, I created a child theme folder inside the WordPress `themes` directory. I created a `style.css` file with the correct theme information and parent theme template name. I also created a `functions.php` file to enqueue the parent and child theme styles correctly.

I also used the browser inspector to test small CSS changes before copying the final code into the child theme stylesheet.

---

## Estimated Hours of Explicit Learning Activity

Approximately 5 hours.

---

## Content Insights

This week I learned that a WordPress child theme allows me to customise an existing theme without directly editing the parent theme files. This is important because changes made directly to a parent theme can be lost when the theme is updated. A child theme keeps custom changes separate and safer.

I learned that a basic child theme needs at least two important files:

* `style.css`
* `functions.php`

The `style.css` file includes information about the child theme, including the theme name and the parent theme template. For example:

```css
/*
Theme Name: Startup Child Theme
Template: twentytwentyfour
*/
```

The `Template` line is very important because it tells WordPress which parent theme the child theme depends on. If the template name is wrong, the child theme may not work properly.

I also learned that `functions.php` is used to load the CSS files correctly. This is called enqueueing styles. Instead of simply linking CSS manually, WordPress uses functions to load styles in the correct way.

Example:

```php
<?php
function startup_child_enqueue_styles() {
    wp_enqueue_style('parent-style', get_template_directory_uri() . '/style.css');
    wp_enqueue_style('child-style', get_stylesheet_directory_uri() . '/style.css', array('parent-style'));
}
add_action('wp_enqueue_scripts', 'startup_child_enqueue_styles');
```

For my child theme, I planned at least six visible customisations, such as:

* Changing the website background colour
* Customising the navigation bar style
* Changing heading fonts and sizes
* Improving button colours and hover effects
* Adding card-style sections for services or features
* Adjusting spacing and layout for a cleaner homepage
* Improving footer design
* Making images have rounded corners or shadow effects

This practical helped me understand that small design changes can make a website look more professional. It also showed me that CSS customisation is easier when I test changes first in the browser inspector and then copy the working code into the stylesheet.

Another thing I learned is that WordPress customisation needs both design thinking and technical accuracy. A small mistake in the `Template` name, file location, or PHP function can stop the child theme from working correctly. This means careful file structure and naming are very important.

---

## Career/Employability/Learning Insights

This week helped me understand why child themes are useful in real WordPress development. Many businesses use existing WordPress themes, but they still need custom branding, colours, layouts, and visual changes. A child theme allows developers to customise a site professionally without damaging the original theme.

From an employability perspective, I think child theme knowledge is useful because WordPress is widely used by small businesses, organisations, and freelance clients. A beginner developer who can create a child theme, edit CSS, and understand the basic WordPress file structure can provide practical value to clients.

The LinkedIn post task also made me think about how I present my learning publicly. Instead of only completing work for marks, I need to explain what I learned in a way that sounds professional and understandable to others. This is useful because employers may look at online profiles, portfolios, GitHub repositories, or LinkedIn posts to understand a student’s skills and attitude.

One lesson I learned from this subject so far is that web development is not only about making a website look good. It also involves workflow, maintainability, deployment, and communication. For example, using a child theme is not just a design choice. It is also a professional way to protect custom work from being overwritten by future updates.

I also noticed that my learning is improving when I connect each weekly practical together. Week 1 introduced static websites, Week 2 introduced Joomla, Week 3 introduced WordPress, Week 4 introduced local development, and Week 5 introduced safer WordPress customisation through child themes. Seeing this progression helped me understand the bigger picture of website development.

For my own learning process, I found that experimenting directly is still the most effective method for me. Reading documentation is useful, but I understand the concept better when I make changes, test them, break something, and then fix the problem. This practical gave me more confidence because I could see my CSS changes visibly affect the website.
