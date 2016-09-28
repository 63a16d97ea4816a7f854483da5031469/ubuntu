#Users Management

list of all users who can login (no system users like: bin,deamon,mail,sys, etc.)

awk -F':' '$2 ~ "\$" {print $1}' /etc/shadow
add new user

	sudo adduser new_username
	
or

sudo useradd new_username

	delete/remove username

	sudo userdel username

If you want to delete the home directory (default the directory /home/username)

	sudo deluser --remove-home username
or

	sudo rm -r /path/to/user_home_dir

If you want to delete all files from the system from this user (not only is the home diretory)

	sudo deluser --remove-all-files