## 1-1 �إ߸s�զW�٬��G mygroup, nogroup   
   
#### * groupadd �s�զW��  
   
## 1-2 �إ߱b���W�٬��G myuser1, myuser2, myuser3 �A�q�q�[�J mygroup�A�B�K�X�� MyPassWord   
## 1-3 �إ߱b���W�٬��G nouser1, nouser2, nouser3 �A�q�q�[�J nogroup�A�B�K�X�� MyPassWord  
   
#### * useradd -G �s�զW�� �Τ�W��   
#### * passwd �Τ�W��   
![1](https://github.com/edmundabc/107-1-ntcu-linux/blob/HW-4/ACS107131/1.png?raw=true)   
#### * �ˬd�O�_���\ tail -�Ʀr(��ܦh�ֲն���) /etc/group   
![2](https://github.com/edmundabc/107-1-ntcu-linux/blob/HW-4/ACS107131/2.PNG?raw=true)   
   
## 1-4 �إߤ@�ӦW�� /srv/myproject ���ؿ��A�o�ӥؿ��i�H�� mygroup �s�դ����ϥΪ̧���ϥΡA�B�i�s## �ت��ɮ׾֦��s�աj�� mygroup �C���L��L�H���঳�����v��   
   
#### * cd /srv   
#### * �إߥؿ� mkdir myproject   
#### * ll   
#### * ���֦��ɮת��s�� chgrp mygroup myproject   
#### * ����v�� chmod u=rwx,g=rwx,o= myproject   
![3](https://github.com/edmundabc/107-1-ntcu-linux/blob/HW-4/ACS107131/3.PNG?raw=true)   
![4](https://github.com/edmundabc/107-1-ntcu-linux/blob/HW-4/ACS107131/4.PNG?raw=true)   
   
## 1-5 �Ȯɤ������� myuser1 �������A�ëe�� /srv/myproject �ؿ��A���իإߤ@�ӦW�� myuser1.data ���ɮסA����n�X myuser1�C   
   
#### * su - myuser1   
#### * cd /srv/myproject   
#### * �إ��ɮ� touch myuser1.data   
#### * �ˬd ls   
#### * �n�X exit  
![5](https://github.com/edmundabc/107-1-ntcu-linux/blob/HW-4/ACS107131/5.PNG?raw=true)   
   
## 1-6 �_��/usr/bin/ls��/usr/local/bin/myls��A�����U�C�ާ@   
   
## ���M nogroup �s�դ����Τ��� /srv/myproject ���ӨS�������v���A���� nogroup �����Τ����/usr/local/bin/myls �ɡA�i�H���ͻP ls �ۦP����T�A�B�Ȯɾ֦� mygroup �s�ժ��v���A�]���i�H�d�ߨ� /srv/myproject �ؿ������ɦW��T�C �]�N�O���A��A�ϥ� nouser1 �����������imyls/srv/myproject�j�ɡA���ӬO����d�\��ӥؿ������ɦW��T�C      
     
#### * �ƻs cp /usr/bin/ls /usr/local/bin/myls   
#### * ����v�� chmod u+s /usr/local/bin/myls  
#### * ������nouser1      
####   su - nouser1  
#### * myls /srv/myproject     
![6](https://github.com/edmundabc/107-1-ntcu-linux/blob/HW-4/ACS107131/6.PNG?raw=true)   
   
## 2 �ϥε{���[����O�A�f�t grep ������r�d�ߥ\��A�N��쪺 rsyslog �������{�Ǫ� PID, 
## PRI, NI, COMMAND ����T��s�� /root/process_syslog.txt �ɮפ��C(�f�t>���ɦV��X)  
  
#### * ps aux | grep rsyslog > /root/process_syslog.txt  
#### * �ˬd�O�_���\    
####   cd /root   
####   cat process_syslog.txt ��ܤ��e    
![02](https://github.com/edmundabc/107-1-ntcu-linux/blob/HW-4/ACS107131/02.PNG?raw=true)   
   
## 3 �ϥ� find ��X /usr/bin �� /usr/sbin ��ӥؿ����A�t�� SUID ���S���ɮ��ɦW�A�èϥ� ls -l �h�C�X��쪺�ɮת������v����A�N�ù������s�� /root/findsuidsgid.txt �ɮפ��C(�ۦ�d��find���O �Ϊk�A�H�Ψϳz�L���ɦV�Ÿ�>��X�ɮ�)    
    
#### * find /usr/bin -perm /u=s -exec ls -l {} \; > /root/findsuidsgid.txt   
#### * find /usr/sbin -perm /u=s -exec ls -l {} \; >> /root/findsuidsgid.txt(>>�O�~���󤺮e)   
#### * �ˬd�O�_���\    
####  cat /root/findsuidsgid.txt    
![03](https://github.com/edmundabc/107-1-ntcu-linux/blob/HW-4/ACS107131/03.PNG?raw=true)     