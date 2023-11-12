# Regular-Expressions
My Most Commonly used Regular Expressions

# Comments with Double Spaces:
This is a Regular Expression for finding comments in a file that have double spaces after the comment character and, before the first space, there is any letter or number.  This is useful for finding comments that are not formatted correctly. 
```
  \S[ ]{2}#
```
