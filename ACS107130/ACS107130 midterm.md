# 1.
## �]�w ver �ܼơA���e���y my kernel version is 3.xx �z�A�䤤 3.xx �� uname -r ��X����T�A����ܥXver�ܼƪ��ȡC
### export ver="my kernel version is 3.10.0-862.e17.x86_64"
### echo $ver
### my kernel version is 3.10.0-862.e17.x86_64
## ����ܥثePATH�����ܼƪ��Ȭ���A�û���PATH���\�ά���?
### echo $PATH
### �b����@�ӫ��O���ɭԡA�t�η|�̷�PATH���]�w�h�C��PATH�w�q�����|�U�j�M�ɮסA���j�M�쪺���O�ɮץ��Q����C
# 2.
## ���@���ɮת��ݩ��v���� drwxrwsr-x 3 root mail 4096 2�� 16 2017 mail/�A�л������ɮת��S�ʡC
### ���ɮ׾֦��̤θs�զ����v���Ҭ��iŪ�i�g�i����A�Ө�L�H�u��Ū�����C
## ���]���@��script.sh�ɮת��v����-rw-r--r--�A�Y�Ʊ����Ҧ��H�i�H������ɮסA�аݸӦp��U�F���O�H�ШϥμƦr�k�P�Ÿ��k�U�ާ@�@���C
### chmod 777 /script.sh
### chmod a=rwx /script.sh
# 3.
## ��������s���P�Ÿ��s�����t���C
### ����s���O�H�h���ɮ׹�����P�@��inode���覡�إߪ��s���A�ӲŸ��s���|�e�Υt�@��inode��Ŷ��C
## �b�a�ؿ��U�إߤ@���ɦW�� hosts.real ������s������ /etc/hosts�H (�Хά۹���|��ܮa�ؿ�)
### ln ./etc/hosts /hosts.real
## �b�a�ؿ��U�إߤ@���ɦW�� hosts.symbo ���Ÿ��s������ /etc/hosts�H (�Хά۹���|��ܮa�ؿ�)
### ln ./etc/hosts /hosts.symbo
# 4.�Ш̤U�z���ҧ����t�ξާ@��A�ά������O�i�����ҡA�Ч����ҫ��O���ϡG
    �إߤ@�Ӯe�q��1GB��xfs�ɮרt�ΡA�C���}��������۰ʪ������� /srv/maildir�A�B�ӥؿ��O�� mailgroup �o�Ӹs�զ@�Ϊ��A��L�H���i�㦳�����v���C�A�إߤ@�ӦW��mailuser���b���A�å[�J mailgroup �s�աA�B���b�����i�ϥ�shell�n�J�t�ΡC
### 