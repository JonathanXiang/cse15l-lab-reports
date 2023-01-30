# Lab 2
By Jonathan Xiang

## Part 1: String Server

The code that I wrote for String Server is below:

```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler{
    String storedString = "";
    public String handleRequest(URI url){
        if(url.getPath().contains("/add-message")){
            String[] parameters = url.getQuery().split("=");
            storedString += parameters[1] + "\n";
            return storedString;
        }
        else{
            return "404 Not Found";
        }
    }
}
class StringServer{
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            return;
        }

        int port = Integer.parseInt(args[0]);
        Server.start(port, new Handler());
    }
}
```

In the screenshot below, the handleRequest method is called. The relevant
values for this method are the URI called url, given as a parameter which the
method uses to see what it should do, and the storedString, which is
the String the method will add to everytime "/add-message" is used.
In this case, storedString was changed since "Hello, this is the first message"
and "\n" were concatenated to it.

![Image](firstmessage.png)


In this screenshot, the handleRequest method is also called. The relevant methods to
this method are the same as above, but this timem storedString is changed differently.
This time, "This is the second message, it is one line down" is the String appended.
You can also see that it is one line down because of "\n" we appended in the first message.

![Image](secondmessage.png)


## Part 2: Bug Testing from Lab 3

In Lab 3, there is a bug in the averageWithoutLowest method in ArrayExamples where
it removes all values that are equal to the lowest instead of just removing one. Below
are the tests I made for this method.

```
@Test
public void testAverageWithoutLowest1(){
  double[] input1 = {3.0, 3.0, 3.0, 9.0};
  assertEquals(5.0, ArrayExamples.averageWithoutLowest(input1), 0);
}
```
This test induces failure. Because multiple of the lowest value exists
in the input list (3.0), all of them are removed and the average is calculated incorrectly.

```
@Test
public void testAverageWithoutLowest2(){
  double[] input1 = {3.0, 4.0, 5.0, 9.0};
  assertEquals(6.0, ArrayExamples.averageWithoutLowest(input1), 0);
}
```
This test doesn't induce failure. Because there is only one of the lowest value (3.0),
only one value is removed and the average is calculated correctly

```
```
