## 1.<br>
### �]�w ver �ܼơA���e���y my kernel version is 3.xx �z�A�䤤 3.xx �� uname -r ��X����T�A����ܥXver�ܼƪ��ȡC<br>

```
ver=my\ kernel\ version\ is\ $(uname -r)
echo $ver
```

### ����ܥثePATH�����ܼƪ��Ȭ���A�û���PATH���\�ά���?<br>

```
echo $PATH
```

PATH�O�����ɷj�M�����|�A�ؿ��P�ؿ������H�_��(:)���j�A�ѩ��ɮת��j�M�O�̧ǥ� PATH ���ܼƤ����ؿ��Ӭd�ߡA�]���ؿ������Ǥ]�O���n����C<br>

## 2.<br>
### ���@���ɮת��ݩ��v���� drwxrwsr-x 3 root mail 4096 2�� 16 2017 mail/�A�л������ɮת��S�ʡC<br>
���ɮ��ɦW��mail/�A�ؿ���(d)�C�ϥΪ�(root)�v�����iŪ�i�g�i����C�s��(mail)�v�����iŪ�i�g�i����A�þ֦�SGID���S���v���C��L�H�v�����iŪ�i����C<br>
�ɮ׳s���Ƭ�3�A�ɮ׮e�q4096�A�̫�@���ק�ɶ���2017�~2��16��C<br>

### ���]���@��script.sh�ɮת��v����-rw-r--r--�A�Y�Ʊ����Ҧ��H�i�H������ɮסA�аݸӦp��U�F���O�H�ШϥμƦr�k�P�Ÿ��k�U�ާ@�@���C<br>

```
chmod 755 script.sh
�άO
chmod u=rwx,g=rx,o=rx script.sh
```

## 3.<br>
### ��������s���P�Ÿ��s�����t���C
����s���|�إ߻P�s���ɦPinode�X���ɮסA�ӲŸ��s���h�|�إ߻P�s���ɤ��Pinode�X���W���ɮ�<br>

### �b�a�ؿ��U�إߤ@���ɦW�� hosts.real ������s������ /etc/hosts�C(�Хά۹���|��ܮa�ؿ�)<br>

```
cd ~bill0330
touch hosts.real
ln ~bill0330/hosts.real /etc/hosts
ll -i ~bill0330/hosts.real /etc/hosts
```

### �b�a�ؿ��U�إߤ@���ɦW�� hosts.symbo ���Ÿ��s������ /etc/hosts�C(�Хά۹���|��ܮa�ؿ�)<br>

```
cd ~bill0330
touch hosts.symbo
ln -s ~bill0330/hosts.symbo /etc/hosts
ll -i ~bill0330/hosts.symbo /etc/hosts
```

## 4.
### �إߤ@�Ӯe�q��1GB��xfs�ɮרt�ΡA�C���}��������۰ʪ������� /srv/maildir�A�B�ӥؿ��O�� mailgroup �o�Ӹs�զ@�Ϊ��A��L�H���i�㦳�����v���C�A�إߤ@�ӦW��mailuser���b���A�å[�J mailgroup �s�աA�B���b�����i�ϥ�shell�n�J�t�ΡC
![image](https://github.com/bill0330/107-1-ntcu-linux/blob/midterm/ACS107137/img/4-1.PNG?raw=true)<br>
![image](https://github.com/bill0330/107-1-ntcu-linux/blob/midterm/ACS107137/img/4-2.PNG?raw=true)<br>


