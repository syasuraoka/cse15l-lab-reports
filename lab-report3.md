# Lab Report 3
## Four interesting command-line options or alternate ways to use `grep`

**1. `grep -r <string>`**

The -r option is used to specify that grep should search for the pattern in a recursive manner, meaning that it should search for the pattern not just in the specified file, but also in all of the files in subdirectories of the current directory.

* Example1: `grep -r "Lucayans"`
  
  <img src="スクリーンショット 2023-01-29 午後4.23.57.png" width="80%">

  Here, I can find a file whose name contains `Lucayans` from skill-demo1-data directory. It's useful for 

* Example2: `grep -r "Shibuya"`

  <img src="スクリーンショット 2023-01-29 午後4.23.57.png" width="80%">

**2. `grep -i <string> <file>`**

The -i option is used to specify that grep should perform a case-insensitive search. This means that the search will match the pattern regardless of whether the letters in the pattern are uppercase or lowercase.

* Example1: `grep -i "SHINAGAWA" written_2/travel_guides/berlitz1/WhereToJapan.txt`
	
  <img src="スクリーンショット 2023-01-29 午後4.23.57.png" width="80%">
	
* Example2: `grep -i "OSAKA" written_2/travel_guides/berlitz1/WhereToJapan.txt`

  <img src="スクリーンショット 2023-01-29 午後4.23.57.png" width="80%">

**3. `grep -e <string> -e <string> <file>`**

The -e option is used to specify a pattern to search for. This option is useful when you need to search for multiple patterns in a single command.

* Example1: `grep -e "Shibuya" -e "Shinagawa" written_2/travel_guides/berlitz1/WhereToJapan.txt`

  <img src="スクリーンショット 2023-01-29 午後4.24.13.png" width="80%">
  
* Example2: `grep -e "Shibuya" -e "Shinagawa" written_2/travel_guides/berlitz1/WhereToJapan.txt`

**4. `grep -c <string> <file>`**

The -c option is used to specify that grep should display only a count of the number of lines that match the pattern, instead of the lines themselves.

* Example1: `grep -c "Shibuya" written_2/travel_guides/berlitz1/WhereToJapan.txt`
  
  <img src="スクリーンショット 2023-01-29 午後4.24.13.png" width="80%">
  
* Example2: `grep -c "Shibuya" written_2/travel_guides/berlitz1/WhereToJapan.txt`
  
  <img src="スクリーンショット 2023-01-29 午後4.24.13.png" width="80%">
 
