# 1</br>
## �إ߸s�զW�٬��Gmygroup, nogroup</br>
��"groupadd (groupname)"�إ߷s�s��</br>
![image](https://github.com/bill0330/107-1-ntcu-linux/blob/HW-4/ACS107137/img/1-1.PNG?raw=true)</br>
## �إ߱b���W�٬��Gmyuser1, myuser2, myuser3 �A�q�q�[�J mygroup�A�B�K�X�� MyPassWord</br>
![image](https://github.com/bill0330/107-1-ntcu-linux/blob/HW-4/ACS107137/img/1-2.PNG?raw=true)</br>
��"useradd -g mygroup (username)"�إߤ@�Ӹs�լ�mygroup���ϥΪ�</br>
## �إ߱b���W�٬��Gnouser1, nouser2, nouser3 �A�q�q�[�J nogroup�A�B�K�X�� MyPassWord</br>
��"useradd -g nogroup (username)"�إߤ@�Ӹs�լ�nogroup���ϥΪ�</br>
![image](https://github.com/bill0330/107-1-ntcu-linux/blob/HW-4/ACS107137/img/1-3.PNG?raw=true)</br>
## �إߤ@�ӦW�� /srv/myproject ���ؿ��A�o�ӥؿ��i�H�� mygroup �s�դ����ϥΪ̧���ϥΡA�B�i�s�ت��ɮ׾֦��s�աj�� mygroup �C(���L��L�H���঳�����v��)</br>
��"mkdir"�إߥؿ��A��"chmod"����v���A��"chgrp"���ܸs�աA�A��"ll"�d��</br>
![image](https://github.com/bill0330/107-1-ntcu-linux/blob/HW-4/ACS107137/img/1-4.PNG?raw=true)</br>
## �Ȯɤ������� myuser1 �������A�ëe�� /srv/myproject �ؿ��A���իإߤ@�ӦW�� myuser1.data ���ɮסA����n�X myuser1</br>
��"su (username)"�����ϥΪ̡A"cd (�ؿ��W)"�e���ӥؿ��A"touch (�ɮצW)"�إ��ɮסA�̫��"exit"�n�X�b��</br>
![image](https://github.com/bill0330/107-1-ntcu-linux/blob/HW-4/ACS107137/img/1-5.PNG?raw=true)</br>
## �ƻs/usr/bin/ls��/usr/local/bin/myls��A�����U�C�ާ@</br>
��"cp -r A B"�NA�����ƻs��B�W(-r�������ƻs���\��)</br>
![image](https://github.com/bill0330/107-1-ntcu-linux/blob/HW-4/ACS107137/img/1-6.PNG?raw=true)</br>
## ���M nogroup �s�դ����Τ��� /srv/myproject ���ӨS�������v���A���� nogroup �����Τ���� /usr/local/bin/myls �ɡA�i�H���ͻP ls �ۦP����T�A�B�Ȯɾ֦� mygroup �s�ժ��v���A�]���i�H�d�ߨ� /srv/myproject �ؿ������ɦW��T�C �]�N�O���A��A�ϥ� nouser1 ����������imyls /srv/myproject�j�ɡA���ӬO����d�\��ӥؿ������ɦW��T�C</br>
��nouser1����myls /srv/myproject�ɡA�L�k�}���ɮ�(�v������)</br>
![image](https://github.com/bill0330/107-1-ntcu-linux/blob/HW-4/ACS107137/img/1-7.1.PNG?raw=true)</br>
�ݭn��"chmod u+s"�����ϥΪ�SUID���v��</br>
![image](https://github.com/bill0330/107-1-ntcu-linux/blob/HW-4/ACS107137/img/1-7.2.PNG?raw=true)</br>
# 2</br>
## �ϥε{���[����O�A�f�t grep ������r�d�ߥ\��A�N��쪺 rsyslog �������{�Ǫ� PID, PRI, NI, COMMAND ����T��s�� /root/process_syslog.txt �ɮפ��C(�f�t>���ɦV��X)</br>
��"ps aux |grep rsyslog"�[��t�Υ����{�ǡA�ñN��rsyslog����r���{�ǧ�X�C�A��">"�N��Ʋ������w�ɮסA�̫�f�t"cat"�˵��ɮפ��e</br>
![image](https://github.com/bill0330/107-1-ntcu-linux/blob/HW-4/ACS107137/img/2-1.PNG?raw=true)</br>
# 3</br>
## �ϥ� find ��X /usr/bin �� /usr/sbin ��ӥؿ����A�t�� SUID ���S���ɮ��ɦW�A�èϥ� ls -l �h�C�X��쪺�ɮת������v����A�N�ù������s�� /root/findsuidsgid.txt �ɮפ��C(�ۦ�d��find���O�Ϊk�A�H�Ψϳz�L���ɦV�Ÿ�>��X�ɮ�)</br>
��"find / -perm /u=s"�C�X�t�Τ��Ҧ� SUID ���ɮסA�æb�᭱�[�J"-exec ls -l {} \\;"����ɮ׬����v��</br>
*����:* "-exec"�i�H���j�M�X�Ӫ����G�A�ϥΨ�L�����O�i����򪺳B�z�ʧ@</br>
![image](https://github.com/bill0330/107-1-ntcu-linux/blob/HW-4/ACS107137/img/3-1.PNG?raw=true)</br>