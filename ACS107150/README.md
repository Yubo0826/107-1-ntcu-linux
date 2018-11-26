# 1.�޲z�s�զ@�θ�ƪ��v���]�p�G

## �إ߸s�զW�٬��G mygroup, nogroup

-  ��groupadd <�s��>�s�W�s��
-  �A��grep <�s��> /etc/group�T�{�s�լO�_�]�ߦ��\

> ![GITHUB](https://github.com/JackyBigNose/107-1-ntcu-linux/blob/HW-4/ACS107150/1.PNG?raw=true)

## �إ߱b���W�٬��G myuser1, myuser2, myuser3 �A�q�q�[�J mygroup�A�B�K�X�� MyPassWord

-  ��useradd -G <�s��> <�b��>�s�W�b���ç�b���[�J���w���s��
-  ��passwd <�b��>�s�W�K�X

> ![GITHUB](https://github.com/JackyBigNose/107-1-ntcu-linux/blob/HW-4/ACS107150/2.PNG?raw=true)

## �إ߱b���W�٬��G nouser1, nouser2, nouser3 �A�q�q�[�J nogroup�A�B�K�X�� MyPassWord

-  �P�W�B�J

> ![GITHUB](https://github.com/JackyBigNose/107-1-ntcu-linux/blob/HW-4/ACS107150/3.PNG?raw=true)

## �إߤ@�ӦW�� /srv/myproject ���ؿ��A�o�ӥؿ��i�H�� mygroup �s�դ����ϥΪ̧���ϥΡA�B�i�s�ت��ɮ׾֦��s�աj�� mygroup �C���L��L�H���঳�����v��

-  ����cd�i�Jsrv�o�ӥؿ�
-  ��mkdir <�ؿ�>�Ы�myproject
-  ��ll�T�{�O�_�s�b�M�T�{�v��
-  ��chgrp <�s��> <�ؿ�>��myproject���s�է��ܦ�mygroup
-  ��chmod��s�ժ��ϥΪ��v���令rwx,���L�H�令�S���v��
-  ��ll�T�{�v���O�_���ܦ��\

> ![GITHUB](https://github.com/JackyBigNose/107-1-ntcu-linux/blob/HW-4/ACS107150/4.PNG?raw=true)

## �Ȯɤ������� myuser1 �������A�ëe�� /srv/myproject �ؿ��A���իإߤ@�ӦW�� myuser1.data ���ɮסA����n�X myuser1�C

-  ��su <�b��>��ϥΪ̤�����myuser1
-  ��cd�i�Jmyproject,�A��touch <�ɮ�>�Ы�myuser1.data
-  ��su root��myuser1�n�X�õn�Jroot

> ![GITHUB](https://github.com/JackyBigNose/107-1-ntcu-linux/blob/HW-4/ACS107150/5.PNG?raw=true)

## �_��/usr/bin/ls��/usr/local/bin/myls��A�����U�C�ާ@

### ���M nogroup �s�դ����Τ��� /srv/myproject ���ӨS�������v���A���� nogroup �����Τ���� /usr/local/bin/myls �ɡA�i�H���ͻP ls �ۦP����T�A�B�Ȯɾ֦� mygroup �s�ժ��v���A�]���i�H�d�ߨ� /srv/myproject �ؿ������ɦW��T�C �]�N�O���A��A�ϥ� nouser1 ����������imyls /srv/myproject�j�ɡA���ӬO����d�\��ӥؿ������ɦW��T�C

-  ��cp��/usr/bin/ls�ƻs��/usr/local/bin/myls
-  ��ll�T�{myls���v��
-  (��:���e�ڤw�g�Nmyls�W�[SUID���v��,�����F����e�{���e,�|�A����O�ܽd�@��)
-  ��chmod 4755����v��
-  �A��ll�T�{myls���v��
-  ��su�����ϥΪ̬�nouser1
-  ����myls /srv/myproject�T�{�i���i�H����

> ![GITHUB](https://github.com/JackyBigNose/107-1-ntcu-linux/blob/HW-4/ACS107150/a.PNG?raw=true)

# 2.�ϥε{���[����O�A�f�t grep ������r�d�ߥ\��A�N��쪺 rsyslog �������{�Ǫ� PID, PRI, NI, COMMAND ����T��s�� /root/process_syslog.txt �ɮפ��C(�f�t>���ɦV��X)

-  ��ps aux |grep rsyslog��M�Prsyslog�������{��
-  �ĤG����ܪ����G�q�`�O�j�M�Prsyslog�������{�ǳo�Ӱʧ@�Ҳ��ͪ��{��,�G�u�ݰO��Ĥ@�ӷj�M�쪺�{��PID���X

> ![GITHUB](https://github.com/JackyBigNose/107-1-ntcu-linux/blob/HW-4/ACS107150/6.PNG?raw=true)

-  ��top -p �Ҭd�{�Ǫ�PID���X
-  �N�|�]�Xrsyslog �������{�Ǫ���T

> ![GITHUB](https://github.com/JackyBigNose/107-1-ntcu-linux/blob/HW-4/ACS107150/7.PNG?raw=true)

> ![GITHUB](https://github.com/JackyBigNose/107-1-ntcu-linux/blob/HW-4/ACS107150/8.PNG?raw=true)

-  ��top -p PID���X > /root/process_syslog.txt��s�J�ɮפ�
-  (��:�p�G�n��s�J���ɮפ��s�b,�t�η|�s�y�@�Ӫ��ɮ�;�Y�s�b,�t�η|�M���ɮת����e�A�s�J���)
-  ��cat�T�{�ɮפ��e

> ![GITHUB](https://github.com/JackyBigNose/107-1-ntcu-linux/blob/HW-4/ACS107150/9.PNG?raw=true)

> ![GITHUB](https://github.com/JackyBigNose/107-1-ntcu-linux/blob/HW-4/ACS107150/10.PNG?raw=true)

# 3.�ϥ� find ��X /usr/bin �� /usr/sbin ��ӥؿ����A�t�� SUID ���S���ɮ��ɦW�A�èϥ� ls -l �h�C�X��쪺�ɮת������v����A�N�ù������s�� /root/findsuidsgid.txt �ɮפ��C(�ۦ�d��find���O�Ϊk�A�H�Ψϳz�L���ɦV�Ÿ�>��X�ɮ�)


-  ��find <�ؿ�> -perm /u=s��M�t��SUID���S���ɮ��ɦW

> ![GITHUB](https://github.com/JackyBigNose/107-1-ntcu-linux/blob/HW-4/ACS107150/11.PNG?raw=true)

-  �Ĥ@�ӥ�ll <�ɮ�> > /root/findsuidsgid.txt�s���,��L����ll <�ɮ�> >> /root/findsuidsgid.txt
-  �]����>�ɷ|�⤧�e����ƥ��M���A�s,�ӥ�>>���|�M�����
-  ��cat�T�{�ɮפ��e

> ![GITHUB](https://github.com/JackyBigNose/107-1-ntcu-linux/blob/HW-4/ACS107150/12.PNG?raw=true)

> ![GITHUB](https://github.com/JackyBigNose/107-1-ntcu-linux/blob/HW-4/ACS107150/13.PNG?raw=true)


