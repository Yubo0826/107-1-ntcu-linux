1.

�]�w ver �ܼơA���e���y my kernel version is 3.xx �z�A�䤤 3.xx �� uname -r ��X����T�A����ܥXver�ܼƪ��ȡC

>> 1.��������Juname -r �Ӭd�ݸ�T��3.10.0-862.e17.x86_64

>> 2.����n�]�wver�o���ܼơA��Jver="my kernel version is 3.10"�A�n�[�W�޸��]���r�������ťղŸ�

>> 3.���ۿ�Jecho $ver �Ӭd�ݬO�_��令�\�A�i�o�{�w��ܬ�my kernel version is 3.10

����ܥثePATH�����ܼƪ��Ȭ���A�û���PATH���\�ά���?

>> 1.��Jecho $PATH�٬d�������ܼƪ��Ȭ�/usr/local/sbin:usr/local/bin:/sbin:/bin:/usr/sbin:/usr/bin:/root/bin

>> 2.�����ܼ�PATH���\�άO�����ɷj�M�����|�A�����ɩΫ��O���j�M�O�̧�PATH�������ܼƤ����ؿ��Ӭd�ߪ�

2.

���@���ɮת��ݩ��v���� drwxrwsr-x 3 root mail 4096 2�� 16 2017 mail/�A�л������ɮת��S��?

>> ���D�ؤ����v���i�o�����ɮרϥΪ̬��yroot�z���v�����y�iŪ�i�g�i����z�A�h���ݸs�լ��ymail�z�v���]���y�iŪ�i�g�i����z�A�yothers�z�h���y�iŪ�i��������i�g�z

���]���@��script.sh�ɮת��v����-rw-r--r--�A�Y�Ʊ����Ҧ��H�i�H������ɮסA�аݸӦp��U�F���O�H�ШϥμƦr�k�P�Ÿ��k�U�ާ@�@���C

>> 1.�Ʀr�k : ��Jchmod 777 script.sh �A�i�N���ɮת��Ҧ��H���v���אּ�y�iŪ�i�g�i����z�A�y4�z�N��iŪ�A�y2�z�N��i�g�J�A�y1�z�N��i����

>> 2.�Ÿ��k : ��Jchmod u=rwx,g=rwx,o=rwx script.sh�A�i�N���ɮת��Ҧ��H���v���אּ�y�iŪ�i�g�i����z�A�yu�z�N��ϥΪ��v���A�yg�z�N��s���v���A�yo�z�N��others���v��

3.

��������s���P�Ÿ��s�����t���C

>> �y�Ÿ��s���z�|�إߤ@�ӿW���ɮשMinode�A�B�s�إߪ��ɮ׷|Ū���쥻�ɮת��ɦW

>>�y����s���z�Φh���ɮ׹��@��inode�ӫإߡA�ɦW�u�P�ؿ������A���ɮפ��e�P inode ����

�b�a�ؿ��U�إߤ@���ɦW�� hosts.real ������s������ /etc/hosts�H

>> 1.������J vi ~/hosts.real �إߤ@���ɮסA�����ESC��A�h�X�s��A��J :wq ���}

>> 2.��Jln hosts.real ./etc/hosts�ӫإ߹���s��

�b�a�ؿ��U�إߤ@���ɦW�� hosts.symbo ���Ÿ��s������ /etc/hosts

>> 1.��J vi ~/hosts.symbo �إߤ@���ɮסA�����ESC��A�h�X�s��A��J :wq ���}

>> 2.��Jln -s hosts.symbo ./etc/hosts�ӫإ߲Ÿ��s��

4.

�Ш̤U�z���ҧ����t�ξާ@��A�ά������O�i�����ҡA�Ч����ҫ��O���ϡG

�إߤ@�Ӯe�q��1GB��xfs�ɮרt�ΡA�C���}��������۰ʪ������� /srv/maildir�A�B�ӥؿ��O�� mailgroup �o�Ӹs�զ@�Ϊ��A��L�H���i�㦳�����v���C�A�إߤ@�ӦW��mailuser���b���A�å[�J mailgroup �s�աA�B���b�����i�ϥ�shell�n�J�t�ΡC
