# Lab Report2
## First input 
![image](https://github.com/Holdenxie/Image1/blob/main/Screenshot%202024-01-30%20002338.png)
In this, the `handleRequest` method is called. 
The revelent argument for the method is the URL, which most likely to change for every input. In this case, the value of URL is `https://0-0-0-0-8000-0ata91q98g0td8an4lpl4b18ps.us.edusercontent.com/add-messages?s=hello&user=hello'. 
The variable `messages`, `user` and `chat` are changed according to the input. In this case the `message` varible becomes `gradres` and the `user` is `hello`.
Because this is the very first input, chat did not store any other previous input, thus chat is `hello: gradres`.

## Second input 
![image](https://github.com/Holdenxie/Image1/blob/main/Screenshot%202024-01-30%20002408.png)
In this, the `handeleRequest` method is called. 
The revelent argument for the method is the URL, which most likely to change for every input. In this case, the value of URL is `https://0-0-0-0-8000-0ata91q98g0td8an4lpl4b18ps.us.edusercontent.com/add-messages?s=hello%20how%20are%20you&user=bug'. 
The variable `messages`, `user` and `chat` are changed according to the input. In this case the `message` varible becomes `hello how are you` and the `user` is `bug`.
This is the second input, therefore, the variable `chat` stored previous inputs, which will also be printed out. 
So chat at this instance would be `hello: gradres\ bug: how are you`. However, the space is replaced by the `+` sign. Lastly, the value of the url changes 
