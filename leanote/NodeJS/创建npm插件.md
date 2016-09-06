###### ��[github](https://github.com/)����һ����Ŀ�����紴����Ϊ[randomNickname](https://github.com/ubuntuvim/randomNickname)����Ŀ��
���������û����npm����Ĵ��롣
###### ������npm[����](https://www.npmjs.com/)�����˺ţ������ύ��npm������Ҫ�õ���
###### `mkdir npmjs`
###### `cd npmjs`
###### `npm init`
###### ������ʾ������Ӧ����Ϣ�����òο��������á�
```shell
ubuntuvimdeMacBook-Pro:randomNichname ubuntuvim$ npm init
This utility will walk you through creating a package.json file.
It only covers the most common items, and tries to guess sensible defaults.

See `npm help json` for definitive documentation on these fields
and exactly what they do.

Use `npm install <pkg> --save` afterwards to install a package and
save it as a dependency in the package.json file.

Press ^C at any time to quit.
name: (randomNichname)
Sorry, name can no longer contain capital letters.
name: (randomNichname) randomNichname
Sorry, name can no longer contain capital letters.
name: (randomNichname) y
version: (1.0.0) 0.1.0
description: Get the name of the three kingdoms.
entry point: (index.js) y
test command:
git repository: https://github.com/ubuntuvim/randomNichname.git
keywords: nickname,random
author: ubuntuvim
license: (ISC) ISC
About to write to /Users/ubuntuvim/codes/my-npm-plugins/randomNichname/package.json:

{
  "name": "y",
  "version": "0.1.0",
  "description": "Get the name of the three kingdoms.",
  "main": "y",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "repository": {
    "type": "git",
    "url": "git+https://github.com/ubuntuvim/randomNichname.git"
  },
  "keywords": [
    "nickname",
    "random"
  ],
  "author": "ubuntuvim",
  "license": "ISC",
  "bugs": {
    "url": "https://github.com/ubuntuvim/randomNichname/issues"
  },
  "homepage": "https://github.com/ubuntuvim/randomNichname#readme"
}


Is this ok? (yes) yes
ubuntuvimdeMacBook-Pro:randomNichname ubuntuvim$
```
�������package.json֮����Ҳ���Ը���ʵ��������޸ġ�

###### ����npm��������Ŀ¼���ļ���Ŀ¼�ṹ���£�

```
npmjs
������ lib
�� ������ npmjs.js
������ test
�� ������ test.js
������ .gitignore
������ .npmignore
������ .travis.yml
������ index.js
������ LICENSE
������ makefile
������ package.json
������ README.md
```
��Щ�ļ��������ǣ�

* libĿ¼�´��ҵ���߼��ļ�
* testĿ¼�´�ŵ�Ԫ��������
* .npmignore��¼��Щ�ļ�����Ҫ��������npmjs.org
* .travis.yml�ǳ������ɷ���travis�������ļ�
* index.js������ļ�
* makefile����������make test���в���
* README.md�Ǵ�module��������ʹ�÷���

###### ��д�������
��Ҫ����ֱ�ӷ���`index.js`�����籾��������ڻ�ȡ����������������ƣ���������(��ϸ�������[github](https://github.com/ubuntuvim/randomNickname/blob/master/index.js)����)��
```javascript
//  ��1099�������л�ȡ��������
(function () {
  'use strict';
    //  һ��1099��
    var arr = [];
    //  ��ȡ�������
    function getNickname() {
        //  ȡ0~1099�������
        var random = Math.floor(Math.random() * 1099);
        if (random >= 1099)
            throw new Error("��ȡ���������±��½ᣡ");
        return arr[random];
    }
    exports.getNickname = getNickname;
  }());
```
###### ����
```javascript
var arr = require('../index');
var s = arr.getNickname();
if (s) {
    console.log(s);
} else {
    throw new Error('The test does not pass...');
}
```

���в��ԡ�
`node ./test/test.js`

###### ��LICENSE�ļ�����������Ϣ

����������[github](https://github.com/ubuntuvim/randomNickname/blob/master/LICENSE)���ء�

###### ��дʹ���ĵ�README.md

**���ʹ�÷�ʽ**

1. ��װ���
`npm install randomNickname`

2. ʹ�ò��
```javascript
var names = require('randomNickname');
var s = names.getNickname();
console.log('�õ�����������Ϊ�� ' + s);
```

###### �ύ���뵽github

�������£�

* `git init`
* `git remote add origin <gitԶ��URL>`
* `git add *`
* `git commit -am '������Ϣ'`
* `git push origin master`
_��������������´���_

```shell
! [rejected]        master -> master (non-fast-forward)
error: failed to push some refs to 'https://github.com/ubuntuvim/randomNickname.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```

�ȸ��ºϲ����ύ��Զ�̴���⡣

* `git pull`
* `git merge origin/master`
* `git push origin/master`

###### ������npmjs����

�������£�

* `npm adduser`   (��������npmjs����ע����˺ź�����)
* `npm publish .`

������ִ���
`no_perms Private mode enable, only admin can publish this module`
ִ�����д������ú���ִ��`npm adduser`��`npm publish .`��
```
npm config set registry http://registry.npmjs.org
```

�ȴ���ɣ�����������Ϣ˵�������ɹ���
```
+ randomnickname@0.1.0
```

_�����Ĵ����޸�������Ҫ���·�����npmjs�ϣ��������޸�`package.json`��İ汾�ţ���ִ��`npm publish .`���ɡ�_

��ʱ����Ե�npmjs�ĸ��������в鿴�ոշ����Ĳ����
�����ҵĸ�������[https://www.npmjs.com/~ubuntuvim](https://www.npmjs.com/~ubuntuvim)��

**�ο����ף�**

1. [http://segmentfault.com/a/1190000000491188](http://segmentfault.com/a/1190000000491188)
2. [http://blog.csdn.net/liuxiao723846/article/details/46237289](http://blog.csdn.net/liuxiao723846/article/details/46237289)
3. [http://www.lellansin.com/npm-publish-%E5%8F%91%E5%B8%83%E7%A4%BA%E4%BE%8B.html](http://www.lellansin.com/npm-publish-%E5%8F%91%E5%B8%83%E7%A4%BA%E4%BE%8B.html)
