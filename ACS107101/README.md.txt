# HW4
#### �Ĥ@�D
+ 1.�إ߸s�աG mygroup, nogroup
![GITHUB](https://imgur.com/h1FKkwT.jpg"git�ϥ�")
+ 2.�إ߱b���W�٬��G myuser1, myuser2, myuser3, nouser1, nouser2, nouser3 
![GITHUB](https://imgur.com/WvKD2fO.jpg"git�ϥ�")
+ 3.�إ߱b�����K�X�A�Ҭ�MyPassWord
![GITHUB](https://imgur.com/rzz5iAR.jpg"git�ϥ�")
+ 4.�Nmyuser1, myuser2, myuser3���O�[�Jmygroup�A�A�Nnouser1, nouser2, nouser3 �[��nogroup
![GITHUB](https://imgur.com/JKO33Wm.jpg"git�ϥ�")
+ 5.�إߤ@�ӦW�� /srv/myproject ���ؿ��A�o�ӥؿ��i�H�� mygroup �s�դ����ϥΪ̧���ϥΡA�B�i�s�ت��ɮ׾֦��s�աj�� mygroup �C���L��L�H���঳�����v��
![GITHUB](https://imgur.com/HhAO7i5.jpg"git�ϥ�")
+ 6.������myuser1�A�إ�myuser1.data���ɮ�
+ 7.�_��/usr/bin/ls��/usr/local/bin/myls��A�����U�C�ާ@
![GITHUB](https://imgur.com/FQim1ji.jpg"git�ϥ�")
+ ��Jcp /usr/bin/ls /usr/ocal/bin/myls
+ �A��Jll /usr/local/bin/myls�A�˵��O�_���\
####�ĤG�D
+ �ϥε{���[����O�A�f�t grep ������r�d�ߥ\��A�N��쪺 rsyslog �������{�Ǫ� PID, PRI, NI, COMMAND ����T��s�� /root/process_syslog.txt �ɮפ��C(�f�t>���ɦV��X)
+ ��Jps aux | grep rsyslog�˵�
![GITHUB](https://imgur.com/epFemVv.jpg"git�ϥ�")
+ ��Jps -l�A�˵�PID�BPRI�BNI�BCMD
+ �Q��top�Bps aux��XPR��NI�����
![GITHUB](https://imgur.com/dSMSVK3.jpg"git�ϥ�")
+ ��Jps aux | grep rsyslog > /root/process_syslog.txt
#### �ĤT�D
+ �ϥ� find ��X /usr/bin �� /usr/sbin ��ӥؿ����A�t�� SUID ���S���ɮ��ɦW�A�èϥ� ls -l �h�C�X��쪺�ɮת������v����A�N�ù������s�� /root/findsuidsgid.txt �ɮפ��C(�ۦ�d��find���O�Ϊk�A�H�Ψϳz�L���ɦV�Ÿ�>��X�ɮ�)
![GITHUB](https://imgur.com/dSMSVK3.jpg"git�ϥ�")
+ ��Jfind /usr/bin /usr/sbin -perm /4000�A�C�X�ɦW
![GITHUB](https://imgur.com/tSHEcDC.jpg"git�ϥ�")
+ find /usr/bin /usr/bin | ls -1 �A�C�X�v��
![GITHUB](https://imgur.com/S6AWRhZ.jpg"git�ϥ�")
+ find /usr/bin /usr/sbin | ls -1 �A�C�X�v��
![GITHUB](https://imgur.com/AnbqSXb.jpg"git�ϥ�")
+ find /usr/bin /usr/bin | ls -1 > /root/findsuidsgid.txt�A�N�ɮצs��findsuidsgid.txt