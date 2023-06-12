[Summary](./README.md)

## Exercises

1. Write the message "hello everyone" in a file called "test" by redirecting the output of the echo command.

> Your command : echo "hello everyone" > test.txt

2. Write the message "goodbye" in the same file "test" by redirecting the output of the echo command and without overwriting the content of "test" and check with the cat command

> Your command : echo "goodbye" >> test.txt

3. Make the ``ls -la`` command redirect to the ``foo`` file

> Your command : ls -la > foo.txt

4. Execute ``find /etc -name *conf*`` command and redirect errors (only errors) to a file named err.txt

> Your command : find /etc -name *conf* 2> err.txt

5. Repeat the previous exercise, this time redirecting the errors to the linux nothingness.

> Your command : find /etc -name *conf* 2> /dev/null

6. Now redirect the standard output and the error output of the ``find /etc -name *conf*`` command to two different files (std.out and std.err)

> Your command : find /etc -name *conf* 2> errors.txt 1> output.txt

7. What does the mkfifo command do?

> No answer required

8. Create a pipe named "MyNammedPipe". Then execute the pwd command which will transmit the data in this pipe. Then use the cat command to read the contents of your "MyNammedPipe" pipe.

> Your commands : mkfifo MyNamedPipe pwd > MyNamedPipe 
> cat MyNamedPipe

9. With cat command, add number the lines in the file /etc/passwd with the command ``nl``

> Your commands : cat /etc/passwd | nl

10. Using the previous nl command, the head and tail commands, display the lines of /etc/passwd between line 7 and line 12

> Your commands : nl /etc/passwd | head -n 11 | tail -n 4

[Next](./Bash_environment.md)