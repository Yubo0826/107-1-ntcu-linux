## 1.(20%)    
   
### 1-1�]�w ver �ܼơA���e���y my kernel version is 3.xx �z�A�䤤 3.xx �� uname -r ��X����T�A����ܥXver�ܼƪ��ȡC(10%)    
    
#### ver=my\ kernel\ version\ is\ 3.xx    
#### echo $ver    
    
### 1-2����ܥثePATH�����ܼƪ��Ȭ���A�û���PATH���\�ά���? (10%)   
     
#### env �N�O�����ɷj�M�����|�ա�ؿ��P�ؿ������H�_��(:)���j�A �ѩ��ɮת��j�M�O�̧ǥ� PATH ���ܼƤ����ؿ��Ӭd��     
       
## 2.(20%)    
    
### 2-1���@���ɮת��ݩ��v���� drwxrwsr-x 3 root mail 4096 2�� 16 2017 mail/�A�л������ɮת��S�ʡC(10%)     
     
#### user �M group �ҥiŪ�g����A��L�H�u��Ū����A����g    
#### ��3�ӳs����    
#### user-root   
#### group-mail    
#### �ɮ׮e�q�O4096    
#### �̫�ק�ɶ�2�� 16 2017   
#### �ɦWmail/    
    
### 2-2���]���@��script.sh�ɮת��v����-rw-r--r--�A�Y�Ʊ����Ҧ��H�i�H������ɮסA�аݸӦp��U�F���O�H�ШϥμƦr�k�P�Ÿ��k�U�ާ@�@���C(10%)     
    
#### chmod u=rwx,g=rx,o=x script.sh    
#### chmod 751 script.sh   
   
## 3(20%)     
     
### 3-1��������s���P�Ÿ��s�����t���C(10%)     
     
#### ����s�� �u�O�b�Y�ӥؿ��U�s�W�@���ɦW�s����Y inode ���X�����s�O��    
#### �Ÿ��s�� �N�O�b�إߤ@�ӿW�ߪ��ɮסA�ӳo���ɮ׷|����ƪ�Ū�����V�L link �������ɮת��ɦW     
     
### 3-2�b�a�ؿ��U�إߤ@���ɦW�� hosts.real ������s������ /etc/hosts�H (�Хά۹���|��ܮa�ؿ�) (5%)     
      
#### ln /etc/hosts  ~/hosts.real    
      
### 3-3�b�a�ؿ��U�إߤ@���ɦW�� hosts.symbo ���Ÿ��s������ /etc/hosts�H (�Хά۹���|��ܮa�ؿ� (5%)     
       
#### ln -s /etc/hosts ~/hosts.symbo   
    
## 4.(40%)     
      
### �Ш̤U�z���ҧ����t�ξާ@��A�ά������O�i�����ҡA�Ч����ҫ��O���ϡG     
       
### �إߤ@�Ӯe�q��1GB��xfs�ɮרt�ΡA�C���}��������۰ʪ������� /srv/maildir�A�B�ӥؿ��O�� mailgroup �o�Ӹs�զ@�Ϊ��A��L�H���i�㦳�����v���C�A�إߤ@�ӦW��mailuser���b���A�å[�J mailgroup �s�աA�B���b�����i�ϥ�shell�n�J�t�ΡC      
        
#### mkfs.xfs /dev/sdb1      
#### mkdir /srv/maildir      
#### mount -t xfs /dev/sdb1 /srv/maildir      
#### groupadd mailgroup      
#### chgrp mailgroup /srv/maildir        
#### useradd -G mailgroup mailuser�@-s�@/sbin/nologin    
#### chmod u=rwx,g=rwx,o= /srv/maildir       
           
                
### 4-1 �Х�`df`���O�t�X`human-readable`�ﶵ�A��ܦ�1GB���ɮרt�Υ�������`/srv/maildir` (8%)        
![1](https://github.com/edmundabc/107-1-ntcu-linux/blob/midterm/ACS107131/1.PNG?raw=true)  
        
### 4-2 �Х�`grep`���Ҧ��]�w�}���۰ʱ����C(8%)         
        
### 4-3 �Х�`ls`�d��`/srv/maildir`�ݩʡA�T�{�i�H��`mailgroup`�s�զ@�ΡA�Ө�L�H��������v���C(8%)        
![3](https://github.com/edmundabc/107-1-ntcu-linux/blob/midterm/ACS107131/3.PNG?raw=true)                 
### 4-4 �Х�`id`�ˬd`mailuser`�ϥΪ̦��b`mailgroup`. (8%)        
![4](https://github.com/edmundabc/107-1-ntcu-linux/blob/midterm/ACS107131/4.PNG?raw=true)                   
### 4-5 �Х�`grep`���Ҧ��b���L�k�z�Lshell�n�J�C(8%) 
                            