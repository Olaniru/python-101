## Introduction
My first experience with the command line interface, CLI or shell scripting was during a Datacapentry Workshop in 2015. 
They have an excellent course on this mainly for genomics but the concepts are generally applicable. You can check it out at https://datacarpentry.org/shell-genomics/

I've also used Dataquest for my learning. It's a subscription based platform. Dataquest is well structured. I like Dataquest as I can always refer to it when I need to.

##Starting with the command line

When you open the terminal, you will see something similar to home/doc$ or username@machinename ~ % or something similar. This is called #Command prompt# or just #promp#. 

To the right of the prompt is where you type the command, and this is known as the command line.

A command may or may not have parameters. Command 'date' for instance needs no parameters

$ date
Output: Thu 19 May 2022 17:43:08 BST

A parameter is either an option or an argument.

option: starts with a dash (-), is a string of symbols, modifies the behaviour of the command. Also called flag or switch.

argument or operand - is an object upon which the command acts.

## Some common commands

diff: get the differences between two files

e.g if west and east are two text files and we want to know the difference between the documents, we can use:

diff -y west east

OUTPUT: prints to the screen the content of both files and marks the rows that are different by having a | next to the rows of the second file that differ from the first

diff is the command name. It has 3 parameters
-y is an option, it starts with a dash
west is an argument upon which diff acts
east is the second argument or the last parameter

without the option -y the contents are not printed on the screen, only where the two files differ will be printed. may be useful for large documents

An option can be short or long. It is short with one dash e.g -y but long with double dash and the function is stated clearly - more descriptive. e.g --side-by-side

diff --side-by-side west east

Options can also be combined. Write the options alphabetically, separated by a space e.g

diff -q -y west east or diff -qy west east

#To access history of commands
use the arrow up and down keys or use the 'history' command

History expansion allows us to very quickly reference lines in the command history by the number to the left of the command. e.g !7

to run the last command type !! or !-1

ls : to list

options: -l long format includes metadata about the file
         -h human readable format
         -p directory has a slash
         -a list all files including hidden files

cd : to change directory

cd ~ this will take you to the home directory
cd .. this will take you to the parent directory of your current directory
cd . will just take you to where you are

cd - takes us to the last used directory. used for switching between directories that don't have parent child relationship

cd ~[username] which takes us to the home directory of the user we insert instead of [username]

mkdir for making (creating) directories

rmdir for deleting empty directories

cp for copying files to their destinations e.g cp source_files destination. If you have multiple arguments, the last argument of cp command is always interpreted as the destination and not as a file to be copied. It takes relative paths as argument, therefore names of the file or directory will suffice rather than their paths. The destination doesn't have to be a directory, it can be a new file name.

Options for cp
            -i for interactive to ask whether to overwrite a file or not if it already exists
            -R stands for recursively, for copyig directories
rm delete files
rm -i interactive
rm -R for deleting directories

mv for moving files.When moving a file, the original file is deleted and a copy is placed in the location of the user's commands


#Glob patterns
            * 
Passing * as an argument to ls will cause it to list all non-hidden files and directories in the working directory, plus all files at the root of the listed directories. 