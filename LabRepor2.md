# Lab Report2

````java
    import java.io.IOException;
    import java.net.URI;
    
    class Handler implements URLHandler {
        // The one bit of state on the server: a number that will be manipulated by
        // various requests
        String chat = "";
        String messages;
        char and = '&';
        int index = 0; 
        String user;
    
        public String handleRequest(URI url) {
            if (url.getPath().equals("/")){
                return String.format(chat);
            } 
            else {
                if (url.getPath().contains("/add-message")) {
                    String[] parameters = url.getQuery().split("=");
                    user = parameters[2];
                    for(int i = 0; i < parameters[1].length(); i++){
                        if(parameters[1].charAt(i) == and){
                            index = i;
                        }
                    }
                    messages = parameters[1].substring(0, index);
                    chat = chat + user + ": " + messages + "\n";
                    return String.format(chat);
                }
                return "404 Not Found!";
            }
        }
    }
    
    class ChatServer {
        public static void main(String[] args) throws IOException {
            if(args.length == 0){
                System.out.println("Missing port number! Try any number between 1024 to 49151");
                return;
            }
    
            int port = Integer.parseInt(args[0]);
    
            Server.start(port, new Handler());
        }
    }
````

## First input 
![image](https://github.com/Holdenxie/Image1/blob/main/Screenshot%202024-01-30%20002338.png)
In this, the `handleRequest` method is called. 
The revelent argument for the method is the URL. In this case, the value of URL is `https://0-0-0-0-8000-0ata91q98g0td8an4lpl4b18ps.us.edusercontent.com/add-messages?s=gradres&user=hello'. 
The variable `messages`, `user` and `chat` are changed according to the input. In this case the `message` varible becomes `gradres` and the `user` is `hello`.
Because this is the very first input, chat did not store any other previous input, thus chat is `hello: gradres`.

## Second input 
![image](https://github.com/Holdenxie/Image1/blob/main/Screenshot%202024-01-30%20002408.png)
In this, the `handeleRequest` method is called. 
The revelent argument for the method is the URL, which is differnt from the first. The argument is likely to change for every input. In this case, the value of URL is `https://0-0-0-0-8000-0ata91q98g0td8an4lpl4b18ps.us.edusercontent.com/add-messages?s=hello%20how%20are%20you&user=bug'. 
The variable `messages`, `user` and `chat` are changed according to the input. In this case the `message` varible becomes `hello how are you` and the `user` is `bug`.
This is the second input, therefore, the variable `chat` stored previous inputs, which will also be printed out. 
So chat at this instance would be `hello: gradres\ bug: how are you`. However, the space is replaced by the `+` sign. Lastly, the value of the url changes 



## Screenshot of private key 
![image](https://github.com/Holdenxie/Image1/blob/main/Screenshot%202024-01-30%20214238.png) <br> 
This is the absolute path to the private key. This can be found by first logging into your `ieng6` account, then enter the `ls` command with the argument `~/.ssh/authorized_keys`.

## Screenshot of public key 
![image](https://github.com/Holdenxie/Image1/blob/main/Screenshot%202024-01-30%20214009.png) <br> 
This is the absolute path to the private key. This can be found by simply entering the `ls` command with the path that the public key is located in. 

## Scrneeshot of logging in without asking for password 
![image](https://github.com/Holdenxie/Image1/blob/main/Screenshot%202024-01-30%20214321.png) <br> 
I can now log into my `ieng6` account without promopted for entering a password from this computer. 

## Learned from lab 2 and 3 
I learned how to set up a server, where I should use a port that's not been used by ohters. I can design my server to give the user some output when the user gives certiain inputs. I also learned how to set up a key that allows my computer to login to my `ieng6` account without entering the password every time. 
