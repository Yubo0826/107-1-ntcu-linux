�Ĥ@�D:
(1)��groupadd mygroup;groupadd nogroup�إ߸s�աC

(2)��useradd -G mygroup myuser1;useradd -G mygroup myuser2;useradd -G mygroup myuser3�إ߱b���A�å[�Jmygroup�A�M���passwd myuser1;passwd myuser2;passwd myuser3(�K�X���OMyPassWord)�C

(3)��useradd -G nogroup nouser1;useradd -G nogroup nouser2;useradd -G nogroup nouser3�إ߱b���A�å[�Jnogroup�A�M���passwd nouser1;passwd nouser2;passwd nouser3(�K�X���OMyPassWord)�C

(4)��mkdir /srv/myproject�إߥؿ��A�M���chgrp mygroup /srv/myproject���ؿ����s�աA���ۥ�chmod 770 /srv/myproject�� mygroup �s�դ����ϥΪ̧���ϥΡA����L�H�S�������v���C(�i��ls -ld /srv/myproject�ˬd�O�_����勵�T)�C

(5)���myuser1�n�J�A�M��cd /srv/myproject�e���ؿ��A���ۥ�touch myuser1.data�إ��ɮסA������n�Xmyuser1�C

(6)��root�n�J��A��cp /usr/bin/ls /usr/local/bin/myls�A���ۧ��nouser1�n�J�A��sudo chmod u+s /usr/local/bin/myls��root��x�v���ܦ�s�A���ۤ�����nouser1�n�J�A����myls /srv/myproject�A�M��N�i�H�d�\��ӥؿ������ɦW��T(myuser1.data)�C


�ĤG�D:
��ps |grep rsyslog���rsyslog �������{�Ǫ� PID, PRI, NI, COMMAND ����T�A����ps aux | grep rsyslog > /root/process_syslog.txt�N�ɮ���s�L�h(�i��vi process_syslog.txt�ˬd�O�_���x�s)�C


�ĤT�D:
��find /usr/bin /usr/sbin -perm /4000��X�t�� SUID ���S���ɮ��ɦW�A���ۥ�find /usr/bin /usr/sbin -perm /4000 -exec ls -l {} \;��X�v���A�̫��find /usr/bin /usr/sbin -perm/4000 -exec ls -l {} \; > /root/findsuidsgid.txt�N�����s�� /root/findsuidsgid.txt(�i��vi findsuidsgid.txt�ˬd�O�_���x�s)�C