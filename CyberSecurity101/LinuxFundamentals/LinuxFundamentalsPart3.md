# Linux Fundamentals Part 3

## task 1 Introduction

Let's proceed!

* No answer needed

## task 2 Deploy Your Linux Machine

* connect ssh like linux part 2
  
I've logged into the Linux Fundamentals Part 3 machine using SSH and have deployed the AttackBox successfully!

* No answer needed

## task 3 Terminal Text Editors

Create a file using Nano

* nano test.txt in the VM
* No answer needed

Edit "task3" located in "tryhackme"'s home directory using Nano. What is the flag?

* nano task3
* the answer is THM{TEXT_EDITORS}

## task 4 General/Useful Utilities

Ensure you are connected to the deployed instance (10.67.179.214)

* echo $SSH_CONNECTION
* No answer needed

Now, use Python 3's "HTTPServer" module to start a web server in the home directory of the "tryhackme" user on the deployed instance.

* python3 -m http.server

Download the file http://10.67.179.214:8000/.flag.txt onto the TryHackMe AttackBox. Remember, you will need to do this in a new terminal.

What are the contents?

* New terminal
* wget 10.67.179.214:8000/.flag.txt
* cat .flag.txt
* the answer is THM{WGET_WEBSERVER}

Create and download files to further apply your learning -- see how you can read the documentation on Python3's "HTTPServer" module. 
Use Ctrl + C to stop the Python3 HTTPServer module once you are finished.

* No answer needed

## task 5 Processes 101

Read me!

* No answer needed

If we were to launch a process where the previous ID was "300", what would the ID of this new process be?

* 301

If we wanted to cleanly kill a process, what signal would we send it?

* SIGTERM

Locate the process that is running on the deployed instance (10.67.179.214). What flag is given?

* ps aux
* the answer is THM{PROCESSES}

What command would we use to stop the service "myservice"?

* systemctl stop myservice

What command would we use to start the same service on the boot-up of the system?

* systemctl enable myservice

What command would we use to bring a previously backgrounded process back to the foreground?

* fg

## task 6 Maintaining Your System: Automation

Ensure you are connected to the deployed instance and look at the running crontabs.

* crontab -e
* No answer needed

When will the crontab on the deployed instance (10.67.179.214) run?

* @reboot

## task 7 Maintaining Your System: Package Management

Since TryHackMe instances do not have an internet connection...this task only requires you to read through the material.

* No answer needed

## task 8 Maintaining Your System: Logs

Look for the apache2 logs on the deployable Linux machine

* cd var/log/apache2
* ls -lh

What is the IP address of the user who visited the site?

* cat access.log (nope permission deniel)
* cat access.log.1
* the answer is 10.9.232.111

What file did they access?

* in the same log
* the answer is catsanddogs.jpg

## task 9 Conclusions & Summaries

Terminate the machine deployed in this room from task 2. 

* No answer needed

Continue your learning in other Linux-dedicated rooms

* No answer needed

### end

