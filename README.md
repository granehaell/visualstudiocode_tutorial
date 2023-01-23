# Visual studio code tutorial

### Download VScode
https://code.visualstudio.com/
### Install git bash 
you also need the program to be able to read shell bash files, which is the programming language for linux. <br />
**https://git-scm.com/downloads**<br />

Select bash as your default language: <br />
    1) Open Visual Studio Code<br />
    2) Press CTRL + SHIFT + P to open the Command Palette<br />
    3) Search for “Terminal: Select Default Profile” (previously “Terminal: Select Default Shell”)<br />
    4) Select your preferred shell. In my case I selected “Git Bash”<br />


### Install the extension ssh FS 
https://marketplace.visualstudio.com/items?itemName=Kelvin.vscode-sshfs <br />
This extension  makes it possible to acces the workstation in a folder format similar to a windows setup. It connects to the workstation via a ssh connection.


Make a new configure for the connection to the workstation in ssh FS.<br />
![ssh FS new](http://www.cse.unsw.edu.au/~learn/homecomputing/_images/image2.png)
"Name": what you want the connection to be called. Can be anything eg. #Workstation” or your username<br />
Click save

On the next page, fill in these fields:<br />
“Host”: type in the IP address the Vienna server: **login0X.lisc.univie.ac.at** <br />
“root” this is which directory you want to connect to. Write `/data01/$your_username` (eg. /data01/granehaell) <br />
“username”. your username <br />
“password” – choose prompt. You will have to type it in every time you want to log in. It is not recommended to put the password in this configuration, as it is not very safe. <br />
Click save

![ssh FS](https://github.com/SchoofsKelvin/vscode-sshfs/raw/HEAD/media/config-editor.png)

4.	Log in<br />

If you are not working connected to Scientific Network SouthTyrol, you need to first access it first through the University VPN<br />


### Log in via ssh fs to access folder 
In SSH FS, right click on the configured connection (upper left corner) and select **Add as workspace folder**<br />
![add as workspace folder](images/ssh_add_workspace.png)

At prompt, put in password<br />	
In the explorer, right click on the Workspace folder and click on **“open remote SSH terminal”**. 

![open terminal](images/ssh_open_terminal.png)

It will not require a password prompt, since you already typed it in when you logged in to workspace folder. It should have started a terminal directly in `/data01/$USER` <br />	

![terminal](images/terminal.png)

### Log in via terminal
If you use another program with a terminal (you'll still need bash), you can simply log in with the following command: 
```
$ ssh -X granehaell@10.11.200.20       #exchange granehaell with your username:
```

![terminal login](images/terminal_login.png)


First time you log in – change the password!<br />
```
$ passwd
```
![change password](https://cdn.mos.cms.futurecdn.net/LU7wmpZXnggLT85ZLYK5Gh-970-80.png)
