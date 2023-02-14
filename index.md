# Lab Report 3: Ruben A Gonzalez
**Researching Commands** : When using the terminal there are several different commmands we can use. Some examples are *less* , *find* , *grep*.
## Using *find* on a directory
![Image](find.png)
In this example, we used find to find every single file inside the directory.
We can also use the command *cd* to takes you back to the root directory of the current drive.
---
## Using *cd* to go to a specific directory.
---
![Image](cd.png)
## Using *find >* to make a new file containing everything inside the written_2/ directory.
![Image](written.png)
## Using *grep* Let's you grab specific string.
![Image](grep.png)
## Using this *.grep -R "(string)" * allows you to grap any specific String.
![Image](grep-r.png)
---
We can see that the command -R in Linux/UNIX system programming training: 
[grep -R website](https://man7.org/linux/man-pages/man1/grep.1.html)
---
**File and Directory Selection**
---
![Image](-R.png)
---
**Example using -R
```
[cs15lwi23agr@ieng6-201]:written_2:550$ ls
non-fiction  travel_guides
[cs15lwi23agr@ieng6-201]:written_2:551$ grep -R "Lucayans"
travel_guides/berlitz2/Bahamas-History.txt:Centuries before the arrival of Columbus, a peaceful Amerindian people who called 
themselves the Luccucairi had settled in the Bahamas. Originally from South America, they had traveled up through the Caribbean
islands, surviving by cultivating modest crops and from what they caught from sea and shore. Nothing in the experience of these 
gentle people could have prepared them for the arrival of the Pinta, the Niña, and the Santa Maria at San Salvador on 12 October 
1492. Columbus believed that he had reached the East Indies and mistakenly called these people Indians. We know them today as the
Lucayans. Columbus claimed the island and others in the Bahamas for his royal Spanish patrons, but not finding the gold and other 
riches he was seeking, he stayed for only two weeks before sailing towards Cuba.

```
---
**Example using -r**
```
[cs15lwi23agr@ieng6-201]:written_2:548$ grep -r "Lucayans"
travel_guides/berlitz2/Bahamas-History.txt:Centuries before the arrival of Columbus, a peaceful Amerindian people who called 
themselves the Luccucairi had settled in the Bahamas. Originally from South America, they had traveled up through the Caribbean 
islands, surviving by cultivating modest crops and from what they caught from sea and shore. Nothing in the experience of these 
gentle people could have prepared them for the arrival of the Pinta, the Niña, and the Santa Maria at San Salvador on 12 October 
1492. Columbus believed that he had reached the East Indies and mistakenly called these people Indians. We know them today as the 
Lucayans. Columbus claimed the island and others in the Bahamas for his royal Spanish patrons, but not finding the gold and other 
riches he was seeking, he stayed for only two weeks before sailing towards Cuba.
```
[Linux Page](https://man7.org/linux/man-pages/man1/find.1.html)
# Different *find* commands, find -P , find -L, find -H
- find -P : This command examines or prints information about different files.
- find -L : Command helps with the information used to be taken from the properties of the file.
- find -H : Helps find information taken from the properties of the symbolic link.
---
```
$ find /tmp
/tmp
/tmp/.ses
/tmp/.squirrel-lock-993566AA4B0BD47CBA9A4D264F058EC017C0F3BB
/tmp/00905ae8-cb90-4c32-b640-d0a9e10cefbc.tmp
/tmp/01b21da0-cda0-4adc-90ec-f44a25ee4f4b.tmp
/tmp/07f0f521-b189-4bae-ba2c-7f732575764a.tmp
...
```
