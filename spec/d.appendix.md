# D. Appendix: File Naming Conventions

In [Directory Layout](#sec-Directory-Layout), we discussed ways we can organize files for different components.

Here we discuss ways to name files.

## Source File Names

When we remove the extension from the filename it should satisfy following conditions:

* All letters should be lower case.
* Filename should be [alphanumeric](https://en.wikipedia.org/wiki/Alphanumeric) and can have the `_` symbol.
* Filename should start with a letter.

Here's the regular expression for the above rules:

```js
/^[a-z]+[a-z0-9_]+$/
```

## Test File Names

This is how we name files inside the `tests` directory. Here are the rules:

* There should be an identical filename in the source directory.
* If not, when removing the postfix, there should be an identical filename in the source directory.

### Postfix

Most of the time, we can have a test file for each source file. Sometimes, we need to create multiple test files for a single source file. That's where we'll use a postfix.

If that source filename is `posts.js`, then with the postfix it'll look like this:

```
posts-part1.js
posts-part2.js
```

This is the regular expression for the above rules:

```js
/^([a-z]+[a-z0-9_]+)(\-[a-z]+[a-z0-9_]+)*$/
```
