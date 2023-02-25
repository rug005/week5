# Lab Report 3: Ruben A Gonzalez
**Researching Commands** : When using the terminal there are several different commmands we can use. Some examples are *less* , *find* , *grep*.
For this lab report I'll be talking about the command "grep".
The command grep searches for lines in one or more files that match the text. After this it prints them to the standard output.

grep [OPTIONS] PATTERN [FILE...]

---
**Option 1: -r**
---
The -r option searches for files recursively in subdirectories.
---
Example 1:
```
[cs15lwi23agr@ieng6-202]:skill-demo1-data:580$ ls
written_2
[cs15lwi23agr@ieng6-202]:skill-demo1-data:581$ grep -r "quiz"
written_2/cse15l:Each week there will be an online, untimed, multiple-tries quiz 
due on Wednesday at 9 am before class (including week 1). The purpose of this quiz
is to make sure everyone has checked in on the concepts we will be using in lab on 
Wednesday and Thursday. They are open for late submission until the end of the quarter, 
but see grading below for how late submissions correspond to grades.
```
Example 2:
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
**Option 2: -i**
---
This command makes the search case-insensitive.
---
We have a file names "file.txt" which contains,
```
[cs15lwi23agr@ieng6-202]:written_2:547$ cat fruit.txt 
APPLE
BANANA
ORANGE
```
Example 1:
```
[cs15lwi23agr@ieng6-202]:skill-demo1-data:543$ grep -i "apple" written_2/fruit.txt
APPLE
```
Example 2:
```
[cs15lwi23agr@ieng6-202]:skill-demo1-data:569$ grep -i "orange" written_2/fruit.txt 
ORANGE
```
We can see from this that we searched the word APPLE using lower case letters. This is something we can't
do when using -r.

---
**Option 3: -v**
---
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

Example 1:

```
[cs15lwi23agr@ieng6-202]:skill-demo1-data:563$ grep -v "negative" written_2/results.txt 
positive
positive
positive
positive
positive
```
Example 2:
```
[cs15lwi23agr@ieng6-202]:skill-demo1-data:571$ grep -v "positive" written_2/results.txt 
negative
negative
negative
negative
negative
negative
negative
negative
```
---
**Option 4: -c**
---
Using the command grep -c prints only the count of lines that match the pattern.
Example 1:
```
[cs15lwi23agr@ieng6-202]:skill-demo1-data:564$ grep -c "negative" written_2/results.txt 
8
```
Example 2:
```
[cs15lwi23agr@ieng6-202]:skill-demo1-data:567$ grep -c "positive" written_2/results.txt 
5
```
---
# Sources 
- [IBM Documentation](https://www.ibm.com/docs/en/aix/7.2?topic=g-grep-command#grep__row-d3e144140) : The IBM Documentation website
listed a varitey of grep commands to choose from and explained their purpose.
- ChatGPT : Provided me with different grep commands and examples. This was helpful for my learning since I was able to visually see
how it works in a few seconds. I did create my own examples for this lab report and tested them out myself.
