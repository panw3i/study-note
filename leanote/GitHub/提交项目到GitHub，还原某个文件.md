�´�������Ŀ����ύ��[GitHub](http://github.com/ubuntuvim)�أ�

### ǰ��

������Ҫ��װ[Git](https://git-scm.com/)����װ������ο������ĵ������߹ȸ����ѣ���

### ����

1. ����������Ŀ
2. ִ��git�����ʼ����ĿΪgit��Ŀ�����`git init`��
3. �޸���Ŀ�µ��ļ�`.gitignore`�����û�����Լ����������ļ���ִ����Щ�ļ�����Ҫ�ύ��GitHub������`node_modules`�Ѿ���Ŀ���е����ÿ��Բ��ύ��
4. ����Զ��git��ַ��ִ�����` git remote add origin https://github.com/ubuntuvim/mongodb_proj.git`��
5. ���£����ύ֮ǰ����ȸ��£�����Ϊ��`git fetch`��`git merge origin/master`
6. �ύ��Ŀ�ļ�������git�⣬���`git add *`Ȼ����ִ��`git commit -am "��ע��Ϣ"`��`-a`��ʾ�ύ���У����ֻ���ύĳ���ļ����Բ����������������Ҫ�ƶ��ύ���ļ����Ǹ������磺`git commit app.js -m "��ע��Ϣ"
7. ͬ����Զ�̵�GitHub�����`git push origin master`������ǵ�һ���ύ��Ҫ�����û��������䣬��������Ϊ��`git config --global user.name "ubuntuvim"`��`
git config --global user.email "1527254027@qq.com" `�������Լ�ע��github�˻����û������������á�
8. ָ���û���������֮���ٴ�ִ��`git push origin master`����������Ҫ��������GitHub���˻������룬�������Լ�ע���û��������롣 
9. �ȴ��ύ��ɣ�Ȼ��GitHub����Ӧ��Ŀ�£����Բ鿴���ո��ύ�����ݡ�

## �ύ��github������

### ��or create a new repository on the command line

```
echo "# ddlisting" >> README.md
git init  //�����ember cli���������Ŀ����Ҫִ���ⲽ
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/ubuntuvim/ddlisting.git
git push -u origin master
```
### ��or push an existing repository from the command line(ǿ���ύ������ԭ���ļ�)
```
git remote add origin https://github.com/ubuntuvim/ddlisting.git
git push -u origin master
```

## git��ԭ�ļ�

������뻹ԭĳ���ļ������°汾����ʹ����������ʵ�֡�
```shell
git checkout fileName
```

��ԭһ���汾���޸ģ������ṩһ�������Git�汾�ţ�����'git revert bbaf6fb5060b4875b18ff9ff637ce118256d6f20'��������ͨ��git log��ѯ�汾�ŵĹ�ϣֵ��
```SHELL
git revert �汾��
```

## ǿ�Ƹ��¸��Ǳ����ļ�
```shell
git fetch --all  
git reset --hard origin/master 
git pull
```
��������������ʹ�����������ǿ�Ƹ���Զ�̿⵽���ء�
```shell
git pull https://github.com/ubuntuvim/ddlisting.git master
```

## ��¡ĳ����֧
����������ǿ�¡��֧master    
```bash
git clone -b master http://xxxx/xx.git
```