## 1.<br>
### (Q1): �]�w ver �ܼơA���e���y my kernel version is 3.xx �z�A�䤤 3.xx �� uname -r ��X����T�A����ܥXver�ܼƪ��ȡC(10%)<br>
Ans:<br>
1.���O:" uname -r "�[����X����T( 3.xx ) <br>
2.���O:" ver= my kernel version is 3.xx "(�ܼ�='�ܼƤ��e')�A�]�wver�ܼơC <br>
3.���O:" echo $ver "��� ver �ܼƪ���<br><br>

### (Q2):����ܥثePATH�����ܼƪ��Ȭ���A�û���PATH���\�ά���? (10%)<br>
Ans:<br>
���O:" echo $PATH " (�`�N"PATH"�����Ҭ��j�g!) ��ܥثePATH�����ܼƪ��ȡC<br>
����: �����ܼ�" PATH "�������ɷj�M�����|~�ؿ��P�ؿ������H�_��(:)���j�A�ѩ������/���O���j�M�O�̧ǥ� PATH ���ܼƤ����ؿ��Ӭd�ߡA�ҥH�A�ؿ������Ǥ]�O���n���C<br><br>

## 2.<br>
### (Q1):���@���ɮת��ݩ��v���� drwxrwsr-x 3 root mail 4096 2�� 16 2017 mail/�A�л������ɮת��S�ʡC(10%)<br><br>
Ans:<br>
���ɮת��֦��̬�' root '�A�s�ճ]�w��' mail '�C<br><br>
�̫e��'d'�N�����ɦW���ؿ��ɡC<br>
������" 'rwx''rws''r-x' "�H�C3�Ӭ��@�աA�ѥ��ӥk���O���֦���(root)�B�s��(mail)�B��L�H(�Droot�B�Dmail)���v���A�䤤:<br>
' r '�N��\Ū�v���A<br>
' w '�N��ק��v���A<br>
' x '�N������v���A<br>
' s '�N��" SUID "�A�b���D�N��u�n����H�֦�x���v���A��Τ����o���ɮ׮ɡA�N�|�۰ʳz�L SUID �ഫ�������� group ���@���A��Y�ܦ��F �s��' mail '���@���C (���Mother���v���u�� r �P x �A���O��other���榹�ɮ׮ɷ|�۰��ഫ���֦��s�� mail �������A�ҥH���ɴN�Ȯɾ֦��F w ���v���C)<br><br>
���ɮת��e�q��4096(bits)�C
���ɮת��̫�׭ק�ɶ���2017 2�� 16��C<br>
���ɮת��ɦW��mail�C<br><br>

### (Q2):���]���@��script.sh�ɮת��v����-rw-r--r--�A�Y�Ʊ����Ҧ��H�i�H������ɮסA�аݸӦp��U�F���O�H�ШϥμƦr�k�P�Ÿ��k�U�ާ@�@���C(10%)<br><br>
Ans:<br>
�Ʀr�k:" chmod 755 script.sh " ( r=4 , w= 2 , x=1 )<br>
�Ÿ��k:" chmod u=rwx, g=rx, o=rx script.sh "  (u= user, g= group, o= other)<br><br>

## 3.<br>
### (Q1):��������s���P�Ÿ��s�����t���C(10%)<br>
Ans: <br>
" Hard Link "�O��@���ɮ׷s�W�X�@�Ӥ��P���ɦW�A���O�o2�Ӥ��P���ɦW�Ҷ}�Ҫ��O�P�@���ɮסA�ҥH�L�̪�inode�|�O�ۦP��(���P�@�ɮ�)�C<br>
" Symbolic Link "�O�إߤ@�ӷs�ɮװ����t�@���ɮ׶}�Ҫ����|�A2�̬����P���ɮסA�ҥH�۵Minode�N���|�ۦP(�����P�ɮ�)�C<br><br>

### (Q2):�b�a�ؿ��U�إߤ@���ɦW�� hosts.real ������s������ /etc/hosts�H (�Хά۹���|��ܮa�ؿ�) (5%)<br>
Ans; <br>
�Ϋ��O"ln"�ӫإ߹���s��(�o�̷|���o�{�@��ϥΪ̷|�����v�����������D�A�ҥH��������ϥΪ̤�����root�A�Ӷi��)<br>
���O:" In /etc/hosts /home/hosts.real "<br>

### (Q3):�b�a�ؿ��U�إߤ@���ɦW�� hosts.symbo ���Ÿ��s������ /etc/hosts�H (�Хά۹���|��ܮa�ؿ� (5%)<br>
Ans:<br>
�� ln -s ���O�ӫإ߲Ÿ��s��(Symbolic Link) (�n������root)<br>
���O:"�@In -s /etc/hosts /home/hosts.symbo "<br><br>

## 4.<br>
### (Q1):�Х�`df`���O�t�X`human-readable`�ﶵ�A��ܦ�1GB���ɮרt�Υ�������`/srv/maildir` (8%)<br>
Ans:<br>
human-readable�ﶵ:"-h"<br>
![image](https://github.com/ACS107135/107-1-ntcu-linux/blob/midterm/ACS107135/photo/1.PNG)<br>

### (Q2):�Х�`grep`���Ҧ��]�w�}���۰ʱ����C(8%)<br>
Ans:<br>
![image](https://github.com/ACS107135/107-1-ntcu-linux/blob/midterm/ACS107135/photo/2.PNG)<br>
### (Q3):�Х�`ls`�d��`/srv/maildir`�ݩʡA�T�{�i�H��`mailgroup`�s�զ@�ΡA�Ө�L�H��������v���C(8%)<br>
Ans:<br>
![image](https://github.com/ACS107135/107-1-ntcu-linux/blob/midterm/ACS107135/photo/3.PNG)<br>



