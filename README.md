Download Link: https://assignmentchef.com/product/solved-eece-1080-lab9-shapes-and-file-i-o
<br>
This assignment is an introduction to the C++ classes and optionally File I/O for bonus points. We will learn the basics of class design, and we will put it to use creating a couple of more advanced classes.

Highlights:​

<ul>

 <li>Please review the chapter on classes (including operator overload).</li>

 <li>Optionally review the chapter on File I/O.</li>

 <li>Review the <strong>grading Rubric</strong>​ at the end of specification.​    <strong>Lab Attendance Milestone: Completion of Part A (all classes)</strong> ● Please ask appropriate questions when necessary.</li>

 <li>This assignment may require completed Point class and/or Line class in Lab8. Wherever required, you can copy in the class definitions of Point and/or Line class or “include”. <strong>Also, make sure to edit these class</strong>​ <strong> definitions to have double instead of int. </strong></li>

 <li>Examine the <a href="https://drive.google.com/open?id=1k4W3puW44fwRZh-gAYVsYbBMTvJbNbdp"><strong>cp</strong></a>​ <a href="https://drive.google.com/open?id=1k4W3puW44fwRZh-gAYVsYbBMTvJbNbdp"><strong>p</strong></a> <u>​ </u>helper file provided with the assignment.</li>

 <li>Take a few minutes to read this entire document, at least once, before beginning to program it.</li>

</ul>

<strong>Part A: More Classes</strong>

<strong>Task 1: Circle Class:</strong>

<strong>Submit as File: circle.cpp </strong>

Notes:

You will want to add an overloaded == operator to the <strong>public section</strong>​           of the Point​ class using the following:

bool operator==(Point &amp;rhs) { return (rhs.x == x &amp;&amp; rhs.y == y);

}

Once you have completed that you should be able to do the following with any Point related objects.

if(P1 == P2) cout &lt;&lt; “Points are equal” &lt;&lt; endl; else cout &lt;&lt; “Points are not equal” &lt;&lt; endl;

You may want to copy the line.cpp file from lab8 to circle.cpp. The circle class is quite similar to the line class. It uses two point objects just like the line class.

Create an object to implement a “circle” class which allows the programming to store a circle object. The object should use the “point” class developed previously.  You will be given the center point and one point on a circle. The object should have at least two constructors, appropriate set/get functions, and overloaded I/O functions. It should also include functions that return the proper value for the following:

<ol>

 <li>Determine if the object is a circle.</li>

</ol>

Point test: If both points are the same, a circle cannot be formed. This should return a bool.

<ol start="2">

 <li>Calculates the radius using the line distance formula</li>

 <li>Calculates the diameter.</li>

 <li>Calculates the area of a circle.</li>

 <li>Calculates the circumference of a circle.</li>

 <li>Overload &gt;&gt; (cin) operator that lets the user provide inputs to construct a Circle. Refer Laboratory 8 for this purpose.</li>

 <li>Overload &lt;&lt; (cout) operator that lets the user display the Circle and its properties (1-5 specifications above).Refer Laboratory 8 for this purpose.</li>

 <li>Overload == operator (<strong>public</strong>​ )​ that compares two Circle objects and returns either <strong>true </strong>​    or ​ ​       IT returns true if both circles are the same (same​</li>

</ol>

center and radius) and false otherwise. To compare them, both circles have to be valid (Use Step 1). <strong>If using “point” class to build circles, assume P1 is</strong>​            <strong> the center. </strong>




<strong>Task 2: Triangle class: </strong>

<strong>Submit as File: triangle.cpp </strong>

<strong>Note:  </strong>

You will want to copy the Circle class implementation to triangle.cpp, rename the class to Triangle, and add another Point object to store the third point of a triangle. After that is complete add a third point to both cin/cout overloaded operators. Remove or modify any remaining circle related functions/methods.

Design a C++ class to implement a “triangle” – which allows the program to store a triangle object. The object should use the “point” class developed previously. The object should have at least two constructors, appropriate set/get functions. It should also include functions that return the proper value for the following:

<ol>

 <li>Determines if your object is a triangle. Use the <strong>collinearity test</strong>​ described​         at the end of this document.</li>

</ol>

This should return a bool

<ol start="2">

 <li>Calculates the area of a triangle.</li>

 <li>Calculates the perimeter of the triangle.</li>

 <li>Determines if the triangle is an equilateral triangle.</li>

 <li>Overload &gt;&gt; (cin) operator that lets the user provide inputs to construct a</li>

</ol>

Triangle. Refer Laboratory 8 for this purpose.

<ol start="6">

 <li>Overload &lt;&lt; (cout) operator that lets the user display the Triangle and its properties (1-4 specifications above). Refer Laboratory 8 for this purpose.</li>

 <li>Overload == operator (<strong>public</strong>​ )​ that compares two triangle objects and returns either <strong>true </strong>​    or ​ ​       IT returns true if both triangles are the same (same​ points) and false otherwise. To compare them, both triangles have to be valid (Use Step 1).</li>

</ol>

<strong>        </strong>

<strong>Task 3: Quadrilateral Class:</strong>

<strong>Submit as File: quad.cpp </strong>

Create an object to implement a Quadrilateral class which allows the programming to store a quadrilateral object. The object can use either the “point” or “line” class developed previously.  The object should have at least two constructors, appropriate set/get functions. It should also include functions that return the proper value for the following:

<ol>

 <li>Determine if your object can be a quadrilateral. 4 points can form a quadrilateral, when no three points lie on the same line. Use the <strong>collinearity</strong>​ <strong> test</strong> described at the end of this document.​</li>

</ol>

This should return a bool.

<ol start="2">

 <li>Calculate the area of the Quadrilateral. A shoelace formula to compute this is posted below.</li>

 <li>Overload &gt;&gt; (cin) operator that lets the user provide inputs to construct a Quadrilateral. Refer Laboratory 8 for this purpose.</li>

 <li>Overload &lt;&lt; (cout) operator that lets the user display the Quadrilateral and its properties (1-3 above specifications). Refer Laboratory 8 for this purpose.</li>

</ol>




Submit <strong>separate</strong>​        source files for all the class implementations above. You can​         test your classes and functionality in main() whenever required.

<strong>Part B (Optional) File I/O: </strong>

<strong>Submit as File: shape-info.cpp</strong>

You are also provided text file – shapes.txt which contains coordinate(s) information about the shapes. For example, the shape information in the text file can look like below (find the meaning in comments – only in this document):

0 0 0 1 1 0   //Three (x,y) pairs – x1 y1 x2 y2 x3 y3

0 0 2.5 0 2.5 2.5 0 2.5 // Four (x,y) pairs – x1 y1 x2 y2 x3 y3 x4 y4

0 0 2 2 //Two (x,y) pairs – x1 y1 x2 y2

……..and many more

Assume that, 3 (x,y) pairs (or 6 numbers) ​<strong>MAY</strong>​ form a Triangle, 4 pairs ​<strong>MAY </strong>​form a Quadrilateral and 2 pairs ​<strong>MAY </strong>​form a circle (one being the center and the other will be a point on the circumference). Any line with different number of coordinates is invalid input.

In this task you will be reading text from shapes.txt file and writing into another file shapes-info.txt.

Steps to  implement file I/O:

<ol>

 <li>Create an ​<strong>ifstream </strong>​object and ​<strong>open</strong>​ the input text file ​<strong>txt</strong>​. Also create an ​<strong>ofstream </strong>​object and open the text file ​<strong>shapes-info.txt</strong>​.</li>

 <li>Read a single line from input file using input stream object into a temporary string. Taking hint from <u>​</u><a href="https://drive.google.com/open?id=1k4W3puW44fwRZh-gAYVsYbBMTvJbNbdp">cpp</a>​ (requires sstream header file), break up the temporary string into a numbers (coordinates).</li>

 <li>Determine if number of coordinates are sufficient to form any of the shapes. If not, print out the invalidity in the output file and repeat step 2 (one example is shown below).</li>

 <li>If from step 3 the number of coordinates are valid, ​<strong>construct </strong>​the specific shape.</li>

 <li>If the shape can indeed be created (collinearity test for Triangle or Quadrilateral and point test for circle), using ofstream object, print all the calculations into the output text file (output examples are shown below).</li>

 <li>Repeat steps 2-5 until end-of-file (eof()) is encountered in the input stream.</li>

</ol>

Submit this File I/O task as a separate file.

<strong>Note:</strong>

Most editors may not find the shapes.txt file even if it is in the same folder as the source code. That can be fixed with:

<strong>infile.open(“</strong><strong>c:\very\specific\spot\shapes.txt”)</strong>​




Considering infile is your ifstream object.

You can copy the path of the file and put it with in “ “.

<strong>Input &amp; Output eg: </strong>

<strong>Input in shapes.txt: </strong>

0 0 1 0 0 1

0 0 1 0 1 1 0 1

<ul>

 <li>0 1 1</li>

 <li>1 2 2 3</li>

 <li>0 2.5 0 2.5 2.5 0 2.5</li>

 <li>1 1 1</li>

</ul>

<strong>Corresponding Output in shapes-info.txt:</strong>

Sufficient coordinates input.

The object is a Triangle.

Area of the triangle: 0.5 sq. units

Perimeter of the triangle 3.414 units

The triangle is not an equilateral triangle

Sufficient coordinates input.

The object is a Quadrilateral.

Area of the Quadrilateral: 1 sq. units

Sufficient coordinates input.

The object is a Circle.

Radius of the Circle: 1 unit

Diameter of the Circle: 2.82 units

Area of the Circle: 6.28 sq units

Circumference of the Circle: 8.88 units

Sufficient coordinates NOT input.

Sufficient coordinates input.

The object is a Quadrilateral.

Area of the Quadrilateral: 6.25 sq. units

Sufficient coordinates input.

The object is not a Circle.














