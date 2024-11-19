java c
Advanced Software Engineering (CSSE7023)
Assignment 2 — Semester 2, 2024Overview This assignment builds on Individual Assignment  1 and will extend your practical experience developing a Java program, including a GUI. Additionally, you must develop and submit JUnit tests for some of the classes in the implementation. You are encouraged to write tests for all your classes and for the GUI part of your implementation as well, but you do not have to submit these. You will be assessed on your ability to
•  implement a program that complies with the specification,
•  develop JUnit tests that can detect bugs in class implementations,
•  and develop code that conforms to the style. conventions of the course.Task - Advanced  Software Engineering In this assignment,  you will update,  modify and extend code written by others. You will modify and extend a command-line version of the DemoWorld packages, written by other programmers (not your own versions) from Assignment 1, in order to extend the functionality to read and interpret (parse) a Character sheet and to provide a GUI for an interactive user to update the Character’s state. This will not only involve developing new interfaces and classes, but will also require you to modify existing code written by others.You will also write tests for some of the classes in the implementation and include these in your submission. Only the tests for specific classes are to be submitted. Any test you write for other aspects of the project are not to be included in your submission.  The required tests that you have designed and submitted will then be assessed for their effectiveness against correct implementations of the code, as well as a number of incorrect implementations specifically written by the staff to test your tests.Your submitted implementation will read and interpret a  Character sheet in a text file specifically named “demo.sheet”. Your submission will be tested against a number of “demo.sheet” files, not only the one included in the supplied code. You cannot change the file name for your submission.  It is referenced from main, which is included in the supplied code, and cannot be changed (supplied code gets overwritten for every submission – modifying supplied code has no effect for assessment).
The specification is provided in the form. of JavaDocs, which describe the classes and interfaces that your assignment must implement.The Character class has not been included in the supplied code. You must develop and submit a new Character class. You should start with the Character class from the Individual Assignment 1 solution and update, modify and refactor it to meet the requirements and use the new methods now described in the supplied specification in the Individual Assignment 2 JavaDoc.   Don’t forget to refactor the JavaDoc comments within your new Character class to match the supplied Individual Assignment 2 JavaDoc.Common Mistakes Please carefully read Appendix A. It outlines common and critical mistakes which you must avoid to prevent a loss of grades.  If at any point you are even slightly unsure, please check as soon as possible with course staff.Plagiarism All work on this assignment is to be your own individual work.  By submitting the assignment you are claiming it is entirely your own work.  You may discuss the overall general design of the application with other students.  Describing details of how you implement your design with another student is considered to be collusion and will be counted as plagiarism.You may not copy fragments of code that you find on the Internet to use in your assignment.  Code supplied by course staff (from this semester) is acceptable, but must be clearly acknowledged as described in the next paragraph.
You may find ideas of how to solve problems in the assignment through external resources (e.g.  StackOver- flow, textbooks, ChatGPT, CoPilot...).  If you use these ideas in designing your solution you must cite them.
To cite a resource, provide the full bibliographic reference for the resource in file called refs .md. The refs .md file must be in the root folder of your project. For example:
> cat refs .md
[1]  E .  W .  Dijkstra ,  "Go  To  Statement  Considered  Harmful , "  Communications  of  the  ACM ,   vol  11  no .  3,  pp  147-148,  Mar .  1968.  Accessed :  Mar .  6,  2024 .  [Online] .  Available : https://www.cs.utexas.edu/users/EWD/transcriptions/EWD02xx/EWD215.html
[2]  B .  Liskov  and  J .  V .  Guttag ,  Program  development in Java :  abstraction ,
specification ,  and  object-oriented  design .  Boston :  Addison-Wesley,  2001 .
[3]  T .  Hawtin ,  "String  concatenation :  concat ()  vs  '+'  operator , "  stackoverflow .com ,
Sep .  6,  2008 .  Accessed :  Mar .  8,  2024 .  Available :
https://stackoverflow.com/questions/47605/string-concatenation-concat-vs-operator [4]  ChatGPT-4,  OpenAI ,  "How  do  I  use  invokeLater  in  Java  Swing? "  (no  code  copied),
Accessed  on :  Sep .  19,  2024 .  [Online] .  Available :  https://chat .openai.com/ >
In the code where you use the idea, cite the reference in a comment. For example:
/**
*  What  method1  does .
*  [1] Used  a method  to  avoid  gotos  in my  logic .
*  [2]  Algorithm  based  on  section  6.4. */
public  void method1 ()  . . .
/**
*  What  method2  does . */
public void method2 ()  {
System.out .println("Some  "  +  "content . ")  //  [3]  String  concatenation  using  +  operator . }
You must be familiar with the university’s policy on plagiarism.
https://uq.mu/rl553
If you have questions about what is acceptable, please ask course staff.Generative Artificial Intelligence You  are required to implement your solution on your own, without using code from generative artificial intelligence (AI) tools, the Internet, or any source other than the supplied code for the assignment.   This  is  a  learning  exercise  and you will harm your learning if you use AI tools inappropriately. Remember, you will be required to write code, by hand, in the final exam.
Specification
The specification document is provided in the form. of JavaDocs.
。Implement the classes and interfaces exactly as described in the JavaDocs.
。Read the JavaDocs carefully and understand the specification before programming.
。Do not change the public specification in any way, including changing the names of, or adding additional, public classes, interfaces, methods, or fields.
。You are encouraged to add ad代 写Advanced Software Engineering (CSSE7023) Assignment 2 — Semester 2, 2024Java
代做程序编程语言ditional private members, classes, or interfaces as you see fit.
。JUnit 4 test cases that you submit must only test the public and protected methods as specified in the JavaDocs. They must not rely on any other members, classes, or interfaces you may have added to the classes being tested. You may create private members and other classes in your test code.
You can download the JavaDoc specification from BlackBoard (Assessment → Individual Assignment 2) or access it at the link below.
https://csse7023.uqcloud.net/assessment/assign2/docs/
Getting Started
To get started, download the provided code from BlackBoard (Assessment → Individual Assignment 2). Extract the archive in a directory and open it with IntelliJ.
Grading
Five aspects of your solution will be considered in grading your submission:
1. Automated functionality test: the classes that you must implement will have a number of JUnit unit tests associated with them that we will use to test your implementation.  The percentage of test cases that pass will be used as part of your grade calculation.  Classes may be weighted differently depending on their complexity.
2. JUnit test cases: your JUnit test cases will be assessed by testing both correct and faulty implementations. The percentage of implementations that are appropriately identified as correct or faulty will be used as part of your grade calculation.
3. Manual functionality test: to ensure that the look and feel of your GUI implementation is the same as the original implementation, and to ensure that the Save  As and Open menu options are properly invoked by the GUI, a small scenario with a number of steps in it will be manually executed by course staff.  The faults identified during these steps will be used as part of your grade calculation.
4. Automated  style. check:  as  for Assignment  1, style. checking on your code will be performed using the Checkstyle tool. The number of style. violations identified by the Checkstyle tool will be used to apply a percentage penalty to your Automated functionality test score. Note: There  is a plug-in available for IntelliJ that will highlight style. violations in your code.  Instructions for installing this plug-in are available in the Java Programming Style. Guide on BlackBoard (Learning Resources → Guides).  If you correctly use the plug-in and follow the style. requirements, it should be relatively straightforward to do well for this part of the assessment.
5. Manal style check:  as for Assignment 1, the style. and structure of your code will also be assessed by course staff. Your performance on these criteria will also be used as part of your grade calculation.  It is therefore critically important that you read and understand the feedback for this part on Assignment 1, as soon as it is made available, so that you can address any issues in this assignment.  See Appendix B for criteria that will be used to assess the readability of your code.
Appendix B shows how the above are combined to determine your grade for the assignment. Automated aspects of the assessmentThree aspects of assessment will performed automatically in a Linux environment:  execution of JUnit test cases, running your JUnit test cases on correct and faulty implementations, and automated style. check using Checkstyle. The environment will not be running Windows, and neither IntelliJ nor Eclipse (or any other IDE) will be involved.  OpenJDK 21 with the JUnit 4 library will be used to compile and execute your code and tests. To prevent infinite loops, or malicious code, from slowing down Gradescope, any test that takes longer than 10 seconds to execute will be killed and identified as failing.  All tests should execute in a small fraction of a second. Any test taking longer than a second to execute indicates faulty logic or malicious code. Similarly, any of your JUnit test cases that take longer than 20 seconds to execute on one of the correct/faulty implementations, or that consume more memory than is reasonable, will be stopped.IDEs like IntelliJ provide code completion hints. When importing Java libraries they may suggest libraries that are not part of the standard library.  These will not be available in the test environment and your code will not compile.  When uploading your assignment to Gradescope, ensure that Gradescope says that your submission was compiled successfully.
Your code must compile.
If your submission does not compile, you will receive no marks.
Submission
Submission is via Gradescope.  Submit your code to Gradescope early and often.  Gradescope will give you some limited feedback on your code. Most importantly, it confirms that your code compiles and runs.
It will not do extensive testing before assessment, and it is not a substitute for testing your code yourself!
What to Submit Your submission must have the following internal structure:
src/          Folders (packages) and  .java files for classes that you modified or created for this assignment.
test/        Folders (packages) and  .java files for the JUnit tests that are required for this assignment.
refs .md    File containing the references for any citations in your code.Included in the root directory of the provided code are the files bundle .sh and bundle .cmd.   For  MacOS and Unix users, run the $bash  ./bundle.sh file to execute it.  For Windows users, double-click or run the .\bundle.cmd file to execute it. This will create a submission.zip file for you to upload to Gradescope.You can create the submission zip file yourself using a zip utility. If you do this, ensure that you do not miss any files or directories.  Also ensure that you do not add any extra files.  We recommend using the provided bundle scripts.
Ensure that your classes and interfaces correctly declare the package they are within. For example, Character.java should declare package  demoworld.model;.
Only submit the src and test folders and the refs .md file in the root directory of your project. Do not submit any other files (e.g. no  .class files or IDE files).Provided tests A small number of unit tests will be provided in Gradescope to show your code compiled and can be tested.  These are meant to provide you with an opportunity to receive feedback on whether the very basic functionality of your code works or not.  Passing the provided unit tests does not guarantee that you will pass all the tests used for functionality grading.





         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
