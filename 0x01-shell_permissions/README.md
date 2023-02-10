Shell permissions
0x01. Shell, permissions

//1.a script that switches the current user to the user betty
#!/bin/bash
su betty

//2.a script that prints the effective username of the current user.
#!/bin/bash
whoami

//3.a script that prints all the groups the current user is part of
#!/bin/bash
groups 


//4.a script that changes the owner of the file hello to the user betty.
#!/bin/bash
chown betty: hello

//5.a script that adds execute permission to the owner of the file hello.
#!/bin/bash
chmod u+x hello

//6.a script that adds execute permission to the owner and the group owner, and read permission 
to other users, to the file hello.
#!/bin/bash
chmod ugo+x hello

//7.Write a script that sets the permission to the file hello as follows:

//Owner: no permission at all
//Group: no permission at all
//Other users: all the permission

#!bin/bash
chmod 007

//8.Write a script that sets the mode of the file hello to this:

-rwxr-x-wx 1 julien julien 23 Sep 20 14:25 hello

#!/bin/bash
chmod 753 hello

//9.
