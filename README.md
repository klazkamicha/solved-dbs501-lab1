Download Link: https://assignmentchef.com/product/solved-dbs501-lab1
<br>
1)  Walkthrough the following PL/SQL code and try to guess what 3 values will be printed during its execution.




<em>SET   SERVEROUTPUT ON</em>

<em>&lt;&lt;big&gt;&gt;</em>

<em>DECLARE</em>

<em>      v_mine  NUMBER(4) := 500;</em>

<em>BEGIN</em>

<em>            &lt;&lt;small&gt;&gt;</em>

<em>            DECLARE</em>

<em>                        v_mine  NUMBER(3) := 700;</em>

<em>            BEGIN</em>

<em>                        dbms_output.put_line(‘Local V_MINE is here: ‘ || v_mine);</em>

<em>                        dbms_output.put_line(‘Outer V_MINE is here: ‘ || big.v_mine);     </em>

<em>                        big.v_mine := v_mine * 2;</em>

<em>            END;</em>

<em>      dbms_output.put_line(‘Outer V_MINE is here: ‘ || v_mine);</em>

<em>END;</em>

<em>/</em>

<em> </em>

2)    Write a PL/SQL block

<ol>

 <li>That includes declarations for the following variables:

  <ul>

   <li>A VARCHAR2 datatype that <u>could </u> accept the string ‘Introduction to Oracle Database’</li>

   <li>A NUMBER that <u>may</u> be assigned 123456.78, but not 123456.789 or 1023456.78</li>

   <li>A CONSTANT that is initialized to the value ‘704B’</li>

   <li>A BOOLEAN</li>

   <li>A DATE data type initialized to one week from today (without the hours)</li>

  </ul></li>

 <li>In the body of the block, place a message with values for each of the variables that received an initialization value.</li>

 <li>In the body of the block, write a code that will perform following tests — use a nested             IF  THEN  ELSE statement when needed

  <ul>

   <li>Check if the VARCHAR2 variable you created contains the word “SQL”.</li>

   <li>If it does, then put a message on the screen that provides the name of the course</li>

   <li>If it does not, then test to see if the CONSTANT you created contains the room number 704B.</li>

   <li>If it does, then check whether  your VARCHAR2 variable has a value and if yes put a message that states the course name and the room name that you’ve reached in this logic. Otherwise, put the message “Course is unknown” and the room name as well.</li>

   <li>If the CONSTANT does not, then put a message on the screen that states that the “Course and location could not be determined”.</li>

  </ul></li>

 <li>Assign the VARCHAR2 variable “C++ advanced” value, just before your IF-THEN logic and observe how the  result has changed</li>

 <li>Provide BOTH results at the end of this question</li>

</ol>

3)    Perform the following tasks:

<ol>

 <li>Create a table called Lab1_tab with two columns (Id as numeric and LName as variable character of maximum 20 characters)</li>

 <li>Create a sequence called Lab1_seq that increments by units of 5 and starts with1.</li>

</ol>

<ol>

 <li>Write a PL/SQL block that performs the following in this order:</li>

</ol>

<ol>

 <li style="list-style-type: none;">

  <ol>

   <li>Declares two variables to hold values for columns of table Lab1_tab</li>

   <li>The block then inserts into the table the last name of the student that is enrolled in the most classes and his/her last name contains less than 9 characters. Here use a sequence for the Id.</li>

   <li>Then  the student with the least enrollments is inserted in the table, use sequence as well.</li>

   <li>Insert the instructor’s last name teaching the least amount of courses if his/her last name does NOT end on “s”. Here do not use the sequence to generate the ID; instead use your first variable.</li>

   <li>Now insert the instructor teaching the most number of courses and use the sequence to populate his/her Id.</li>

   <li>Save your changes and display the content of  your table Lab1_tab</li>

   <li>You will need to plan for the Exception when  more than one student is enrolled in the Maximum (Minimum) number of courses. Same for the Instructor teaching Maximum (Minimum) number of courses. The message stored in the table in that case should be “Multiple Names” (instead of the last name).</li>

  </ol></li>

</ol>

<u>Hint:</u> You may use ONE outer block and FOUR INNER blocks (each of them with its EXCEPTION section) followed by the appropriate INSERT statement.