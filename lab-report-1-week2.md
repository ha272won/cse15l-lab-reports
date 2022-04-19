## Installing VScode
![Screen Shot 2022-04-09 at 7 45 02 PM](https://user-images.githubusercontent.com/103228431/162599064-65694736-95d9-475d-81ab-f970c70c1d5f.png)
 
Installing VS code will start from visiting the website. What you need is simply go on to the [website](https://code.visualstudio.com/) and download VS code. Both Window and Mac work. After installing VS code, it is **ready** to start coding.

## Remotely Connecting
![Screen Shot 2022-04-09 at 7 45 33 PM](https://user-images.githubusercontent.com/103228431/162599077-db018d45-7f77-4c28-ba04-0c2069de76aa.png)

This lab report used Mac. Open the terminal, and enter the following command : 
`ssh cs15lsp22zz@ieng6.ucsd.edu "ls"` 
`cs15lsp22zz@ieng6.ucsd.edu` was replaced by my own account.

## Trying Some Commands
![Screen Shot 2022-04-09 at 11 50 46 PM](https://user-images.githubusercontent.com/103228431/162606186-85408529-80da-4ed3-bd77-d4e500ab07ac.png)
This step was to use various command to get along with the those. The following image is an example of usage of the command `ls -a` to test the command.

## Moving Files with scp
![Screen Shot 2022-04-09 at 7 45 59 PM](https://user-images.githubusercontent.com/103228431/162599102-4ca61555-7691-497b-bdfa-276dcf7019ba.png)
After create the file call whereAmI.java, run the following command :
`scp WhereAmI.java cs15lsp22zz@ieng6.ucsd.edu:~/` 
After logging in, use 'ls' so the file can be stored in ieng computer.  

## Setting an SSH Key
![Screen Shot 2022-04-09 at 7 46 22 PM](https://user-images.githubusercontent.com/103228431/162599110-c4e1d75f-d76f-4af0-b3d1-9162e92b43fb.png)

Using `ssh` command, save the key in the computer. They will require the password and after you enter that then it's all done. Once it is confirmed that the terminal printed the rendered image of key, then it is possible to login without typing the password.

## Optimizing Remote Running
![Screen Shot 2022-04-18 at 5 20 15 PM](https://user-images.githubusercontent.com/103228431/163896675-95d012ff-316a-4286-a2df-d458d1fbaa20.png)

First, edit the file and copy and replace it in the remote server by typing:
`scp WhereAmI.java cs15lsp22zz@ieng6.ucsd.edu:~`

Complie and run the code by typing the follow code:
`ssh cs15lsp22zz@ieng6.ucsd.edu "javac WhereAmI.java; java WhereAmI"`
