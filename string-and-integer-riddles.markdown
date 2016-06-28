## String and Integer Riddles

### Strings

* How can I tell how many characters are in a string? Do spaces count?
    * .length method will return # of characters. spaces do count. 

* How can I capitalize the first character of a string? What
happens if it is a number?
    * .capitalize capitalizes the first letter, a number does nothing when capitalized.

* How can I turn a string backwards?
    * reverse a string with .reverse, you can

* How can I tell if two words have the same number of characters?
    * string1.length == string2.length

* How can I tell if a word has all capital letters?
    * string.upcase == string

* How can I tell if a word has all lower case letters?
    * string.downcase == string

* How can I tell if a word is a palindrome? (The word is the same forwards and
  backwards.)
    * string.reverse == string

* How can I tell if a sentence is the same forwards and backwards? (ignoring spaces and punctuation)
    * To completely remove punctuation, regex is the best solution. To ignore punctuation at the end .chop is useful
    * string.delete(" ").chop.reverse == string
    * or more sanely - de-spaced_string = string.delete(" ")
    * ending_punctuation_removed_string = string.chop
    * ending_punctuation_removed_string.reverse === string
    * better alternative to chop and delete space - string.delete(" ,.!?'-")

* How can I replace an occurrence of a single character in a string with another
character?
    * string.sub("replaced char","replacing char")

* How can I replace ALL occurrences of a single character in a string with
another character?
    * string.gsub("replaced char","replacing char")

* How do I insert 5 asterisks at the start of a string? What about at the end of
a string? What about x asterisks?
    * string.prepend(" * "*5)
    * string << " * "*5
    * replace 5 w/ x

* What if I wanted to have a string that's four characters long, but I want to
make a big string thats 14 characters in length, with the original string in the
middle, with asterisks on either side of the original string to make it reach
the desired length?
    * length = n
    * padding_character = "char"
    * extra_length = length - word_to_pad.length
    * word_to_pad.prepend(padding_chaacterr*extra_length/2)
    * word_to_pad << padding_character*extra_length/2
    * 
    * center
    * ljust
    * rjust

* What if I wanted to replace the padding character with spaces? And a variable
total length?
    * see above

* What are two ways in which you can determine if an integer is odd? (Or even.)
    * num % 2 == 0 (returns true if even, false if odd)
    * num.even? num.odd?

* How can I convert a string into a number?
    * string.to_i, though this wouldn't get something like "five"

* How can you tell if a number is a palindrome? (303, 1221, 123321)
    * number.to_s.reverse == number.to_s

* How can you tell if a number is divisible by 3? By 9? By x?
    * number % 3 == 0, number % 9 == 0, number % x == 0
