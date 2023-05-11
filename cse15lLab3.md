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
<h3>Part 1</h3>
here is my code for StringServer: ![Image](Screenshot 2023-04-24 at 9.10.00 PM.png)
Here is the first screenshot using /add-message: ![Image](Screenshot 2023-05-05 at 3.16.05 PM.png) <br>
For this screenshot, the handleRequest method is called. The relevant argument is the url that is typed in. The method takes the query of the url if
the path is /add-member. Then, the substring after the '=' is taken from the query is added to our String s, which is returned. In this specific request
the value of s changes from "" to "what'sup\n". 
Here is the second screenshot using \add-message: ![Image](Screenshot 2023-05-05 at 3.19.28 PM.png) <br>
For this screenshot, the `handleRequest` method is called. The relevant argument is again the url that is typed in. The method takes the query of the url
if the path is `/add-member`. Then the substring after the '=' from the query is added to our String `s`, which is returned. In this specific request
the value of s changes from `"what's up"` to `"what's up\nhow are you doing\n"`
<h3>Part 2</h3>
I chose the bug in the reverseInPlace(int[] arr) method from ArrayExamples in lab3. A failure inducing input for the buggy program was:
```
@Test
  public void testReverseInPlace2() {
    int[] input1 = { 3,2,1 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 1,2,3 }, input1);
  }
 ```
 An input that didn't induce a failure was:
 ```
 	@Test 
	public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
	}
 ```
 Here is the symptom of the bug:
 ![Image](Screenshot 2023-04-24 at 9.28.53 PM.png)
 The bug was that the for loop should only interate until halfway through the array, and we need to swap the two numbers rather than setting
 arr[i] = arr[arr.length-i-1].
 Before:
 ```
 static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
  ```
  After:
  ```
  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length/2; i += 1) {
      int temp = arr[i];
      arr[i] = arr[arr.length - i - 1];
      arr[arr.length-i-1] = temp;
    }
  }
  ```
  This fix addresses the issue because before the method would copy the right half of the array onto the left, and then copy the left onto the right,
  but the left was already set to the right, so it copies the right onto the right. Therefore, the right half of the array experiences no changes. So
  we need to swap the two terms rather than setting left = right. If we do this, then we only need to swap until halfway, since then we will be swapping twice.
  <h3>Part 3</h3>
  In lab 2, I learned how to make a local host website. I thought it was one of the coolest cs exercises I've done yet, since all my coding knowledge
  so far has simply been in an IDE and terminal. However this time, I actually got to develop a website. Even though it was extremely simple, it made me 
  feel proud for coming this far in computer science and keeps me eager to learn more. 

