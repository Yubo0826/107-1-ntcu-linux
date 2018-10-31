## �޲z�s��
1.�إ߸s��
   * groupadd mygroup
   * groupadd nogroup
2.�إ߷s�ϥΪ�+�s��
   * useradd -G mygroup myuser1~3
   * useradd -G mygroup nouser1~3
     -G:���w�s��
   * passwd myuser1~3 �]�w�K�X
   * passwd nouser1~3 �]�w�K�X
3.�ˬd
   * id myuser1
      uid=1004(myuser1) gid=1006(myuser1) groups=1006(myuser1),1004(mygroup)
   * id myuser2
      uid=1005(myuser2) gid=1007(myuser2) groups=1007(myuser2),1004(mygroup)
   * id myuser3
      uid=1006(myuser3) gid=1008(myuser3) groups=1008(myuser3),1004(mygroup)
   * id nouser1
      uid=1007(nouser1) gid=1009(nouser1) groups=1009(nouser1),1005(nogroup)
   * id nouser2
      uid=1008(nouser2) gid=1010(nouser2) groups=1010(nouser2),1005(nogroup)
   * id nouser3
      uid=1009(nouser3) gid=1011(nouser3) groups=1011(nouser3),1005(nogroup)
4.�إ�/srv/myproject + �ק�s�թM�v��
   (1)mkdir /srv/myproject
   (2)chgrp mygroup /srv/myproject
   (3)chmod 770 /srv/myproject
   (4)ls -ld /srv/myproject
      * drwxrwx---. 2 root mygroup 6 Oct 28 11:26 /srv/myproject
5.������myuser1�A�إ�myuser1.data���ɮ�
   (1)su myuser1
   (2)cd /srv/myproject
   (3)vi myuser1.data
      * [Esc] :wq
6.�ƻs /usr/bin/ls��/usr/local/bin/myls
   (1)cp /usr/bin/ls /usr/local/bin/myls
   (2)ll /usr/local/bin/myls
      * -rwxr-xr-x. 1 root root 117672 Oct 28 11:46 /usr/local/bin/myls
7.��������nouser1
   su nouser1
   (1)�Ĥ@������
    * ls : permission denied
    * ll /usr/local/bin/myls
       -rwxr-xr-x. 1 root root 117672 Oct 28 11:46 /usr/local/bin/myls
    * myls /srv/myproject : permission denied
  (2)�ĤG������
     �ק�s��
    [root����]
    * ll /usr/local/bin/myls
       -rwxr-xr-x. 1 root root 117672 Oct 28 11:46 /usr/local/bin/myls
    * chgrp mygroup /usr/local/bin/myls
    * ll /usr/local/bin/myls
       -rwxr-xr-x. 1 root mygroup 117672 Oct 28 11:46 /usr/local/bin/myls
    * su nouser1
    * myls /srv/myproject : permission denied
  (3)�ĤT������
    [root����]
    * sudo chmod u+s /usr/local/bin/myls
    * ll /usr/local/bin/myls
       -rwsr-xr-x. 1 root mygroup 117672 Oct 28 11:46 /usr/local/bin/myls
           �ɦW�ܦ�����
    * su nouser1
    * myls /srv/myproject
    * myuser1.data ���\����
----------------------------------------------------

## �{�ǫ��O
1.�Q��grep �M��rsyslog�����{�Ǹ��
  * PID:955
  * PR:20
  * NI:0
  * COMMAND:/usr/bin/rsyslogd -n
  (1)�Ĥ@������
   * ps aux | grep rsyslog
   ��XPID��955
   ��XCOMMAND��/usr/bin/rsyslogd -n
  (2)�ĤG������
   * ps -l
   �S�����������
  (3)�ĤT������
   * ps -1
   �o�{�i�H�d�߸�PID�����
  (4)�ĥ|������
   * ps -955
   ��XCOMMAND��/usr/bin/rsyslogd -n
  (5)�Ĥ�������
   * top
   ��XPR��20
   ��XNI��0
  (6)�Ĥ�������
   * ps aux
   �]��XPR��20
   ��XNI��0
2.�N����쪺rsyslog���ɮ��x�s��/root/process_syslog.txt
  * ps aux | grep rsyslog > /root/process_syslog.txt
  * vi process_syslog.txt
     �o�{��Ƥw�s���ɮפ�
----------------------------------------------------

## find���O�ξާ@
1.find /usr/bin /usr/sbin -perm /4000
   * SUID��4��
   * -perm /mode �G�j�M�ɮ��v���y�]�t���@ mode ���v���z���ɮ�
2.find /usr/bin /usr/sbin -perm /4000 -exec ls -l {} \;
   * -exec (���O) : �N�ɮ��ন(���O)�A���D���নls -l�C�X��
  �S���ɦW:
   - chfn
   - chsh
   - mount
   - chage
   - gpasswd
   - newgrp
   - su
   - umount
   - sudo
   - pkexec
   - crontab
   - passwd
   - pam_timestamp_check
   - unix_chkpwd
   - usernetct1
3.�s���ɮר�findsuidsgid.txt
  * find /usr/bin /usr/sbin -perm /4000 -exec ls -l {} \; >  /root/findsuidsgid.txt
  * vi findsuidsgid.txt
     �o�{��Ƥw�s���ɮפ�