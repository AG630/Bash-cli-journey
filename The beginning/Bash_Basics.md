## Some Bash basics

Much like PowerShell, you can add comments to your scripts. PowerShell uses the same syntax,
the hash symbol.

![image](https://github.com/user-attachments/assets/987e6eb6-4146-46df-8a6c-5023f50d7bd8)

Like PowerShell, it's possible to create variables in Bash. Variables allow you to store data.
In my example, I've assigned Polska=bialo_czerwoni, and you can see from my example how I used echo to call the Polska variable and realised I didn't include the $ symbol. Once I had, it gave me my output of bialo_czerwoni.

![image](https://github.com/user-attachments/assets/0b5a3e54-9470-44e3-8f9d-2f96f6b90e1b)

I've been practising along with the FreeCodeCamp article by Zaira - (https://www.freecodecamp.org/news/bash-scripting-tutorial-linux-shell-script-and-command-line-for-beginners/). There's some important things to make note of with naming conventions in Bash scripting. Firstly, variable names require either a letter or underscore as the first letter. Variable nmame can contain either letters, _ or numbers. They are case sensitve so echo polska would not have worked, for example. No space are allowed and the best practive for variable names is something descriptive.

![image](https://github.com/user-attachments/assets/dcc48935-96f2-4234-8097-eb7816671cdd)

Linux keeps surprising me... in a really good way. You can generate the lines of text/code etc. in the terminal of a specific file. I've already created the test_script.sh so I decided to output that one and it worked beautifully. You can see where I typed the incorrect syntax and missed out the < in the first attempt.

![image](https://github.com/user-attachments/assets/388ca8ab-0953-4857-ae0f-b86be2f85d65)

Something that I was aware of, and am glad is covered in the bash scripting article is echoing some text, and creating a file at the same time. So useful and timesaving:

![image](https://github.com/user-attachments/assets/0a1c9f44-ad23-4ae5-bb7f-4a5361e5dbfd)

# Debugging 
Running scripts and debugging them is important for any scripting language. Seeing the errors in the scripts will help the scripter identify the bugs and issues they need to resolve, to achieve the desired outcome.

In Zaira's freecodecamp article, multiple avenue's are discussed so let's dive into them!

The first debugging technique suggested is set -x. So naturally I added the set -x into the script_text.sh file:

![image](https://github.com/user-attachments/assets/aef093d0-f768-451c-8072-2b0c3ecf2318)

And the outcome we got after running this was:

![image](https://github.com/user-attachments/assets/0533aff9-75f1-43ae-82c0-1f842b2f58b6)

Another very smart way of testing for bugs within a script is to add $echo segments throughout. The idea being that you can see where the last one is printed to the terminal, meaning the next segment has the bug where the error is returning. For me this seems slightly longer winded, especially if the script is on the longer length.

Looking through the system logs is another useful way of verifying errors in scripts. I'm using an Ubuntu VM and I can find mine in the /Var/log/syslog.
