# midterm

## 1.

### �]�w ver �ܼơA���e���y my kernel version is 3.xx �z�A�䤤 3.xx �� uname -r ��X����T�A����ܥXver�ܼƪ��ȡC

-   ver="my kernel version is $(uname -r)"
-   echo $ver
-   ��ܥX�Ȭ�my kernel version is 3.10.0-862.e17.x86_64

### ����ܥثePATH�����ܼƪ��Ȭ���A�û���PATH���\�ά���?

-   ��echo $PATH��ܥX/usr/local/sbin:/usr/local/bin:/sbin:/bin:/usr/sbin:/usr/bin:/root/bin
-   PATH���\��O��PATH�ܼƤ����ؿ��d�߰����ɷj�M�����|

## 2.

### ���@���ɮת��ݩ��v���� drwxrwsr-x 3 root mail 4096 2�� 16 2017 mail/�A�л������ɮת��S�ʡC

-   drwxrwsr-x�N��᭱���ɦW�O�ؿ���,user�֦��v���Orwx,group�֦����v���]�Orwx,��other�b����ɦ]���x���v��,�gSGID�ᨭ���নgroup,�v���]�ܦ�rwx
-   3�O�ɮ׳s����
-   root�O�ɮ׾֦���
-   mail�O�ɮש��ݸs��
-   4096�O�ɮ׮e�q
-   2�� 16 2017�O�ɮ׳̫�@���Q�ק諸����ɶ�
-   mail/�O�ɦW

### ���]���@��script.sh�ɮת��v����-rw-r--r--�A�Y�Ʊ����Ҧ��H�i�H������ɮסA�аݸӦp��U�F���O�H�ШϥμƦr�k�P�Ÿ��k�U�ާ@�@���C

-   �Ʀr�k:chmod 755 script.sh
-   �Ÿ��k:chmod a+x script.sh

## 3.

### ��������s���P�Ÿ��s�����t���C

-   �ϥ�hard link��,�ϺЪŶ��Minode�ƥس����|����
-   �ϥ�symbolic link��,�|�إߤ@�ӿW�ߪ��ɮרåe��inode�Mblock

### �b�a�ؿ��U�إߤ@���ɦW�� hosts.real ������s������ /etc/hosts�H (�Хά۹���|��ܮa�ؿ�) 

-   ln /etc/hosts ~/hosts.real

### �b�a�ؿ��U�إߤ@���ɦW�� hosts.symbo ���Ÿ��s������ /etc/hosts�H (�Хά۹���|��ܮa�ؿ�)

-   ln -s /etc/hosts ~/hosts.symbo

## 4.

### �إߤ@�Ӯe�q��1GB��xfs�ɮרt�ΡA�C���}��������۰ʪ������� /srv/maildir�A�B�ӥؿ��O�� mailgroup �o�Ӹs�զ@�Ϊ��A��L�H���i�㦳�����v���C�A�إߤ@�ӦW��mailuser���b���A�å[�J mailgroup �s�աA�B���b�����i�ϥ�shell�n�J�t�ΡC


#### �Х�`df`���O�t�X`human-readable`�ﶵ�A��ܦ�1GB���ɮרt�Υ�������`/srv/maildir`

> ![github](https://github.com/JackyBigNose/107-1-ntcu-linux/blob/midterm/ACS107150/1.PNG?raw=true)

#### �Х�`grep`���Ҧ��]�w�}���۰ʱ����C

> ![github](https://github.com/JackyBigNose/107-1-ntcu-linux/blob/midterm/ACS107150/2.PNG?raw=true)

#### �Х�`ls`�d��`/srv/maildir`�ݩʡA�T�{�i�H��`mailgroup`�s�զ@�ΡA�Ө�L�H��������v���C

> ![github](https://github.com/JackyBigNose/107-1-ntcu-linux/blob/midterm/ACS107150/3.PNG?raw=true)

#### �Х�`id`�ˬd`mailuser`�ϥΪ̦��b`mailgroup`.

> ![github](https://github.com/JackyBigNose/107-1-ntcu-linux/blob/midterm/ACS107150/4.PNG?raw=true)

#### �Х�`grep`���Ҧ��b���L�k�z�Lshell�n�J�C




