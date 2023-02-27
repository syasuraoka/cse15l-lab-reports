# Lab Report 3
## Four interesting command-line options or alternate ways to use `grep`

**1. `grep -r <string>`**

The -r option is used to specify that grep should search for the pattern in a recursive manner. It should search for the pattern not just in the specified file, but also in all of the files in subdirectories of the current directory.

(Source: https://eng-entrance.com/linux-command-grep)

* Example1: `grep -r "Lucayans"`
  
  <img src="スクリーンショット 2023-02-09 午後1.03.19.png" width="80%">

  Here, I can find a file which contains `Lucayans` from skill-demo1-data directory. It's useful when I don't know which file has Lucayans.
  
* Example2: `grep -r "Shibuya"`

  <img src="スクリーンショット 2023-02-09 午後1.22.17.png" width="80%">
  
  Here, I can find a file which contains `Shibuya` from skill-demo1-data directory. It's useful when I don't know which file has Shibuya.

**2. `grep -i <string> <file>`**

The -i option is used to specify that grep should perform a case-insensitive search, meaning that the search will match the pattern regardless of whether the letters in the pattern are uppercase or lowercase.

(Source: https://eng-entrance.com/linux-command-grep)

* Example1: `grep -i "SHINAGAWA" written_2/travel_guides/berlitz1/WhereToJapan.txt`
	
  <img src="スクリーンショット 2023-02-09 午後1.24.49.png" width="80%">
  
  Here, I can find a word `SHINAGAWA`(case-insensitive) from `WhereToJapan.txt` file. It's useful when I am not sure whether to use upper or lower case letters to find Shinagawa.
	
* Example2: `grep -i "SHIBUYA" written_2/travel_guides/berlitz1/WhereToJapan.txt`

  <img src="スクリーンショット 2023-02-12 午後6.43.42.png" width="80%">
  
  Here, I can find a word `SHIBUYA`(case-insensitive) from `WhereToJapan.txt` file. It's useful when I am not sure whether to use upper or lower case letters to find Shibuya.

**3. `grep -e <string> -e <string> <file>`**

The -e option is used to specify multiple search patterns, each preceded by the -e option. This option is useful when I need to search for multiple patterns in a single command.

(Source: https://eng-entrance.com/linux-command-grep)

* Example1: `grep -e "Shibuya" -e "Shinagawa" written_2/travel_guides/berlitz1/WhereToJapan.txt`

  <img src="スクリーンショット 2023-02-12 午後6.50.07.png" width="80%">
  
  Here, I can find two words `Shibuya` and `Shinagawa` from `WhereToJapan.txt` file. It's useful when I need to search both Shibuya and Shinagawa in a single command.
  
* Example2: `grep -e "Shinjuku" -e "Ginza" written_2/travel_guides/berlitz1/WhereToJapan.txt`
  
  <img src="スクリーンショット 2023-02-12 午後6.45.10.png" width="80%">
  
  Here, I can find two words `Shinjuku` and `Ginza` from `WhereToJapan.txt` file. It's useful when I need to search both Shinjuku and Ginza in a single command.

**4. `grep -c <string> <file>`**

The -c option is used to specify that grep should display only a count of the number of lines that match the pattern, instead of the lines themselves.

(Source: https://chat.openai.com/chat)

* Example1: `grep -c "Shibuya" written_2/travel_guides/berlitz1/WhereToJapan.txt`
  
  <img src="スクリーンショット 2023-02-12 午後6.45.32.png" width="80%">
  
  Here, I can find the number of lines that has `Shibuya` in `WhereToJapan.txt` file. It's useful when I want to know the number of lines on which Shibuya is written.
  
* Example2: `grep -c "Shinagawa" written_2/travel_guides/berlitz1/WhereToJapan.txt`
  
  <img src="スクリーンショット 2023-02-12 午後6.45.49.png" width="80%">
  
  Here, I can find the number of lines that has `Shinagawa` in `WhereToJapan.txt` file. It's useful when I want to know the number of lines on which Shinagawa is written.
 
