#����s���ɮת��ظm�欰:

## 1.�b /etc/hosts �ɮסA�Ч�X

## (1)���ɮת� inode ���X���X���H
## �M��inode(��J ls -ail /etc/hosts)���̫e�����@�C�Ʀr�N�O�o���ɮת�inode����16796072
## (2)�o�� inode �@���X���ɦW�b�ϥΡH
## �i���v���᭱�ӼƦr�ݥX�u���@���ɦW�b�ϥ�
## 2.�إ߹���s���A��l�ɮ׬� /etc/hosts �ӷs���ɮ��ɦW�� /srv/hosts.hard�A�Ч�X
## (1)/srv/hosts.hard�� inode ���X���X���H
## �إ߹���s��(��J ln /etc/hosts /srv/hosts.hard)���i�J /srv(��J cd /srv)���d��hosts.hard��inode(��J ls -ail)�M���ɦW��hosts.hard��inode��1678194
## (2)�o�� inode �@���X���ɦW�b�ϥΡH
## �i���v���᭱�ӼƦr�ݥX������ɦW�b�ϥ�
## (3)������]
## �]���L�̨��O�P�@���ɮ�
##  3.�إ߲Ÿ��s���A��l�ɮ׬� /etc/hosts �ӷs���ɮ��ɦW�� /srv/hosts.soft�A�Ч�X
## (1)/srv/hosts.soft�� inode ���X���X���H
## �إ߲Ÿ��s��(��J ln -s /etc/hosts /srv/hosts.soft)���d��hosts.soft��inode(��J ls -ail /srv/hosts.soft)��inode��50777406
## (2)�o�� inode �@���X���ɦW�b�ϥΡH
## �i���v���᭱�ӼƦr�ݥX�u���@���ɦW�b�ϥ�
## (3)������]
## �]���o�O�@�ӿW�ߪ��ɮ�