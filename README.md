Download Link: https://assignmentchef.com/product/solved-comp1020-lab9-linked-lists
<br>
<ul>

 <li>Linked Lists</li>

</ul>

Notes:

<ul>

 <li>The three exercises in this lab are cumulative – each builds on the previous one, and they must be done in order.</li>

 <li>Only one of the three exercises is required, but try to do as many as you can.</li>

</ul>

Create two classes <strong>Node</strong> and <strong>PointList</strong> which will implement a list of (x,y) points using a linked list.

<ol>

 <li>A <strong>Node</strong> should have three private instance variables: two <strong>double</strong> values <strong>x</strong> and <strong>y</strong>, and a link to the next <strong><sub>Node</sub></strong> in the list. Provide a constructor which will initialize all three of these instance variables. Provide a <strong>Node getLink()</strong> method which will allow access to the link. You do not need any other get/set methods for the Bronze exercise.</li>

 <li>Provide a <strong>String toString()</strong> method in the <strong>Node</strong> class which will return a <strong>String</strong> showing the <strong>x</strong> and <strong>y</strong> values in the format <strong>“(0.343,0.982)”</strong> . Use the built-in method</li>

</ol>

<strong>String.format(“%5.3f”,dataValue)</strong> to ensure that both the <strong>x</strong> and <strong>y</strong> values display exactly 3 decimal places.

<ol start="3">

 <li>A <strong>PointList</strong> should have a single private instance variable (usually named “top”) containing a reference to the first <strong>Node</strong> in the list (or <strong>null</strong> if there are none). Provide a constructor which will create an empty list.</li>

 <li>Provide a <strong>void add(double x, double y)</strong> method to the <strong>PointList</strong> class which will add the point (x,y) to this list of points, <strong><em>at the beginning</em></strong>. Provide the usual <strong>String toString()</strong> method which will return a <strong>String</strong> showing all of the points in the list, in the following format: <strong>“[ (0.435,0.234) (0.123,0.876)  (0.321,0.789) ]”</strong>. Note that, to keep it simple, you can simply surround each point with some blank space.</li>

 <li>Run the supplied <strong>java</strong> program to test your classes. This program will generate and print a list of 5 random points.</li>

</ol>

Modify your classes so that the list of points can be kept sorted, with the x co-ordinates in ascending order. (The y coordinates will not be in any particular order.) You will also add a method that will display the list of points in the <strong>StdDraw</strong> window by “connecting the dots” – joining the sequence of points by lines.

<ol>

 <li>Modify the <strong>Node</strong> class by adding the usual get/set methods <strong>getX</strong>, <strong>getY</strong>, and <strong>setLink</strong> which you will need. (You already have a <strong><sub>getLink</sub></strong> You still don’t need <strong><sub>setX</sub></strong> or <strong><sub>setY</sub></strong>.)</li>

 <li>Add a <strong>void insert(double x, double y)</strong> method to the <strong>PointList</strong> class, which will add the point (<strong><sub>x</sub></strong>,<strong><sub>y</sub></strong>) to the list of points, <em>in the correct location so that the list will remain sorted</em>, with the x coordinates in ascending order (assuming that the existing points in the list are already sorted, of course).</li>

 <li>Add a <strong>void connectTheDots()</strong> method to the <strong>PointList</strong> class which will draw a series of lines in the <strong>StdDraw</strong> window that connect the points in the list. A line should connect the 1<sup>st</sup> point to the 2<sup>nd</sup>, another line should connect the 2<sup>nd</sup> point to the 3<sup>rd</sup>, etc. Do not connect the last point to the first point. If there are fewer than 2 points in the list, it shouldn’t draw anything at all – but it shouldn’t crash, either. This will be tested. The <strong><sub>StdDraw</sub></strong> method to draw a line is simply <strong>line(x1,y1,x2,y2)</strong>.</li>

 <li>Run the supplied <strong>java</strong> program to test your new classes. If the sorting is working properly, then you should see a (random) image something like the one below. The lines should go strictly left-to-right, and should never “double back”.</li>

</ol>

There is no rule that says that a <strong>Node</strong> has to be on just <em>one</em> list. Modify your <strong>Node</strong> and <strong>PointList</strong> classes so that the points are kept sorted by <em>both</em> the <strong><sub>x</sub></strong> coordinate, <em>and</em> the <strong><sub>y</sub></strong> coordinate, at the same time. You will not have to write any completely new code at all, but you will have to duplicate and modify a lot of existing code to provide two different versions – one for <strong><sub>x</sub></strong>, and one for <strong><sub>y</sub></strong>.

<ol>

 <li>Modify your <strong><sub>Node</sub></strong> class so that every node now has 2 links: one to the next point in a list sorted by <strong><sub>x</sub></strong> coordinate, and one to the next point in a list sorted by <strong><sub>y</sub></strong> Add a 4<sup>th</sup> parameter to your constructor to match. You will now need <strong>getXLink</strong>, <strong>getYLink</strong>, <strong>setXLink</strong>, and <strong>setYLink</strong> methods. (The <strong>getX</strong>, <strong>getY</strong>, and <strong>toString</strong> methods are not affected.)</li>

 <li>Modify your <strong>PointList</strong> class so that it has <em>two</em> top/first pointers and not just one – one to the first <strong>Node</strong> in the list of nodes sorted by <strong>x</strong>, and another to the first <strong>Node</strong> in the list of nodes sorted by <strong><sub>y</sub></strong>. Change the constructor to match. You can delete the <strong><sub>add</sub></strong> method entirely, since it should no longer be used. The <strong>toString</strong> method should continue to list the nodes in ascending order by <strong><sub>x</sub></strong></li>

 <li>Modify the <strong>void insert(double x, double y)</strong> method so that it still creates a single new <strong>Node</strong>, but now inserts it into <em>both</em> lists (the one sorted by <strong>x</strong>, and the one sorted by <strong>y</strong>).</li>

 <li>Provide <em>two</em> versions of the connect-the-dots method: <strong>connectTheXDots</strong> and <strong>connectTheYDots</strong>, one of which will connect the points in the order given by the <strong>x</strong> coordinates, and the other by the <strong><sub>y</sub></strong></li>

 <li>Run the supplied <strong>java</strong> program to test your new classes. If the sorting in both directions is working properly, then you should see a (random) image something like the one below. The black lines should go strictly left-to-right, and the red lines should go strictly bottom-to-top, but both should join the same set of points. Modern art!!</li>

</ol>


