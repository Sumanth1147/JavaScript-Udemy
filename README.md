Containes javascript important code snippets(reference- udemy js course) and react udemy resources
   Javascript, ( udemy )



Useful shortcuts (VS Code)
CTRL + S (save) - save file

CTRL + C (copy) - copy

CTRL + V - paste

CTRL + X - cut

CTRL + Z - undo the action

CTRL + Y - redo the action

CTRL + F (find) - looking in file

CTRL + A (all) - selecting all files

TAB - indent

SHIFT + TAB - back indent

END / HOME - jump to the end / beginning of line

SHIFT + END / SHIFT + HOME - selecting line to the end / to the beginning from the caret place

SHIFT + ARROWS up / down - selecting/deselecting full lines

SHIFT + ARROWS left / right - selecting a letter to the left / right

CTRL + SHIFT + arrow keys left/right - selecting full word left/right

CTRL + SHIFT + arrows keys down/up - copying full line down

CTRL + HOME - jumping to the beginning of file

CTRL + END - jumping to the end of file

CTRL + SHIFT + HOME - selecting text from caret to the beginning of file

CTRL + SHIFT + END - selecting text from caret to the end of file





Scope of Variables - fast text summary
Global variables can be accessed everywhere in your script.
A local variable created inside the function is hidden from other functions and other scripting code. When you create a local and a global variable with the same name you can access / change both and they won't interfere with each other.
Local variable is deleted after the function returns the value freeing memory.
Variables created without the keyword var are always global even if they are created inside a function. So be careful because assigning value to the variable that was not yet declared is creating a new global variable.



var a = 5;


function ex() {


   var a = 3;
  console.log(a);
}
ex();
// a=4;
console.log(a);
3
5



The name of function should be a verb (action) like getValueFromListItem.
Function constructor (class) name shouldn't be a verb.
It allows you to distinguish easier which one is which.




=>The name of function should be a verb (action) like getValueFromListItem.
Function constructor (class) name shouldn't be a verb.
It allows you to distinguish easier which one is which.



=> Prototype is used for adding properties / methods to existing function constructor (class).The change using prototype is affecting all objects that are gonna be created in future. It is used for example for creating plugins for frameworks.





for (var i = 0; i < 4; i++) //  first take i=0, then send value further , then make increment
{
 alert(i);
}
what will be the last alerted value?
3






You should be careful when using innerHTML because it is gonna re-parse everything inside the element which means you gonna lose references to variables. If you want to keep references it's most time better to use createElement.
True

   





RegExp Object reference
REGEXP
regular expressions - formulas
/pattern/modifiers
stringToSearch.search(formula) - searches and return the index
stringToSearch.match(formula) - searches and returns an array
regExpVar.exec(stringToSearch) - same as above but it returns only one result after each execution
stringToSearch.replace(formula, "forWhat"); - replacing things in formula by "forWhat"
formula.test(stringToSearch); - testing if something from formula exists in stringToSearch
Modifiers:
g - global - searching through full string
i - insensitive - case Insensitive
What formulas(patterns) can you create using RegExp?
-----------------------------------------------------------------------------
. - any character
formula: /.ag/ - it will find rag, bag, 4ag, $ag etc.
formula: /A..k/ - it will find Arek A4Gk, etc.
-----------------------------------------------------------------------------
* - Matches any string that contains zero or more occurrences of the preceding character
formula /M*arek/i - it will match Arek, arek, Marek, marek, mmarek,MMarek MMarek, MmMmmmmmarek ...
-----------------------------------------------------------------------------
+ - Matches any string that contains one or more occurrences of the preceding character
conclusion: it requires preceding character at LEAST once.
formula /fe+d/ matches feed and fed but doesn't match fd
-----------------------------------------------------------------------------
? -Matches any string that contains zero or one occurrences of the preceding character
conclusion: the character can exist but it doesn't need to
formula /M?arek/ - it will match Arek, arek, Marek, marek.
-----------------------------------------------------------------------------
{n} - Matches any string that containts EXACTLY n occurences of the preceding character
formula /Zo{2}/ - it will match only Zoo.
-----------------------------------------------------------------------------
{n,} - Matches any string that containts n or more occurences of the preceding character
formula /Zo{2,}/ - it will match Zoo, Zooooo, Zoooooooo
-----------------------------------------------------------------------------
{n,m} - Matches any string that containts minimally n occurences or maximally m occurences of preceding character
formula/Zo{2,4}/ - it will match Zoo, Zooo, Zoooo
-----------------------------------------------------------------------------
^ - Only matches the beginning of a string
formula /^the/i - it will match "The hole" it won't match "In the hole";
-----------------------------------------------------------------------------
$ - Only matches the end of a string
formula /g$/i - it will match only string that ends with 'g' character
-----------------------------------------------------------------------------
[ao] - Match any of the character enclosed in the character set. (think as it it was a single character to match)
for example /A[BT]C/ - matches ABC and ATC - doesn't match ABTC or AKC
-----------------------------------------------------------------------------
[^ao] -
for example /A[^BT]C/ - matches everything EXCEPT ABC and ATC so it matches ADC, AKC etc.
-----------------------------------------------------------------------------
[a-d] - matches any single character in a scope from 'a' to 'd'
so a, b, c, d
Conclusion: [0-9] - any number - same as \d
[a-z] - any small case character
[A-Z] - any large case character
[a-zA-Z] - any character
/w - any character [A-Za-z0-9_]
-----------------------------------------------------------------------------
[^a-d] - matches every single character except a,b,c,d
-----------------------------------------------------------------------------
\ - this character allows you to interpret reserved character like *, ., ^ etc. as a character to search for
formula /f\*\*\*/ will match f***
-----------------------------------------------------------------------------
\s - white character
-----------------------------------------------------------------------------
(x) - saves x;
np.
var d = "ViolaArkadiusz";
var e = d.replace(/(V)(i)(o)(la)/gi, "$4$3$2$1");
results in: laoiVArkadiusz
([a-z][0-9])+ any number of occurences like a4j5j5n5
[a-z][0-9]+ means: a1241241241241241
-----------------------------------------------------------------------------
x(?=y) - will match x only if y is after the x
var a = "Arek Wlodarczyk, Arkadiusz Kowalski, Arek Nowak";
var b = a.replace(/Arek.(?=Wlodarczyk)/gi, ""); - will remove Arek with Wlodarczyk surname because it's only name with Wlodarczyk after Arek
-----------------------------------------------------------------------------
x(?!y) - same as above x(?=y), but it will find x only if there is no y
-----------------------------------------------------------------------------
x|y - matches x or y
great for checking extensions: /jpg|gif/gi - will match = "landscape.GIF" the GIF word.

The JavaScript prototype property allows you to add new properties,methods to object constructors:






