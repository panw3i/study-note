�����linuxϵͳ�ﰲװ����JDK�أ�

* ����JDK��װ����`/opt/jdk`�£���������
```shell
sudo cp -r /home/ubuntuvim/software/jdk1.7.0_65 /opt/jdk/
```
�ҵ�JDK����`/home/ubuntuvim/software/`Ŀ¼�¡�

* ���û�������

�༭�ļ�` ~/.bashrc`
```shell
sudo  ~/.bashrc
// �������ļ�ĩβ������������
export JAVA_HOME=/opt/jdk/jdk1.7.0_65
export PATH=$JAVA_HOME/bin:$PATH
export CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar
```
ִ������ʹ��������Ч
```
source ~/.bashrc
```

* �����Ƿ����óɹ�

���ն�������
```shell
java -version
```
��������������Ϣ˵�����óɹ���
```
java version "1.7.0_65"
Java(TM) SE Runtime Environment (build 1.7.0_65-b17)
Java HotSpot(TM) 64-Bit Server VM (build 24.65-b04, mixed mode)
```