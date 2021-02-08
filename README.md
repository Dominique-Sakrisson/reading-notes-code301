# Template Literals

template literals are made by using the backticks under the ESC key. 

These allow for functionality to be embedded into strings. Used to be called template strings in ES2015

`They can be used for multiline strings.`
Template literals can contain placeholders and those can be passed expressions 


# Getting Literal (google read)
ES6 Template Strings introduce a way to define strings with domain-specific languages (DSLs), bringing better
- string interpolation
- Embedded expressions
- Multiline strings without hacks
- String formatting
- String tagging for safe HTML escaping,localization and more

### String substitution
Substitution allows us to take any valid js expressions and inside a template literal the result will be the output as part of the string

template strings can contain placeholders using the syntax: ${expression}
template strings deliver the opportunity for multiline strings without doing any hacky type of workarounds 

# Template literals CSS
Covered much of the same information from the previous topics with the explained difference of HTML Templates

This has to do with typing out our html tags in combination with placeholders to grab data from an api which is used to create the display to the html page

# MDN Foreach 

The .forEach() executes a provided function once for each array element

```
arr.forEach(callback(currentValue[, index[, array]]) {
  // execute something
}[, thisArg]);
```
### Parameters
- callback, Function to execute on each element. It accepts between one and three arguments
- currentValue, Ther current element being processed in the array
- index, The indec of currentValuye in the array
- array, The array forEach() was called upon
- thisArg, value to use as this when executing callback
- return value, undefined

If an index is not defined or has been deleted the forEach will skip over those indexes 

The forEach gives greater functionality with dryer code than a regular for loop. 


# For loops VS forEach() 
The forEach is a method on the Array prototype. So it can be used on anything that is an array. 

Basically the forEach seems to be better all around than the regular for loop. This can be given a counter variable as well just like the regular for loop if you need to count. 
