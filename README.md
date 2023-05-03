Download Link: https://assignmentchef.com/product/solved-cs300-homework-2-search-engine
<br>
<strong>Brief Description</strong>

In this homework, you will write a search engine. The search engines in real life, search hundreds of millions web pages to see if they have the words that you have typed, and they can do this for thousands of users at a given time. In order to do these searches really fast, search engines such as Google do a lot of what we call preprocessing of the pages they search; that is, they transform the contents of a web page (which for the purposes of this homework, we will assume to consist of only strings) into a structure that can be searched very fast.

In this homework, you are going to preprocess the documents provided to you. For each unique word, you will insert a node into your <strong>AVL Search Tree</strong>​ . Of course you will also keep track of the details such as​ the document name which the word appears in and the number of times the word appears in each document. So, you need to implement a templated <strong>AVL Search Tree </strong>​        first.​







<strong>  </strong>

<strong>Program Flow </strong>

You need to get the number of documents that you need to preprocess first. Then, after getting the names of all documents from the console, you need to preprocess all the text in the documents. Only the alphabetical characters are considered, and the unique words need to be case insensitive (for example; “izmir” and “Izmir” are the same). The rest (such as digits or punctuation characters) will be ignored. For each unique word appearing in the text, you need to insert a new node into the tree. If the node is already there, you need to update the node with the information about this document. For example; you have preprocessed the “a.txt” document first and there is only one “the” word in this document. You need to insert “the” word into the <strong>AVL</strong>​<strong> Search Tree</strong>​. Then, while preprocessing the “b.txt” document, “the” word appears 4 times. So, you need to add this information ({“b.txt”, 4}) into the existing node in your BST and the node of “the” word becomes {{“a.txt”, 1}, {“b.txt”, 4}}.

After you preprocessed all the documents, you need to get a query from the console which consists of a line of strings (HINT: You may use getline(cin, line)). This line might consist of more than one word. Then, you need to output the document names which all words in the query appears including the number of times that each word appears in that document.

<strong>Hint: </strong>

<strong>struct</strong>​ ​<strong>DocumentItem</strong>​<strong> {</strong> <strong>string documentName; int count; </strong>

<strong>};</strong>

<strong>struct</strong>​ ​<strong>WordItem</strong>​<strong> {</strong> <strong>string word; </strong>

<strong><em>// List of DocumentItem’s. In order to keep the documents  </em></strong>

<strong><em>//you can again use the BST that you are going to implement. </em></strong>

<strong>}; </strong>

<strong>template </strong>​<strong>&lt;</strong>​<strong>class</strong>​<strong> Key, </strong>​<strong>class </strong>​<strong>Value&gt; </strong><strong>class</strong>​<strong> AVLSearchTree </strong>

<strong>{ </strong>

<strong>   … </strong>

<strong>};</strong>




and then when you create a ​<strong>AVL Search Tree </strong>​object it looks like this:

<strong>AVLSearchTree&lt;</strong>​<strong>string</strong>​<strong>, </strong>​<strong>WordItem</strong>​ ​<strong>*&gt; myTree;</strong>

<strong>DEMO </strong>

<strong>a.txt: </strong>

Sabanci sabanci cs CS FENS Engineering Computer <strong>b.txt: </strong>

Homeworks are so fun. WoW, What a story!!!

Sabanci is so cool. I love 2 CS CS CS CS




<strong>Sample Run 1: </strong>

Enter number of input files: 2

Enter 1. file name: a.txt

Enter 2. file name: b.txt

Enter queried words in one line: Sabanci in Document a.txt, sabanci found 2 times. in Document b.txt, sabanci found 1 times.




<strong>Sample Run 2: </strong>

Enter number of input files: 2

Enter 1. file name: a.txt

Enter 2. file name: b.txt

Enter queried words in one line: cs sabanci in Document a.txt, cs found 2 times, sabanci found 2 times. in Document b.txt, cs found 4 times, sabanci found 1 times.




<strong>Sample Run 3: </strong>

Enter number of input files: 2

Enter 1. file name: a.txt

Enter 2. file name: b.txt

Enter queried words in one line: fun computer Engineer

No document contains the given query




<strong> </strong>

<strong>Sample Run 4: </strong>

Enter number of input files: 2

Enter 1. file name: a.txt

Enter 2. file name: b.txt

Enter queried words in one line: sabanci fens in Document a.txt, fens found 1 times, sabanci found 2 times.

<strong> </strong>

<strong> </strong>

<h1>General Rules and Guidelines about Homeworks</h1>




The following rules and guidelines will be applicable to all homeworks, unless otherwise noted.




<strong>How to get help?</strong>

You may ask questions to TAs (Teaching Assistants) of CS300. Office hours of TAs are at the syllabus. Recitations will partially be dedicated to clarify the issues related to homework, so it is to your benefit to attend recitations.




<h2>What and Where to Submit</h2>

Please see the detailed instructions below/in the next page. The submission steps will get natural/easy for later homeworks.




<h2>Grading and Objections</h2>

<u>Careful about the semi-automatic grading:</u> Your programs will be graded using a semi-automated system. Therefore, you should follow the guidelines about input and output order; moreover, you should also use same prompts as given in the Sample Runs. Otherwise semi-automated grading process will fail for your homework, and you may get a zero, or in the best scenario you will lose points.




<u>Grading:</u>

<ul>

 <li>Late penalty is 10% off the full grade and only two late days are allowed.</li>

 <li><strong>Having a correct program is necessary, but not sufficient to get the full grade. Comments, indentation, meaningful and understandable identifier names, informative introduction and prompts, and especially proper use of required functions, unnecessarily long program (which is bad) and unnecessary code duplications will also affect your grade.</strong></li>

 <li>Please submit your own work only (even if it is not working). It is really easy to find out “similar​ ” programs!​</li>

 <li>For detailed rules and course policy on plagiarism, please check out</li>

</ul>







<a href="http://myweb.sabanciuniv.edu/gulsend/courses/cs201/plagiarism/">http://myweb.sabanciuniv.edu/gulsend/courses/cs201/plagiarism/</a>







<u>Grade announcements:</u> Grades will be posted in SUCourse, and you will get an Announcement at the same time. You will find the grading policy and test cases in that announcement.




<u>Grade objections:</u> It is your right to object to your grade if you think there is a problem, but before making an objection please try the steps below and if you still think there is a problem, contact the TA that graded your homework from the email address provided in the comment section of your announced homework grade or attend the specified objection hour in your grade announcement.

<ul>

 <li>Check the comment section in the homework tab to see the problem with your homework.</li>

 <li>Download the .zip file you submitted to SUCourse and try to compile it.</li>

 <li>Check the test cases in the announcement and try them with your code. Compare your results with the given results in the announcement.</li>

</ul>

<h1>What and where to submit (IMPORTANT)</h1>




Submissions guidelines are below. Most parts of the grading process are automatic. Students are expected to strictly follow these guidelines in order to have a smooth grading process. If you do not follow these guidelines, depending on the severity of the problem created during the grading process, 5 or more penalty points are to be deducted from the grade.




<u>Add your name to the program:</u> It is a good practice to write your name and last name somewhere in the beginning program (as a comment line of course).




<u>Name your submission file:</u>

<ul>

 <li><u>Use only English alphabet letters, digits or underscore in the file names. Do not use blank,</u> <u>Turkish characters or any other special symbols or characters.</u></li>

 <li>Name your cpp file that contains your program as follows.</li>

</ul>

<h2>                                 “​ SUCourseUserName_yourLastname_yourName_HWnumber.cpp​ ”​</h2>

<ul>

 <li>Your SUCourse user name is actually your SUNet username which is used for checking sabanciuniv e-mails. Do NOT use any spaces, non-ASCII and Turkish characters in the file name. For example, if your SUCourse user name is cago, name is Çağlayan, and last name is Özbugsızkodyazaroğlu, then the file name must be:</li>

</ul>

<strong>cago_ozbugsizkodyazaroglu_caglayan_hw2.cpp</strong> ●       Do not add any other character or phrase to the file name.

<ul>

 <li>Make sure that this file is the latest version of your homework program.</li>

 <li>You need to submit ALL .cpp and .h files in addition to your main.cpp in your VS solution.</li>

</ul>




<u>Submission:</u>

<ul>

 <li>Submit via SUCourse ONLY! You will receive no credits if you submit by other means</li>

</ul>

(e-mail, paper, etc.).

<ol>

 <li>Click on “Assignments” at CS300 SUCourse.</li>

 <li>Click Homework 2 in the assignments list.</li>

 <li>Click on “Add Attachments” button.</li>

 <li>Click on “Browse” button and select the zip file that you generated.</li>

 <li>Now, you have to see your zip file in the “Items to attach” list.</li>

 <li>Click on “Continue” button.</li>

 <li>Click on “Submit” button. We cannot see your homework if you do not perform this step even if you upload your file.</li>

</ol>




<u>Resubmission:</u>

<ul>

 <li>After submission, you will be able to take your homework back and resubmit. In order to resubmit, follow the following steps.

  <ol>

   <li>Click on “Assignments” at CS300 SUCourse.</li>

   <li>Click Homework 2 in the assignments list.</li>

   <li>Click on “Re-submit” button.</li>

   <li>Click on “Add/remove Attachments” button</li>

   <li>Remove the existing zip file by clicking on “remove” link. This step is very important. If you don’​ t delete the old zip file, we get both files and the old one may be graded.​</li>

   <li>Click on “Browse” button and select the new zip file that you want to resubmit.</li>

   <li>Now, you have to see your new zip file in the “Items to attach” list.</li>

   <li>Click on “Continue” button.</li>

   <li>Click on “Submit” button. We cannot see your homework if you do not perform this step even if you upload your file.</li>

  </ol></li>

</ul>