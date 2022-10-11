---
title: Linux(CentOS7.2)安装cnpm
date: 2022-10-11 15:38:38
categories: 前端
tags: 
	- 前端 
	- cnpm 
	- npm 
	- centos
---
1、安装cnpm
```
npm install -g cnpm --registry=https://registry.npm.taobao.org
```
2、如下安装成功
```
/root/node-v10.16.3-linux-x64/bin/cnpm -> /root/node-v10.16.3-linux-x64/lib/node_modules/cnpm/bin/cnpm
+ cnpm@6.1.1
added 686 packages from 950 contributors in 17.057s
```
3、测试是否安装成功
```
cnpm -v
```
4、如果出现这样证明需要设置软引
```
-bash: cnpm: command not found
```
5、设置软引
```
ln -s /root/node-v10.16.3-linux-x64/bin/cnpm /usr/local/bin/cnpm
#OR
ln -sf /root/node-v10.16.3-linux-x64/bin/cnpm /usr/local/bin/cnpm
```
6、再次**cnpm -v**测试，如下表示成功
```
cnpm@6.1.1 (/root/node-v10.16.3-linux-x64/lib/node_modules/cnpm/lib/parse_argv.js)
npm@6.14.1 (/root/node-v10.16.3-linux-x64/lib/node_modules/cnpm/node_modules/npm/lib/npm.js)
node@10.16.3 (/root/node-v10.16.3-linux-x64/bin/node)
npminstall@3.27.0 (/root/node-v10.16.3-linux-x64/lib/node_modules/cnpm/node_modules/npminstall/lib/index.js)
prefix=/root/node-v10.16.3-linux-x64 
linux x64 3.10.0-957.21.3.el7.x86_64 
registry=https://r.npm.taobao.org

```