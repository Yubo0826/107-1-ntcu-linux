#1-1�إߤT�ӥΤ�A�b���W�٤��O���G examuser1, examuser2, examuser3 �A�P�ɤT�ӥΤ᪺�K�X���O�y ItIsExam �z�C
*1.����root�b��
*2.�Q��"useradd"���O�إ�examuser1/examuser2/examuser3�b��
*3.�Q��"passwd"���O�]�wexamuser1/examuser2/examuser3���K�X��**ItIsExam **

#1-2�ЧR���t�Τ��� examuser3 �o�ӱb���A�P�ɱN�o�ӱb�����a�ؿ��P�l���ɮצP�B�R���C
*1."userdel -r examuser3"
*2."id examuser3"��"no such user"

#1-3examuser1 ���p�߳Q�޲z���R���F�A���O�o�ӱb�����a�ؿ��P�����l���٦s�b�C�аѦҳo�ӱb���i�઺�a�ؿ��ҫO�d�� UID �P GID�A �ù��եH�ӱb���즳�� UID/GID ��T�ӭ��ظӱb���C
**1."id examuser1"�d��examuser1��UID�MGID�A�ðO�U�C
**"userdel examuser1"�R��examuser1�C�ѩ���O�S����J"-r"�A�ҥH�a�ؿ��M�����l���٦s�b�C(��"id examuser1"�٬O�|"no such user")**
*1."useradd -u ���d�ݪ�UID -g ���d�ݪ�GID examuser1"
*2."passwd examuser1"�K�XItIsExam

#2-1�إ�examuser4�ϥΪ̱b���A�K�X���N�C
*1."useradd examuser4"��"passwd examuser4"

#2-2�ϥ� root �N /etc/securetty �ƻs�� examuser4�A�B�o�ӱb���n�������ϥθ��ɮפ~��A(�Y���Ҧ����v��)�C
*1.�إ�/etc/securetty
*2."chown examuser4 /etc/securetty"��"chmod u=rwx,g=rw,o=r /etc/securetty"

#2-3�إߤ@�ӦW�� /examdata/change.txt �����ɮסA�o���ɮת��֦��̬� sshd�A�֦��s�լ� users�Asshd �iŪ�i�g�Ausers �s�զ����iŪ�A ��L�H�S�v���C�B�o���ɮת��ק����нվ㦨 2012 �~ 12 �� 21 �� (������T�Y�i�A�ɶ��H�K)
*1."mkdir examdata"��"cd examdata"��"vi change.txt"
*2."chown sshd change.txt"��"chdrp users change.txt"��"chmod u=rw,g=r,o=0 change.txt"
*3."touch -t 201212211357 change.txt"

#3-1�Шϥ� root �������إߩ��U���ɮ׻P�v���G
**�إ�/dev/shm/unit05**
*1."cd dev"��"cd shm"��"chmod u=rwx,g=rwx,o=rx unit05"
*2."cd unit05"��"mkdir dir1"��"chmod u=rwx,g=rx,o=r dir1"
*3."cd dir1"��"mkdir file1"��"cp /etc/hosts /dev/shm/unit05/dir1/file1"��"chmod u=rw,g=r,o=r file1"
*4."cd unit05"��"mkdir dir2"��"chmod u=rwx,g=rx,o=x dir2"
*5."cd dir2"��"mkdir file2"��"cp /etc/hosts /dev/shm/unit05/dir1/file2"��"chmod u=rw,g=r,o=r file2"
*6."cd unit05"��"mkdir dir3"��"chmod u=rwx,g=rx,o=rx dir3"
*7."cd dir3"��"mkdir file3"��"cp /etc/hosts /dev/shm/unit05/dir1/file3"��"chmod u=rw,g=rw,o=rw file3"
*8."cd unit05"��"mkdir dir4"��"chmod u=rwx,g=rwx,o=rwx dir4"
*9."cd dir4"��"mkdir file4"��"cp /etc/hosts /dev/shm/unit05/dir1/file4"��"chmod u=rw,g=0,o=0 file4"

#3-2�ϥΤ@��ϥΪ� �������i��U���u�@


#3-3�Шϥ� ls -l /dev/shm/unit05/dir[1-4] �̾ڿ�X�����G��������|���ͳo�ǰ��D�H
*1.��J"ls -l /dev/shm/unit05/dir[1-4]"
**dir1�v����u=rwx,g=rx,o=r��root�ϥΪ̥iŪ�i�g�i����Aroot�s�եiŪ�i����A�@��ϥΪ̥iŪ
**dir2�v����u=rwx,g=rx,o=x��root�ϥΪ̥iŪ�i�g�i����Aroot�s�եiŪ�i����A�@��ϥΪ̥i����
**dir3�v����u=rwx,g=rx,o=rx��root�ϥΪ̥iŪ�i�g�i����Aroot�s�եiŪ�i����A�@��ϥΪ̥iŪ�i����
**dir4�v����u=rwx,g=rwx,o=rwx��root�ϥΪ̥iŪ�i�g�i����Aroot�s�եiŪ�i�g�i����A�@��ϥΪ̥iŪ�i�g�i����

#3-4�Шϥ� ls -l /dev/shm/unit05/dir1/file1 �A�̧ǱN�W�z���ɦW�� dir1/file1 ~ dir4/file4 ����A�̾ڲ��ͪ����G��������|�p���H
*1.��J"ls -l /dev/shm/unit05/dir1/[dir1/file1 ~ dir4/file4]"
**dir1/file1�v����u=rw,g=r,o=r��root�ϥΪ̥iŪ�i�g�Aroot�s�եiŪ�A�@��ϥΪ̥iŪ
**dir2/file2�v����u=rw,g=r,o=r��root�ϥΪ̥iŪ�i�g�Aroot�s�եiŪ�A�@��ϥΪ̥iŪ
**dir3/file3�v����u=rw,g=rw,o=rw��root�ϥΪ̥iŪ�i�g�Aroot�s�եiŪ�i�g�A�@��ϥΪ̥iŪ�i�g
**dir4/file4�v����u=rw,g=0,o=0��root�ϥΪ̥iŪ�i�g�Aroot�s�ըS���v���A�@��ϥΪ̨S���v��

#3-5�Шϥ� vim /dev/shm/unit05/dir1/file1 ~ vim /dev/shm/unit05/dir4/file4�A�����x�s (�αj���x�s)�A��������i�H/���i�H�x�s�H
*1."vim /dev/shm/unit05/[dir1/file1 ~ dir4/file4]"��"command not found"
**vim /dev/shm/unit05/dir1/file1�A���G�L�k�x�s�A�]���v����r--
**vim /dev/shm/unit05/dir2/file2�A���G�L�k�x�s�A�]���v����r--
**vim /dev/shm/unit05/dir3/file3�A���G�i�H�x�s�A�]���v����rw-
**vim /dev/shm/unit05/dir4/file4�A���G���i�x�s�A�]���v����---