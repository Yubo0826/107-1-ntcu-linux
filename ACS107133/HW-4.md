1.��Jgroupadd mygroup�Mnogroup�إ߸s�աA�A��Jgpasswd mygroup�i�H�]�w�K�X�A���L�ڤW���d���q�`�����|�N�s�ճ]�w�K�X�C
2.��Juseradd myuser1�إ߱b���A�A��Jpasswd myuser1�]�w�K�X��MyPassWord�C
3.��Juseradd myuser2�إ߲ĤG�ӱb���A�A��Jpasswd myuser2�]�w�K�X��MyPassWord�C
3.��Juseradd myuser3�إ߲ĤT�ӱb���A�A��Jpasswd myuser3�]�w�K�X��MyPassWord
4.�ڥ��ӬO��Juseradd -G mygroup myuser1�A���|�L�k���\�A�ҥH�令��Jusermod -g mygroup myuser1���ܦ��b�������ݸs�աA�A��Jid myuser1�d�ݡA�i�o�{�ܬ�mygroup
5.��Jusermod -g mygroup myuser2���ܦ��b�������ݸs�աA�A��Jid myuser2�d�ݡA�i�o�{�ܬ�mygroup
6.��Jusermod -g mygroup myuser3���ܦ��b�������ݸs�աA�A��Jid myuser3�d�ݡA�i�o�{�ܬ�mygroup
7.��Juseradd nouser1�إ߱b���A�A��Jpasswd nouser1�]�w�K�X��MyPassWord�C
8.��Juseradd nouser2�إ߱b���A�A��Jpasswd nouser2�]�w�K�X��MyPassWord�C
9.��Juseradd nouser3�إ߱b���A�A��Jpasswd nouser3�]�w�K�X��MyPassWord�C
10.��Jusermod -g nogroup nouser1���ܦ��b�������ݸs�աA�A��Jid nouser1�d�ݡA�i�o�{�ܬ�nogroup
11.��Jusermod -g nogroup nouser2���ܦ��b�������ݸs�աA�A��Jid nouser2�d�ݡA�i�o�{�ܬ�nogroup
12.��Jusermod -g nogroup nouser3���ܦ��b�������ݸs�աA�A��Jid nouser3�d�ݡA�i�o�{�ܬ�nogroup
13.��J mkdir srv�إߥؿ��A�A��Jcd srv�i�J�A�bsrv�ؿ��U��Jmkdir myproject�إߥؿ��C
14.��Jcd ..�h�^srv�A�A��Jcd ..�h�^~�A��Jchgrp mygroup srv�A�H�ο�Jchmod 770 srv�A���s�ժ��Ҧ��H�iŪ�i�g�i����A��L�H�h������A�b��Jls -l�A�i�o�{srv���s�թM�v���w���
15.��Jcd srv�i�J�ؿ��A�A��Jcdgrp mygroup myproject�A�M��Jchmod 770 myproject�A�A��Jls -l�d�ݥi�o�{�s�դw�ܧ�mygroup�B�v����drwxrwx---
16.��Jcd ~�h�^�h�A�A��Jsu myuser1�n�J�b��
17.��Jcd /srv/myproject�i�J�ؿ��A��Jvi myuser1.data�إ��ɮסA�L�|�n�A�s���ɮסA���UESC��h�X�A�ڭ쥻��J:wq���L�k�h�X�令:q�N�i�H�F�C
18.��Jcp /from/usr/bin/ls /to/usr/local/bin/myls�A�i�N�ؿ��q/usr/bin/ls�ƻs��/usr/local/bin/myls�A�[�W-R�Ѽƥi�ƻs�������e�C

1.�ڭ쥻��Jps -l�[��{�ǡA�����䤣��rsyslog�A��ӵo�{�n��Jps aux�~����A�]��ps -l�u���[���ۤv��process�A�n�ϥ�ps aux�~��ݨ�Ҧ���process�C
2.�@�}�l�ϧڥ�grep 'rsyslog' ps aux�A�Q��rsyslog�����G�A���L���䤣��s��aux���ɮסA�ҥH����o�˰��A�]���ڱNps aux�����G��X���@��txt�ɮסA�Ϋ��Ops aux > test.txt�A���ۨϥ�vi test.txt�A�[��test.txt�̪����e���T�Ops aux�����G�A�b���UESC�A��J:q�h�X�C
3.�ϥ�grep 'rsyslog' test.txt�A���G���\���d�ߤFrsyslog�����G�C�]���ڳ̫�ϥΫ��Ogrep 'rsyslog' test.txt > process_syslog.txt �N�d�ߪ����G��X�C

1.��Jfind /usr/bin -prem /7000 �i�d��/usr/bin�o�ӥؿ����t��SUID���S���ɮ��ɦW�A�䤤���@�ӥs��wall�C
2.��Jcd /usr/bin�i�J�ؿ��A�A��Jls -l wall�A�i�d���v����-r-xr-sr-x�A�X�{�Fs�A�i�ҩ��䬰SUID���S���ɮ��ɦW�C
3.���ۿ�Jfind /usr/bin -prem /7000 > /root/findsuidsgid.txt�A�N�ù������s�즹�ɮסC
4.��Jvi findsuidsgid.txt �s���ɮסA�i�o�{�w�s�bSUID���S���ɮ��ɦW�C
5.�~���Jfind /usr/sbin -prem /7000�A�d��/usr/sbin�o�ӥؿ����t��SUID���S���ɮ��ɦW�A�䤤���@�ӥs��postdrop�C
6.��Jcd /usr/sbin�i�J�A��Jls -l postdrop�d���v����-rwxr-sr-x�A�o�{��s�v���A�ҩ��䬰SUID���S���ɮ��ɦW�C
7.���ۿ�Jfind /usr/sbin -prem /7000 > /root/findsuidsgid.txt�A�N�����s�즹�ɮסC
8.��Jvi findsuidsgid.txt �s���ɮסA�i�o�{�S�W�[�FSUID���S���ɮ��ɦW�C


