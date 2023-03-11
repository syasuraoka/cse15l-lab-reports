# Lab Report 5
## Four interesting command-line options or alternate ways to use `find`

**1. `find <directory> -name <pattern>`**

`find -name` is a command used in the terminal or command prompt to search for files and directories that match a specific name or pattern. Note that `.` as `<directory>` indicates current directory.

(Source: [https://eng-entrance.com/linux-command-find](https://eng-entrance.com/linux-command-find))

* Example1: `find . -name '*a'`
  
  <img width="586" alt="スクリーンショット 2023-03-10 午後7 19 46" src="https://user-images.githubusercontent.com/115061986/224462614-f9698d52-2da1-4f8d-ae40-eacb2254c630.png">

  Here, I can find files ending with a. This is more efficient than manually searching through directories to find files ending with a.
  
* Example2: `find . -name 'a*'`

  <img width="586" alt="スクリーンショット 2023-03-10 午後7 19 57" src="https://user-images.githubusercontent.com/115061986/224462618-43dd0efc-be9d-486f-8a9e-732f3d4ac6ea.png">
  
  Here, I can find files starting with a. This is more efficient than manually searching through directories to find files starting with a.

**2. `find <directory> -size <size>`**

`find -size` is a command used in the terminal or command prompt that lists files of a specified size or smaller. Note that `.` as `<directory>` indicates current directory.

(Source: [https://eng-entrance.com/linux-command-find](https://eng-entrance.com/linux-command-find))

* Example1: `find . -size -6c`

  <img width="586" alt="スクリーンショット 2023-03-10 午後7 38 24" src="https://user-images.githubusercontent.com/115061986/224463123-00a4f598-cb75-4cf3-8589-1d17e773011e.png">

  Here, I can find several files under 6 bytes (6c means 6 bytes). This is useful when searching/listing files of 6 bytes or less.
  
* Example2: `find . -size -60c`

  <img width="586" alt="スクリーンショット 2023-03-10 午後7 38 05" src="https://user-images.githubusercontent.com/115061986/224463107-9aa3932f-d49b-465c-aa3b-e09857eeeb04.png">
  
  Here, I can find several files under 60 bytes (60c means 60 bytes). This is useful when searching/listing files of 60 bytes or less.


**3. `find <directory> -atime <time>`**

`find -atime` is a command used in the terminal or command prompt that lists files accessed at a specified time or later/earlier. Note that `-` in `<time>` indicates later, and `+` indicates earlier. Also note that `.` as `<directory>` indicates current directory.

(Source: [https://eng-entrance.com/linux-command-grep](https://eng-entrance.com/linux-command-grep))

* Example1: `find . -atime -3`

  <img width="586" alt="スクリーンショット 2023-03-10 午後8 19 15" src="https://user-images.githubusercontent.com/115061986/224464776-fcd698a6-e81f-4b5a-a088-cffdd9152251.png">

  
  Here, I can find files that are accessed within 3 days. It's useful when searching/listing files accessed within 3 days.
  
* Example2: `find . -atime +3`
  
  <img width="593" alt="スクリーンショット 2023-03-10 午後8 28 37" src="https://user-images.githubusercontent.com/115061986/224464861-6283f6a6-bda7-4a7e-a48c-a8d2dba84108.png">
  
  Here, I can find files that are accessed prior to the past 3 days. It's useful when searching/listing files accessed prior to the past 3 days.

**4. `find <directory> -empty`**

`find -empty` is a command used in the terminal or command prompt that lists empty files. Note that `.` as `<directory>` indicates current directory.

(Source: [https://chat.openai.com/chat](https://chat.openai.com/chat))

* Example1: `find . -empty `
  
  <img width="593" alt="スクリーンショット 2023-03-10 午後8 37 00" src="https://user-images.githubusercontent.com/115061986/224465187-9d610ae6-ea54-4141-b265-50a6cc6a0892.png">

  
  Here, I can find empty files in my current directory. It's useful when searching/listing emtpy files in current directory.
  
* Example2: `find ./skill-demo1-data -empty`
  
  <img width="699" alt="スクリーンショット 2023-03-10 午後8 37 51" src="https://user-images.githubusercontent.com/115061986/224465189-437fe5dc-c805-4996-a3ef-82e262048169.png">

  Here, I can find empty files in `./skill-demo1-data`. It's useful when searching/listing empty files in `./skill-demo1-data`.
 

