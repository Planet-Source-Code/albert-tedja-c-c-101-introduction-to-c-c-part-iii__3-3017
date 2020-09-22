<div align="center">

## C/C\+\+ 101: Introduction to C/C\+\+ \(Part III\)


</div>

### Description

This tutorial is made to help people learning C/C++ language which is commonly believed as a hard language.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Albert Tedja](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/albert-tedja.md)
**Level**          |Beginner
**User Rating**    |4.5 (54 globes from 12 users)
**Compatibility**  |C, C\+\+ \(general\), Microsoft Visual C\+\+, Borland C\+\+, UNIX C\+\+
**Category**       |[Documents](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/documents__3-27.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/albert-tedja-c-c-101-introduction-to-c-c-part-iii__3-3017/archive/master.zip)





### Source Code

<html>
<head>
<title>C/C++ 101: Introduction to C/C++ (Part III)</title>
</head>
<body>
<p><font face="Arial" size="4">C/C++ 101: Introduction to C/C++</font></p>
<p><font face="Arial" size="2">&nbsp;</font></p>
<p><font size="2" face="Arial"><b>Part III: more about printing, special
characters, comments.</b></font></p>
<p><font face="Arial" size="2">&nbsp;</font></p>
<p><font face="Arial" size="2"><i>Quote from the previous part:</i></font></p>
<p><i><font face="Arial" size="2">There's one thing I need to say regarding this
include stuff. </font><font size="2" face="Courier New" color="#000080">#include</font><font face="Arial" size="2">
is unique to C/C++ and sometimes it causes great confusion for non-C
programmers. C language doesn't have built-in functions like other languages. It
only has some keywords and symbols. So, every time we want to use a function, we
need to get it from other sources. That sources are called libraries. In order
to access these libraries, we need header files. The header files are just
regular files that contain C/C++ language, just like our code. However, they are
made to access the libraries which are written using Assembly language.
Different compilers have different header files. </font><font size="2" face="Courier New" color="#000080">stdio.h</font><font face="Arial" size="2">
in compiler A may be different with </font><font size="2" face="Courier New" color="#000080">stdio.h</font><font face="Arial" size="2">
in compiler B, so, don't mix them up.</font></i></p>
<p>&nbsp;</p>
<p><font face="Arial" size="2">OK, we have learned how to print in C using </font><font face="Courier New" size="2" color="#000080">printf()</font><font face="Arial" size="2"> function. However, what we printed was only one line. In this tutorial,
we are going to learn how to print multiple lines by calling </font><font face="Courier New" size="2" color="#000080">printf()</font><font face="Arial" size="2"> function
multiple times. Therefore, we will also learn some special characters we can use.
I'll also discuss about comments in this tutorial.</font></p>
<p><font face="Arial" size="2">Printing multiple lines of text by calling </font><font face="Courier New" size="2" color="#000080">printf()</font><font face="Arial" size="2">
function multiple times seems very promising and the most logical way. Why don't we
try it? Here's an example:</font></p>
<table border="0" width="100%">
 <tr>
  <td width="100%" bgcolor="#99FFCC"><font face="Courier New" size="2">#include
   &lt;stdio.h&gt;<br>
   <br>
   int main() {<br>
   &nbsp;&nbsp;&nbsp; printf(&quot;Hello World&quot;);<br>
   <font color="#0000FF">&nbsp;&nbsp;&nbsp; printf(&quot;Hello World line
   2&quot;);<br>
   &nbsp;&nbsp;&nbsp; printf(&quot;Hello World line 3&quot;);</font><br>
   <br>
   &nbsp;&nbsp;&nbsp; return 0;<br>
   }</font></td>
 </tr>
</table>
<p><font face="Arial" size="2">But, when we compile it, what do we get?</font></p>
<table border="0" width="100%">
 <tr>
  <td width="100%" bgcolor="#C0C0C0"><font face="Courier New" size="2">Hello
   WorldHello World line 2Hello World line 3</font></td>
 </tr>
</table>
<p><font face="Arial" size="2">It seems that our code doesn't work so well.
Here's why. We all know what the word &quot;cursor&quot; means. It is a pointer
to location where we are going to type words. </font><font face="Courier New" size="2" color="#000080">printf()</font><font face="Arial" size="2"> function is &quot;cursor
dependent.&quot; It means that it prints where the cursor is. Before we print
the first string (</font><font face="Courier New" size="2" color="#000080">&quot;Hello World&quot;</font><font face="Arial" size="2">), the cursor position is at the
top-left corner of the screen. Therefore, the </font><font face="Courier New" size="2" color="#000080"> &quot;Hello World&quot;</font><font face="Arial" size="2"> string
will be printed at the top-left corner. Once the </font><font face="Courier New" size="2" color="#000080"> &quot;Hello World&quot;</font><font face="Arial" size="2"> is
printed, the cursor points after the word </font><font face="Courier New" size="2" color="#000080"> &quot;World.&quot;</font><font face="Arial" size="2"> Here's an
illustration:</font></p>
<table border="0" width="100%">
 <tr>
  <td width="100%" bgcolor="#C0C0C0"><font face="Courier New" size="2">Hello
   World_</font></td>
 </tr>
</table>
<p><font face="Arial" size="2"><i>The underscore (&quot;_&quot;) is the cursor.</i></font></p>
<p><font face="Arial" size="2">After &quot;Hello World&quot; is printed, we call
another </font><font face="Courier New" size="2" color="#000080">printf()</font><font face="Arial" size="2"> function. This time the string is &quot;Hello World line
2.&quot; As stated before, </font><font face="Courier New" size="2" color="#000080">printf()</font><font face="Arial" size="2"> will print where the cursor is, therefore,
the string &quot;Hello World line 2&quot; will be printed at the position of the
cursor--after the word </font><font face="Courier New" size="2" color="#000080"> &quot;World&quot;</font><font face="Arial" size="2">-- resulting a result like this:</font></p>
<table border="0" width="100%">
 <tr>
  <td width="100%" bgcolor="#C0C0C0"><font face="Courier New" size="2">Hello
   WorldHello World line 2_</font></td>
 </tr>
</table>
<p><font face="Arial" size="2">And the same thing happens with the third call of
the </font><font face="Courier New" size="2" color="#000080">printf()</font><font face="Arial" size="2"> function, and we get a continuous string in one line instead of
three lines. How do we fix this? C has provided a special character to perform
an action that we call &quot;line feed and carriage return.&quot; Line feed
means change to the next line, and carriage return means back to the beginning
of the line. If combined, it has a meaning: &quot;go to the next line at the
beginning,&quot; the same like when we press Enter key. The special character is
a letter 'n' preceded by a backslash: </font><font face="Courier New" size="2" color="#000080">\n</font><font face="Arial" size="2">. We want our code to work properly, so
we are going to add the special character we have just learned to our code.
Here's the modified code:</font></p>
<table border="0" width="100%">
 <tr>
  <td width="100%" bgcolor="#99FFCC"><font face="Courier New" size="2">#include
   &lt;stdio.h&gt;<br>
   <br>
   int main() {<br>
   &nbsp;&nbsp;&nbsp; printf(&quot;Hello World<font color="#0000FF">\n</font>&quot;);<br>
   &nbsp;&nbsp;&nbsp; printf(&quot;Hello World line 2<font color="#0000FF">\n</font>&quot;);<br>
   &nbsp;&nbsp;&nbsp; printf(&quot;Hello World line 3<font color="#0000FF">\n</font>&quot;);<br>
   <br>
   &nbsp;&nbsp;&nbsp; return 0;<br>
   }</font></td>
 </tr>
</table>
<p><font face="Arial" size="2">We put </font><font face="Courier New" size="2" color="#000080">\n</font><font face="Arial" size="2"> at the end of each string because we
want our compiler to know that our string ends there and move to the next line
to print another string. </font><font face="Courier New" size="2" color="#000080">\n</font><font face="Arial" size="2"> must be put inside a string and should not be
excluded from the string. Here's what we get when we compile the modified code
above:</font></p>
<table border="0" width="100%">
 <tr>
  <td width="100%" bgcolor="#C0C0C0"><font face="Courier New" size="2">Hello
   World<br>
   Hello World line 2<br>
   Hello World line 3<br>
   _</font></td>
 </tr>
</table>
<p><font face="Arial" size="2">Maybe you're not used with this, but keep
practicing as you are going to need this for the rest of your programming life
(especially in DOS).</font></p>
<p><font face="Courier New" size="2" color="#000080">\n</font><font face="Arial" size="2"> that we learned is one of the special
characters that we can use in C/C++. There are many special
characters and what interesting is that they are all preceded by a backslash
character. Backslashes play important role in printing some output on the screen
because they like &quot;identifier&quot; of the special action we are going to
take. Let me give you brief descriptions of these special characters.</font></p>
<table border="1" width="97%" height="14">
 <tr>
  <td width="20%" height="1"><b><font size="2" face="Arial">\n</font></b></td>
  <td width="80%" height="1"><font size="2" face="Arial">line-feed and
   carriage-return.</font></td>
 </tr>
 <tr>
  <td width="20%" height="1"><b><font size="2" face="Arial">\b</font></b></td>
  <td width="80%" height="1"><font size="2" face="Arial">backspace</font></td>
 </tr>
 <tr>
  <td width="20%" height="1"><b><font size="2" face="Arial">\t</font></b></td>
  <td width="80%" height="1"><font size="2" face="Arial">tab</font></td>
 </tr>
 <tr>
  <td width="20%" height="1"><b><font size="2" face="Arial">\&quot;</font></b></td>
  <td width="80%" height="1"><font size="2" face="Arial">double quotation mark</font></td>
 </tr>
 <tr>
  <td width="20%" height="1"><font size="2" face="Arial">\\</font></td>
  <td width="80%" height="1"><font size="2" face="Arial">backslash</font></td>
 </tr>
 <tr>
  <td width="20%" height="1"><b><font size="2" face="Arial">\0</font></b></td>
  <td width="80%" height="1"><font size="2" face="Arial">null terminator</font></td>
 </tr>
</table>
<p><font face="Arial" size="2">There are more than these but they are not used
so often. As you can see from the above table, we can use some special
characters like double quotation mark (</font><font size="2" face="Courier New" color="#000080">&quot;</font><font face="Arial" size="2">)
or a tab in our string. Use them to see what they do.</font></p>
<p>&nbsp;</p>
<p><font face="Arial" size="3"><b>Comments</b></font></p>
<p><font face="Arial" size="2">I guess you already know what comments are, so
I'll be straight forward for this one.</font></p>
<p><font face="Arial" size="2">There are two ways of commenting in C/C++. One is
used for commenting a line, and the other one is used for commenting a block of
code. The one we use for commenting a line is a double slash (//). Here's an
example of how to do that.</font></p>
<table border="0" width="100%">
 <tr>
  <td width="100%" bgcolor="#99FFCC"><font face="Courier New" size="2">#include
   &lt;stdio.h&gt;<br>
   <br>
   int main() {<br>
   &nbsp;&nbsp;&nbsp; <font color="#008000">// This is a comment</font><br>
   &nbsp;&nbsp;&nbsp; printf(&quot;Hello World&quot;);<br>
   &nbsp;&nbsp;&nbsp; printf(&quot;Hello World line 2&quot;);<br>
   &nbsp;&nbsp;&nbsp; printf(&quot;Hello World line 3&quot;);<br>
   <br>
   &nbsp;&nbsp;&nbsp; return 0;<br>
   }</font></td>
 </tr>
</table>
<p><font face="Arial" size="2">A double slash comments only one line and it
won't interfere with the other lines. The other one, however, will comment a
block of code. It means that it will comment the rest of the code until it
reaches its terminator. Somewhat similar like BEGIN and END. We use </font><font color="#000080" face="Courier New" size="2">/*</font><font face="Arial" size="2">
to BEGIN commenting, and </font><font size="2" face="Courier New" color="#000080">*/</font><font face="Arial" size="2">
to END commenting.</font></p>
<table border="0" width="100%">
 <tr>
  <td width="100%" bgcolor="#99FFCC"><font face="Courier New" size="2">#include
   &lt;stdio.h&gt;<br>
   <br>
   int main() {<br>
   &nbsp;&nbsp;&nbsp; <font color="#008000">/*<br>
   &nbsp;&nbsp;&nbsp; This whole block is commented<br>
   &nbsp;&nbsp;&nbsp; printf(&quot;Hello World&quot;);<br>
   &nbsp;&nbsp;&nbsp; printf(&quot;Hello World line 2&quot;);<br>
   &nbsp;&nbsp;&nbsp; */</font><br>
   &nbsp;&nbsp;&nbsp; printf(&quot;Hello World line 3&quot;);<br>
   <br>
   &nbsp;&nbsp;&nbsp; return 0;<br>
   }</font></td>
 </tr>
</table>
<p>&nbsp;</p>
<p><font face="Arial" size="2">Note: all words, materials, and definitions
defined in this tutorial are my own opinions which I consider true. If in any
case you find them wrong, corrections would be very helpful. This tutorial is
made to help people learning C/C++ language which is commonly believed as a hard
language.</font></p>
<p><font face="Arial" size="2">Copyright (C) 2001, Albert Tedja.</font></p>
</body>
</html>

