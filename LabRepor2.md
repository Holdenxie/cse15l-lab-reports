# Lab Report2
![image](https://github.com/Holdenxie/Image1/blob/main/Screenshot%202024-01-30%20002338.png)
In this, the `handleRequest` method is called. 
The revelent argument for the method is the URL. 
The variable `messages`, `user` and `chat` are changed according to the input. In this case the `message` varible becomes `gradres` and the `user` is `hello`.
Because this is the very first input, chat did not store any other previous input, thus chat is `hello: gradres`.

![image](https://github.com/Holdenxie/Image1/blob/main/Screenshot%202024-01-30%20002408.png)
In this, the `handeleRequest` method is called. 
The revelent argument for the method is the URL 
The variable `messages`, `user` and `chat` are changed according to the input. In this case the `message` varible becomes `hello how are you` and the `user` is `bug`.
This is the second input, therefore, the variable `chat` stored previous inputs, which will also be printed out. 
So chat at this instance would be `hello: gradres\ bug: how are you`. However, the space is replaced by the `+` sign. 
