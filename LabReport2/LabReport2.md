# Lab Report Two
This page is the Lab Report2


## Part One
The following is the code block of a web server called `StringServer` that supports the path and behavior described in the write-up :
```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    // The one bit of state on the server: a string that will be manipulated by
    // various requests.
    StringBuilder message = new StringBuilder();

    public String handleRequest(URI url) {
        if (url.getPath().equals("/add-message")) {
            String query = url.getQuery();
            if (query == null) {
                return "400 Bad Request: Missing message parameter!";
            }
            String[] parameters = query.split("=");
            if (parameters[0].equals("s")) {
                String newMessage = parameters[1];
                message.append(newMessage).append("\n");
                return message.toString();
            } else {
                return "400 Bad Request: Invalid parameter!";
            }
        } else {
            return "404 Not Found!";
        }
    }
}

class StringServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}
```

The following are two screenshots of using `/add-message`

