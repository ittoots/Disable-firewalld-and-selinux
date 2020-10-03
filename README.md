# Disable-firewalld-and-selinux

# Disable SeLinux
#check status of SELinux
sestatus

#Open selinux file and set SELINUX to disabled
vi /etc/sysconfig/selinux
SELINUX=disabled

#Confirm status of SELinux
sestatus

# Disable Firewalld
#Check state of firewall
sudo firewall-cmd --state

#Stop firewalld
sudo systemctl stop firewalld

#permanently disable firewalld
sudo systemctl disable firewalld

#confirm firewall is disabled
sudo firewall-cmd --state
