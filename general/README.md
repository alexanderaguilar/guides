![image](https://dl.dropboxusercontent.com/u/2402696/external/logo-sancho.png)

#General Guidelines

*version 1.0.0*

##Table of Contents
1. [**Introduction**](#introduction)
1. [**Formatting Rules**](#formatting-rules)
1. [**Style Rules**](#style-rules)
1. [**Comments Policy**](#comments-policy)
  - [Annotations](#annotations)
1. [**References**](#references)
1. [**Contributors**](#contributors)
1. [**License**](#license)

##Introduction

This document defines general purpose formatting and style rules. It aims at
improving collaboration, code quality, and enabling supporting
infrastructure. It applies to raw, working files. Tools are free to
obfuscate, minify, and compile as long as the general code quality is
maintained.

Every file must apply this rules **except** when overridden by specific
filetype, framework or project guidelines.

To keep consistency across the project, some rules can be globally overridden
based on the main language or framework used - e.g. If a PHP framework's guide
suggests using tabs instead of spaces, tabs should be used not only on the PHP
files but on stylesheets, markup and scripts as well.

Tune up your IDE or text editor to follow this rules.

**[[⬆]](#table-of-contents)**

##Formatting Rules

- Use UTF-8 without BOM
- Use Unix line endings - LF, **not** CR (MacOS) or LF+CR (Windows)
- Use 4 white spaces indentation

  ```javascript
  // Way to go:
  if (indent === 4) {
  ····var imHappy = true;
  }
  ```

  ```javascript
  // Avoid this:
  ··var twoSpaces;
  ↦   var orTabs;
  ```

- Remove trailing white spaces

  ```html
  <div class="error">Trailing white spaces ahead</div>····
  ```

- Use a single blank line to separate code blocks

  ```javascript
  // This is cool:
  var me = 'Hello';
  ····
  me = me + ' world!';
  me = me + ' Wazzup?!';
  ····
  var world = 'I am fine';
  ```

  ```javascript
  // This is not:
  var me = 'Hello';
  ····
  ····
  ····
  var world = 'Sorry, too many white lines, I cannot hear you';
  ```

- Leave a single blank line at the end of the file

  ```javascript
  // Don't:
  endOfFile = true;
  ····
  ····
  ····
  ```

  ```javascript
  // Don't:
  endOfFile = true; // That's it, no blank lines
  ```

  ```javascript
  // Do:
  endOfFile = true;
  ····
  ```

- Limit lines to 80 characters ✍

**[[⬆]](#table-of-contents)**

##Style Rules

- Identifiers and arbitrary names
  - Must be written in **English**
  - Should be meaningful
  - Should be as short as possible but as long as necessary
  - Should be abbreviated only if it's a well known convention (e.g. ```nav```
    instead of ```navigation```)
  - Should be consistent across the project, even across different filetypes

    ```html
    <!-- This is awful (song, mp3 and audio to refer the same thing) -->

    <script>
        var song = $('.mp3');
        ····
    </script>

    ····

    <a href="····" class="mp3">
        <?php echo $audio; ?>
    </a>

    ····
    ```

    ```html
    <!-- This is much nicer (track everywhere) -->

    <script>
        var track = $('.track');
        ····
    </script>

    ····

    <a href="····" class="track">
        <?php echo $track; ?>
    </a>

    ····
    ```

**[[⬆]](#table-of-contents)**

##Comments Policy

- Write self-explanatory expressive code instead of heavily documented one
- Keep existing comments up-to-date
- Write comments in **English**
- Avoid commented lines of code
- Avoid superfluous comments

> **TODO**: When to use comments

**[[⬆]](#table-of-contents)**

###Annotations ✍

- Mark todos and action items with ```TODO```
- Use the following format: ```TODO(contact): action item``` where ```contact```
  is your username or email
- Avoid using other annotations like ```FIXME```, ```OPTIMIZE```, etc
- Annotations should be written one line immediately above the relevant code

```html
<!-- TODO(joe.doe): remove optional tags -->
<ul>
    <li>Apples</li>
    <li>Oranges</li>
</ul>
```

**[[⬆]](#table-of-contents)**

##References

- Comments Policy based on:
  - [The Ruby Style Guide](https://github.com/bbatsov/ruby-style-guide#comments)
  - [Google HTML/CSS Style Guide](http://google-styleguide.googlecode.com/svn/trunk/htmlcssguide.xml)

**[[⬆]](#table-of-contents)**

##Contributors

  - [View Contributors](../../../graphs/contributors)

**[[⬆]](#table-of-contents)**

##License

(The MIT License)

Copyright (c) 2013 Sancho BBDO

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

**[[⬆]](#table-of-contents)**

