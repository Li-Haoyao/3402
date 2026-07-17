# Week 7

## Learning Activities & Resources

This week I focused on learning the basic features of PHP and how PHP can be used to create dynamic web pages. Compared with HTML and CSS, PHP runs on the server side, so it can make decisions, repeat content, use functions, and reuse common page parts such as headers and footers.

Resources used:

* PHP official documentation
  https://www.php.net/docs.php

* PHP echo documentation
  https://www.php.net/manual/en/function.echo.php

* PHP if/else documentation
  https://www.php.net/manual/en/control-structures.if.php

* PHP loops documentation
  https://www.php.net/manual/en/language.control-structures.php

* PHP include documentation
  https://www.php.net/manual/en/function.include.php

* W3Schools PHP tutorial
  https://www.w3schools.com/php/

During the practical, I wrote and tested PHP code that demonstrated `echo`, `if/else` decisions, loops, arrays, functions with parameters, and `include`. I also created more than one PHP page and used a shared header or footer file to avoid repeating the same HTML structure.

---

## Estimated Hours of Explicit Learning Activity

Approximately 5 hours.

---

## Content Insights

This week I learned that PHP is different from normal HTML because PHP code is processed by the server before the final page is shown in the browser. HTML is static, but PHP can generate different HTML output depending on conditions, variables, arrays, and functions.

One basic feature I learned was `echo`. PHP can use `echo` to output normal text, HTML tags, headings, links, lists, and other page content. For example, instead of writing all HTML manually, PHP can generate part of the page:

```php
echo "<h1>Welcome to My Startup Website</h1>";
echo "<p>This page is generated using PHP.</p>";
```

I also learned how decision-making works in PHP through `if/else` statements. This allows the website to show different messages depending on a condition. For example, a startup website could show a different message depending on whether a user is a guest or a returning customer.

Loops were another important part of this week. I practised using `for`, `while`, and `foreach`. The `foreach` loop was especially useful with arrays because it allowed me to display a list of services or products without writing repeated HTML manually.

Example:

```php
$services = ["Website Design", "CMS Setup", "Basic SEO"];

foreach ($services as $service) {
    echo "<li>$service</li>";
}
```

This helped me understand how PHP can make websites easier to update. If I need to add another service, I can update the array instead of copying and pasting another HTML list item.

I also learned how functions with parameters can make code more reusable. A function can receive information and then produce output based on that information. This makes the code cleaner because repeated tasks can be placed in one function.

Another useful feature was `include`. I learned that `include` can be used to reuse common page sections such as a header, navigation bar, or footer. This is important because most websites have repeated elements on multiple pages. Instead of copying the same header into every file, I can create one `header.php` file and include it in different pages.

For example:

```php
include "header.php";
```

This practical helped me understand why dynamic websites are easier to maintain than fully static websites. When repeated sections are stored in one place, I only need to change one file to update multiple pages.

---

## Career/Employability/Learning Insights

This week helped me understand that PHP is still an important skill for web development because many websites and CMS platforms use it. WordPress, Joomla, and many older business websites depend on PHP. Even if I do not become a full PHP developer, understanding basic PHP makes it easier to understand how CMS websites work behind the scenes.

From an employability perspective, this practical showed me that employers may value developers who understand both frontend and backend basics. HTML and CSS control what users see, while PHP can control logic, repeated content, and server-side behaviour. Knowing this difference helps me understand how real websites are built.

I also realised that PHP can make code more maintainable. At first, writing PHP felt more complicated than writing HTML because I needed to think about syntax, variables, brackets, semicolons, and server setup. However, after using arrays, loops, functions, and include files, I could see how PHP reduces repetition and makes the website easier to manage.

This week also reminded me that small syntax mistakes can cause big problems. Missing a semicolon, using the wrong bracket, or placing a file in the wrong folder can stop the page from working. Because of this, I need to slow down when writing PHP and test my code step by step instead of writing too much before checking.

For my learning process, I found that PHP is easier to understand when I connect it to a real page idea instead of only following tutorial examples. For example, using arrays to list startup services or using a function to display a feature card made the code feel more meaningful. This also matched the practical requirement because the page content needed to be original, not copied from a tutorial.

I also continued thinking about group work this week. Even though the practical focused on PHP, the reminder about group work is important. A technical project can fall behind if the team only focuses on individual tasks and does not keep communicating. For the group project, I should continue checking Slack, updating the project board, and making sure my assigned work is clear.

Overall, this week helped me move from static website thinking to dynamic website thinking. I now understand that PHP is not only about writing code, but also about making websites more reusable, flexible, and easier to maintain.
