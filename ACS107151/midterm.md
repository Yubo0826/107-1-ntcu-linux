### �@.
+ 1.��J **uname -r** �ݪ�����T
+ 2.��J **ver=my kernel version is 4.17.0-kali-amd64**
+ 3.��J **echo $PATH "�i�H�ݨ�PATH���Ȥ嬰 /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
+ 4.PATH���\��:�@�~�t�η|�̷�PATH�����ܼƤ��ҳ]�w�����|���ǡA����M��Ӹ��|�U�O�_���n�ϥΪ����O�A�Y�䤣��A�N�|���command not found �Y�h�ӥؿ��U�������O�A�w�u����쪺���D�C
***
### �G.
+ 1.d: �N��᭱���ɦW���ؿ��ɡC
+ 2.�֦��̬� root�Aroot �㦳 rwx ���v�� (�Ĥ@���v��)�A�s�ճ]�w�� mail�A�h�Ҧ��[�J mail �o�Ӹs�ժ��b���i�H�㦳 rwx ���v�� (�ĤG���v��)�A���O root �]�S���[�J mail ����A�u�� rx ���v�� (�ĤT���v��)�A���O root �]�S���[�J mail ����A�u�� rx ���v�� (�ĤT���v��)
+ 3.�֦��̥i�H�i�HŪ.�g.����A�s�ե�O�A��L�ϥΪ̥u��Ū�M����C
+ 4.��3�ӳs���ɮ�
+ 5.�ɮת��e�q��4096
+ 6.���ɮ׳̫�@���Q�ק�/�׭q������ɶ��� 2017/02/16
+ 7.�ɦW��mail
+ 8.��J **chmod 777 script.sh** �� **chmod u=rwx.g=rwx,o=rwx script.sh**
***
### �T.
+ 1.�Ÿ��s���N�O�b�إߤ@�ӿW�ߪ��ɮסA�ӳo���ɮ׷|����ƪ�Ū�����V�L link �������ɮת��ɦW�A�ӹ���s�� �u�O�b�Y�ӥؿ��U�s�W�@���ɦW�s����Y inode ���X�����s�O���Ӥw�C
+ 2.�ϥ� **cd~** ��a�ؿ��A��J **ln /etc/hosts hosts.real** �إ߹���s��
+ 3.�ϥ� **cd~** ��a�ؿ��A��J **ln -s /etc/hosts hosts.symbo** �إ߲Ÿ��s��
***
### �|.
+ 1.�s�W�@�ӺϺ�
![image](https://imgur.com/6piwOtW.png)
+ 2.�� **fdisk /dev/sdd** ���ΥX1G���Ϻ�
![image](https://imgur.com/6APSHTL.png)
+ 3.�A�� **mkfs.xfs /dev/sdd1** �إߤ@�Ӯe�q��1GB��xfs�ɮרt��
![image](https://imgur.com/a/IVo9z6V.png)
+ 4.��J **mkdir /srv/maildir** �� **mount /dev/sdd1 /srv/maildir**����
+ 5.�ק� /etc/fstab�A��J **/etc/fstab**
+ 6.�� **blkid** ��/dev/sdd1�� UUID�Ψ�L���
+ 7.��J **vim /etc/fstab**��J�s�W/dev/sdd1�����
![image](https://imgur.com/K87NV6G.png)
+ 8.��J **df -T** �i�H�ˬd��1GB���ɮרt�Υ�������/srv/maildir
~[image](https://imgur.com/fXGd6Cp.png)
+ 9.���� **groupoadd mailgroup** �إ�mailgroup�o�Ӹs��
+ 10.�� **useradd -G mailgroup mailuser** �s�Wmailuser�ϥΪ̨å[�Jmailgroup
+ 11.�� **id mailuser** �ϥΪ̦��bmailgroup
![image](https://imgur.com/czYLvd1.png)
+ 12.��J **cat /etc/fstab | grep mailuser** ���Ҧ��]�w�}���۰ʱ���
+ 13.�� **chgrp mailgroup /srv/maildur** ���s��
+ 14.��J **ls -ali /srv/maildir** �d���ɮת��ݩ�
![image](https://imgur.com/cdJrXUi.png)
