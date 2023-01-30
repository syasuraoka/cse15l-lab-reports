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
**I chose `ArrayExamples.java` as a buggy program.**
```
public class ArrayExamples {

  // Changes the input array to be in reversed order
  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }

  // Returns a *new* array with all the elements of the input array in reversed
  // order
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }

  // Averages the numbers in the array (takes the mean), but leaves out the
  // lowest number when calculating. Returns 0 if there are no elements or just
  // 1 element in the array
  static double averageWithoutLowest(double[] arr) {
    if(arr.length < 2) { return 0.0; }
    double lowest = arr[0];
    for(double num: arr) {
      if(num < lowest) { lowest = num; }
    }
    double sum = 0;
    for(double num: arr) {
      if(num != lowest) { sum += num; }
    }
    return sum / (arr.length - 1);
  }


}
```
**1. A failure-inducing input for the buggy program**

**2. An input that doesn’t induce a failure.**

**3. The symptom.**

**4. The bug**
- Before fixed
- After fixed

## Part3
From lab in week 2, I learned the relationship between java files and the internet server. I didn't know 

