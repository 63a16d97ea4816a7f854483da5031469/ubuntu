##Logrotate
http://www.ducea.com/2006/06/06/rotating-linux-log-files-part-2-logrotate/

Logrotate will look into /etc/logrotate.conf for its configuration directives.

	cat /etc/logrotate.conf
	
		
	# see "man logrotate" for details
	# rotate log files weekly
	weekly
	
	# keep 4 weeks worth of backlogs
	rotate 4
	
	# create new (empty) log files after rotating old ones
	create
	
	# uncomment this if you want your log files compressed
	#compress
	
	# packages drop log rotation information into this directory
	include /etc/logrotate.d
	
	# no packages own wtmp, or btmp -- we'll rotate them here
	/var/log/wtmp {
	missingok
	monthly
	create 0664 root utmp
	rotate 1
	}
	
	/var/log/btmp {
	missingok
	monthly
	create 0664 root utmp
	rotate 1
	}
	
	# system-specific logs may be configured here