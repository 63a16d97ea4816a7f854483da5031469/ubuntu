#VIEW UTMP, WTMP AND BTMP FILES

http://www.linuxnix.com/read-view-utmp-wtmp-btmp-file-linuxunix/

<b>utmp</b> will give you complete picture of users logins at which terminals, logouts, system events and current status of the system, system boot time (used by uptime) etc.  
<b>wtmp</b> gives historical data of utmp.  
<b>btmp</b> records only failed login attempts.  



last -f /var/log/btmp

Sample output of last -f wtmp command output.

	last -f wtmp.1

	root pts/1 ae.ptr10.public. Sun Sep 30 13:01 – 13:11 (00:10) 
	surendra pts/1 :0 Sun Sep 30 09:23 – 10:55 (01:32) 
	reboot system boot 3.2.0-30-generic Sun Sep 30 07:36 – 20:12 (1+12:36) 
	reboot system boot 3.2.0-30-generic Sat Sep 29 21:56 – 01:19 (03:23) 
	surendra pts/1 :0 Sat Sep 29 09:36 – 14:37 (05:01)
	
	<–output clipped here–>
	reboot system boot 3.2.0-30-generic Fri Sep 28 22:51 – 14:37 (15:46) 
	reboot system boot 3.2.0-30-generic Fri Sep 28 21:39 – 21:45 (00:05) 
	reboot system boot 3.2.0-29-generic Sat Sep 1 22:53 – 23:07 (00:14)

