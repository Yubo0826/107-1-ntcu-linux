****����s���ɮת��ظm�欰
1.�b/etc/hosts�ɮסA�Ч�X
#���ɮת� inode ���X���X���H
--ls -ali /etc/hosts
��16809512 -rw-r--r-- 1 root root 158 Jun 7 2013 /etc/hosts
#�o�� inode �@���X���ɦW�b�ϥΡH
�q�v���᭱���D��1���ɦW�b�ϥ�

****�إ߹���s���A��l�ɮ׬� /etc/hosts �ӷs���ɮ��ɦW�� /srv/hosts.hard�A�Ч�X
#/srv/hosts.hard�� inode ���X���X���H
--ln /etc/hosts /srv/hosts.hard
--cd /srv
--ls
��hosts.hard
--ls -ali hosts.hard
��16809512 -rw-r--r-- 2 root root 158 Jun 7 2013 hosts.hard
--ls -ld hosts.hard
�ؿ�������䥴�׹�����P��inode���X�ҥH��2�ӦW�٦b�ϥ�
****�إ߲Ÿ��s���A��l�ɮ׬� /etc/hosts �ӷs���ɮ��ɦW�� /srv/hosts.soft�A�Ч�X
#/srv/hosts.soft�� inode ���X���X���H
--ln -s /etc/hosts /srv/hosts.soft
--ls -ali /srv/host.soft
��16809512 -rw-r--r-- 3 root root 158 Jun 7 2013 /srv/host.soft
�]���s�إ��ɮשҥHŪ���ɪ���Ū����ơAinode�����X�u���@���ɮצb�ϥ�