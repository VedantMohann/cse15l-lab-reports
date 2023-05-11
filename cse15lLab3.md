
For this lab report, I chose the grep command, and I am exploring the command-line options `-i, -v, -c, -l`. I found information on this command on [wikipedia](https://en.wikibooks.org/wiki/Grep). 

 <h4> Command 1 </h4> 
`-i` ignores upper and lower case when searching for lines
<h6> example 1 </h6>
```
  grep -i "six" biomed/1468-6708-3-1.txt <br>
        Six large controlled population-based studies of <br>
          examining health status over time, we added a sixth <br>
 ```
 In this example, `-i` finds all uses of the letters "six" ignoring case. This is important because generally when looking
 for a word, we don't care about whether it is upper or lower case. 
 <h6> example 2 </h6>
```
grep -i "many" biomed/1468-6708-3-1.txt <br>
        Many healthy older adults report gradual weight gain<br>
          of health events in many studies [ 17 ] . Because we are<br>
          results from many studies. However, health measures<br>
 ```
In this example, we do a similar search as the first one but look for the word "many"
 <h4> Command 2 </h4> 
`-v` inverts our match 
<h6> example 1 </h6>
```
 grep -v "e" 911report/chapter-1.txt <br>
"WE HAVE SOME PLANES" <br>
INSIDE THE FOUR FLIGHTS <br>
IMPROVISING A HOMELAND DEFENSE <br>
    NEADS: On its way towards Washington? <br>
    NEADS: Okay. <br>
NATIONAL CRISIS MANAGEMENT <br>
What If? <br>
 ```
 In this example, `-v` looks for all lines that don't have the letter "e". This can be useful for when we need
 to find lines that don't have a certain character. 
 <h6> example 2 </h6>
  We can also combine command-line options to ignore upper and lower case
```
grep -i -v "e" 911report/chapter-1.txt <br>
What If? <br>
 ```
 In this example, we amplify our search from the previous example but make our search not case sensitive. 
  <h4> Command 3 </h4> 
`-c` outputs the count of matching lines 
<h6> example 1 </h6>
```
 grep -c "diversity" government/About_LSC/diversity_priorities.txt
44
 ```
 in this example, we find how many lines contain the word diversity, this way we can see how relative a word is in 
 a file without getting huge outputs.
 <h6> example 2 </h6>
```
grep -c "hello" government/About_LSC/diversity_priorities.txt 
0
 ```
 In this example, we find if the word "hello" is in the file. This way, we realize that the word hello is irrelevant to our file
   <h4> Command 4 </h4> 
`-l` outputs matching files only
<h6> example 1 </h6>
```
 grep -l "chemical reaction" biomed/*.txt
biomed/1471-2105-3-38.txt
biomed/1471-2148-2-14.txt
biomed/1471-2164-3-19.txt
biomed/1471-2180-3-4.txt
biomed/1471-2229-1-2.txt
biomed/gb-2001-2-4-research0012.txt
biomed/gb-2002-3-5-research0024.txt
```
In this example, we output files with the word "chemical reaction" to see where we can look to learn about chemical reactions
 <h6> example 2 </h6>
```
grep -l "hammer" */*.txt
911report/chapter-12.txt
biomed/1471-2091-3-14.txt
biomed/1471-2105-3-14.txt
biomed/1471-2105-3-26.txt
biomed/1471-2407-2-18.txt
biomed/1472-6750-2-21.txt
```
In this example, we search all directories for the word "hammer" to see what files in all directories could be related to hammers
