1.
(1)
version=$(uname -r)
ver="my kernel version is $version"
echo $ver
(2)
echo $PATH
�����ɷj�M�����|

2.
(1)
�ɦW���ؿ���
�֦��̬�:root
�֦��s�լO:mail
�e�q:4096
�̫�@���Q�ק�/�׭q������ɶ�:2��16��2017�~
�ɦW:mail
�ɮ׳s����:3
user:�iŪ�g����
group:�iŪ�g����
others:�iŪ���i�g�i����
(2)
chmod 755 script
chmod u=rwx,g=rx,o=rx script

3.
(1)
Hard Link ����s��:
�C���ɮ׳��|���Τ@�� inode �A�ɮפ��e�� inode ���O���ӫ��V�F
Ū�����ɮסA�����n�g�L�ؿ��O�����ɦW�ӫ��V�쥿�T�� inode ���X�~��Ū���C
Symbolic Link �Ÿ��s��:
�إߤ@�ӿW�ߪ��ɮסA�ӳo���ɮ׷|����ƪ�Ū�����V�Llink�������ɮת��ɦW
�|���α� inode �P block
(2)
ln /etc/hosts ~/hosts.real
(3)
ln -s /etc/hosts ~/hosts.symbo

4.
fdisk /dev/sda
n
p
1
1048576
3145728
w






