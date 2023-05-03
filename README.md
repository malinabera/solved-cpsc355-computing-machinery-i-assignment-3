Download Link: https://assignmentchef.com/product/solved-cpsc355-computing-machinery-i-assignment-3
<br>
<strong>Sorting One-Dimensional Arrays </strong>

Create an ARMv8 assembly language program that implements the following algorithm:

#define  SIZE 50

int main() {

int v[SIZE], i, j, temp;

/*  Initialize array to random positive integers, mod 256  */   for (i = 0; i &lt; SIZE; i++) {     v[i] = rand() &amp; 0xFF;     printf(“v[%d]: %d
”, i, v[i]);

}

/*  Sort the array using an insertion sort  */   for (i = 1; i &lt; SIZE; i++) {     temp = v[i];

for (j = i; j &gt; 0 &amp;&amp; temp &lt; v[j-1]; j–) {       v[j] = v[j-1];

}

v[j] = temp;

}

/*  Print out the sorted array  */   printf(“
Sorted array:
”);   for (i = 0; i &lt; SIZE; i++)     printf(“v[%d]: %d
”, i, v[i]);

return 0;

}

Create space on the stack to store all local variables, using the techniques described in lectures. Use m4 macros or assembler equates for all stack variable offsets. Optimize your code so that it uses as few instructions as possible. Be sure, however, that you always read or write memory when using or assigning to the local variables. Name the program assign3.asm.

Also run the program in gdb, first displaying the contents of the array before sorting, and then displaying it again once the sort is complete (use the x command to examine memory). You should show that the algorithm is working as expected. Capture the gdb session using the script UNIX command, and name the output file script.txt.

<strong>Other Requirements </strong>

Make sure your code is readable and fully documented, including identifying information at the top of each file. You must comment each line of assembly code. Your code should also be well designed:  make sure it is well organized, clear, and concise.

<strong>New Skills Needed for this Assignment: </strong>

<ul>

 <li>Use of the stack to store local variables</li>

 <li>Addressing stack variables</li>

 <li>Use of <em>m4</em> macros or assembler equates for stack variable offsets</li>

 <li>Storing and addressing one-dimensional arrays on the stack</li>

</ul>




<strong>Submit the following: </strong>

<ol>

 <li>Your assembly source code files for the program, and your script output file. Use the <em>Assignment 3 </em>Dropbox Folder in D2L to submit electronically. The TA will assemble and run your program to test it.</li>

</ol>

Be sure to name your program and script file as described above.


