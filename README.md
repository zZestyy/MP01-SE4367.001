# MP01-SE4367.001
### **Author:** Val Evander M. Wong (vmw170030)
Machine Project 1 for CS 4367.001. Exploration of the Soot Static Program Analysis Framework.

## Importing the files
1. 

## Part 0 - Getting Started
**Files Utilized:**
- TestSoot.java
- HelloThread.java

Description:
Utilize Soot, through 'TestSoot.java', to analyze 'HelloThread.java'. 'TestSoot.java' outputs Jimple statements in each method of the class HelloThread.

Execution Instruction(s):
1. Add necessary java files into the same project source folder.
2. Run 'TestSoot.java'.

## Part 1 - Control Flow Analysis (Dominators)
**Files Utilized:**
- TestDominator.java
- DominatorFinder.java
- GCD.java

Description:
Given a program GCD, utilize Soot to build a control graph where each object in the control graph is an object of type DominatorFinder. Then finds all the dominators using DominatorFinder class.

Execution Instruction(s):
1. Add necessary java files into the same project source folder.
2. Run 'TestDominator.java'

## Part 2 - Data Flow Analysis (Call Graph Construction)
**Files Utilized:**
- Example.java
- TestSootCallGraph.java

Description:
Run and Compare class hierarchy analysis (CHA) and points-to-analysis (PTA).

Execution Instruction(s):
1.  Add necessary java files into the same project source folder.
2.  Run 'TestSootCallGraph.java'

Question: Which method does animal.saySomething() in the main method of Example.java call?\
Answer: animal.saySomething() calls Cat.saySomething through points-to-analysis (PTA).

Question: Compare the precision and speed between CHA and PTA.\
Answer: PTA is much more precise because it won't report false calls which CHA may do. PTA, however, has a higher runtime of 2120 milliseconds as opposed to CHA's faster time of 1927 milliseconds.

## Part 3 - Program Instrumentation with Soot
**Files Utilized:**
- Example.java
- TestSootLogging.java
- HelloThread.java
- Log.java
- TestSootLoggingHeap.java

Description:
TestSootLogging.java logs all method calls in the main method of Example.java. TestSootLoggingHeap.java logs every read and write statement that accesses data on the heap.

Execution Instruction(s):
1. Add 'Example.java' and 'TestSootLogging.java' to the same project source folder.
2. Run 'TestSootLogging.java'.
3. Add 'HelloThread.java', 'Log.java', and 'TestSootLoggingHeap.java' to the same project source folder.
4. Run 'TestSootLoggingHeap.java'.
