## 1-1.�]�w ver �ܼơA���e���y my kernel version is 3.xx �z�A�䤤 3.xx �� uname -r ��X����T�A����ܥXver�ܼƪ��ȡC<br>
### Ans:<br>
![image](https://github.com/percy890713/107-1-ntcu-linux/blob/midterm/ACS107145/exam1-1.PNG)<br>
## 1-2.����ܥثePATH�����ܼƪ��Ȭ���A�û���PATH���\�ά���?
### Ans:<br>
![image](https://github.com/percy890713/107-1-ntcu-linux/blob/midterm/ACS107145/exam1-2.PNG)<br>
###�N�O�����ɷj�M�����|�ա�ؿ��P�ؿ������H�_��(:)���j�A �ѩ��ɮת��j�M�O�̧ǥ� PATH ���ܼƤ����ؿ��Ӭd�ߡA�ҥH�A�ؿ������Ǥ]�O���n����C<br>
## 2-1.���@���ɮת��ݩ��v���� drwxrwsr-x 3 root mail 4096 2�� 16 2017 mail/�A�л������ɮת��S�ʡC<br>
### Ans:���ɦWmail/,�ؿ���(d).�ϥΪ�(root)�v�����iŪ�i�g�i����.�þ֦�SGID���S�O�v��.��L�H���iŪ�i����.�ɮ׳s���Ƭ�3,�ɮ׮e�q4096,�̫�@���ק�ɶ���2017/2/16<br>
## 2-2.���]���@��script.sh�ɮת��v����-rw-r--r--�A�Y�Ʊ����Ҧ��H�i�H������ɮסA�аݸӦp��U�F���O�H�ШϥμƦr�k�P�Ÿ��k�U�ާ@�@���C<br>
### Ans:�Ʀr�k:chmod 755 script.sh<br>  
### Ans:�Ÿ��k:chmod a+x script.sh<br>
## 3-1.��������s���P�Ÿ��s�����t���C<br>
### Ans:�Ÿ��s��:�@�جO���� Windows �����|�\�઺�ɮסA�i�H���A�ֳt���s����ؼ��ɮ�(�Υؿ�)�F ����s��:�O�z�L�ɮרt�Ϊ� inode �s���Ӳ��ͷs�ɦW�A�Ӥ��O���ͷs�ɮ�<br>
## 3-2.�b�a�ؿ��U�إߤ@���ɦW�� hosts.real ������s������ /etc/hosts�H<br>
### Ans:cd ~percy -> touch hosts.real -> ln ~percy/hosts.real /etc/hosts -> ll -i ~percy/hosts.real /etc/hosts<br>
## 3-3.�b�a�ؿ��U�إߤ@���ɦW�� hosts.symbo ���Ÿ��s������ /etc/hosts�H<br>
### Ans:cd ~percy -> touch hosts.symbo -> ln -s ~percy/hosts.symbo /etc/hosts -> ll -i ~percy/hosts.symbo /etc/hosts<br>