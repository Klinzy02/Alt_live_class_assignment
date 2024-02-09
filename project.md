# Solution to 1st Assignment

### Preamble

1. Create a login user: `sudo useradd -m Altschool`
2. Switch to Altschool: `su - altschool`
3. Create the requested directories (code, tests, personal and misc): `mkdir code tests personal misc`

### Solution to task a-m


| Tasks | Task description | Solution |
|-------|------------------|------------|
|a      | Change to the tests directory using absolute pathname | `cd /home/altschool/tests` |
|b      | Change to the tests directory from your home directory using relative pathname | `cd ./test` |
|c      |  Use echo command to create a file named fileA with text content ‘Hello A’ in the misc directory | `echo "Hello A" > /home/altschool/misc/fileA`   |
|d      | Create an empty file named fileB and populate it with dummy contents | `touch ./misc/fileB` and `head -c 200 /dev/urandom ./misc/fileB` |
|e      | Copy contents of fileA into fileC               | `cp ./misc/fileA ./misc/fileC` |
|f      | Move contents of fileB into fileD | `mv ./misc/fileB ./misc/fileD`  |
|g      | Create a tar archive called misc.tar for the contents of the misc directory | `tar -cf misc.tar misc` |
|h      | Compress the tar archive to create a misc.tar.gz file | `gzip misc.tar` |
|i      | Create a user and force the user to change his password upon login | first of create a user with `sudo adduser user1` then force user to change password with `sudo chage -d 0 user1` |
|j      | Lock a users password | `sudo passwd -l user1` |
|k      | Create a user with no login shell | `sudo useradd -s /sbin/nologin` |
|l      | Disable password based authentication for ssh | `sudo vi /etc/ssh/sshd_config` and  insert `PasswordAuthentication no` |
|m      | Disable root login for ssh | `sudo vi /etc/ssh/sshd_config` and set `PermitRootLogin no`   |


 
