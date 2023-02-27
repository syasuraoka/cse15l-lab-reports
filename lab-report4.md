# Lab Report 4
## Reproduce the task from the competition on your own

For each numbered step starting right after the timer (so steps 4-9), take a screenshot, and write down exactly which keys you pressed to get to that step. For special characters like <enter> or <tab>, write them in angle brackets with code formatting. Then, summarize the commands you ran and what the effect of those keypresses were.

For example, when you run the tests, you might want to use the up arrow or Ctrl-R to access your bash history rather than typing in the full command with classpath, etc. You might say something like this accompanying the screenshot for running the tests:

Keys pressed: <up><up><up><up><enter>, <up><up><up><up><enter>

The javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java command was 4 up in the search history, so I used up arrow to access it. Then the java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore command was 4 up in the history, so I accessed and ran it in the same way.

Add this lab report to your Github Pages site, and submit a PDF of it as usual.

**Step4. Log into ieng6**

<img src="スクリーンショット 2023-02-09 午後1.03.19.png" width="80%">
  
Keys pressed: `<up><up><enter>`

`ssh cs15lwi23ahs@ieng6.ucsd.edu` command was 2 up in the search history, so I used up arrow to access it.

**Step5. Clone your fork of the repository from your Github account**
  
<img src="スクリーンショット 2023-02-09 午後1.03.19.png" width="80%">
  
Keys pressed: `git clone git@github.com:syasuraoka/lab7.git`, `<enter>`
  
I typed `git clone git@github.com:syasuraoka/lab7.git` to clone lab7 repository. Then, I pressed `<enter>` as a passphrase for key `/home/linux/ieng6/cs15lwi23/cs15lwi23ahs/.ssh/id_rsa`.
  
**Step6. Run the tests, demonstrating that they fail**
  
<img src="スクリーンショット 2023-02-09 午後1.03.19.png" width="80%">
  
Keys pressed: `cd lab7`,`<up><up><up><up><up><up><enter>`, `<up><up><up><up><up><up><enter>`
  
I typed `cd lab7` to go to lab7 directory. Then, the `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` command was 6 up in the search history, so I used up arrow to access it. Then, the `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests` command was 6 up in the history, so I accessed and ran it in the same way.
  
**Step7. Edit the code file to fix the failing test**
  
<img src="スクリーンショット 2023-02-09 午後1.03.19.png" width="80%">
  
Keys pressed: `<up><up><up><up><up><up><enter>`, many keys to fix the ListExamples.java file, `^X`, `Y`, `<enter>` 
  
I typed `cd lab7` to go to lab7 directory. Then, the `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` command was 6 up in the search history, so I used up arrow to access it. Then, the `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests` command was 6 up in the history, so I accessed and ran it in the same way.
  
**Step8. Run the tests, demonstrating that they now succeed**
  
<img src="スクリーンショット 2023-02-09 午後1.03.19.png" width="80%">
  
Keys pressed: `<up><up><enter>`, `<up><up><enter>`

The `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` command was 2 up in the search history, so I used up arrow to access it. Then the `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests` command was 2 up in the history, so I accessed and ran it in the same way.
  
**Step9. Commit and push the resulting change to your Github account**
  
<img src="スクリーンショット 2023-02-09 午後1.03.19.png" width="80%">
  
Keys pressed: `git add .`, `git commit -m "updated`, `git push`

I typed `git add .` to stage the files. Then, I typed `git commit -m "updated` to commit the files. Then, I typed `git push` to push the changes to the remote repository.
