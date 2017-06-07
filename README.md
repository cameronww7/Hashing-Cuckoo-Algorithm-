# Hashing-Cuckoo-Algorithm-

CPSC 335 Project 4: Hashing
Prof. Doina Bein, CSU Fullerton
dbein@fullerton.edu
Introduction
In this project you will design, implement, and analyze one algorithm for the hashing problem. The algorithm is called Cuckoo Hashing, presented in the class.
For this problem, you will design and implement one algorithm in C/C++/Java/Python, test it on various inputs and complete a hash table with a given input. No algorithm analysis is needed for this project.

The Cuckoo Hashing Algorithm 

There are several versions of cuckoo hashing. The version we learned in class is the simplest, where there are two hash functions, and thus only two places where any given item could be stored in the table. Let us consider the set of keys to be printable ASCII strings of length no more than 80. Let us consider the hash table size to be 17 .

If key is the string representing the key, then let keysize be the size of the string and key[i] be the ASCII code of the (i+1)th character in the string key read from left to right: 
Java uses the following hash function on strings:
 

Let us consider two hash functions, f1 and f2. Function f2 will compute the hash value using Java’s hash function formula, while the function f1 computes a different hash value using a different hash function. Function f1 computes first a large number then it brings the result into the proper range using the formulas below:


if then =+ tablesize
 
Function f2 computes first a large number then it brings the result into the proper range using the formulas below:



if then =+ tablesize
Both functions  f1 and f2 compute first a large number then it brings the result into the proper range 0..tablesize-1. But we bring the intermediate results into the proper range after each calculation, we do not need to wait until we compute the final result. Also, we can ring the power term into the proper range before multiplying it with 

You need to insert the strings  below (also given in the input file in6.txt) into the hash table provided next. Please put an empty line at the end of the file.

Algorithm Engineering
California State University
Fullerton
College of Engineering
and Computer Science
Department of Computer
Science
Dynamic Programming
Monge Properties
String Matching
Matrix Searching
Optimal Tree Construction
Online algorithms
emphasis on
Server Problem
Some related problem
Self-Stabilization
One of the greatest
mysteries in science
Quantum Nature of Universe
In physics and
are known
Cuckoo hashing is fun

into the hash table (next page) using f1 for the first table and f2 for the second table. Show the result of the insertion in the table shown on next page.

Hint: consider a two-dimensional table of strings t, where t[0] is T1 and t[1] is T2. Consider a variable index that oscillates between 0 and 1as it would have oscillated between T1 and T2. In C++, the value of index could be changed using the tertiary operator: index = index? 0:1. Depending on the value of index, either apply hash function f1 (index == 0) or f2 (index == 1).
 
What to do
1. Write clear pseudocode for the algorithm.
2. Type these notes (electronically or on paper) and submit it as a PDF report.
3. Implement your algorithm in C/C++/Java/Python.  You may use the templates provided at the end of this file.
4. Compile and execute the program. 
5. Complete the table using the strings from the file in6.txt as the input and insert it into the PDF report.
6. Create a file with the output of the program for an input value and submit it together with the program. Note, the output can be redirected to a file (for easy printing). For example, the following command line will create an output file in Linux-based operating system called a1out.txt by re-directing the output from the screen (display) to the file a1out.txt:
K:\cpscs335> a.out > a4out.txt
