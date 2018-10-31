HW-4
#�إ߸s�զW�٬��G mygroup, nogroup
�ѨM��k:
(1)��Jgroupadd mygroup�A�A��Jgrep mygroup /etc/group�A�ˬd�O�_�إߦ��\
(2)��Jgroupadd nogroup�A�A��Jgrep nogroup /etc/group�A�ˬd�O�_�إߦ��\

#�إ߱b���W�٬��G myuser1, myuser2, myuser3 �A�q�q�[�J mygroup�A�B�K�X�� MyPassWord
�ѨM��k:
��Juseradd -G mygroup myuser1�Buseradd -G mygroup myuser2�Buseradd -G mygroup myuser3
�A��J id myuser1,id myuser2,id myuser3�˵�myuser1,myuser2,myuser3���s�լO�_��mygroup
�K�X�]�w������: 
(1)��Jecho MyPassWord | passwd --stdin myuser1�|�X�{Changing password for user myuser1�Mpasswd:all authentication tokens updated successfully�N��K�X���\�]�w�n
(2)��Jecho MyPassWord | passwd --stdin myuser2�|�X�{Changing password for user myuser2�Mpasswd:all authentication tokens updated successfully�N��K�X���\�]�w�n
(3)��Jecho MyPassWord | passwd --stdin myuser3�|�X�{Changing password for user myuser3�Mpasswd:all authentication tokens updated successfully�N��K�X���\�]�w�n

#�إ߱b���W�٬��G nouser1, nouser2, nouser3 �A�q�q�[�J nogroup�A�B�K�X�� MyPassWord
�ѨM��k:
��Juseradd -G nogroup nouser1�Buseradd -G nogroup nouser2�Buseradd -G nogroup nouser3
�A��J id nouser1,id nouser2,id nouser3�˵�nouser1,nouser2,nouser3���s�լO�_��nogroup
�K�X�]�w������: 
(1)��Jecho MyPassWord | passwd --stdin nouser1�|�X�{Changing password for user nouser1�Mpasswd:all authentication tokens updated successfully�N��K�X���\�]�w�n
(2)��Jecho MyPassWord | passwd --stdin nouser2�|�X�{Changing password for user nouser2�Mpasswd:all authentication tokens updated successfully�N��K�X���\�]�w�n
(3)��Jecho MyPassWord | passwd --stdin nouser3�|�X�{Changing password for user nouser3�Mpasswd:all authentication tokens updated successfully�N��K�X���\�]�w�n

#�إߤ@�ӦW�� /srv/myproject ���ؿ��A�o�ӥؿ��i�H�� mygroup �s�դ����ϥΪ̧���ϥΡA�B�i�s�ت��ɮ׾֦��s�աj�� mygroup �C���L��L�H���঳�����v��
**��Jmkdir /srv/myproject�A�A��Jchgrp mygroup /srv/myproject�A�A����v����Jchmod 770 /srv/myproject�A�A��Jls -1d /srv/myproject�ݬݬO�_�v����令�\

#�Ȯɤ������� myuser1 �������A�ëe�� /srv/myproject �ؿ��A���իإߤ@�ӦW�� myuser1.data ���ɮסA����n�X myuser1�C
**����myuser1�A��Jsu myuser1,���������Jcd /srv/myproject�A�i��ؿ��ɫإߤ@���ɮסA��Jmkdir myuser1.data�A��Jls �[�ݬO�_���ɦ��\�A�̫��Jcd ..�n�X

#�ƻs/usr/bin/ls��/usr/local/bin/myls��A�����U�C�ާ@
(1)��Jcp /usr/bin/ls /usr/local/bin/myls
(2)�˵��ۤv���S���ƻs���\�A��Jll /usr/local/bin/myls
(3)���\�|��� -rwxr-xr-x. 1 root root 117672 Oct 28 16:23 /usr/local/bin/myls(/usr/local/bin/myls�|�e�{����)
**SUID-���ӵ{���ӻ��A�����x���v��
**����̦b����L�{���N�|�����ӵ{���s�ժ��v��
(4)��Jsudo chmod u+s /usr/local/bin/myls
(5)��J�˵�ll /usr/local/bin/myls
(6)���\�|��� -rwxr-xr-x. 1 root root 117672 Oct 28 16:23 /usr/local/bin/myls(/usr/local/bin/myls�|�e�{����)
(7)����su nouser1
(8)��Jmyls /srv/myproject
(9)myuser1.data ���\����

#�ϥε{���[����O�A�f�t grep ������r�d�ߥ\��A�N��쪺 rsyslog �������{�Ǫ� PID, PRI, NI, COMMAND ����T��s�� /root/process_syslog.txt �ɮפ��C(�f�t>���ɦV��X)
(1)�Q��grep��M
��J-- ps aux | grep rsyslog
��XPID---977�A��Xcommand��/usr/bin/rsyslogd-n
(2)��Jps -l
�o�{�i�H�d��PID���
(3)��Xps -977
�o�{�i�H��Xcommand��/usr/bin/rsyslogd-n
(4)���ۧQ��top�Bps aux��XPR��NI�����
(5)�̫��x�s���
(6)��Jps aux | grep rsyslog > /root/process_syslog.txt
(7)��Jvi process_syslog.txt

#�ϥ� find ��X /usr/bin �� /usr/sbin ��ӥؿ����A�t�� SUID ���S���ɮ��ɦW�A�èϥ� ls -l �h�C�X��쪺�ɮת������v����A�N�ù������s�� /root/findsuidsgid.txt �ɮפ��C(�ۦ�d��find���O�Ϊk�A�H�Ψϳz�L���ɦV�Ÿ�>��X�ɮ�)
(1)find /usr/bin /usr/sbin -perm /4000
�C�X�����ɦW
chfn,chsh,mount,chage,gpasswd,newgrp,su,umount,sudo,pkexec,crontab,passwd,pam_timestamp_check,uniz_chkpwd,usernetct1
(2)find /usr/bin /usr/sbin -perm /4000 -exec ls -l {} \;(�N�v�����C�L�X��)
(3)�s���ɮר�findsuidsgid.txt
find /usr/bin /usr/sbin -perm/4000 -exec ls -l {} \; > /root/findsuidsgid.txt
(4)��Jvi findsuidsgid.txt�ݬO�_�s�����\