# Streamlining ssh Configuration
## Show your .ssh/config file, and how you edited it (with VScode, another program, etc)
![Screen Shot 2022-04-28 at 7 48 03 PM](https://user-images.githubusercontent.com/103228431/167058168-a4282aae-d044-4dd0-a5f9-bd09232bb861.png)
Using `vim`, create a configuration file. Then, put the lines that is instructed in lab 5.

## Show the ssh command logging you into your account using justthe alias you chose.
![Screen Shot 2022-05-05 at 7 48 10 PM](https://user-images.githubusercontent.com/103228431/167058778-841ff968-39e2-4d39-9503-e90b34118d86.png)

Only typing `ssh ieng6`, it shows that it is successfully logged in.

## Show an scp command copying a file to your account using just the alias you chose.
![Screen Shot 2022-05-11 at 6 11 39 PM](https://user-images.githubusercontent.com/103228431/167972736-9af6064b-168f-47e2-b273-21ccf0b90cb1.png)

Not only `ssh`, but also `scp` command allows us to copy the file to the remote server. 

# Setup Github Access from ieng6
## Show where the public key you made is stored on Github and in your user account.
On Github, go setting -> SSH and GPG keys -> click on the green button call 'New SSH key'. 
![Screen Shot 2022-05-08 at 9 18 45 PM](https://user-images.githubusercontent.com/103228431/167339953-ed71a257-49d1-4a8c-98ea-d5b7188d43da.png)
This shows that the key that allows to access to the remote server has been added to the github.

## Show where the private key you made is stored on your user account (but not its contents) as a screenshot.
![Screen Shot 2022-05-08 at 9 26 37 PM](https://user-images.githubusercontent.com/103228431/167340644-0f5603a2-003a-49fa-818e-94fb72be6a73.png)
Using `vim`, open the config file and add github. Private key is located in the same file that I used in section 1.

## Show running git commands to commit and push a change to Github while logged into your ieng6 account.
commit
![Screen Shot 2022-05-14 at 7 47 42 PM](https://user-images.githubusercontent.com/103228431/168663809-996db5ce-cd6b-46ee-908d-719f7af3dac8.png)

To commit it, I have copied the 'check.txt' file to the existed repository.

push
![Screen Shot 2022-05-16 at 11 59 59 AM](https://user-images.githubusercontent.com/103228431/168663888-2077e9ca-5f34-4de1-8a88-e30fcecbf8fd.png)

This shows that it has been successfully pushed.

## Show a link for the resulting commit.

[result](https://github.com/ha272won/week5skilldemo/commit/06f388e7f5aec89971fee2ddb7e2be00d9d4545a)

# Copy whole directories with scp -r
## Show copying your whole markdown-parse directory to your ieng6 account.
`scp -r /Users/alien/Documents/GitHub/markdown-parser ieng6:~/markdown-parser`
This command is used to copy markdown-parser. 
![Screen Shot 2022-05-16 at 4 36 11 PM](https://user-images.githubusercontent.com/103228431/168699052-a5fb63d1-8cf2-4186-b18e-6ed5a184701b.png)


## Show logging into your ieng6 account after doing this and compiling and running the tests for your repository.

![Screen Shot 2022-05-16 at 7 38 20 PM](https://user-images.githubusercontent.com/103228431/168717066-20b3e7dd-edf8-41b9-8147-ef10f83d7afc.png)
![Screen Shot 2022-05-16 at 7 38 26 PM](https://user-images.githubusercontent.com/103228431/168717069-ea6a59c2-b8de-42ca-9556-4014a90e67f6.png)

## Show (like in the last step of the first lab) combining scp, ;, and ssh to copy the whole directory and run the tests in one line.
The processes listed : copying, compiling and running can be commited by typing this command: 
`scp -r /Users/alien/Documents/GitHub/markdown-parser ieng6:~/markdown-parser; ssh ieng6 'cd markdown-parser; /software/CSE/oracle-java-17/jdk-17.0.1/bin/javac MarkdownParse.java; /software/CSE/oracle-java-17/jdk-17.0.1/bin/javac -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar MarkdownParseTest.java; /software/CSE/oracle-java-17/jdk-17.0.1/bin/java -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar org.junit.runner.JUnitCore MarkdownParseTest'`


![Screen Shot 2022-05-16 at 7 39 51 PM](https://user-images.githubusercontent.com/103228431/168717454-96a3f255-af9b-485e-ade5-3ae33be2973a.png)
![Screen Shot 2022-05-16 at 7 40 14 PM](https://user-images.githubusercontent.com/103228431/168717458-a66b6b3b-c92a-46a5-9b50-fd9460cb6bf1.png)
![Screen Shot 2022-05-16 at 7 40 22 PM](https://user-images.githubusercontent.com/103228431/168717478-27c6ef55-0bd0-4e8b-8012-2b651bc0a4aa.png)
![Screen Shot 2022-05-16 at 7 41 11 PM](https://user-images.githubusercontent.com/103228431/168717481-77819310-1514-49cb-8c4c-faa66c159d65.png)


