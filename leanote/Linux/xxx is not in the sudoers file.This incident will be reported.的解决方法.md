1.�л���root�û���,��ô�л��Ͳ���˵�˰�,������Լ��ٶ�ȥ.

2.���sudo�ļ���дȨ��,������:
```
chmod u+w /etc/sudoers
```

3.�༭sudoers�ļ�
```
vi /etc/sudoers
```
�ҵ����� `root ALL=(ALL) ALL`,�����������`xxx ALL=(ALL) ALL` (�����`xxx`������û���)

ps:����˵�������`sudoers`�����������������һ��
```
youuser            ALL=(ALL)                ALL
%youuser           ALL=(ALL)                ALL
youuser            ALL=(ALL)                NOPASSWD: ALL
%youuser           ALL=(ALL)                NOPASSWD: ALL
```

��һ��:�����û�youuserִ��sudo����(��Ҫ��������).
�ڶ���:�����û���youuser������û�ִ��sudo����(��Ҫ��������).
������:�����û�youuserִ��sudo����,������ִ�е�ʱ����������.
������:�����û���youuser������û�ִ��sudo����,������ִ�е�ʱ����������.

4.����sudoers�ļ�дȨ��,����:
```
chmod u-w /etc/sudoers
```

������ͨ�û��Ϳ���ʹ��sudo��.