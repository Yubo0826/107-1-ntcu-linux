### ������

## �Ĥ@�j�D
 1. �]�wver�ܼ� 
    *  `uname -r`
         `3.10.0-862.e17.x86_64`
    *  `3.xx=3.10.0-862.e17.x86_64`
    *  `ver="my kernel version is $3.xx"`
    *  `echo $ver`
    *    `my kernel version is 3.10.0-862.e17.x86_64`

 2. ���PATH�����ܼƪ���
    
    ```
    /usr/local.sbin:/usr/local/bin:/sbin:/bin:/usr/sbin:/usr/bin:/root/bin
    ```

   *  PATH���\��: �������ܼơA���w���ҥؿ��A�H����i������

=============================================================================

## �ĤG�j�D
 1. `drwxrwsr-x 3 root mail 4096 2�� 16 2017 mail/`
    *  �ɮ�����:�ؿ���
    *  �ɮ��v��:
         -  user: �iŪ�i�ק�i����
         -  group: �iŪ�i�ק�i����  ( �v����s����v���X�Ш�P�s�լۦP�A�]���b���s�դ����H�ҥi�ܧ󤺮e )
         -  others: �iŪ�i����A�����i�ק�
    *  �ɮ׳s����:3 (inode��)
    *  �ɮ׾֦���:root
    *  �ɮ׸s��:mail
    *  �ɮ׮e�q:4096
    *  �ɮפ��:2�� 16 2017
    *  �ɦW: mail/

 2. script.sh�ɮת��v����`-rw-r--r--`
    * `chmod a+x script.sh`
    * `chmod 755 script.sh`

=============================================================================

## �ĤT�j�D
 1.����s��:
    *  inode���ܡA�M�ӷ��ɬۦP
    *  ���ҦW�R���Ainode�Mblock�Ҧs�b�A����s���Ƭ�0����
    *  �s���Ƨ���: ��إ߷s���ؿ��ɡA�s���Ƭ�2�A�ӤW�h�ؿ���1
    *  `ln �ӷ��� �ت���`
   �Ÿ��s��:
    *  inode���ܡA�إ߿W�ߪ��ɮ�
    *  �ӷ��ɩΥت��ɧR���A�Y�L�k�}���ɮ�
    *  �s�����ɮפj�p�����|����
    *  `ln -s �ӷ��� �ت���`

 2. �إ߹���s��  `hosts.real`
    *  `ln /etc/hosts ~hosts.real`
    *  `ll`
         `-rw-r--r--. 3 root root 158 Jun 7 2013 ~hosts.real`
    *  `ls -ali`
         `16820904 -rw-r--r--. 3 root root 158 Jun 7 2013 ~hosts.real`
    *  `ls -ali /etc/hosts`
         `16820904 -rw-r--r--. 3 root root 158 Jun 7 2013 /etc/hosts`

 3. �إ߲Ÿ��s��  `hosts.symbo`
    *  `ln -s /etc/hosts ~hosts.symbo`
    *  `ll`
         `lrwxrwxrwx. 1 root root 10 Nov 14 15:17 ~hosts.symbo -> /etc/hosts`
    *  `ls -ali`
         `25628245 lrwxrwxrwx. 1 root root 10 Nov 14 15:17 ~hosts.symbo -> /etc/hosts`

=============================================================================

## �ĥ|�j�D
 1.  �إ��ɮרt��
    *  `fdisk /dev/sdb`
         `command (m for help):n` �إߤ���/dev/sdb1
         `Last sectors: +1GB`
         `command (m for help):p`
         `Device     Boot   Start     End        Block      Id    System`
         `/dev/sdb1         2048     1955839     976896     83     Linux`
         `command (m for help):w`
         `mkds.xfs /dev/sdb1`
  2.  �إ߷s�ؿ�
       * `mkdir /srv/maildir`
  3.  �إ߷s�b��
       * `groupadd mailgroup`
       * `useradd -G mailgroup mailuser`
       * `chgrp mailgroup /srv/maildir`
       * `chmod o-rw /srv/maildir`
       * `ll /srv/maildir`
           `drwxr-x---. 2 root mailgroup 6 Nov 14 16:16 maildir`
  4.  ����
       * `blkid`
           `UUID="c758211a-52d1-41a7-810d-7d362f0089e9",TYPE="xfs"`
       * `mount /dev/sdb1 /srv/maildir`
       * `cat /etc/fstab`
       * `vi /etc/fstab`
           �s�WUUID="c758211a-52d1-41a7-810d-7d362f0089e9" /srv/maildir xfs default 0 0`
       * `mount -a`
  5.  �˵�
       * `df -T`
          `/dev/sdb1    xfs    973476   32944  940532  4%  /srv/maildir`
       * `/etc/passwd | grep /dev/sdb1`
           
       * `ls -al /srv/maildir`
           `drwxr-x---. 2 root mailgroup 6 Nov 14 16:16 maildir`
       * `id mailuser`
            `uid=101(mailuser) gid=1013(mailuser) groups=1013(mailuser),1012(mailgroup)`
       * `/etc/passwd | grep /srv/maildir`
           `/srv/maildir:/sbin/nologin`

(�Ѯv�藍�_�A�ڪ��q���������󤣯�I�ϡA�ҥH�ڵL�k����)