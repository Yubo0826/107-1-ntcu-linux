# HW-4



# �Ĥ@�D



### �Ĥ@�B



![1.1](https://images2.imgbox.com/70/49/jiKEyPxN_o.png)



>�����n�إߨ�Ӹs�աA�Q��**groupadd**�����O�إߡA�èϥ�**grep group /etc/group**�Ӭd�ݬO�_���\�إߡC



![1.2](https://images2.imgbox.com/08/b0/yV817Reb_o.png)



>�ϥΫ��O**useradd**�ӫإߤ��ӨϥΪ̡A�å[�W **-g** ���Ѽƨӫ��w�U�ӨϥΪ̪�initial group�C



![1.3](https://images2.imgbox.com/3f/12/Uxzo7sO7_o.png)



>�M**HW-3**���ɭԤ@�ˡA�ϥ�**echo password | passwd --stdin username**�����O�]�m�K�X�A�������O�ԲӦb**HW-3**�w�g�y�L���L�A�ҥH���A�ԭz�@���F�C



![1.4](https://images2.imgbox.com/55/7d/62QhEUBI_o.png)



>�ϥΫ��O**mkdir**�إߥؿ��÷f�t **-m** ���ѼƳ]�w�U���v���A�A�ϥ�**chgrp**�����O�ܧ�֦��s�աA�̫�ϥ�**ll**���O�ˬd�ɮ��ݩʡC



### �ĤG�B



![1.5](https://images2.imgbox.com/6d/dc/eTKbWiov_o.png)



>�ϥ�**su**���O������myuser1���ϥΪ̡A�Q��**cd**�i�J�ؿ�/srv/myproject�èϥ�**touch**���O�إ�myuser1.data�ɮסA�A�����^root�A�M��ϥ�**cp**�N/usr/bin/ls�����e�ƻs�@����/usr/local/bin/myls�C



![1.6](https://images2.imgbox.com/0c/7d/79rRwQYu_o.png)



>�����^root�A���ϥ�**ll**�ˬd�ɮ��ݩʡA�A��**chmod**����ɮ��ݩʡC�䤤�A�ھ�**HW-3**�ҾǨ쪺�A�ڭ̪��D**��T�X**���֦��̡B�֦��s�աB��L�H��rwx�v���A��**�T�X�e��**�A�[**�@�X**�i�H���w�ɮת��ݩʦ�**SUID�BSGID�BSBIT**���ݩʡA**SUID=4**�B**SGID=2**�B**SBIT=1**�A�̫��**ll**�ˬd�ϥΪ̪�**x**�O�_�ܦ�**s**�C



![1.7](https://images2.imgbox.com/69/1d/ZnFPgb41_o.png)



>�����ϥΪ̬�nouser1�A����/srv/myproject�A�åB�T�{���i���檺�C



# �ĤG�D



![2.1](https://images2.imgbox.com/7f/e5/XC5r0NUV_o.png)



>�ϥΫ��O**ps aux**�C�X�Ҧ����{�ǡA�A�f�t **|** �M **grep**�N��**rsyslog**����r���{�ǧ�X�ӡC


>�T�{��A�N�쥻�����O�[�W **>** �����O�H���s�ɦV����� **(�����O���إ߷s�����л\)** �A�̫�Q��**cat**���O�T�{�ɮפ��e�C



# �ĤT�D



![3.1](https://images2.imgbox.com/54/be/r0jD4T0j_o.png)



>�Q��**find**���O�j�M��ƨ÷f�t **-prem** ���Ѽƨ��ǥѫ��w�ɮ��v�����覡�j�M�A�]���n�j�M���O**�Ҧ��֦�SUID�ݩʪ��ɮ�**�A�]���f�t **-prem /u=s** �����O�ӷj�M��ӥؿ��C



![3.2](https://images2.imgbox.com/c8/fb/BSMRCXwg_o.png)



>���O������: **find  �ɮ�  �M��覡���Ѽ�  ���ѴM�䪺���  -exec/-ok  ��������O  {} \\;**



>���U�Өϥ�**find**���Ѽ� **-exec** �M **-ok** �A���ϥΪ̥i�H���쪺�ɮשΥؿ�����S�w�����O�A�� **{ }** �]�۩ҧ�쪺��ơA**\\;** �Ψӧ����ʧ@�C�䤤 **-exec** �M **-ok** ���t�O��: **-ok** �|�n�D�ϥΪ̤@���@���T�{�A�� **-exec** �h�_�C�ӧڭ̧Ʊ����**ls -l**�����O�åB���s�ɦV�S�w�ɮסC



>��X�_�ӡA�Ĥ@���ϥ� **find /usr/bin -perm /u=s -ok ls -l > findsuidsgid.txt {} \\;** �����O�A�@���@���T�{�ᱵ�۲ĤG���C�ĤG���ϥ� **find /usr/bin -perm /u=s -ok ls -l 1>> findsuidsgid.txt {} \\;**�����O�A�t���b��N **>** ��אּ **1>>** �����s�ɦV�覡�C



> **>** �M **1>>** ���t�O��: **>** ���إߩ��л\�A�� **1>>** ���л\�β֥[�A�ڭ̧Ʊ��ӳ��s�b�A�ҥH�ϥβ֥[�C



![3.3](https://images2.imgbox.com/04/21/aQzVjcJw_o.png)



>�̫�ϥ�**cat**���O�ˬd�ɮפ��e�C


