# Introduction to Unix
- File management
- Scheduling 
- Memory management 
- I/O management 

```sh
.. : parent of the current directory
. : current directory
~ : home directory 

ls
    -a : all files in home directory
    -rwx : access bits (regular file, determine the access right for user, group and the others: read, write and execute)

mkdir


cp file1 file2 
cp file1 . : copy file to current directory
mv file1 file2 
rm : remove file
rmdir : rm directory 

clear 

cat 
less [space-bar]: another page, [q]: quit reading, [/word-to-find][n: next occurence]
head -number-of-lines (default: 10)
tail -number-of-lines (default: 10)

grep word-to-find file.file_format 
    -i: ignore upper/lower case distinction
    -v: display those line that do not match 
    -n: precede each matching line with the line number 
    -c: print only the total count of the matched lines 

wc -option file.file_format: word count
    -w: word count 
    -l: line count

bg (running process in the background), fg (foreground), CTRL-C, CTRL-Z

kill : kill a process 
ps : lists the running process 

kill ps od diff ln echo
```
### Redirection 
```sh
cat # without specifying a file to read 
-> Read input and on receiving the end of file (Ctrl-D), copies it to the standard output 
```

- Use __>__ to redirect the output of the command
```sh
cat > name_of_the_file 
content of the file 
[Ctrl-D] # to stop 
cat name_of_the_file # read content of the file

cat >> name_of_the_file : appends the standard output to a file 
cat file_1 file_2 > file_join : concatenate file_1 and file_2 
```

- Use __<__ to redirect the input of the command, can direct the input to come from a file rather than keyboard
```sh
sort 
list of things to sort [Return] after each one 
[Ctrl-D] to stop 
sort < file_name_to_receive_input > file_name_to_write_output
```

### Pipes 
```sh
who : to see who is on the system with you

# Get sorted list of names is to type (slow, have to delete temporary files)
who > file_name 
sort < file_name 

# Pipe, connecting the output of who command and the input of sort command 
who | sort 

# Find how many users are logged on
who | wc -l
```


### Processes
- Each program running is called a proces
- Each process has its own identification PID 
- If the program is running twice, even by the same user, there're 2 different processes
- / -> bin -> awk (program), boot, ..., cs -> include (aio.h), ..., cs, home

### Devices 
- `/dev` contains devices, just like any other file (fopen, fread, fwrite, ...) but it communicates with a device 



