1.
--echo $var(�]�w�@�ӦW��var���ܼ�)
--var=my\ kernel\ version\ is\ $(uname -r)
--echo ${var}(�Y�i���var�ܼƤ��e����?)
##/usr/local/bin:/bin:/usr/local/sbin::/usr/sbin:/home/yizhen/ .local/bin:/home/yizhen/bin var
(�W�z���Ȼ����ϥ�$PATH�����ܼơA�i�H�j�M�����ɪ������|~�ؿ��P�ؿ������H�_���Ů�

2.-1drwxrwsr-x 3 root mail 4096 2�� 16 2017 mail/
A.drwxrwsr-x --�����v�����D�A�ݨ�e����d�^��r����ܫ᭱�ɦW�����Y��
�ϥΪ̥iŪ�i�g�i�ק�A�s�զ��ϥΨ�SGID�v���A�s�թҦ��H���iŪ�g�ק�A��L�H�iŪ�i���������g
B.2 --����ɮ׳s����
C.root --���ɮת��֦���
D.mail --���ɮש��ݪ��s��
E.4096 --���ɮת��e�q
F.2�� 16--���ɮ׳̫�@���Q�ק諸�ɶ����
G.�ɦW

2.-2
*�Ÿ����
--chmod u=rwx,g=rwx,o=rwx script.sh
*�Ʀr���
--chmod 777 script.sh

3.
**����s��--hardlink�b�Y�ؿ��U�s�W�@���ɦW�s����Yinode���X�����p�����A�������filesystem�M����link�ؿ�
**�Ÿ��s��--symbolic link--�b�إߤ@�ӿW�ߪ��ɮסA�ӳo���ɮ׷|����ƪ�Ū�����V�Llink�������ɮת��ɦW�A�ҥH��ӷ��ɮ׳Q�R���Asymbolic link���ɮ׷|�}���F
**����s��
--cd /home(cd�^��a�ؿ�)
--touch hosts.real(�إߤ@���ɮ�)
--cd/(cd�^��ڥؿ�)
--ln ~/hosts.real /etc/hosts(�إߤ@�ӹ���s��)
**�Ÿ��s��
--cd /home(cd�^��a�ؿ�)
--touch hosts.symbo(�إߤ@���ɮ�)
--cd/(cd�^��ڥؿ�)
--ln -s ~/host.symbo /etc/hosts(�إߤ@�ӲŸ��s��)

4.
����
