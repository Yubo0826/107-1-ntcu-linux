# HW-4
## �Ĥ@�D
* (1)�ϥ�groupadd�إ� mygroup�Bnogroup�s��
![](https://i.imgur.com/dJpTfMx.png)
* (2)�إ߱b���W�� myuser1~3 �åB�[�Jmygroup 
![](https://i.imgur.com/kah7GFM.png)
* (3)�إ߱b���W�� nouser1~3 �[�Jnogroup
![](https://i.imgur.com/KGjRGAy.png)
* (4)�ϥ�mkdir �إߥؿ� �M��ϥ� (chmod 770)��mygroup�s�դ����ϥΪ̧���ϥ� ���L��L�H���঳�����v��
![](https://i.imgur.com/BD30mUz.png)
* (5)������myuser1 �b/srv/myproject �ؿ����ϥ� touch myuser1.data�إ��ɮ�
![](https://i.imgur.com/M6agCgk.png)
* (6)������root �ϥ�(cp /usr/bin/ls /usr/local/bin/myls)    �_��/usr/bin/ls��/usr/local/bin/myls![](https://i.imgur.com/kDfE2hx.png)
* (7)�ϥ�(chmod u+s /usr/local/bin/myls)����v��
![](https://i.imgur.com/MNrpDMt.png)
* (8)������nouser1 �ϥ�(myls /srv/myproject) ���� ����O�_���\�ק��v��
![](https://i.imgur.com/aCU4ssh.png)

## �ĤG�D
* �ϥ� (ps |grep rsyslog) ��쪺 rsyslog �������{�Ǫ� PID, PRI, NI, COMMAND �A�ϥ�(ps aux | grep rsyslog > /root/process_syslog.txt)
![](https://i.imgur.com/o5SKjCq.png)

## �ĤT�D
* (1)�ϥ�(find /usr/bin /usr/sbin -perm /4000)��X /usr/bin �� /usr/sbin ��ӥؿ��� �t�� SUID ���S���ɮ��ɦW
![](https://i.imgur.com/JuBnRKR.png)
* (2)�A�ϥ�(find /usr/bin /usr/sbin -perm /4000 -exec ls -l {} \;)�C�X��쪺�ɮת������v��
![](https://i.imgur.com/XCBSKrX.png)
* (3)�̫�ϥ�(find /usr/bin /usr/sbin -perm/4000 -exec ls -l {} \; > /root/findsuidsgid.txt)�N�ù������s�� /root/findsuidsgid.txt �ɮפ�
![](https://i.imgur.com/sztl9Pq.png)


