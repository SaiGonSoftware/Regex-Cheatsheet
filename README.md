# Regex Cheat Sheet

### The original cheat sheet can be found here https://www.rexegg.com/regex-quickstart.html

## Characters
| Character  | Legend  | Example  | 	Sample Match  |
| ------------ | ------------ | ------------ | ------------ |
| \d  | Most engines: one digit from 0 to 9  | file_\d\d  |  file_25 |
| \w  |  Most engines: "word character": ASCII letter, digit or underscore  | \w-\w\w\w	  | A-b_1  |
|  \s  |  Most engines: "whitespace character": space, tab, newline, carriage return, vertical tab |  a\sb\sc  |  	a b <br></brc>c |
|  \D |  	One character that is not a digit as defined by your engine's \d |  \D\D\D  |  ABC |
|  \W |  	One character that is not a word character as defined by your engine's \w |  \W\W\W\W\W	 |  *-+=) |
|  \S |  One character that is not a whitespace character as defined by your engine's \s |  \S\S\S\S	 |  Yoyo |

## Quantifiers
| Character  | Legend  | Example  | 	Sample Match  |
| ------------ | ------------ | ------------ | ------------ |
|  +  |  One or more	  | Version \w-\w+	 | Version A-b1_1  |
| {3}	  | Exactly three times	  | \D{3}	  | ABC  |
| {2,4}	  | Two to four times	  | \d{2,4}	  | 156  |
| {3,}	  | Three or more times	  |  \w{3,}	  | regex_tutorial  |
| *  | Zero or more times	  | A*B*C*	  |  AAACC |
|  ? |  Once or none	 |  plurals?	 |  plural |

## More Characters
| Character  | Legend  | Example  | 	Sample Match  |
| ------------ | ------------ | ------------ | ------------ |
|  .  | 	Any character except line break  | a.c  | abc  |
|  .  | 	Any character except line break  | .*  |  whatever, man. |
|  \\. | 	A period (special character: needs to be escaped by a \)  | a\\.c |  	a.c |
|  \ |  Escapes a special character |  \\.\\*\+\?    \$\^\/\\\ | 	.*+?    $^/\  |
|  \ |  Escapes a special character |  \\[\\{\(\\)\}\\]	 |  [{()}] |

## Logic
| Character  | Legend  | Example  | 	Sample Match  |
| ------------ | ------------ | ------------ | ------------ |
| &#124; | Alternation / OR operand	  | 22&#124;33	  | 33  |
|  ( … )  | Capturing group	  | A(nt&#124;pple) |  Apple (captures "pple") |
|  \\. | 	A period (special character: needs to be escaped by a \)  | a\\.c |  	a.c |
|  \ |  Escapes a special character |  \\.\\*\+\?    \$\^\/\\\ | 	.*+?    $^/\  |
|  \ |  Escapes a special character |  \\[\\{\(\\)\}\\]	 |  [{()}] |

## More white space
| Character  | Legend  | Example  | 	Sample Match  |
| ------------ | ------------ | ------------ | ------------ |
| \t | Tab	  | T\t\w{2}  | T     ab  |
|  \r  | Carriage return character	  |  see below	 |   |
|  \n	 | Line feed character	 | see below	 |  |
|  \r\n | Line separator on Windows	 | AB\r\nCD	| AB <br/> CD  |

## More Quantifiers
| Character  | Legend  | Example  | 	Sample Match  |
| ------------ | ------------ | ------------ | ------------ |
| + | 	The + (one or more) is "greedy"  | \d+	  | 12345  |
|  ?  | Makes quantifiers "lazy"	 |   \d+?	 |  1 in 12345 |
|  *  | The * (zero or more) is "greedy"	 | A* |  AAA |
|  ? | Makes quantifiers "lazy"	 | A*?| empty in AAA  |
|  {2,4} | Two to four times, "greedy" 	 | \w{2,4} | abcd  |
|  ? | Makes quantifiers "lazy"		 | \w{2,4}?	| ab in abcd |

## Character Class
| Character  | Legend  | Example  | Sample Match  |
| ------------ | ------------ | ------------ | ------------ |
| [ … ]  | 	One of the characters in the brackets  | [AEIOU]	  | One uppercase vowel|
| [ … ]  |  	One of the characters in the brackets | T[ao]p	  | Tap or Top  |
|  -  | Range indicator	  | [a-z]	  | One lowercase letter  |
|  [ … ]	  | One of the characters in the brackets	  | [AB1-5w-z]	   |  One of either: A,B,1,2,3,4,5,w,x,y,z|
| [x-y]  | One of the characters in the range from x to y	  | [ -~]+	  | Characters in the printable section of the ASCII table.  |
| [^x]  | One character that is not x	  | [^a-z]{3}	  | A1!  |
| [^x-y]  | One of the characters not in the range from x to y	  | [^ -~]+	  | Characters that are not in the printable section of the ASCII table.  |
| [\d\D]	  | One character that is a digit or a non-digit  | [\d\D]+	  | Any characters, including new lines, which the regular dot doesn't match |
| [\x41]  |  Matches the character at hexadecimal position 41 in the ASCII table, i.e. A | [\x41-\x45]{3}	  |  ABE |

## Character Class
| Character  | Legend  | Example  | Sample Match  |
| ------------ | ------------ | ------------ | ------------ |
| [ … ]  | 	One of the characters in the brackets  | [AEIOU]	  | One uppercase vowel|
| [ … ]  |  	One of the characters in the brackets | T[ao]p	  | Tap or Top  |
|  -  | Range indicator	  | [a-z]	  | One lowercase letter  |
|  [ … ]	  | One of the characters in the brackets	  | [AB1-5w-z]	   |  One of either: A,B,1,2,3,4,5,w,x,y,z|
| [x-y]  | One of the characters in the range from x to y	  | [ -~]+	  | Characters in the printable section of the ASCII table.  |
| [^x]  | One character that is not x	  | [^a-z]{3}	  | A1!  |
| [^x-y]  | One of the characters not in the range from x to y	  | [^ -~]+	  | Characters that are not in the printable section of the ASCII table.  |
| [\d\D]	  | One character that is a digit or a non-digit  | [\d\D]+	  | Any characters, including new lines, which the regular dot doesn't match |
| [\x41]  |  Matches the character at hexadecimal position 41 in the ASCII table, i.e. A | [\x41-\x45]{3}	  |  ABE |

## Anchors and Boundaries
| Character  | Legend  | Example  | Sample Match  |
| ------------ | ------------ | ------------ | ------------ |
|  ^	 | 	Start of string or start of line depending on multiline mode. (But when [^inside brackets], it means "not")  | ^abc .*  |  abc (line start) |
| $  |  End of string or end of line depending on multiline mode. Many engine-dependent subtleties. |  .*? the end$	 | this is the end  |
| \A  | 	Beginning of string (all major engines except JS)  | \Aabc[\d\D]*	  |  	abc (string......start) |
|  \z	 |  	Very end of the string Not available in Python and JS |  the end\z	 |  this is...\n...the end|
|  \Z |  End of string or (except Python) before final line break Not available in JS |  the end\Z	 |  this is...\n...the end |
|  \G  |  Beginning of String or End of Previous Match .NET, Java, PCRE (C, PHP, R…), Perl, Ruby |   |   |
|  \b |  	Word boundary Most engines: position where one side only is an ASCII letter, digit or underscore |  Bob.*\bcat\b	 | Bob and the cat  |
| \b  | 	Word boundary .NET, Java, Python 3, Ruby: position where one side only is a Unicode letter, digit or underscore  | Bob.*\b\кошка\b	  | Bob ate the кошка  |
| \B	|  	Not a word boundary | c.*\Bcat\B.*	|copycats |

## POSIX Classes
| Character  | Legend  | Example  | Sample Match  |
| ------------ | ------------ | ------------ | ------------ |
| [:alpha:]   | PCRE (C, PHP, R…): ASCII letters A-Z and a-z  | [8[:alpha:]]+	  | WellDone88  |
| [:alpha:]  | Ruby 2: Unicode letter or ideogram	  | [[:alpha:]\d]+	  | кошка99  |
| [:alnum:]	 | PCRE (C, PHP, R…): ASCII digits and letters A-Z and a-z	  | [[:alnum:]]{10}	  |  ABCDE12345 |
| [:alnum:]	  |  Ruby 2: Unicode digit, letter or ideogram	 | [[:alnum:]]{10}	  | кошка90210  |
|  [:punct:]	 | PCRE (C, PHP, R…): ASCII punctuation mark	  | [[:punct:]]+	  | ?!.,:;  |
| [:punct:]	  | Ruby: Unicode punctuation mark	  | [[:punct:]]+	  |  ‽,:〽⁆ |

## Inline Modifiers
| Character  | Legend  | Example  | Sample Match  |
| ------------ | ------------ | ------------ | ------------ |
| (?i)   | 	Case-insensitive mode (except JavaScript) |(?i)Monday	 |  monDAY |
| (?s)   | 	DOTALL mode (except JS and Ruby). The dot (.) matches new line characters (\r\n). Also known as "single-line mode" because the dot treats the entire input as a single line | (?s)From A.*to Z	 |  	From A to Z |
| (?m) | 	Multiline mode (except Ruby and JS) ^ and $ match at the beginning and end of every line | (?m)1\r\n^2$\r\n^3$	 |  1<br>2 <br>3 |
| (?m)  |  In Ruby: the same as (?s) in other engines, i.e. DOTALL mode, i.e. dot matches line breaks| (?m)From A.*to Z	| From A to Z  |
| (?x)   | 	Free-Spacing Mode mode (except JavaScript). Also known as comment mode or whitespace mode ||   |
| (?n)   | 	.NET, PCRE 10.30+: named capture only | Turns all (parentheses) into non-capture groups. To capture, use named groups.	 |   |
| (?d)  | 	Java: Unix linebreaks only |The dot and the ^ and $ anchors are only affected by \n	 |   |
| (?^)  | PCRE 10.32+: unset modifiers |Unsets ismnx modifiers	 |   |

## Lookarounds
| Character  | Legend  | Example  | Sample Match  |
| ------------ | ------------ | ------------ | ------------ |
|(?=…)   | Positive lookahead |(?=\d{10})\d{5}	| 01234 in 0123456789 |
| (?<=…)   | Positive lookbehind |(?<=\d)cat	 |  cat in 1cat|
| (?!…)	  | Negative lookahead | (?!theatre)the\w+	 | theme|
| (?<!…) | Negative lookbehind |\w{3}(?<!mon)ster	 | Munster  |
