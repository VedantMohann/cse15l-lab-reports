
For this lab report, I chose the grep command, and I am exploring the command-line options `-i, -v, -c, -l`. I found information on this command on [wikipedia](https://en.wikibooks.org/wiki/Grep). 

 <h4> Command 1 </h4> 
`-i` ignores upper and lower case when searching for lines
<h6> example 1 </h6>
```
  grep -i "six" biomed/1468-6708-3-1.txt <br>
        Six large controlled population-based studies of <br>
          examining health status over time, we added a sixth <br>
 ```
 <h6> example 2 </h6>
```
grep -i "many" biomed/1468-6708-3-1.txt <br>
        Many healthy older adults report gradual weight gain<br>
          of health events in many studies [ 17 ] . Because we are<br>
          results from many studies. However, health measures<br>
 ```

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
 <h6> example 2 </h6>
  We can also combine command-line options to ignore upper and lower case
```
grep -i -v "e" 911report/chapter-1.txt <br>
What If? <br>
 ```
