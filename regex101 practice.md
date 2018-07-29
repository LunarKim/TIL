
Exercise 1: Matching Characters  
Task	Text  	 
Match	abcdefg	To be completed  
Match	abcde	To be completed  
Match	abc  


```python
ab[cdefg]

# []Range(c or d or e or f or g)
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    <ipython-input-1-8ed45c38fd5d> in <module>()
    ----> 1 ab[cdefg]
    

    NameError: name 'ab' is not defined



Exercise 1½: Matching Digits  

Task	Text	   
Match	abc123xyz	To be completed  
Match	define "123"	To be completed  
Match	var g = 123;	To be completed  
 


```python
123
```

Exercise 2: Matching With Wildcards  
Task	Text	   
Match	cat.	To be completed  
Match	896.	To be completed  
Match	?=+.	To be completed  
Skip	abc1  
 
 


```python
[^abc1]

#not a or b or c or 1

(cat.|896|\?=+)

# alternation

cat. or 896 or \?=+ 

```

Exercise 3: Matching Characters  
Task	Text	   
Match	can	Success  
Match	man	Success  
Match	fan	Success  
Skip	dan	To be completed  
Skip	ran	To be completed  
Skip	pan	To be completed 



```python
[^drp]an
```

Exercise 4: Excluding Characters  
Task	Text	   
Match	hog	To be completed  
Match	dog	To be completed  
Skip	bog  


```python
[^b]og
```


      File "<ipython-input-2-cdc70d3a8db0>", line 1
        [^b]og
         ^
    SyntaxError: invalid syntax
    


Exercise 5: Matching Character Ranges  
Task	Text  	 
Match	Ana	To be completed  
Match	Bob	To be completed  
Match	Cpc	To be completed  
Skip	aax	To be completed  
Skip	bby	To be completed  
Skip	ccz  


```python
^[A-C]\w+

# ^ : start of line
# [A-C] : Upper case letter, between A and C
# \w : Word
# uantifiers
# + : 1 or more 
```

Exercise 6: Matching Repeated Characters  
Task	Text	   
Match	wazzzzzup	Success  
Match	wazzzup	Success  
Skip	wazup	To be completed  



```python
waz{3,5}up

# quantifiers
#{} : specify how many repetitions of each character I want.
```

Exercise 7: Matching Repeated Characters  
Task	Text	   
Match	aaaabcc	Success  
Match	aabbbbc	Success  
Match	aacc	Success  
Skip	a  


```python
a{2,4}b*c+

# {2,4} : range between 2 and 4
# * : zero or more of any character
```

Exercise 8: Matching Optional Characters  
Task	Text	   
Match	1 file found?	To be completed  
Match	2 files found?	To be completed  
Match	24 files found?	To be completed  
Skip	No files found.  



```python
\d+ files? found\?

# \d : digit
# ? : optinal. 0 or more
# \? : to match a plain question mark character in a string
```

Exercise 9: Matching Whitespaces  
Task	Text	   
Match	1.   abc	To be completed  
Match	2.	abc	To be completed  
Match	3.           abc	To be completed  
Skip	4.abc	To be completed  



```python
\d\.\s+abc

# \: escape character
# \s : any of the specific whitespaces
```

Exercise 10: Matching Lines  
Task	Text	   
Match	Mission: successful	To be completed  
Skip	Last Mission: unsuccessful	To be completed  
Skip	Next Mission: successful upon capture of target  


```python
^Mission:\ssuccessful

# ^ : to match only a line that begins with the word what I want
# ^ is called a hat ; looks like a hat? ,,, so cute ,,,
```

Exercise 11: Matching Groups  
Task	Text	Capture Groups	     
Capture	file_record_transcript.pdf	file_record_transcript	  
Capture	file_07241999.pdf	file_07241999	  
Skip	testfile_fake.pdf.tmp		  

Regular expressions allow us to not just match text but also to extract
information for further processing. 
This is done by defining groups of characters and capturing them using
the special parentheses(and) metacharacters.


```python
^(file_[\d|\w]+).pdf$

# () : Any subpattern inside a pair of parentheses will be captured.
# $ : end of line
```

Exercise 12: Matching Nested Groups  
Task	Text	Capture Groups	   
Capture	Jan 1987	Jan 1987 1987	To be completed  
Capture	May 1969	May 1969 1969	To be completed  
Capture	Aug 2011	Aug 2011 2011	To be completed  

Lesson 12: Nested groups
When you are working with complex data, you can easily find yourself having to extract multiple layers of information, which can result in nested groups. Generally, the results of the captured groups are in the order in which they are defined (in order by open parenthesis).

복잡한 데이터를 분석할 때, 우리는 다수의 레이어로 된 데이터를 추출해야할 필요가 있습니다. 이 레이어들은 nested groups로 나타납니다. 

Take the example from the previous lesson, of capturing the filenames of all the image files you have in a list. If each of these image files had a sequential picture number in the filename, you could extract both the filename and the picture number using the same pattern by writing an expression like ^(IMG(\d+))\.png$ (using a nested parenthesis to capture the digits).

이전 lesson에서 예를 들어보자면, 이미지 파일의 리스트에서 파일네임을 캡쳐하는 경우에 관해 보겠습니다.  각각의 이미지들이 파일명 속에 사진 순차적인 사진 번호를 가지고 있다면 너는 파일이름과 사진번호를 둘다 뽑아낼 수 있습니다.  ^(IMG(\d+))\.png$라는 표현식을 이용하면 됩니다. 

The nested groups are read from left to right in the pattern, with the first capture group being the contents of the first parentheses group, etc.

nested groups은 왼쪽에서 오른쪽으로 읽힙니다. 

For the following strings, write an expression that matches and captures both the full date, as well as the year of the date.


```python
(\w+\s(\d+))

# (()) : using a nested parenthesis to capture the digit

```

Exercise 13: Matching Nested Groups
Task	Text	Capture Groups	 
Capture	1280x720	1280 720	To be completed
Capture	1920x1600	1920 1600	To be completed
Capture	1024x768	1024 768	To be completed



```python
((\d{4})x(\d{3,4}))
```

Exercise 14: Matching Conditional Text  
Task	Text	   
Match	I love cats	To be completed  
Match	I love dogs	To be completed  
Skip	I love logs	To be completed  
Skip	I love cogs  


```python
I love ([cd]ats|[dh]ogs)
```

Exercise 15: Matching Other Special Characters  
Task	Text	   
Match	The quick brown fox jumps over the lazy dog.  	To be completed  
Match	There were 614 instances of students getting 90.0% or above.	To be completed  
Match	The FCC had to censor the network for saying &$#*@!.  


```python
^The\w*
```

Exercise 1: Matching Numbers  
Task	Text	 
Match	3.14529	To be completed  
Match	-255.34	To be completed  
Match	128	To be completed  
Match	1.9e10	To be completed  
Match	123,340.00	To be completed  
Skip	720p  


```python
^-?\d+(,\d+)*(\.\d+(e\d+)?)?$

[^]이게 안먹힐 땐 끝에 나와야하는 것을 쓰고 $을 달자. 
```

Exercise 2: Matching Phone Numbers  
Task	Text	Capture Groups	   
Capture	415-555-1234	415	To be completed  
Capture	650-555-2345	650	To be completed  
Capture	(416)555-3456	416	To be completed  
Capture	202 555 4567	202	To be completed  
Capture	4035555678	403	To be completed  
Capture	1 416 555 9292	416  


```python
^\(?1?\s*(\d{3})
```


```python
(  : metacharcters , must be escaped
```

Exercise 3: Matching Emails  
Task	Text	Capture Groups	   
Capture	tom@hogwarts.com	tom	To be completed  
Capture	tom.riddle@hogwarts.com	tom.riddle	To be completed  
Capture	tom.riddle+regexone@hogwarts.com	tom.riddle	To be completed   
Capture	tom@hogwarts.eu.com	tom	To be completed  
Capture	potter@hogwarts.com	potter	To be completed  
Capture	harry@hogwarts.com	harry	To be completed  
Capture	hermione+regexone@hogwarts.com	hermione  


```python
(^\w+\.?\w+)
```

Exercise 4: Capturing HTML Tags    
Task	Text	Capture Groups	     
Capture	<a>This is a link</a>	a	To be completed    
Capture	<a href='https://regexone.com'>Link</a>	a	To be completed    
Capture	<div class='test_style'>Test</div>	div	To be completed    
Capture	<div>Hello <span>world</span></div>	div	To be completed    



```python
<(\w+)\s*
```

Exercise 5: Capturing Filename Data  
Task	Text	Capture Groups	   
Skip	.bash_profile		To be completed  
Skip	workspace.doc		To be completed  
Capture	img0912.jpg	img0912 jpg	To be completed  
Capture	updated_img0912.png	updated_img0912 png	To be completed  
Skip	documentation.html		To be completed  
Capture	favicon.gif	favicon gif	To be completed  
Skip	img0912.jpg.tmp		To be completed  
Skip	access.lock  


```python
((updated_)?img0912|favicon).(jpg|png|gif)?$
```

Exercise 6: Matching Lines  
Task	Text	Capture Groups	   
Capture				The quick brown fox...	The quick brown fox...	To be completed  
Capture	   jumps over the lazy dog.	jumps over the lazy dog.	To be completed  



```python
^\s*(\w*\s*.*$)
```

Exercise 7: Extracting Data From Log Entries  
Task	Text	Capture Groups	   
Skip	W/dalvikvm( 1553): threadid=1: uncaught exception		To be completed  
Skip	E/( 1553): FATAL EXCEPTION: main		To be completed  
Skip	E/( 1553): java.lang.StringIndexOutOfBoundsException		To be completed  
Capture	E/( 1553):   at widget.List.makeView(ListView.java:1727)	  makeView ListView.java 1727	To be completed  
Capture	E/( 1553):   at widget.List.fillDown(ListView.java:652)	fillDown ListView.java 652	To be completed  
Capture	E/( 1553):   at widget.List.fillFrom(ListView.java:709)	fillFrom ListView.java 709  


```python
at widget.List.(makeView|fillDown|fillFrom)\((\w+.java):(\d*)
```

Exercise 8: Extracting Data From URLs  
Task	Text	Capture Groups	   
Capture	ftp://file_server.com:21/top_secret/life_changing_plans.pdf	ftp file_server.com 21	To be completed  
Capture	https://regexone.com/lesson/introduction#section	https regexone.com	To be completed  
Capture	file://localhost:4040/zip_file	file localhost 4040	To be completed  
Capture	https://s3cur3-server.com:9999/	https s3cur3-server.com 9999	To be completed  
Capture	market://search/angry%20birds	market search	To be completed  

