+�ϥ�echo ${ver}�Becho ${kernel}�إ��ܼ�ver�Bkernel�A�M��]�wkernel=$(uname -r)
 �̫�]�wver="my kernel version is $kernel"�Y�i

+�ϥ�echo $PATH�i�H�d�ݸ��|�����������ܼ�
![GITHUB](https://imgur.com/O8Sk2kq.jpg"git�ϥ�")
 
+drwxrwsr-x 3 root mail 4096 2�� 16 2017 mail/
+���ɮׯS�ʬ�:�v�����ϥΪ̥i�g�iŪ�i�ϥΡA�㦳SGID���\��A��L�H����ɥi��o�s�ժ��v��
+�ɮ׳s���Ƭ�3��
+�֦��̬�root
+�ɮש��ݸs�լ�mail
+�ɮפj�p��4096
+�̫�ק�����2017�~2��16��
+�ɮצW��mail/
 
+�v����-rw-r--r--�]�����S��x���v���ҥH����u��³]SUID
+�Ʀr�k:chmod 4755 script.sh
+�Ÿ��k:chmod u=rwx g=rx o=rx script.sh��chmod u+s script.sh

+hard link���C���ɮ׳��|���Τ@��inode��soft link���|
 hard link���ݥ��s���R���~��R���ɮסAsoft link�ت��ɧR����s���N����ϥΤF
 hard link�����Filesystem��soft link�i
+�إ߹���s��hosts.real�b�a�ؿ�:ln /etc/hosts ~hosts.real
+�إ߲Ÿ��s��hosts.real�b�a�ؿ�:ln -s /etc/hosts ~hosts.real

+�ϥ�ud -m�i�����@�Ӥj�p��1014mb�ɮרt�Υ�������/srv/maildir
![GITHUB](https://imgur.com/U5HZQD6.jpg"git�ϥ�")
+�ϥ�grep "maildir" /etc/fstab�i���w�]���}���۰ʱ���
![GITHUB](https://imgur.com/bovvHXr.jpg"git�ϥ�")
+�ϥ�ls -al /srv/maildir�i����s�լ�mailgrpup
![GITHUB](https://imgur.com/vlYIegs.jpg"git�ϥ�")
+�ϥ�id mailuser�i����bmailgroup��
![GITHUB](https://imgur.com/2YyDt9T.jpg"git�ϥ�")
+�ѤU�ϥi���Dmailuser����n�J
![GITHUB](https://imgur.com/jSeJPIH.jpg"git�ϥ�")
