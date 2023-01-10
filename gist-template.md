# Regex Tutorial

Usually, when looking for a certain string in a JavaScript file, users would usually do the "Ctrl+F" function and search for a specific word/letter to find what they're looking for. In some cases though, this may not work. What if a user is looking for ALL emails in the JavaScript file? Or they are looking for ALL the usernames? This is when Regex comes in play. Regex is short for "Regular Expression", which are a series of special characters that define the criteria the user is searching for. Using Regex, you can search for a specific string of characters using the special characters assigned to them. 

## Summary

In this tutorial, we'll be deciphering an example of regex which searches for emails.

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

In this case,
- "[a-z0-9_\.-]" means that the first section contains letters between a-z, numbers between 0-9, and can contain "_", ".", and "-". 
- "+@" means that there is a mandatory "@" sign between the first two sections 
- "[\da-z\.-]" means that the second section can contain a digit -- "d" --, and can also contain letters between a-z. 
- "\." means that there is a mandatory "." between the second and third section
- "[a-z\.]" means that the third section must contain letters between a-z and can contain a "."

We will now be breaking down each individual component in the regex example. 

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping](#grouping)
- [Bracket Expressions](#bracket-expressions)

## Regex Components

### Anchors
We''ll start breaking with Anchors, here is the regex example we are looking at again: 

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

Anchors signify the start and end of a regex. In this case, the "^" symbol signifies the start of the regex string and the "$" signifies the end of the regex string. 

### Quantifiers

Quantifiers are identified with the "{}" symbols.  They set the limits to the entire string, or a section of the string that they are looking for. In this case, with our example being: 

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

The only set of quantifers we see are at the last "()" of the string, meaning we are only limiting that particular part of the regex. 

### Character Classes

Character classes are variables used to define a set of characters, in our examples case -- 

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

"a-z" defines any letter between a-z,
"0-9" defines any numeral digit between 0-9,
"d" defines any numeral digit as well

### Grouping

Grouping is seen as "()" and it's purpose is to split up in regex into sections. Each section can have it's own search parameters using brackets, which are explained a little later afer this. In our example: 

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

We have three sets of "()" which is the usual format for emails. 

### Bracket Expressions

Bracket Expressions are anything inside the "[]" symbols. These symbols are used to signify the items that we are looking for. 

## Author

Github Profile -- https://github.com/ssangwang