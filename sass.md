##  SASS_REFERENCE ##

### Sass (Syntactically Awesome StyleSheets) ###
Sass is an extension of CSS that adds power and elegance to the basic language. It allows you to use variables, nested rules, mixins, inline imports, and more, all with a fully CSS-compatible syntax. Sass helps keep large stylesheets well-organized, and get small stylesheets up and running quickly, particularly with the help of the Compass style library.

### Features ###
 
----------

- Language extensions such as variables, nesting, and mixins
- Many useful functions for manipulating colors and other values
- Advanced features like control directives for libraries
- Well-formatted, customizable output

### Syntax ###

----------
There are two syntaxes available for Sass. The first, known as SCSS (Sassy CSS) and used throughout this reference, is an extension of the syntax of CSS. This means that every valid CSS stylesheet is a valid SCSS file with the same meaning. In addition, SCSS understands most CSS hacks and vendor-specific syntax, such as IE’s old filter syntax. This syntax is enhanced with the Sass features described below. Files using this syntax have the .scss extension.

The second and older syntax, known as the indented syntax (or sometimes just “Sass”), provides a more concise way of writing CSS. It uses indentation rather than brackets to indicate nesting of selectors, and newlines rather than semicolons to separate properties. Some people find this to be easier to read and quicker to write than SCSS. The indented syntax has all the same features, although some of them have slightly different syntax; this is described in the indented syntax reference. Files using this syntax have the .sass extension.

Either syntax can import files written in the other. Files can be automatically converted from one syntax to the other using the sass-convert command line tool:

```
# Convert Sass to SCSS
$ sass-convert style.sass style.scss

# Convert SCSS to Sass
$ sass-convert style.scss style.sass
```

Note that this command does not generate CSS files. For that, use the sass command described elsewhere.

### Using Sass ###

----------
Sass can be used in three ways: as a command-line tool, as a standalone Ruby module, and as a plugin for any Rack-enabled framework, including Ruby on Rails and Merb. The first step for all of these is to install the Sass gem:

```
gem install sass
```

If you’re using Windows, you may need to install Ruby first.

To run Sass from the command line, just use

```
sass input.scss output.css
```

You can also tell Sass to watch the file and update the CSS every time the Sass file changes:

```
sass --watch input.scss:output.css
```

If you have a directory with many Sass files, you can also tell Sass to watch the entire directory:

```
sass --watch app/sass:public/stylesheets
```
