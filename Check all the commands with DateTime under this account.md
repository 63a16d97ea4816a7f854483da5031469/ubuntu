#Check all the commands with DateTime under this account

Open terminalCtrl+Alt+T and run,

HISTTIMEFORMAT="%d/%m/%y %T "
then,

history



Yes, you can: if you set $HISTTIMEFORMAT, the .bash-history will be properly timestamped. That doesn't help with existing .bash-history content, but will help in the future.

cat /home/userName/.bash_history