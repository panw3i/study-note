�޸�`pom.xml`�ļ��������������ã�
```xml
<plugin>
    <groupId>org.apache.maven.plugins</groupId>
    <artifactId>maven-compiler-plugin</artifactId>
    <version>2.5.1</version>
	<configuration>
    	<source>1.6</source>
    	<target>1.6</target>
    	<encoding>UTF-8</encoding>
    	<compilerArguments>
            <extdirs>${project.basedir}/svnkit1.8</extdirs>
    	</compilerArguments>
	</configuration>
</plugin>
```
**ע��**������`<extdirs>${project.basedir}/svnkit1.8</extdirs>`ָ�����ⲿjar������Ŀ¼��
���������ļ���`svnkit1.8`������Ŀ�ĸ�Ŀ¼�¡�


��Ŀ
  |__svnkit1.8
  |__src