# Lab 2
By Jonathan Xiang

##Part 1: String Server

The code that I wrote for String Server is

`
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
`

![Image](firstmessage.png)

![Image](secondmessage.png)
