# A new beginning
Starting anything new is scary. I've worked on the service desk for just shy of two years (at the time of writing/typing) and I've never used Bash, nor have I ever needed to. Learning new technology is overwhelming, and with shortcuts like ChatGPT, its easy to be lazy. But knowing how to use in-demand technology without external resources will separate you from a 'vibe scripter/programmer' (not to mention how impressive it is). Sometimes, trying new things takes courage, and I just want to push myself to learn new things. If you're reading this then you might too, and hopefully you might feel inspired to keep track of what you're learning to level up. I also wanted to write this in a relateable way because reading people's experiences on forums and other spaces can be less forgiving if you're understanding isn't that of someone with years of experience. Writing this is part of my journey. I've built a litle Proxmox server (I used an old crappy laptop) and everything I'm going to be learning on will be on there but by all means use an ISO key. As long as you can practice, that's what matters the most.

## Bash
If you search 'Bash' into a browser, you will be presented with a whole host of sites but for learning purposes I've chosen W3 schools.com explanation (https://www.w3schools.com/bash/). You will read that it's a Linux/Unix system, that it stands for Bourne Again SHell (like anyone will need that) and that it's popular due to how easy it is to use. Let's be the judges of that eh?

I also popped over to a link from FreeCodeCamp (https://www.freecodecamp.org/news/bash-scripting-tutorial-linux-shell-script-and-command-line-for-beginners/) just to read around some more on Bash. The article is by Zaira Hira and Zaira explains that "A bash script is a file containing a sequence of commands that are executed by the bash program line by line. It allows you to perform a series of actions, such as navigating to a specific directory, creating a folder, and launching a process using the command line." It's sounding a lot like an operating system software combined with a programming language. Zaira lays out what some uses of shell scripting are: Automation, Portability, Flexbility, Accessibility, Integration and Debugging. The main few that stick out are automation and debugging but that might change in the days or weeks ahead.

There are some barebones basics to run. I've started off with"date" and got the output:

![image](https://github.com/user-attachments/assets/45cf6921-11e2-43d1-815f-095f1a44fb58)

We can view the contents of the current directory we're working in with "ls":

![image](https://github.com/user-attachments/assets/72651a7a-1ddc-4f78-9e8b-5d7afe556ea8)

In PowerShell, you can use "Writehost" or "writeoutput"to present text in the terminal, in Linux it's simply "echo":

![image](https://github.com/user-attachments/assets/48b0f615-015c-402e-940d-79fb0290d398)

Most command line interfaces have a command that show more commands, in PowerShell you can type "get-help" to explore your options but in linux you can type "man man" to see a reference manual

![image](https://github.com/user-attachments/assets/cb72019b-d839-48d3-b80e-de88afac1c93)


Let's look at something more challenging - creating a script.
In Zaira's article, the naming convention of bash scripts are ".sh" albiet, they will run without the "sh" in the filename. Which is quite different to Windows where you have to add a ".bat" or ".ps1" in the title of your file.

To execute a bash script via the bash terminal, you can use what's called "shebang". This tell the shell to execute the file via the bash shell.

Using the change directory command "cd", I've selected my desktop:

![image](https://github.com/user-attachments/assets/e9b170e7-0bbb-4cd8-8669-13e575de82c8)

And then created a new file with "vi" called first_script.sh, which allows me to create the file in the terminal which I think is a really nice feature:

![image](https://github.com/user-attachments/assets/a2214d53-13dc-4101-8e00-a6d87d433681)

I didn't know that this was entering "vim" - something I know nothing of. I couldn't see how to edit in Vim and I was getting random errors at the bottom of my text editor. I was trying to add a hashtag symbol as per Zaira's "#!/bin/bash" on the first line but was getting E348: No string under cursor error

![image](https://github.com/user-attachments/assets/55dcca91-654f-437c-8947-6dd31cb16c23)

After some researching I found out that you need to enter the letter i add text. The other issue I was having with Vim was deleting or backspacing because hitting the delete or backspace keys doesn't work. You have to hit Escape and press x when the cursor is on the letter you are trying to delete or double pressing the d key to remove the line. And then editing with i again. But this is how you learn - from mistakes and uncertainty.

After working all of this out, I was finally able to type out my text I wanted:

![image](https://github.com/user-attachments/assets/acb98fa9-ffb4-4287-8ab1-987bfa8b4850)

To exit Vim, I entered :wq and I had my script_test.sh file on my desktop - success!

The script still requires some modification at this stage, in Linux chmod changes the ownership of the files. I selected u as per Zaira's explanation, and +x adds execution rights so that I (as the user) have ownership of this script and can run it. You can see where I messed up in the screenshot the first time it ran as I hadn't typed the directory my script was located in but after another try, it worked! I used sh script_test.sh but Zaira points out that using bash or ./ before the file name also runs it.

![image](https://github.com/user-attachments/assets/821e5323-ba52-4e79-87c8-c80817678d1c)

So there we have it, some beginner level commands and a first script run. Linux is very fiddly and I can understand more and more why it's such a niche OS. It's very manual but I'm sure this is just the beginning of it all.



