# HW-5

# �Ĥ@�D

### �Ĥ@�B

![1.1](https://images2.imgbox.com/38/d2/FekxpOji_o.png)

>�����ϥ�**ls**���O�f�t�Ѽ� **-i** �C�X�ɮת�inode�A�ðt�X **-l** �ѼƦC�X�ԲӸ�ơC

���ɮת�inode���W��**����**�ҥܪ� **4235656**�A��**���**�h��ܪ��h�O **���h�֭��ɦW�s���즹inode** �A�]���ڭ̪��D��inode�u���@���ɦW�ϥΡC

### �ĤG�B

![1.2](https://images2.imgbox.com/d2/16/rpb3If5f_o.png)

>�ϥ�**ln**���O�إߨӷ���: **/etc/hosts** ��**hardlink** ��ت���: **/srv/hosts.hard**�A�ðt�X **ls **�M�ѼƦC�X���ɡC

������ܥX/srv/hosts.hard�ɪ�inode��**4235656**�A�䤤�A���ҥH�M/etc/hosts�ɪ�inode�ۦP�O�]��**hardlink**���S�ʡC**hardlink**�O**�b�Y�ؿ��U�s�W�@���ɦW�s���inode���X�����s�O��**�C

�Ӿ����ܦ��P�@inode���s���ɦW��1���K��2���A�O�]��**hardlink**�����Y�Ӧh�F�@���ɦW�s����Pinode�C

**hardlink**��²��B�@�ܷN�Ϧp�U:

![1.3](https://images2.imgbox.com/f1/e9/eXiArIU6_o.png)

![1.4](https://images2.imgbox.com/f1/4d/llFchWiw_o.png)

>�ϥΫ��O **ln** �f�t�Ѽ� **-s** �ӫإ� **Symbolic link** �A�ðt�X **ls** �M��ѼƦC�X�ɮסC

������ܥX/srv/hosts.soft�s����( **l**rwxrwxrwx )��inode�� **6370784** �A���P��/etc/hosts��**4235656** �A�]��**Symbolic link**�|**�إߤ@�ӿW�ߪ��ɮ�**�A�ӳo�ɮ׷|����ƪ�Ū�����V�Llink�������ɮ��ɦW�A**�إ߿W���ɮ�**�����O�n�ϥΤ@�շs��inode�A�]�����s���ɪ�inode���P��쥻�ɮת�inode�C

��/srv/hosts.soft���s���ɥB���s�إߪ��A�]�������ܥX��inode�����@���ɦW�s���C

�t�~�A**���**��ܳs���ɤj�p��10bytes�A�]��**�Ů�**�ɦW **/etc/hosts** �@�Q�Ӧr�A�ӨC�Ӧr����1bytes�A�]���@�ΤF10bytes�C

**Symbolic link**��²��B�@�ܷN�Ϧp�U:

![1.5](https://images2.imgbox.com/0c/dd/BXzlx6Au_o.png)