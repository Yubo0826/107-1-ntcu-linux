## �b /etc/hosts �ɮסA�Ч�X<br>
### 1.���ɮת� inode ���X���X���H<br>
#### Ans:2107882<br>
### 2.�o�� inode �@���X���ɦW�b�ϥΡH<br>
#### Ans:1<br>
��"ls -ali (�ɦW)"���[��inode�X�Plink��<br>
![image](https://github.com/bill0330/107-1-ntcu-linux/blob/HW-5/ACS107137/img/1-1.png?raw=true)<br><br>

## �إ߹���s���A��l�ɮ׬� /etc/hosts �ӷs���ɮ��ɦW�� /srv/hosts.hard�A�Ч�X<br>
### 1./srv/hosts.hard�� inode ���X���X���H<br>
#### Ans:2107882<br>
### 2.�o�� inode �@���X���ɦW�b�ϥΡH<br>
#### Ans:2<br>
��"ln"�إ߹���s���A�å�"ll -i"�[��inode�X�Plink��(�]���ɮ��v�������Y�A�O�o������root)<br>
![image](https://github.com/bill0330/107-1-ntcu-linux/blob/HW-5/ACS107137/img/1-2.png?raw=true)<br>
### 3.������]<br>
#### ����s��(hard link)�O�b�Y�ӥؿ��U�s�W�@�Ӹ��ɮת����s��ƦӤw�A����ɦW�s����P�@��inode�X�A�ҥH�ɮ׳s���Ƭ�2<br>
#### �t�~�A���רϥέ��@���ɦW�ӽs��A���G���O�ۦP����!<br><br>

## �إ߲Ÿ��s���A��l�ɮ׬� /etc/hosts �ӷs���ɮ��ɦW�� /srv/hosts.soft�A�Ч�X<br>
### 1./srv/hosts.soft�� inode ���X���X���H<br>
#### Ans:6709889<br>
### 2.�o�� inode �@���X���ɦW�b�ϥΡH<br>
#### Ans:1<br>
��"ln -s"�إ߲Ÿ��s���A�å�"ll -i"�[��inode�X�Plink��<br>
![image](https://github.com/bill0330/107-1-ntcu-linux/blob/HW-5/ACS107137/img/1-3.png?raw=true)<br>
### 3.������]<br>
#### �Ÿ��s��(soft link)�O�إߤ@�ӿW�ߪ��ɮסA�ӳo���ɮ׷|����ƪ�Ū�����V�L link �������ɮפ��e<br>
#### �]���O�s���W���ɮסA�ҥH�|���@�ӷs��inode�X�A�ɮ׳s���Ƭ�1<br>
