1.�n���b��
2.������root
3.��useradd examuser1�إ߱b���A�̧A�һݭ��ƲĤT�I�إ��ɮ�
4.��passwd examuser1���K�X��ItIsExam
5.��cd /home��ll���Y�i�d�ݦ��L���\
�R���t�Τ��� examuser3 �o�ӱb���A�P�ɱN�o�ӱb�����a�ؿ��P�l���ɮצP�B�R���C
1.��userdel -r examuser3
2.��cd /home��ll���Y�i�d�ݦ��L���\
examuser1 ���p�߳Q�޲z���R���F�A���O�o�ӱb�����a�ؿ��P�����l���٦s�b�C
1.����id examuser1�d��examuser1��GID�MUID
2.��userdel examuser1��cd /home��ll���Y�i�d�ݦ��L���\
����examuser1
1.��useradd -u ���O�U��GID�MUID examuser1��passwd examuser1��cd /home��ll���Y�i�d�ݦ��L���\
�� root �N /etc/securetty �ƻs�� examuser4�A�B�o�ӱb���n�������ϥθ��ɮפ~��A(�Y���Ҧ����v��)�C
1.�إ�examuser4
2.��cp /etc/securetty /home/examuser4��chmod u=rwx,g=rwx,o=rwx /home/examuser4/securetty��su - examuser4��cd /home/examuser4��ll���Y�i����
�إߤ@�ӦW�� /examdata/change.txt �����ɮסA�o���ɮת��֦��̬� sshd�A�֦��s�լ� users�Asshd �iŪ�i�g�Ausers �s�զ����iŪ�A ��L�H�S�v���C�B�o���ɮת��ק����нվ㦨 2012 �~ 12 �� 21 �� (������T�Y�i�A�ɶ��H�K)
�ഫ��root���إ�examdata��cd examdata��vi change.txt��chown sshd change.txt(���֦���)��chdrp users change.txt(���s��)��chmod u=rw,g=r,o= change.txt(����v��)��ll�d�ݦ��L���\��touch -t �~���ɶ� change.txt��ll -l������
�Шϥ� root �������إߩ��U���ɮ׻P�v��
1.�e���Od�N��O�ؿ�
2.��mkdir �ؿ��W�١�cd �ؿ��W�١A�i�J�ؿ��̡����D�ةһݭ��ƤW����Ӱʧ@
3.�e��-�N��O�ɮ�
4.��vi �ɮצW�١����X�e������esc��:wq���Y�i�إ��ɮ�
�ϥΤ@��ϥΪ� �������i�J
su �b��
�ϥ� ls -l /dev/shm/unit05/dir[1-4] �̾ڿ�X�����G��������|���ͳo�ǰ��D�H
��ls -l /dev/shm/unit05/dir1���G����A�]���e���Or--�A�ҥH�S���v��
��ls -l /dev/shm/unit05/dir2���G�i�H�A�]���e���O--x�A�ҥH���v��
��ls -l /dev/shm/unit05/dir3���G�i�H�A�]���e���Or-x�A�ҥH���v��
��ls -l /dev/shm/unit05/dir4���G�i�H�A�]���e���Orwx�A�ҥH���v��
��ls -l /dev/shm/unit05/dir1/file1�A���G����A�]��examuser��file1���v����r--
��ls -l /dev/shm/unit05/dir1/file2�A���G����A�]��examuser��file2���v����r--
��ls -l /dev/shm/unit05/dir1/file3�A���G�i�H�A�]��examuser��file3���v����rw-
��ls -l /dev/shm/unit05/dir1/file4�A���G�i�H�A�]��examuser��file1���v����---
��vim /dev/shm/unit05/dir1/file1�A���G�L�k�x�s�A�]���v����r--
��vim /dev/shm/unit05/dir2/file2�A���G�L�k�x�s�A�]���v����r--
��vim /dev/shm/unit05/dir3/file3�A���G�i�H�x�s�A�]���v����rw-
��vim /dev/shm/unit05/dir4/file4�A���G���i�x�s�A�]���v����---