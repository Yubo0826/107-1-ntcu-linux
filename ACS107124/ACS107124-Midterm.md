�@.
1.https://ppt.cc/fl08qx

2.PATH��²���I�N�O�@�Ӧr���ܼơA���J�R�O���ɭ�LINUX�|�h�d��PATH�̭��O�������|�C
   �Ӱ����ɷj�M�����|�A�ؿ��ؿ����|�H�_�����j

�G.
1.
    drwxrwsr-x 3 �����O���ɮצ�3�ӳs���A�ɮת��֦��̬�root�A�M����ݸs�լ�mail�A
    �ɮפj�p��4096 bytes�A�̫᪺�ק�ɶ���2017�~2��16��A�̫�L���ɦW��mail�C

2.
(1)�Ʀr:����Jls -al script.sh�A�M��A��Jchmod [-R] 755
(2)�Ÿ�: ��J chmod u+x,g+x,o+x script.sh



�T.

1.
(1)����s�����C�Ӥ�󳣷|���@��inode�ӰO����󤺮e��block���X�A�Q�nŪ���@�Ӥ��A
�����n�q�L�ؿ��O�������W�ӫ��V�Ӥ�󥿽T��inode���X

(2)�ӲŸ��s���b�Ыؤ@�ӿW�ߪ����A�ӳo�Ӥ��|���ƾڪ�Ū�����V�L link �����Ӥ�󪺤��W�I
�ѩ�u�O�Q�Τ��Ӱ������V���ʧ@�A �ҥH�A��ӷ����Q�R������Asymbolic link 
�����|�u�}���F�v�A �|�@�����u�L�k���}�Y���I�v�C��ڤW�N�O�䤣���l�u���W�v�Ӥw

(3)�]�N�O������s���۹��Ÿ��s������w���A�Y�ϬY�@�ӥؿ��U�����s�ƾڳQ�R���F�A �]�S�����Y
������s����������h�A�L�k���u�ؿ��v���s���A�ҥH�b�γ~�W���O���������
�ϦӬO�Ÿ��s�����ϥΤ譱���s�C

2.
��������Jtouch hosts.real�إߤ@�ӥshosts.real���ɮ�
�M���J ls -ali �T�{���ɮת�inode�X



3.
��������Jtouch hosts.symbol�إߤ@�ӥshosts.symbol���ɮ�




�|.
1.�ϥ� gdisk /dev/vda �i�J gdisk ���ɭ�
���U p ���o�ثe�����Ϊ�A���U n �i��s�W���ʧ@�G
�b Partition number ���a��"4"�F
�b First sector ���a��]�i�H�������U Enter�F
�b Last sector ���a���J +1G �Ӵ��� 1G ���e�q�F
�b Hex code or GUID) ���a��A�]���������U [enter] �Y�i
���U p �Ӭd�\�@�U�O�_���o���T���e�q
�W�z�ʧ@�[���A�Y�S�����D�A���U�y w �z���x�s�����}
�t�η|�߰ݡy Do you want to proceed? (Y/N): �z���U y �ӽT�{�Y�i 
�Ϥ�:https://ppt.cc/f61rRx