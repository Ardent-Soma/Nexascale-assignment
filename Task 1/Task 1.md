## Task 1: User and Roles Management

### i.Creating users
!(C:\Users\SOMA\Documents\GitHub\Nexascale-assignment\Images)
The users were created by running this command "sudo useradd -m developername" changing the developers name on each code.  
The -m command is to create a home directory for the users so they will have where to save their personal files.
#### a. Adding them to the developers group
!(C:\Users\SOMA\Documents\GitHub\Nexascale-assignment\Images)
Then the developers group was created with this command "sudo groupadd developers"
After, the users are added to the group using this command "sudo usermod -aG developers developername"
The "usermod" with the -aG option adds//appends the user to the group without removing them from the groups they are in before.
#### b. Verify adding them to groups
!(C:\Users\SOMA\Documents\GitHub\Nexascale-assignment\Images)
This command "group developername" to verify that they are added to the group successfully

### ii. Setting permissions for /var/www/project
!(C:\Users\SOMA\Documents\GitHub\Nexascale-assignment\Images)
#### a. Creating of the directory
First, the directory was created with the command "sudo mkdir -p /var/www/project". 
The -p option is to create the parent directory.
#### b. Setting ownership of the directory
Then this command"sudo chown -R root:developers /var/www/project" was to set the owner of the directory to remain and the root and the group set to the developers.  
This will be the same for all the sub directories in the directory.
#### c. Setting permissions for developers
The developers are given the read and execute permissions with this command "sudo chmod -R g+rx,o-rwx /var/www/project".
The o-rwx option was used so that other people in the server can not access the directory ensuring confidentiality of the contents of the directory.

### iii. Restricting access for two users who should log in locally
#### a. Editing of the configuration file
The configuration file was edited with the command "sudo nano /etc/ssh/sshd_config" which opened the file in a text editor and the text "DenyUsers developer3 developer4" was wriiten at the end of the file to restrict them
### b. Restarting the ssh
The command "sudo systemctl restart ssh" was used to restart the ssh to apply the changes.
