1.
(1).
ver="my kernel version is 3.10.0-862.e17.x86_64"
echo $ver
echo ${ver}

(2).
PATH=/myhome/bin:$PATH
��ڭ̦b����@�ӫ��O�ɡA�t�η|�̷�PATH���]�w�h�C��PATH�w�q�����|�U�j�M�ɮסA���j�M�쪺������A�p�G�ӫ��O�L�k����b�o�Ӹ��|�L�k����A�N��Ӹ��|�������ܼƨS���ӥO�C

2.
(1).
�o�O�@�ӦW��mail����Ƨ��Aroot ���v���iŪ�i�g�i����Agroup���v���iŪ�i�g�i����A�Ө�L�H���v���iŪ�i���椣�i�g�A�o���ɮת��s���Ƭ�2�Aroot �O�o���ɮת��֦��̡A�o���ɮש��ݩ�mail�o�Ӹs�աA���ɮפj�p��4096�A�̫�@���Q�׵����ɶ���2017/2/16�C
(2).
�p�G�H�Ʀr�e�{:
�i�H�ϥ�(chmod XXX script.sh) �Ĥ@��x��root���v���A�ĤG��x�����ɮש��ݸs�ժ��v���A��3��x����L�H���v���A�p�G�n����L�H�i�g�i����Nx�אּ7�A�iŪ�i���椣�i�g�אּ5�A�i�g�i���椣�iŪ�אּ3�A�u�i����אּ1�C
�p�G�H�Ÿ��e�{:
�i�H�ϥ� (chmod u=rwx,g=rwx,o= �ɦW) �e���N����w��H(o�N���L�H�Ar�N��root�Ag�N��group�Aa�N�����)�A�᭱��ܫ��w�v��(x�N�����Ar�N��Ū�Aw�N��g�A�S�g�N���򤣦氵)�C
3.(1).
����s��(hard link):
����s�����C���ɮ׷|�e�Τ@��inode�A�ɮפ��e��inode�������ӫ��V�C
�Q�nŪ�����ɮסA�����n�g�L�ؿ��������ɦW�ӫ��V���T��inode�~�i����C
�h���ɦW�i�H����1��inode�C
�ϥ�hard link�]�w�s���ɮɡA�ϺлPinode�A���ƥؤ��|���ܡC
�N����@���ɦW�R���Ainode�Mblock���M�s�b�C
���ץέ����ɦW�s��A�̲׳��|�g�J�ۦP��inode�Mblock�C

�Ÿ��s��(soft link):
soft link�O�إߤ@�ӿW�ߪ��ɮסA�L�|���V�ت��ɮסA����Ū���ɥL�|���V��link���ɮסC
soft link���W�ߪ��s�ɮסA�|�e��inode�Mblock�C
��ت��ɮ׳Q�R���Alink�|�ܦ���link�A�L�k�A�}�Ҹ��ɮסC
(2).
ll -i /etc/hosts
ln /etc/hosts .
ll -i/etc/hosts hosts.real
(3).
ll -s /erc/hosts hosts.symbo
ll -i /etc/hosts /root/hosts.symbo
4.
(1).
mount /dev/vda1 /sev/maildir
vim /etc/fstab
mount -a
swapon -a
df -T /dev/sda2
swapon -s
(2).

(3).
cd /srv
mkdir maildir
ll
chgrp mailgroup
chmod o= maildir
![](https://i.imgur.com/uCDgybl.png)

(4).
useradd mailuser
id mailuser
usermod -a -G mialgroup mailuser
![](https://i.imgur.com/AFV909b.png)
(5).