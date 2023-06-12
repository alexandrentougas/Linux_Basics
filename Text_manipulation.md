[Summary](./README.md)

## Exercises

1. Search all sequences containing "Loxondota" in ``/home/student/lorem.txt``

> Flag : BC{GREP_ME_LOREM_FL4G}

2. Copy the file /etc/passwd to your home directory. Display the line starting with ``student`` name.

> Your commands : cp passwd /home/student/passwd

> grep "^student" passwd

3. Display the lines in the passwd file starting with login names of 3 or 4 characters.

> Your commands : ``egrep "^[a-zA-Z0-9]{3,4}:" passwd``

4. In the file ``/home/student/sample.txt`` how many different values are there in the first column? in the second?

> Your response : 4 for both

> Your command : cut -d "," -f 1 /home/student/sample.txt | sort -u | wc -l

> cut -d "," -f 2 /home/student/sample.txt | sort -u | wc -l

5. In the file ``/home/student/sample.txt`` sort the values in the second column by frequency of occurrence. (uniq -c can be useful)

> Your command : cut -d "," -f 2 /home/student/sample.txt | sort | uniq -c | sort

6. In the file ``/home/student/iris.data`` Change the column separator (comma) to tab (make sure that the changes are applied to the file)

> Your command : sed -i 's/,/\t/g' /home/student/iris.data

7. In the file ``/home/student/iris.data``, extract from this file the column 3 (petal length in cm) (use cut )

> Your command : cut -f 3 /home/student/iris.data

8. In the file ``/home/student/iris.data``, count the number of flower species (cut and uniq)

> Your response : 3

> Your command : cut -f 5 /home/student/iris.data | uniq | grep . | wc -l

9. In the file ``/home/student/iris.data``, sort by increasing petal length (see sort options)

> Your command : sort -k 3 /home/student/iris.data

10. In the file ``/home/student/iris.data``, show only lines with petal length greater than the average size

> Your command : average=`awk '{ total += $3 } END {print total/NR}' /home/student/iris.data`

> awk -v avg="$average" '$3 > avg {print}' /home/student/iris.data

11. Using ``/etc/passwd``, extract the user and home directory fields for all users on your student machine for which the shell is set to ``/bin/false``.

> Your command : grep "/bin/false$" /etc/passwd | cut -d ":" -f 1,6

[Next](./Piping_and_redirection.md)