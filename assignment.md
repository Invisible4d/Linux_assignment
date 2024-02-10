| Task                                                                                                             | Command                                                                                                               | Screenshot                                         |
| :--------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------- |
| a.Change directory to the tests directory using absolute pathname                                                | cd /home/altschool/tests                                                                                              | ![1707597477995](image/assignment/1707597477995.png) |
| b.Change directory to the tests directory using relative pathname                                                | cd tests/                                                                                                             | ![1707598014045](image/assignment/1707598014045.png) |
| c.Use echo command to create a file named fileA<br />with text content ‘Hello A’ in the misc directory         | echo "Hello A" > FileA                                                                                                | ![1707598187671](image/assignment/1707598187671.png) |
| d.Create an empty file named fileB in the misc directory.<br />Populate the file with a dummy content afterwards | touch /home/altschool/misc/FileB<br /><br /><br />`base64 /dev/urandom \| head -c 1000 > /home/altschool/misc/FileB` | ![1707598324972](image/assignment/1707598324972.png) |
| e.Copy contents of fileA into fileC                                                                              | cp FileA FileC                                                                                                        | ![1707598640831](image/assignment/1707598640831.png) |
| f.Move contents of fileB into fileD                                                                              | mv FileB FileD                                                                                                        | ![1707598805981](image/assignment/1707598805981.png) |
| g.Create a tar archive called misc.tar for the contents of misc directory                                        | tar -rvf misc.tar misc                                                                                                | ![1707599018777](image/assignment/1707599018777.png) |
| h.Compress the tar archive to create a misc.tar.gz file                                                          | tar -czvf misc.tar.gz misc.tar                                                                                        | ![1707599077860](image/assignment/1707599077860.png) |
| I. Create a user and force the user to change his/her password upon login                                        | sudo passwd --expire `<newuser>`                                                                                    | ![1707599200927](image/assignment/1707599200927.png) |
| J. Lock a users password                                                                                         | sudo passwd -l `<user>`                                                                                             | ![1707599291370](image/assignment/1707599291370.png) |
| K. Create a user with no login shell                                                                             | sudo useradd -s /usr/sbin/nologin `<newuser>`                                                                       | ![1707599369359](image/assignment/1707599369359.png) |





---
L. Disable password based authentication for ssh

sudo nano /etc/ssh/sshd_config 
## set PasswordAuthentication no
## set PubkeyAuthentication yes
SAVE AND CLOSE
Restart SSH service >> sudo systemctl restart sshd

---
![1707599665577](image/assignment/1707599665577.png)



---
M. Disable root login for ssh

sudo nano /etc/ssh/sshd_config 
## PermitRootLogin no
SAVE AND CLOSE
Restart SSH service >> sudo systemctl restart sshd

---
![1707599589250](image/assignment/1707599589250.png)
