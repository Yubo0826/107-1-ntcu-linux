##HW-3

<ol>
<li>��J"ls -ali /etc/hosts"</li>
![](https://i.imgur.com/u03xGHq.png)
<p>�̫e�����Ʀr��inode</p>
<p>1���ɦW�b�ϥ�</p>
</ol>

<ol>
<li>��J"ln /etc/hosts /srv/hosts.hard"�إ߹���s��</li>
<li>��J"ls -ali /srv/hosts.hard"</li>
![](https://i.imgur.com/AAzOcjO.png)
<p>�̫e�����Ʀr��inode</p>
<p>2���ɦW�b�ϥ�</p>
*/etc/hosts�M�إߪ�����s��/srv/hosts.hard���b�ϥΡA�ҥH������ɦW
</ol>

<ol>
<li>��J"ln -s /etc/hosts /srv/hosts.soft"�إ߲Ÿ��s��</li>
<li>��J"ls -ali /srv/hosts.soft"</li>
![](https://i.imgur.com/n2NKr6b.png)
<p>�̫e�����Ʀr��inode</p>
*�Ÿ��s�����W�ߪ��ɮסA�ҥH���|������s���@�˦@�ΦP�@��inode
</ol> 
