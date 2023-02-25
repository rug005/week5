# Lab Report 3: Ruben A Gonzalez
**Researching Commands** : When using the terminal there are several different commmands we can use. Some examples are *less* , *find* , *grep*.
## grep command.

## Using *grep* Let's you grep specific string.
---
Option 1: -r
---
The -r option searches for files recursively in subdirectories.
## Using this *.grep -r "(string)"...
```
[cs15lwi23agr@ieng6-202]:skill-demo1-data:523$ grep -r "Lucayans" ./written_2
./written_2/travel_guides/berlitz2/Bahamas-History.txt:Centuries before the 
arrival of Columbus, a peaceful Amerindian people who called themselves the 
Luccucairi had settled in the Bahamas. Originally from South America, they 
had traveled up through the Caribbean islands, surviving by cultivating modest 
crops and from what they caught from sea and shore. Nothing in the experience 
of these gentle people could have prepared them for the arrival of the Pinta, 
the Niña, and the Santa Maria at San Salvador on 12 October 1492. Columbus 
believed that he had reached the East Indies and mistakenly called these people
Indians. We know them today as the Lucayans.
```
When we try to do the same command, but instead in lower case we get...
```
[cs15lwi23agr@ieng6-202]:skill-demo1-data:527$ grep -r "lucayans" ./written_2
[cs15lwi23agr@ieng6-202]:skill-demo1-data:528$ 
```
---
Option 2: -i
---
We have a file names "file.txt" which contains,
```
[cs15lwi23agr@ieng6-202]:written_2:547$ cat fruit.txt 
APPLE
BANANA
ORANGE
```
```
This command makes the search case-insensitive.
[cs15lwi23agr@ieng6-202]:skill-demo1-data:543$ grep -i "apple" written_2/fruit.txt
APPLE
```
We can see from this that we searched the word APPLE using lower case letters. This is something we can't
do when using -r.
---
Option 3: -v 
This command prints all lines that do not match the pattern.
```
[cs15lwi23agr@ieng6-202]:written_2:558$ cat results.txt 
negative
positive
positive
negative
positive
negative
positive
negative
negative
positive
negative
negative
negative
```
As we can see below, this can be very helpful whenever you'd like to avoid printing out a specific text (in this example being the times people have tested negative)
```
[cs15lwi23agr@ieng6-202]:skill-demo1-data:563$ grep -v "negative" written_2/results.txt 
positive
positive
positive
positive
positive
```


