���������ѧϰ����NodeJs��ʹ�õ�express��ܣ��������ϵ�ѧϰ�������٣���˱��˻ᾭ���ڿ�������һЩ�ܽᡣ

express��ȡ���������ַ�����������������
```
Checks route params (req.params), ex: /user/:id
Checks query string params (req.query), ex: ?id=12
Checks urlencoded body params (req.body), ex: id=
```
1�����磺`127.0.0.1:3000/index`����������£�����Ϊ�˵õ�`index`�����ǿ���ͨ��ʹ��`req.params`�õ���ͨ�����ַ������ǾͿ��ԺܺõĴ���Node�е�·�ɴ������⣬ͬʱ���������Էǳ������ʵ��MVCģʽ��
2�����磺`127.0.0.1:3000/index?id=12`����������£����ַ�ʽ�ǻ�ȡ�ͻ���get��ʽ���ݹ�����ֵ��ͨ��ʹ��`req.query.id`�Ϳ��Ի�ã�������PHP��get������

3�����磺`127.0.0.1��300/index`��Ȼ��post��һ��`id=2`��ֵ�����ַ�ʽ�ǻ�ȡ�ͻ���post���������ݣ�����ͨ��`req.body.id`��ȡ��������PHP��post������