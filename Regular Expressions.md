# Regular Expressions

Regular expressions are patterns used to match character combinations in strings. In JavaScript, regular expressions are also objects.

## Creating a regular expression

You construct a regular expression in one of two ways:

Using a regular expression literal, which consists of a pattern enclosed between slashes, as follows:

```JS

const re = /ab+c/;


```

Regular expression literals provide compilation of the regular expression when the script is loaded. If the regular expression remains constant, using this can improve performance.
Or calling the constructor function of the RegExp object, as follows:

```JS

const re = new RegExp("ab+c");


```

Using the constructor function provides runtime compilation of the regular expression. Use the constructor function when you know the regular expression pattern will be changing, or you don't know the pattern and are getting it from another source, such as user input.

## Writing a regular expression pattern

A regular expression pattern is composed of simple characters, such as /abc/, or a combination of simple and special characters, such as /ab*c/ or /Chapter (\d+)\.\d*/. The last example includes parentheses, which are used as a memory device.

## Using special characters

When the search for a match requires something more than a direct match, such as finding one or more b's, or finding white space, you can include special characters in the pattern. For example, to match a single "a" followed by zero or more "b"s followed by "c", you'd use the pattern /ab*c/: the * after "b" means "0 or more occurrences of the preceding item." In the string "cbbabbbbcdebc", this pattern will match the substring "abbbbc".

The following pages provide lists of the different special characters that fit into each category, along with descriptions and examples.

## Assertions

Assertions include boundaries, which indicate the beginnings and endings of lines and words, and other patterns indicating in some way that a match is possible (including look-ahead, look-behind, and conditional expressions).

## Character classes

Distinguish different types of characters. For example, distinguishing between letters and digits.

## Groups and backreferences

Groups group multiple patterns as a whole, and capturing groups provide extra submatch information when using a regular expression pattern to match against a string. Backreferences refer to a previously captured group in the same regular expression.

## Quantifiers

Indicate numbers of characters or expressions to match.

If you want to look at all the special characters that can be used in regular expressions in a single table, see the following:

<figure class="table-container">
<table class="standard-table">
 <caption>Special characters in regular expressions.</caption>
  <thead>
    <tr>
      <th scope="col">Characters / constructs</th>
      <th scope="col">Corresponding article</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <code>[xyz]</code>, <code>[^xyz]</code>, <code>.</code>,
        <code>\d</code>, <code>\D</code>, <code>\w</code>, <code>\W</code>,
        <code>\s</code>, <code>\S</code>, <code>\t</code>, <code>\r</code>,
        <code>\n</code>, <code>\v</code>, <code>\f</code>, <code>[\b]</code>,
        <code>\0</code>, <code>\c<em>X</em></code>, <code>\x<em>hh</em></code>,
        <code>\u<em>hhhh</em></code>, <code>\u<em>{hhhh}</em></code>,
        <code><em>x</em>|<em>y</em></code>
      </td>
      <td>
        <p><a href="/en-US/docs/Web/JavaScript/Guide/Regular_expressions/Character_classes">Character classes</a></p>
      </td>
    </tr>
    <tr>
      <td>
        <code>^</code>, <code>$</code>, <code>\b</code>, <code>\B</code>,
        <code>x(?=y)</code>, <code>x(?!y)</code>, <code>(?&lt;=y)x</code>,
        <code>(?&lt;!y)x</code>
      </td>
      <td>
        <p><a href="/en-US/docs/Web/JavaScript/Guide/Regular_expressions/Assertions">Assertions</a></p>
      </td>
    </tr>
    <tr>
      <td>
        <code>(<em>x</em>)</code>, <code>(?&lt;Name&gt;x)</code>, <code>(?:<em>x</em>)</code>,
        <code>\<em>n</em></code>, <code>\k&lt;Name&gt;</code>
      </td>
      <td>
        <p><a href="/en-US/docs/Web/JavaScript/Guide/Regular_expressions/Groups_and_backreferences">Groups and backreferences</a></p>
      </td>
    </tr>
    <tr>
      <td>
        <code><em>x</em>*</code>, <code><em>x</em>+</code>, <code><em>x</em>?</code>,
        <code><em>x</em>{<em>n</em>}</code>, <code><em>x</em>{<em>n</em>,}</code>,
        <code><em>x</em>{<em>n</em>,<em>m</em>}</code>
      </td>
      <td>
        <p><a href="/en-US/docs/Web/JavaScript/Guide/Regular_expressions/Quantifiers">Quantifiers</a></p>
      </td>
    </tr>
  </tbody>
</table></figure>


