<h1> CSE 15l Lab Report 3 <h1>
For this lab report, I chose the grep command, and I am exploring the command-line options `-i, -v, -c, -l`. I found information on this
command on [wikipedia](https://en.wikibooks.org/wiki/Grep). 
<h3> `-i` <h3>
  `-i` ignores upper and lower case when searching for lines
<h6> example 1 <h6>
  ```
  grep -i "six" biomed/1468-6708-3-1.txt
        Six large controlled population-based studies of
          examining health status over time, we added a sixth
  ```
<h6> example 2 <h6>
  ```
  grep -i "many" biomed/1468-6708-3-1.txt
        Many healthy older adults report gradual weight gain
          of health events in many studies [ 17 ] . Because we are
          results from many studies. However, health measures
  ```
<h3> `-v` <h3>
  `-v` inverts our match 
<h6> example 1 <h6>
  ```
 grep -v "e" 911report/chapter-1.txt
"WE HAVE SOME PLANES"
INSIDE THE FOUR FLIGHTS
IMPROVISING A HOMELAND DEFENSE
    NEADS: On its way towards Washington?
    NEADS: Okay.
NATIONAL CRISIS MANAGEMENT
What If?
  ```
<h6> example 2 <h6>
  We can also combine command-line options to ignore upper and lower cae
  ```
 grep -i -v "e" 911report/chapter-1.txt
What If?
  ```
  
<h3> `-c` <h3>
  `-c` outputs the count of matching lines 
<h6> example 1 <h6>
  ```
 grep -c "diversity" government/About_LSC/diversity_priorities.txt
44
  ```
<h6> example 2 <h6>
  ```
grep -c "hello" government/About_LSC/diversity_priorities.txt 
0
  ```
  
<h3> `-l` <h3>
  `-l` outputs matching files only
<h6> example 1 <h6>
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
<h6> example 2 <h6>
  ```
grep -l "hammer" */*.txt
911report/chapter-12.txt
biomed/1471-2091-3-14.txt
biomed/1471-2105-3-14.txt
biomed/1471-2105-3-26.txt
biomed/1471-2407-2-18.txt
biomed/1472-6750-2-21.txt
  ```
