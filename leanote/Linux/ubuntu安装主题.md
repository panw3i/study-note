* ���ư�װ����`/opt/apache-maven-3.0.5`��
* ���ã���`sudo gedit ~/.bashrc`

```shell
export M2_HOME=/opt/apache-maven/apache-maven-3.0.5
export M2=$M2_HOME/bin
export MAVEN_OPTS="-Xms256m -Xmx512m"  // ��ѡ
export PATH=$M2:$PATH
```

* ���������ļ���ʹ����Ч

```shell
source ~/.bashrc
```

* �����Ƿ����óɹ�

���ն�����`mvn -v`�������������������Ϣ˵�����óɹ���

```shell
Apache Maven 3.0.5 (r01de14724cdef164cd33c7c8c2fe155faf9602da; 2013-02-19 21:51:28+0800)
Maven home: /opt/apache-maven/apache-maven-3.0.5
Java version: 1.7.0_65, vendor: Oracle Corporation
Java home: /opt/jdk/jdk1.7.0_65/jre
Default locale: zh_CN, platform encoding: UTF-8
OS name: "linux", version: "4.4.0-21-generic", arch: "amd64", family: "unix"
```


����������ѹ��Ȼ���Ƶ�`/usr/share/themes`�������������޸����⼴�ɡ�

���������޸�Ȩ��
```shell
sudo cp -r ./themeName /usr/share/themes
sudo chmod -R 777 /usr/share/themes/themeName
```