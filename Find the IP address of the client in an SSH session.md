#Find the Login Users' IP address of the client in an SSH session


	server:~# pinky
that will give to you somehting like this:

Login      Name                 TTY    Idle   When                 Where 

root       root                 pts/0         2009-06-15 13:41     192.168.1.133



	$ w
	 21:12:09 up 6 days,  7:42,  1 user,  load average: 0.27, 1.08, 1.64
	USER     TTY      FROM              LOGIN@   IDLE   JCPU   PCPU WHAT
	h3xx     pts/11   192.168.1.3      21:12    2.00s  0.04s  0.04s -bash



	last -f wtmp.1




The 'last' command reads data from /var/log/wtmp file. If you have logrotate service enabled it probably rotates wtmp file. Check if you have wtmp.1 or wtmp.1.gz file inside of /var/log directory. If you have it (or more similar with next numbers: wtmp.2 wtmp.3, etc) it means wtmp log is rotated. Then you can adjust/disable rotation or use 'last -f wtmp_file' command to check older data.








The last command uses the binary file /var/log/wtmp to show a listing of last logged in users.

But /var/log/wtmp is a rotated file where old entries are archived into /var/log/wtmp.x where x is a digit [0-9].

So If you need to look deeper in the login history, try to open one of those files:

last -2000 -f /var/log/wtmp.1 | less





You can also use the command lastlog command on Linux. It gives you more granular controls as to ranges of dates when looking through the logs of user logins.

excerpt from lastlog man page

   lastlog - reports the most recent login of all users or of a given user
Example

To find out the users that have logged into a system in the last 100 days.

	$ lastlog -b 0 -t 100
	Username         Port     From             Latest
	sam              pts/0    pegasus          Wed Jan  8 20:32:25 -0500 2014
	joe              pts/0    192.168.1.105    Thu Dec 12 12:47:11 -0500 2013