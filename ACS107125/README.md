# 1.
�ϥ�"**echo**"����ܼ�

![image](https://github.com/freshdiefish/107-1-ntcu-linux/blob/midterm/ACS107125/01.png)

PATH�����ܼƩw�q�F�b����ؿ��U�ҥi�H�ϥΪ����O

![image](https://github.com/freshdiefish/107-1-ntcu-linux/blob/midterm/ACS107125/02.png)

# 2.

## 2-1

> drwxrwsr-x 3 root mail 4096 2�� 16 2017 mail/

�ڭ̱q�e���ѪR�o�ɮ��ݩʪ����e
>d

���ɮת��榡��"**�ؿ�**"
>rwx_rws_r-x

�e�T�ӥN���֦��ͪ��v��

��T���b�P�@�Ӹs�ժ��v��

�̫�T�ӥN����L�H���v��


(���F��K�AŪ�ڥ[�J�F���u�T�T���Ϲj)

�v���@�G�@r=Ū�@w=��g�@x=����

��"**-**"�N���㦳�Ӷ��v��

�䤤�ĤG�զ��@�ӯS���v��"**s**"���٧@SUID���S���v��

�Y����Ӥ��ɱN�㦳�Ӥ��֦��ͪ��v��


>3

�N���s���즹�ɮ�**inode**���X�����ɮ׼�

>root

�֦���(Owner)

>mail

�Ҧb�s�աA�s�դ����ϥΎ;֦�"**rws**"���v��

>4096

���ɮץ]�t�ؿ����U���j�p

>2�� 16 2017

���e�̫�ק�ɶ�

>mail/

�ɦW

## 2-2


>chmod�@777�@./script.sh

or

>chmod�@ugo=rwx�@./script.sh

# 3.

����s��(hard link)���x�s���ɮ�"**indode**"��T���ɮסA***���ɮקR���ᤴ�i����***

�Ÿ��s��(symbolic link)���x�s���ɮ�"**���|**"��T���ɮסA�֦��P���ɮק������P��"**inode**"���X�A***���ɮקR����L�k����***

>ln�@/etc/hosts�@~/hosts.real

>ln�@-s�@/etc/hosts�@~/hosts.symbo


# 4.