##1.
#�]�w ver �ܼơA���e���y my kernel version is 3.xx �z�A�䤤 3.xx �� uname -r ��X����T�A����ܥXver�ܼƪ��ȡC
*{{{ver="my kernel version is 3.10.0-862.e17.x86_64"}}}
*{{{echo $ver}}} +version is 3.10.0-862.e17.x86_64
*�ѦҹϤ�1
#����ܥثePATH�����ܼƪ��Ȭ���A�û���PATH���\�ά���?
*�ѦҹϤ�2
*{{{echo $PATH}}}
*PATH�\��:�����ɷj�M�����|�A�ؿ��P�ؿ������H�_��(:)���j�A �ѩ��ɮת��j�M�O�̧ǥ� PATH ���ܼƤ����ؿ��Ӭd�ߡC

##2.
#���@���ɮת��ݩ��v���� drwxrwsr-x 3 root mail 4096 2�� 16 2017 mail/�A�л������ɮת��S�ʡC
*+�ؿ��� +�֦��̥iŪ�i�g�i���� +�֦��s�եiŪ�i�g��SUID�v�� +�@��ϥΪ̥iŪ���i�g�i���� +�֦���root +�֦��s��mail +�ɮ׮e�q:4096
*���ɮ׳̫�@���Q�ק�/�׭q������ɶ�:2�� 16 2017 +�ɦW:mail/
#���]���@��script.sh�ɮת��v����-rw-r--r--�A�Y�Ʊ����Ҧ��H�i�H������ɮסA�аݸӦp��U�F���O�H�ШϥμƦr�k�P�Ÿ��k�U�ާ@�@���C
*{{{chmod 755 script.sh}}}
*{{{chmod u=rwx,g=r-x,o=r-x script.sh}}}

##3.
#��������s���P�Ÿ��s�����t���C
*����s��=>�إߤ@��inode�X�@�˪��ɮסA���ިϥέ����ɦW���i�H���� real ���� inode �hŪ����̲׸�ơA�p�G�N����@�ӡy�ɦW�z�R��
�A��� inode �P block ���٬O�s�b���I ���ɧA�i�H�z�L�t�@�ӡy�ɦW�z��Ū���쥿�T���ɮ׸�ơC���רϥέ��ӡy�ɦW�z�ӽs��A
�̲ת����G���|�g�J��ۦP�� inode �P block ���A�]������i���ƪ��ק�C
*�Ÿ��s��=>�إ߱��|�A�إߤ@�ӿW�ߪ��ɮסA�ӳo���ɮ׷|����ƪ�Ū�����V�Llink�������ɮת��ɦW�I
#�b�a�ؿ��U�إߤ@���ɦW�� hosts.real ������s������ /etc/hosts�H (�Хά۹���|��ܮa�ؿ�) 
*{{{cd ~[�ϥΪ̦W��]}}}
*{{{ln /etc/hosts /hosts.real}}}
#�b�a�ؿ��U�إߤ@���ɦW�� hosts.symbo ���Ÿ��s������ /etc/hosts�H (�Хά۹���|��ܮa�ؿ�)
*{{{cd ~[�ϥΪ̦W��]}}}
*{{{ln -s /etc/hosts /hosts.symho}}}