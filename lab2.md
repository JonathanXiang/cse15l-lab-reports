# Lab 2
By Jonathan Xiang

##Part 1: String Server

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

![Image](firstmessage.png)

In this screenshot, the handleRequest method is called. The relevant
values for this method are the url, given as a parameter which the
method uses to see what it should do, and the storedString, which is
the String the method will add to everytime "/add-message" is used.
In this case, storedString was changed since "Hello" and "\n" were
concatenated to it.

![Image](secondmessage.png)
