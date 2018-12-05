### HW6

# 1.�Цb�a�ؿ��U��```.bashrc```�̷s�W�@��shell�ܼ�```HOSTS_PATH=/etc/hosts```�A(�`�N���ݥ�export)�A�����p�󤣵n�X��```HOSTS_PATH```�ܼƥͮġA����```cat $HOST_PATH```�T�{��Ū�����ɮפ��e�C

 * ��J```vi ~/.bashrc```�}�ҽs���ɮ�
> ���U```a```,```i```,```o```�Y�i�}�l�s��C 
 * ��J```HOST_PATH="/etc/hosts```
> ���U```esc```�ÿ�J```:wq```�A�Y�x�s���}�C
![](https://i.imgur.com/nF9tMXn.png)

 * ��J```source ~/.bashrc```�������ҳ]�w�ɫ��O
 * ��J```cat $HOSTS_PATH```���ҬO�_Ū�����\
 ![](https://i.imgur.com/JbzMk59.png)


# 2.�bC�y���{���i�H��```getenv()```Ū��LINUX�������ܼơA�d�ҵ{���p�U�C�ЦbLinux�̽sĶ���d�ҵ{���ð���A�аݧ_��Ū��```HOSTS_PATH```�H��```$?```���Ȭ���A�л����C�]�\�ݳz�L```yum groupinstall "Development Tools"```�w��gcc�C

 * ��J```yum groupinstall "Development Tools```�w��gcc�C
> �p�G�X�{```cannot find a valid baseurl for repo base/7/x86_64```�n���s�W����
 * ��J```vi cprogram.c```��J�U���{���X�A�ë��U```esc```��J```:wq```�x�s���} 
>  ```	#include <stdio.h>
		#include <stdlib.h>
		int main()
		{
    	const char* s = getenv("HOSTS_PATH");
    	if(s == NULL){
        	printf("getenv() return NULL\n");
        	return 1;
    	}
    
    	printf("HOSTS_PATH :%s\n",(s!=NULL)? s : "getenv returned NULL");
    	printf("\n %s content is: \n", s);

    	int c;
    	FILE *file;
    	file = fopen(s, "r");
    	if (file) {
        	while ((c = getc(file)) != EOF)
           	     putchar(c);
        	fclose(file);
    		}
		}```
 * ��J```gcc cprogram.c```�sĶ
 * ��J```gcc -c cprogram.c```
 * ��J```ll cprogram*```�|�ݨ�:
![](https://i.imgur.com/7pVvqnB.png)
 * ��J```gcc -o cprogram cprogram.o```���Ͱ�����
 * ��J```ll cprogram*```�|�ݨ�:
![](https://i.imgur.com/tskpEr5.png)
 * ��J```./cprogram```����
> �X�{```getenv() returrn NULL```�C 
 * ��J```echo $?```
> ��Ȭ�```1```�C 
>	>```HOSTS_PATH```���ϰ��ܼơA�ӫD�����ܼơA�ҥH```getenv```�L�kŪ��A�|�X�{```NULL```�A��O�sĶ�ð���^�ǤF```1```�C

# 3.�b```.bashrc```�̭n�p��ץ��A��C�y���{���i�HŪ�������ܼƨñN�ɮפ��e��ܡC
 * ��J```vi~/.bashrc```�A�s��אּ```export HOSTS_PATH```
> ���U```esc```�ÿ�J```:wq```�A�Y�x�s���}�C 
 * ��J```source ~/.bashrc```�O���O�ͮ�
 * ��J```./cprogram```����ÿ�J```echo $?```���G�p�U
![](https://i.imgur.com/SKKrAfb.png) 
  

