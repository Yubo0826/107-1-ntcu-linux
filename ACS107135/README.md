## 1.�޲z�s�զ@�θ�ƪ��v���]�p�G<br>
-------------------------------<br>
### �إ߸s�զW�٬��G mygroup, nogroup<br>
��groupadd�إ߷s�s��<br>
![image](https://github.com/ACS107135/107-1-ntcu-linux/blob/HW-4/ACS107135/photo/1.PNG)<br>
-------------------------------<br>
### �إ߱b���W�٬��G myuser1, myuser2, myuser3 �A�q�q�[�J mygroup�A�B�K�X�� MyPassWord<br>
��useradd -g groupname username�إߤ@�ӭӸs�լ�"mygroup"���b��<br>
![image](https://github.com/ACS107135/107-1-ntcu-linux/blob/HW-4/ACS107135/photo/2.PNG)<br>
### �إ߱b���W�٬��G nouser1, nouser2, nouser3 �A�q�q�[�J nogroup�A�B�K�X�� MyPassWord<br>
��useradd -g groupname username�إߤ@�ӭӸs�լ�"nogroup"���b��<br>
![image](https://github.com/ACS107135/107-1-ntcu-linux/blob/HW-4/ACS107135/photo/3.PNG)<br>
-------------------------------<br>
### �إߤ@�ӦW�� /srv/myproject ���ؿ��A�o�ӥؿ��i�H�� mygroup �s�դ����ϥΪ̧���ϥΡA�B�i�s�ت��ɮ׾֦��s�աj�� mygroup �C���L��L�H���঳�����v��<br>
��"mkdir"�إ߷s�ؿ��A��"chmod"����v���A��"chgrp"���s�աA�̫��"ll"�˵��C<br>
![image](https://github.com/ACS107135/107-1-ntcu-linux/blob/HW-4/ACS107135/photo/4.PNG)<br>
### �Ȯɤ������� myuser1 �������A�ëe�� /srv/myproject �ؿ��A���իإߤ@�ӦW�� myuser1.data ���ɮסA����n�X myuser1�C<br>
cd�����ؿ��A����touch�s���ɮסA�M��exit�n�X�b���C<br>
![image](https://github.com/ACS107135/107-1-ntcu-linux/blob/HW-4/ACS107135/photo/5.PNG)<br>
-------------------------------<br>
### �_��/usr/bin/ls��/usr/local/bin/myls��A�����U�C�ާ@<br>
### ���M nogroup �s�դ����Τ��� /srv/myproject ���ӨS�������v���A���� nogroup �����Τ���� /usr/local/bin/myls �ɡA�i�H���ͻP ls �ۦP����T�A�B�Ȯɾ֦� mygroup �s�ժ��v���A�]���i�H�d�ߨ� /srv/myproject �ؿ������ɦW��T�C �]�N�O���A��A�ϥ� nouser1 ����������imyls /srv/myproject�j�ɡA���ӬO����d�\��ӥؿ������ɦW��T�C<br>
�p�D�A���O�̫�b��nouser1����imyls /srv/myproject�j�ɡA�o�L�k�q�L�v���C<br>
![image](https://github.com/ACS107135/107-1-ntcu-linux/blob/HW-4/ACS107135/photo/6.PNG)<br>
���ըϥ�chmod u+s�����ϥΪ�SUID���v���C(�u�n����H��x���v���A����ɦ۰ʳz�LSUID�ഫ������owner)<br>
���\����imyls /srv/myproject�j�C<br>
![image](https://github.com/ACS107135/107-1-ntcu-linux/blob/HW-4/ACS107135/photo/7.PNG)<br>
-------------------------------<br>
## 2.�ϥε{���[����O�A�f�t grep ������r�d�ߥ\��A�N��쪺 rsyslog �������{�Ǫ� PID, PRI, NI, COMMAND ����T��s�� /root/process_syslog.txt �ɮפ��C(�f�t>���ɦV��X)<br>
��"ps aux | grep rsyslog"��"top | grep rsyslog"�[��{�ǡA�M���">"�N��Ʋ������w�ɮסA�A��"cat"�˵��ɮפ��e�C<br>
(grep +(name)������r�j��)<br>
![image](https://github.com/ACS107135/107-1-ntcu-linux/blob/HW-4/ACS107135/photo/8.PNG)<br>
![image](https://github.com/ACS107135/107-1-ntcu-linux/blob/HW-4/ACS107135/photo/9.PNG)<br>
-------------------------------<br>
## 3.�ϥ� find ��X /usr/bin �� /usr/sbin ��ӥؿ����A�t�� SUID ���S���ɮ��ɦW�A�èϥ� ls -l �h�C�X��쪺�ɮת������v����A�N�ù������s�� /root/findsuidsgid.txt �ɮפ��C(�ۦ�d��find���O�Ϊk�A�H�Ψϳz�L���ɦV�Ÿ�>��X�ɮ�) <br>
��"find / -perm /u=s"�C�X�t�Τ��Ҧ� SUID ���ɮסA�æb�᭱�[�J"-exec ls -l {} ;"�C<br>
��">"�N��Ʋ���C<br>
![image](https://github.com/ACS107135/107-1-ntcu-linux/blob/HW-4/ACS107135/photo/10.PNG)<br>
��"cat"�˵��ɮפ��e<br>
![image](https://github.com/ACS107135/107-1-ntcu-linux/blob/HW-4/ACS107135/photo/11.PNG)
