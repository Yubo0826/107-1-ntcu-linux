# �Ĥ@�D

## 1. �b /etc/hosts �ɮסA�Ч�X���ɮת� inode ���X���X���H inode �@���X���ɦW�b�ϥΡH
* �H**ls -ali /etc/hosts**��ܥX/etc/hosts���ɮת��ԲӸ�� 
* �}�Y��7�Ӹ��X�Y��inode���X
* �v������ܤ��Ʀr�Y��inode�@���X���ɦW�b�ϥ�
* inode �� 4220520
* �@��1���ɦW�b�ϥ�
![](https://i.imgur.com/dvPogFl.png)

## 2. �إ߹���s���A��l�ɮ׬� /etc/hosts �ӷs���ɮ��ɦW�� /srv/hosts.hard�A�Ч�X/srv/hosts.hard�� inode ���X���X���H  �o�� inode �@���X���ɦW�b�ϥΡH �åB������]�C
* ���H**ln**�إ߳s���A��J**ln /etc/hosts /srv/hosts.hard**�إ߷s�s��
* �A�H**cd /srv**�i�J�Ӹ�Ƨ����A�H**ls -ali hosts.hard**��ܸ��ɮ׸ԲӸ��
* inode �� 4220520
* �@��2���ɦW�b�ϥ�
![](https://i.imgur.com/q9T0sed.png)
* **������]:** �]��l�ɮ׸g**ln**�إ߹���s����A�M��l���@�ɬۦPinode�ҳy��

## 3. �إ߲Ÿ��s���A��l�ɮ׬� /etc/hosts �ӷs���ɮ��ɦW�� /srv/hosts.soft�A�Ч�X/srv/hosts.soft�� inode ���X���X���H  �o�� inode �@���X���ɦW�b�ϥ�? �åB������]�C
* �H**ln -s /etc/hosts /srv/hosts.soft** ���إ߲Ÿ��s��
* �A��J**ls -ali hosts.hard** ��ܥX���ɮ׸��
* inode �� 6291536
* �@��1���ɦW�b�ϥ�
![](https://i.imgur.com/LjwSvld.png)
* **������]:**�ϥβŸ��s������ �إߪ��|�O�W�߳s�����ɮ� �]��inode�u�|��1��(�u���ۤv�b�ϥ�)