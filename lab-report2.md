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

<img src="https://raw.githubusercontent.com/syasuraoka/cse15l-lab-reports/main/スクリーンショット%202023-01-16%20午前10.20.25.png" width="35%">

  * Here, two methods `public String handleRequest(URI url)` and `public static void main(String[] args) throws IOException` are called.
  * `list += "\n" + Hello`, `int port = Integer.parseInt(5555)` are the relevant arguments to those methods, and ?? are the values of any relevant fields of the class.
  * From this specific request, the value of `list` changes from `""` to `"" + "\n" + "Hello"`.

**3. And after I type `http://localhost:5555/add-message?s=Bye`, the page shows**

<img src="https://raw.githubusercontent.com/syasuraoka/cse15l-lab-reports/main/スクリーンショット%202023-01-16%20午前10.20.25.png" width="35%">

  * Here, two methods `public String handleRequest(URI url)` and `public static void main(String[] args) throws IOException` are called.
  * `list += "\n" + Bye`, `int port = Integer.parseInt(5555)` are the relevant arguments to those methods, and ?? are the values of any relevant fields of the class.
  * From this specific request, the value of `list` changes from `"" + "\n" + "Hello"` to `"" + "\n" + "Hello" + "\n" + "Bye"`.

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

## Part3
From lab in week 2, I learned the relationship between java files and the internet server. I didn't know 

