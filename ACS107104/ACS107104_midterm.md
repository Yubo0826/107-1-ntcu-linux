#�]�w ver �ܼơA���e���y my kernel version is 3.xx �z�A�䤤 3.xx �� uname -r ��X����T�A����ܥXver�ܼƪ��ȡC

  *uname -r��ver='my kernel version is 3.10'��echo $ver

#����ܥثePATH�����ܼƪ��Ȭ���A�û���PATH���\�ά���?

  *���:���ϡA�\��:�O���ڭ̥h�s���˦b�ܼƸ̭�����ơA�t�η|�ӵ�PATH���ҳ]�w�����|���ǡA�M��O�_���n�Ϊ����O

#���@���ɮת��ݩ��v���� drwxrwsr-x 3 root mail 4096 2�� 16 2017 mail/�A�л������ɮת��S�ʡC

  *���O�@���ɮסA�֦��̪��v�����iŪ�i�g�i����A�s�ժ��v�����iŪ�i�g�B����̦b���檺�L�{���N��o�ӵ{���s�ժ��v���A�֦��̬�root�A�s�լ�mail�A�ɮ׮e�q��4096�A�ɮ׳̫�@���Q�ק諸�ɶ���2017�~2��16��A�ɦW��mail/

#���]���@��script.sh�ɮת��v����-rw-r--r--�A�Y�Ʊ����Ҧ��H�i�H������ɮסA�аݸӦp��U�F���O�H�ШϥμƦr�k�P�Ÿ��k�U�ާ@�@���C
  
##�Ʀr�k

  *chmod 755 script.sh�Y�i�ק�

##�Ÿ��k

  *chmod u=rwx,g=r-x,o=r-x script.sh�Y�i�ק�

#��������s���P�Ÿ��s�����t���C

##�t��

  *�ϥγo�ӫ��O�]�w�s���ɮɡA�ϺЪ��Ŷ��Pinode�ƥؤ��|���ܡA�u�O�b�ؿ��̭��W�[�@��inode�P�ɦW�������A���Ÿ��s���O�b�إߤ@�ӿW�ߪ��ɮסA�o���ɮ׷|���V�ت��ɮסA����Ū���ɡA�|���V�Llink�������ɮצW�١A�]���L�O�W�߫إߪ��ɮסA�ҥH�|�e��inode��block

#�b�a�ؿ��U�إߤ@���ɦW�� hosts.real ������s������ /etc/hosts�H (�Хά۹���|��ܮa�ؿ�) 

  *ln /etc/hosts ~/hosts.real��ll -i /etc/hosts ~/hosts.real

#�b�a�ؿ��U�إߤ@���ɦW�� hosts.symbo ���Ÿ��s������ /etc/hosts�H (�Хά۹���|��ܮa�ؿ� 

  *ln -s /etc/hosts ~/hosts.symbo��ll -i /etc/hosts ~/hosts.symbo

#�إߤ@�Ӯe�q��1GB��xfs�ɮרt�ΡA�C���}��������۰ʪ������� /srv/maildir�A�B�ӥؿ��O�� mailgroup �o�Ӹs�զ@�Ϊ��A��L�H���i�㦳�����v���C�A�إߤ@�ӦW��mailuser���b���A�å[�J mailgroup �s�աA�B���b�����i�ϥ�shell�n�J�t�ΡC

  *�Х�`df`���O�t�X`human-readable`�ﶵ�A��ܦ�1GB���ɮרt�Υ�������`/srv/maildir`

  *����

  *�Х�`grep`���Ҧ��]�w�}���۰ʱ����C

  *����

  *�Х�`ls`�d��`/srv/maildir`�ݩʡA�T�{�i�H��`mailgroup`�s�զ@�ΡA�Ө�L�H��������v���C

  *����

  *�Х�`id`�ˬd`mailuser`�ϥΪ̦��b`mailgroup`. 

  *����
   
   �ڪ�mailuser1=mailuser

  *�Х�`grep`���Ҧ��b���L�k�z�Lshell�n�J�C

  *����