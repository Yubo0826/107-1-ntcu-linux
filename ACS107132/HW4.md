##�@
#1-1�إ߸s�զW�٬��G mygroup, nogroup
*"groupadd mygroup", "groupadd nogroup"�A�إ�mygroup, nogroup�s��

#1-2�إ߱b���W�٬��G myuser1, myuser2, myuser3 �A�q�q�[�J mygroup�A�B�K�X�� MyPassWord
*"useradd -g mygroup [myuser1, myuser2, myuser3]"�A�إ�myuser1, myuser2, myuser3�å[�Jmygroup�s��
*"passwd [myuser1, myuser2, myuser3]"�]�w�K�X��MyPassWord

#1-3�إ߱b���W�٬��G nouser1, nouser2, nouser3 �A�q�q�[�J nogroup�A�B�K�X�� MyPassWord
*��1-2���B�J�@�ˡA�s�ո�ϥΪ̦W�٤��@�˦Ӥw
+"id"���O�i�H�T�w�ϥΪ̸��

#1-4�إߤ@�ӦW�� /srv/myproject ���ؿ��A�o�ӥؿ��i�H�� mygroup �s�դ����ϥΪ̧���ϥΡA�B�i�s�ت��ɮ׾֦��s�աj�� mygroup �C���L��L�H���঳�����v��
*�إߤ@�ӦW�� /srv/myproject ���ؿ�:"cd srv"��"mkdir myproject"
*"chgrp mygroup myproject"�]�wmygroup���s�լ�mygroup��"chmod 770 myproject"�]�w�v��mygroup�i�H����ϥΡA��L�ϥΪ̤���ϥ�

#1-5�Ȯɤ������� myuser1 �������A�ëe�� /srv/myproject �ؿ��A���իإߤ@�ӦW�� myuser1.data ���ɮסA����n�X myuser1
*"su myuser1"�n�Jmyuser1��"cd srv"��"cd myproject"��"vi myuser1.data"�إ�myuser1.data�ɮ�
*"exit"�n�X

#1-6�ƻs/usr/bin/ls��/usr/local/bin/myls��A�����U�C�ާ@
*"cp /from/usr/bin/ls /to/usr/local/bin/myls"�ƻs
*"su nouser1"�n�Jnouser1��"myls /srv/myproject"

##�G
#�N��쪺 rsyslog �������{�Ǫ� PID, PRI, NI, COMMAND
*"ps aux | grep rsyslog"��PID:950, command:/usr/bin/rsyslogd -n
*"top"��PR:20, NI:0
#�N��T��s�� /root/process_syslog.txt �ɮפ�
*"ps aux | grep rsyslog > /root/process_syslog.txt"��"vi process_syslog.txt"

##�T
#�ϥ� find ��X /usr/bin �� /usr/sbin ��ӥؿ����A�t�� SUID ���S���ɮ��ɦW
*"find /usr/bin /usr/sbin -perm /4000"
+chfn
+chsh
+mount
+chage
+gpasswd
+newgrp
+su
+umount
+sudo
+pkexec
+crontab
+passwd
+pam_timestamp_check
+unix_chkpwd
+usernetct1
#�ϥ� ls -l �h�C�X��쪺�ɮת������v����A�N�ù������s�� /root/findsuidsgid.txt �ɮפ�
*"find /usr/bin /usr/sbin -perm /4000 -exec ls -l {} \; >  /root/findsuidsgid.txt"
*"vi findsuidsgid.txt"