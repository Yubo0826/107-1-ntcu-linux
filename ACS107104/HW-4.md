#�޲z�s�զ@�θ�ƪ��v���]�p
##�إ߸s��
###�n�Jroot
###�إ߸s��(��Jgroupadd mygroup,nogroup)
##�إ߱b���å[�J�s��
###�إ߱b���å[�J�s��(��Juseradd -G �s�զW�� �ϥΪ̦W��)����K�X(��Jpasswd �ϥΪ̦W��)
##�إߤ@�ӦW�� /srv/myproject ���ؿ��A�o�ӥؿ��i�H�� mygroup �s�դ����ϥΪ̧���ϥΡA�B�i�s�ت��ɮ׾֦��s�աj�� mygroup �C���L��L�H���঳�����v��
###�إߥؿ�(��Jmkdir �ؿ��W��)��chgrp mygroup �ɮצW�١�chmod u=rwx,g=rwx,o= �ɮצW�١��ˬd���L���\ls -l��end
##�Ȯɤ������� myuser1 �������A�ëe�� /srv/myproject �ؿ��A���իإߤ@�ӦW�� myuser1.data ���ɮסA����n�X myuser1�C
###����myuser1(��Jsu myuser1)���i�J/srv/myproject(��Jcd /srv/myproject)���إ��ɮ�(vi myuser1.data)����esc��:wq���n�Xmyuser1(��Jsu root)����J�K�X��end
##�ƻs/usr/bin/ls��/usr/local/bin/myls
###�ƻscp /usr/bin/ls /usr/local/bin/myls���d�ݦ��L���\(��Jll /usr/local/bin/myls)��end
###���M nogroup �s�դ����Τ��� /srv/myproject ���ӨS�������v���A���� nogroup �����Τ���� /usr/local/bin/myls �ɡA�i�H���ͻP ls �ۦP����T�A�B�Ȯɾ֦� mygroup �s�ժ��v���A�]���i�H�d�ߨ� /srv/myproject �ؿ������ɦW��T�C �]�N�O���A��A�ϥ� nouser1 ����������imyls /srv/myproject�j�ɡA���ӬO����d�\��ӥؿ������ɦW��T�C
####��Jchgrp mygroup �ɮצW�١��n�Jnouser1���նi�J/srv/myproject�����G�L�k�A�]���S���v�����^��root(��Jsu root)����J�K�X������ɮ��v��(��Jsudo chmod u+s �ɮצW��)���d�ݦ��L���\(��Jll �ɮצW��)������nouser1(��Jsu nouser1)�����նi�J/srv/myproject�����G���\
##�ϥε{���[����O�A�f�t grep ������r�d�ߥ\��A�N��쪺 rsyslog �������{�Ǫ� PID, PRI, NI, COMMAND ����T��s�� /root/process_syslog.txt �ɮפ��C(�f�t>���ɦV��X)
###�^��root���d�߸ԲӸ��(��Jps aux | grep rsyslog)���x�s(��Jps aux | grep rsyslog> /root/process_syslog.txt)���d�ݦ��L���\(��Jvi process_syslog.txt)��end
##�ϥ� find ��X /usr/bin �� /usr/sbin ��ӥؿ����A�t�� SUID ���S���ɮ��ɦW�A�èϥ� ls -l �h�C�X��쪺�ɮת������v����A�N�ù������s�� /root/findsuidsgid.txt �ɮפ��C(�ۦ�d��find���O�Ϊk�A�H�Ψϳz�L���ɦV�Ÿ�>��X�ɮ�)
###find /usr/bin /usr/sbin -perm /4000 -exec ls -l {} \;
####*perm:��X�S���v�����ɮ�
####*4000:�]��SUID�O�|��
####*{}:��ܪ��O��find��쪺���e
####*-exec��\;�O����r�A-exec�O�}�l�A\;�O����
####*�]��;�bbash���Ҥ��O���N�q���A�ҥH�[\�Ӹ���
###�����x�s(��Jfind /usr/bin /usr/sbin -perm /4000 -exec ls -l {} \;> /root/findsuidsgid.txt)���d�ݦ��L���\(��Jvi findsuidsgid.txt)��end
 