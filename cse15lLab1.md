Hey future students, I'll walk you through how to log into a course specific account on `ieng6`
1. First, we will need to install VScode. When I tried this lab, I already had VScode installed, however, some of you might not. To download VScode, click on this [link](https://code.visualstudio.com/download) which will take you over to the download website. Simply follow the steps and you should have VScode set up fairly quickly. When you open VScode, it should look like this:
![Image](Screenshot 2023-04-09 at 5.50.47 PM.png)
2. Next, we will remotely connect to the remote server. Although we were supposed to use the AD domains that are issued to us for the course, my lab found issues using these domains, so instead we used our tritonlink username + "ieng6.ucsd.edu" along with our tritonlink password. For example, my account would be `vemohan@ieng6.ucsd.edu`. In the terminal type `$ ssh vemohan@ieng6.ucsd.edu` but use your email instead of mine. If it asks a yes/no question, just say yes. Then, type in your tritonlink password. The characters will not show while typing your password in. Afterwards, your terminal might look something like this:
![Image](Screenshot 2023-04-09 at 6.02.22 PM.png)
3. Now, let's run some commands. some useful commands you can run are
```
cd ~
cd
ls -lat
ls -a
cp /home/linux/ieng6/cs15lsp23/public/hello.txt ~/
```
What shows up when you type in these commands? Take note of it. Also see if you can produce any error messages. Here's mine:
![Image](Screenshot 2023-04-09 at 6.05.12 PM.png)
