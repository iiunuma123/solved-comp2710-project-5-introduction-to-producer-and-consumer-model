Download Link: https://assignmentchef.com/product/solved-comp2710-project-5-introduction-to-producer-and-consumer-model
<br>



<strong><u>Objectives:</u> </strong>

<ol>

 <li>Complete the source code to simulate producer/consumer problem.</li>

 <li>Understand the basics of the POSIX thread library.</li>

 <li>Build a binary program on a Linux machine.</li>

 <li>Run the program and record the result of the simulation.</li>

</ol>

<strong><u>Requirements:</u> </strong>

<ul>

 <li></li>

 <li>To embark on this project, you may choose one of the following four options.</li>

</ul>

○ Important! Option 1: For Mac and Linux users, use SSH to connect to a remote Linux server. Please read files in “tutorial” on Canvas for details.

○ Important! Option 2: For Window 10 users, Please read “enviro_tutorial”, “Putty Tutorial” and “Win subsystem Linux” for details.

<ul>

 <li>Important! Read the I/O format specification carefully and follow. It is very important to your final grade of this project!</li>

 <li>You are highly recommended to use a Linux operating system.</li>

</ul>




<h1>1.  Introduction to producer and consumer model</h1>




Producer and consumer model is a model to schedule how concurrent processes and threads access the resources. It contains:




<ol>

 <li>Producer: one or multiple processes/threads that produce data or release hardware resource</li>

 <li>Consumer: the one process/threads that take in data or use hardware resource to do computation.</li>

</ol>




A producer could also be relatively a consumer to the output of another producer, vice versa.




<ol start="3">

 <li>Buffer: the destination to store the output from producer or resources and later accessed by another consumer.</li>

</ol>

Other concepts involved in our project:




<ol start="4">

 <li>POSIX thread: threads mechanism that satisfy POSIX standard (most operating system)</li>

 <li>Mutex: a “lock” that guarantee that only one person have the access.</li>

</ol>




In this project we use POSIX threads. The “pthread” is a POSIX thread library written in C++ and provides the basic functions.




To simplify our simulation, we assume there are only 2 posix threads. One is the consumer, the other is the producer. The producer generates 1 unit data each time to the buffer, and the consumer takes 1 unit data from the buffer each time. The size of the buffer is 1. One unit data is just one integer. The producer generates integers 7, 14, 21 …. into the buffer and consumer read them out from the buffer.




<h1>2.  Follow the Format Specification (10 Points)</h1>




In the source file “Firstname_Lastname.cpp”, you will find first four comment lines:




<strong>// #0#BEGIN# DO NOT MODIFY THIS COMMENT LINE! </strong>

<strong>// Firstname </strong>

<strong>// Lastname </strong>

<strong>// #0#END# DO NOT MODIFY THIS COMMENT LINE! </strong>

<strong> </strong>

Your first task is modifying the two lines <strong>between</strong> the beginning line and end line. Change them into your first name and last name. Remember the strings are case-sensitive, so capitalize the first letter of the word and follow exactly the syntax of the example.




You can see lots of similar code blocks in the file. You are free and supposed to fill your answer between those special beginning and ending comment lines. You can insert and edit multiple lines between special comment lines in anyways, however(Important!), as the comment indicated, do not modify the special begin and comment lines <strong>themselves</strong>!




Let’s do the second task. Scroll down to the bottom of the file and find those lines (press “shift + g” if you are using vi/vim):




<strong>// #8#BEGIN# DO NOT MODIFY THIS COMMENT LINE! banner_id = </strong><strong>903900281</strong><strong>; </strong>

<strong>// #8#END# DO NOT MODIFY THIS COMMENT LINE!</strong>




Look at your student ID card, check your banner ID. Again, change the “banner_id” value to your own ID. Your unique student id will be compiled into the program, and the input of the experiment also uniquely depends on your ID.




Warning: Since every student has a unique id number, the later compiled binary file is also unique. Copy binary file from other students will be easily detected!




<h1>3.  Complete Source Code</h1>




Read the source code and rest comments, try to understand the function of each line of code. Try to understand the basic usage of pthread library function from the example code of producer and the from the main function.




Follow the instructions in the comments and insert proper code into the rest 7 blocks to implement a producer/consumer model. (Only .cpp file acceptable in this project).




<h1>4.  Run and Record Simulation Result</h1>




Compile your source code into a binary program. For example, use following command to include the pthread library:




<strong>$ gcc Firstname_Lastname.c -o Firstname_Lastname -lpthread </strong>

<strong> </strong>

After you compile the c source code successfully, please use the script command to record the running result of the program Firstname_Lastname:




<strong>$ script Firstname_Lastname.script </strong>

<strong>Script started, file is Firstname_Lastname.script </strong>

<strong>./Firstname_Lastname </strong>




After you run the program, you will have the following results:




<strong>Banner id: 903900281 producer produce item 7 consumer consume item 7 producer produce item 14 consumer consume item 14 producer produce item 21 consumer consume item 21 producer produce item 28 consumer consume item 28 producer produce item 35 consumer consume item 35 producer produce item 42 consumer consume item 42 producer produce item 49 consumer consume item 49 producer produce item 56 consumer consume item 56 producer produce item 63 consumer consume item 63 producer produce item 70 </strong>

<strong>consumer consume item 70</strong>




You should have the same result except the different in the banner ID. Then exit recording and save it into typescript file “Firstname_Lastname.script” by the following command:




<strong>$ exit  </strong>

<strong>exit Script done, file is Firstname_Lastname.script </strong>

<strong> </strong>

Warning: Since every student has a unique id number, the result of the simulation is also unique. Copy simulation results from other students will be easily detected!




<h1>5.  Deliverables</h1>




Since you have generated multiple script files, please save all the script files in one directory. Create a folder “Firstname_Lastname” first. Please make sure the <strong>folder name</strong> in correct form. You can use the command mv to rename the folder:




<strong>$ mv folder-name Firstname_Lastname</strong>




Make sure all the three files are into this folder. You should have those following files inside the folder:




<ol>

 <li>commands recording file: Firstname_Lastname.script</li>

 <li>executable binary file: Firstname_Lastname</li>

 <li>source code file: Firstname_Lastname.c</li>

</ol>




Achieve all the folder into a single tarred and compressed file with a tar command.




<strong>tar -zcvf Firstname_Lastname.tar.gz Firstname_Lastname </strong>




You need to submit one tarred file with a format: Firstname_Lastname.tar.gz


