# MP01-SE4367.001
### **Author:** Val Evander M. Wong (vmw170030)
Machine Project 1 for CS 4367.001. Exploration of the Soot Static Program Analysis Framework.

***NOTE: Must use JAVA 8 or below.***

## Prior Instructions:
1. Designate a project folder for a Java Project. Create a folder within that Java Project and name it 'lib'.
2. Add 'Soot-3.3.0.jar' within the lib folder.
3. Create a Java Project within Eclipse IDE using the designated project folder.
4. Import all .java files into the **same project source folder** and **under the default package**.
5. Right Click on the project. Select 'Properties'.
6. Select 'Java Build Path'. Select 'Libraries' tab.
7. Add External JARs and select the 'Soot-3.3.0.jar' within the lib folder.


## Part 0 - Getting Started
**Files Utilized:**
- TestSoot.java
- HelloThread.java

**Description:**\
Utilize Soot, through 'TestSoot.java', to analyze 'HelloThread.java'. 'TestSoot.java' outputs Jimple statements in each method of the class HelloThread.

Execution Instruction(s):
1. Add necessary java files into the same project source folder.
2. Run 'TestSoot.java'.


## Part 1 - Control Flow Analysis (Dominators)
**Files Utilized:**
- TestDominator.java
- DominatorFinder.java
- GCD.java

**Description:**\
Given the program GCD, utilize Soot to build a control graph where each object in the control graph is an object of type DominatorFinder. Then finds all the dominators using DominatorFinder class.

Execution Instruction(s):
1. Add necessary java files into the same project source folder.
2. Run 'TestDominator.java'


## Part 2 - Data Flow Analysis (Call Graph Construction)
**Files Utilized:**
- Example.java
- TestSootCallGraph.java

**Description:**\
Run and Compare class hierarchy analysis (CHA) and points-to-analysis (PTA).

Execution Instruction(s):
1.  Add necessary java files into the same project source folder.
2.  Run 'TestSootCallGraph.java'

**Question:** Which method does animal.saySomething() in the main method of Example.java call?\
**Answer:** animal.saySomething() calls Cat.saySomething proven through points-to-analysis (PTA).

**Question:** Compare the precision and speed between CHA and PTA.\
**Answer:** PTA is much more precise because it won't report false calls which CHA may do. PTA, however, has a higher runtime of 2120 milliseconds as opposed to CHA's faster time of 1927 milliseconds. PTA needs to analyze the data flow in the whole program, and often takes much more time and memory than CHA


## Part 3 - Program Instrumentation with Soot
**Files Utilized:**
- Example.java
- TestSootLogging.java
- HelloThread.java
- Log.java
- TestSootLoggingHeap.java

**Description:**\
'TestSootLogging.java' logs all method calls in the main method of 'Example.java'. 'TestSootLogging.java' also creates a folder 'sootOutput' in the project folder that contains Jimple files. 'TestSootLoggingHeap.java' logs every read and write statement that accesses data on the heap of 'HelloThread.java'.

Execution Instruction(s):
1. Add 'Example.java' and 'TestSootLogging.java' to the same project source folder.
2. Run 'TestSootLogging.java'.
3. Add 'HelloThread.java', 'Log.java', and 'TestSootLoggingHeap.java' to the same project source folder.
4. Run 'TestSootLoggingHeap.java'.
