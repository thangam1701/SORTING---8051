
# SORTING---8051

**AIM:**

To write and execute Assembly language Program for sorting of data using 8051 keil.

**APPARATUS REQUIRED: Personal computer with Keil software**

**(i) Descending order ALGORITHM:**

1.	Initialize the register r7 with count.
2.	Get first two elements in two registers.
3.	Compare the two elements of data. If value of R0 register is low, then exchange A & R0 data else increment pointer and decrement register R7.
4.	Check R7 is zero, and then move the register R0 & A.
5.	Again increment pointer and decrement R7,
6.	Check R7 is zero. If no repeat the process from step 2.
7.	Otherwise stop the program.

**PROGRAM:**
~~~
ORG 0000H 

MOV R7,#4

LOOP1:MOV R0,#40H 

MOV R6,#04

LOOP: MOV A,@R0 

INC R0

MOV 50H,@R0 

CJNE A,50H,NEXT 

SJMP DOWN 

NEXT:JNC DOWN 

MOV @R0,A

DEC R0

MOV @R0,50H 

DOWN:DJNZ R6,LOOP 

DJNZ R7,LOOP1

END
~~~

**OUTPUT:**


**MEMORY WINDOW:**

Before execution: D:0x40H:
<img width="1919" height="1199" alt="image" src="https://github.com/user-attachments/assets/70248ef3-4d74-46d7-ab77-b6dbc4b574de" />


After execution: D:0x40H:
<img width="1918" height="1193" alt="image" src="https://github.com/user-attachments/assets/df65cd7e-20f3-4e05-8eb3-959067c08768" />



**(ii)	Ascending order**
 
**ALGORITHM:**

1.	Initialize the register r7 with count.
2.	Get first two elements in two registers.
3.	Compare the two elements of data. If value of R0 register is high then exchange A & R0 data else increment pointer and decrement register R7.
4.	Check R7 is zero, and then move the register R0 & A.
5.	Again increment pointer and decrement R7,
6.	Check R7 is zero. If no repeat the process from step 2.
7.	Otherwise stop the program.

**PROGRAM:**
~~~
ORG 0000H 

MOV R7,#4

LOOP1:MOV R0,#40H

MOV R6,#04

LOOP: MOV A,@R0

INC R0

MOV 50H,@R0 

CJNE A,50H,NEXT

SJMP DOWN 

NEXT:JC DOWN

MOV @R0,A

DEC R0

MOV @R0,50H 

DOWN:DJNZ R6,LOOP 

DJNZ R7,LOOP1

END
~~~
**OUTPUT:**

**MEMORY WINDOW:** 

**Before execution:**
D:0x40H:
<img width="1920" height="1200" alt="ASC(in)_MPMC" src="https://github.com/user-attachments/assets/5f77b602-4185-46c0-9d86-bc7ba6f58cf6" />



After execution:
D:0x40H:
<img width="1920" height="1200" alt="ASC(out)_MPMC" src="https://github.com/user-attachments/assets/d3ec0d57-c35f-4476-bb66-c0052950cc0d" />


**Result:**

Thus the sorting of given data was done using 8051 keil and shown the output.

