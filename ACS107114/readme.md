## �Ĥ@�D
### 1.�]�w ver �ܼơA���e���y my kernel version is 3.xx �z�A�䤤 3.xx �� uname -r ��X����T�A����ܥXver�ܼƪ��ȡC
* Ans:  
* 1.�ϥ�```uname -r```��X������**3.10.0-862.el7.x86_64**
* 2.�ϥ�```ver="my kernel version is 3.10"```
* 3.�ϥ�```echo $ver```�L�X�ܼƭ� �Y����

### 2.����ܥثePATH�����ܼƪ��Ȭ���A�û���PATH���\�ά���?
* Ans:
* 1.�ϥ�```echo $PATH```��ܥX�ثe�����ܼƪ��Ȭ� **usr/local/bin:/bin:/usr/bin:/usr/local/sbin:/usr/sbin:/home/kenny/.local/bin:/home/kenny/bin**

* 2.Path�����ܼƬO�@�~�t�Υ~���u�R�O�v�j�����| ��ϥΪ̿�J�@���O�� �@�~�t�η|��Path����M���C�䤤�����| �æb��Ƨ����M��ŦX��R�O�ݨD���ɮ� �̲ױo�H�Ұʨð���C




## �ĤG�D
### 1.���@���ɮת��ݩ��v���� `drwxrwsr-x  3 root mail   4096  2�� 16  2017 mail/`�A�л������ɮת��S�ʡC
* Ans:
* 1.�@�}�Y**d**��ܦ��ɮ׬��ؿ��A�ӫ�**rwxrwsr-x**�h�N�� 
* �o���ɮ׾֦���**root**�֦��������v��
* ���ɮשҦs�b�s�ժ��ϥΪ̦]���v����**rws** �㦳SGID���Y �N��p�G�s�ըϥΪ̪��v���㦳**x**���� �s�ըϥΪ̫h�i�H�i�J���ؿ� ��l�v���h�P�ɮ׾֦��̤@��
* �Ө�L�H�]�v����**r-x** �N��i�HŪ���ð��榹�ɮ� �C

### 2.���]���@��script.sh�ɮת��v����-rw-r--r--�A�Y�Ʊ����Ҧ��H�i�H������ɮסA�аݸӦp��U�F���O�H�ШϥμƦr�k�P�Ÿ��k�U�ާ@�@���C
* Ans:
* 1.**�Ʀr�k**�F�ϥ�```chmod 770 script.sh```�Y�i����
* 2.**�Ÿ��k**�F�ϥ�```chmod a=rwx script.sh```�Y�i����


## �ĤT�D
### 1.��������s���P�Ÿ��s�����t���C
* Ans:
* 1.**����s��**�O�b�Y�ӥؿ��U�s�W�@���ɦW�s���� inode ���X�����s�O���A��**�Ÿ��s��**�N�O�b�إߤ@�ӿW�ߪ��ɮסA�ӳo���ɮ׷|����ƪ�Ū�����V�s���������ɮת��ɦW�A����**���|**�������C
### 2.�b�a�ؿ��U�إߤ@���ɦW�� hosts.real ������s������ /etc/hosts�H (�Хά۹���|��ܮa�ؿ�)
* Ans:�ϥ� ```cd ~``` ������ثe�ϥΪ̪��a�ؿ� �A�ϥ� **ln** ���O�ӫإ߹���s��```ln /etc/hosts hosts.real``` �Y����
### 3.�b�a�ؿ��U�إߤ@���ɦW�� hosts.symbo ���Ÿ��s������ /etc/hosts�H (�Хά۹���|��ܮa�ؿ�)
* Ans:�ϥ� ```cd ~``` ������ثe�ϥΪ̪��a�ؿ� �A�ϥ� **ln -s** ���O�ӫإ߲Ÿ��s��  ```ln -s /etc/hosts hosts.symbo``` �Y����


## �ĥ|�D
### 1.�Х�`df`���O�t�X`human-readable`�ﶵ�A��ܦ�1GB���ɮרt�Υ�������`/srv/maildir`
![](https://i.imgur.com/B1bWknZ.png)
### 2. �Х�`grep`���Ҧ��]�w�}���۰ʱ����C
![](https://i.imgur.com/WynwQXs.png)
### 3. �Х�`ls`�d��`/srv/maildir`�ݩʡA�T�{�i�H��`mailgroup`�s�զ@�ΡA�Ө�L�H��������v���C
![](https://i.imgur.com/ae4w6dJ.png)
### 4.�Х�`id`�ˬd`mailuser`�ϥΪ̦��b`mailgroup`.
![](https://i.imgur.com/e9FNboy.png)