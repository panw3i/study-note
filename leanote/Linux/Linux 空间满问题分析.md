## ���������� 
 
�û���ϵͳ�ڽ��д����ļ���ʱ�򣬳��ֿռ䲻����ʾ����No space left on device ���� 
 
## ������̣� 
 
Linux ϵͳ�ռ�����������ԭ������� 
��1�������������� 
��2������inode�ľ��� 
��3����ʬ�ļ�����ɾ���ļ�������ռ��δ�ͷŵ�����Ӧ�ռ�δ�ͷš� 
 
 
����3������Ĵ���˼·�ֱ�˵�����£� 

#### 1�����������������ռ�ʹ�÷��� 
  a)   ʹ������ָ��鿴�ռ�ʹ�����  
```shell
# df -hT

Filesystem          Type   Size  Used Avail Use% Mounted on
tmpfs               tmpfs   16G  228K  16G   1% /dev/shm
/dev/sda1           ext4   477M   59M 393M  13% /boot
```
  b)    ʹ������ָ����������Ŀ¼�Ŀռ�ռ�����  
```
du -m --max-depth=1 |sort -gr
```
������ռ�ռ����ߵ�Ŀ¼������ִ������ָ��𲽶�λռ�ù��߿ռ���ļ���Ŀ¼��Ȼ�������Ӧ���� 

#### 2��inode����������inodeʹ�÷��� 
 
 a)     ʹ������ָ��鿴inodeʹ����� 
```
df -i
```
b)     ʹ������ָ�����inodeʹ�����  
```
for i in /*; do echo $i; find $i | wc -l; done
```
������inodeռ����ߵ�Ŀ¼������ִ������ָ��𲽶�λռ�ù��߿ռ���ļ���Ŀ¼��Ȼ�������Ӧ���� 

#### 3����ʬ�ļ����� 

a)     ʹ������ָ��鿴�Ѿ�ɾ�������Ǿ��δ���ͷŵ��ļ���ʬ�ļ�����ռ�ռ������� 
```
for i in `lsof | grep delete | awk -F" "'{print $9}'` ;do du -h $i;done | sort -gr
```
b)     ʹ������ָ�����������ʬ�ļ���������ID 
```
 for i in `lsof | grep delete | awk -F" "'{print $9}'` ;do du -h $i;done | sort -gr
```
c)     ʹ������ָ��鿴��Ӧ�Ľ�����Ϣ�� 
```
ll /proc/[size=font-size:9.0pt,9.0pt]<pid[size=font-size:9.0pt,9.0pt]��Ϣ>/exe
[size=font-size:9.0pt,9.0pt]���磺
# ll /proc/10835/exe
```

d)     ������Ӧ���̺󣬾����ͷ���Ӧ������ͷű�ռ�õĿռ䡣 


ԭ�ģ�[https://bbs.aliyun.com/read/252526.html?spm=5176.bbsl229.0.0.oGEWk1&fpage=2](https://bbs.aliyun.com/read/252526.html?spm=5176.bbsl229.0.0.oGEWk1&fpage=2)
 