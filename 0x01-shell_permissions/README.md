0x01. Shell, permissions

//0.a script that switches the current user to the user betty
#!/bin/bash
su betty

//1.a script that prints the effective username of the current user.
#!/bin/bash
whoami
====================================================================================
//2.a script that prints all the groups the current user is part of
#!/bin/bash
groups 
====================================================================================

//3.a script that changes the owner of the file hello to the user betty.
#!/bin/bash
chown betty: hello
====================================================================
//4.script create an empty file "hello"
4-empty
#!/bin/bash
touch hello
=================================================================================
//5.a script that adds execute permission to the owner of the file hello.
#!/bin/bash
chmod u+x hello
=======================================================================================
//5.a script that adds execute permission to the owner and the group owner, and read permission 
to other users, to the file hello.
#!/bin/bash
chmod ugo+x hello
======================================================================================


//.6 a script that adds execute permission to the owner and the group owner, and read permission
 to other users, to the file hello
 #!/bin/bash
chmod 754 hello
==============================================================================

//7. a script that adds execution permission to the owner, the group owner and the other users,
 to the file hello
#!/bin/bash
chmod ugo+x hello
=====================================================
 
 
//8.Write a script that sets the permission to the file hello as follows:

//Owner: no permission at all
//Group: no permission at all
//Other users: all the permission

#!bin/bash
chmod 007
======================================================================================
//9.Write a script that sets the mode of the file hello to this:

-rwxr-x-wx 1 julien julien 23 Sep 20 14:25 hello

#!/bin/bash
chmod 753 hello
============================================================================================
//10.a script that sets the mode of the file hello the same as olleh’s mode.
chmod --reference=reference_file target_file
#!bin/bash
chmod --reference=olleh hello
================================================================================================
//.11 a script that adds execute permission to all subdirectories of the current directory for the owner,
 the group owner and all other users.
#!/bin/bash
chmod -R ugo+X .

=======================================================================================
//.12
a script that creates a directory called my_dir with permissions 751 in the working directory.
#!/bin/bash
mkdir -m 751 my_dir

==============================================================================================
//.13
a script that changes the group owner to school for the file hello
chgrp group_name file_name
#!/bin/bash
chgrp school hello
