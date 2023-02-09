# Lab Report 2
## Part1
**1. My java code for `StringServer`**
```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.
    String list;

    public String handleRequest(URI url) {
        if (url.getPath().equals("/add-message")) {
            String[] parameters = url.getQuery().split("=");
            if (parameters[0].equals("s")) {
                list += "\n" + parameters[1];
                return String.format(list);
            }
            
        }
        return "";
    }
}

class StringServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println
                ("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}
```
**2. If I type `http://localhost:5555/add-message?s=Hello`, the page shows**

<img src="スクリーンショット 2023-01-29 午後4.23.57.png" width="80%">

  * Here, two methods `public String handleRequest(URI url)` and `public static void main(String[] args) throws IOException` are called.
  * `http://localhost:5555/add-message?s=Hello` is the relevant argument to method `public String handleRequest(URI url)`, and `5555` is the relevant argument to method `public static void main(String[] args) throws IOException`. And `String list = ""`, `int port = Integer.parseInt(args[0])` are the value of any relevant fields of the class.
  * From this specific request, the value of `list` changes from `""` to `"" + "\n" + "Hello"`, and the value of `port` becomes `5555`.

**3. And after I type `http://localhost:5555/add-message?s=Bye`, the page shows**

<img src="スクリーンショット 2023-01-29 午後4.24.13.png" width="80%">

  * Here, two methods `public String handleRequest(URI url)` and `public static void main(String[] args) throws IOException` are called.
  * `http://localhost:5555/add-message?s=Bye` is the relevant argument to method `public String handleRequest(URI url)`, and `5555` is the relevant argument to method `public static void main(String[] args) throws IOException`. And `String list = "" + "\n" + "Hello"`, `int port = 5555` are the values of any relevant fields of the class.
  * From this specific request, the value of `list` changes from `"" + "\n" + "Hello"` to `"" + "\n" + "Hello" + "\n" + "Bye"`, but the value of `port` doesn't change because the argument is the same.

## Part2 
**I chose `static void reverseInPlace(int[] arr)` from `ArrayExamples.java` as a buggy program.**
```
// Changes the input array to be in reversed order
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
        arr[i] = arr[arr.length - i - 1];
    }
}
```
**1. A failure-inducing input for the buggy program**
```
public void testReverseInPlace() {
    int[] input1 = { 3, 4 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 4, 3 }, input1);
	}
```
**2. An input that doesn’t induce a failure.**
```
public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
	}
```
**3. The symptom.**

<img src="スクリーンショット 2023-01-29 午後6.15.52.png" width="80%">

**4. The bug**
- Before fixed
```
// Changes the input array to be in reversed order
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
        arr[i] = arr[arr.length - i - 1];
    }
}
```
- After fixed
```
// Changes the input array to be in reversed order
  static void reverseInPlace(int[] arr) {
    int[] newArr = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArr[i] = arr[arr.length - i - 1];
    }
    for (int i = 0; i < arr.length; i+= 1) {
      arr[i] = newArr[i];
    }
  }
```
Since this fixed program put `newArr` as a temporary array to store the reverded array, the elements of the reversed array can be stored correctly in the first for loop. Thus, the reversed array can be substituted correctly into the original array. 

## Part3
From lab in week 2, I learned the connection between java files and the search bar. I didn't know the way java files read URI and show the output on screen. Lab in week 2 was really good time for me to get familiar with processing URIs in java using specific commands such as `getPath()` and `getQuery()`.

