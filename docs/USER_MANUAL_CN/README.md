# 用户手册

此文档将详细介绍ElasticAmbari的安装和使用。

# 安装

## 从源码构建发布包

````bash
git clone https://github.com/ChengYingOpenSource/ElasticAmbari.git
cd ElasticAmbari
make
````

## 安装发布包

````bash
ambari-server install-mpack --mpack=elastic-service-mpack.tar.gz -v
````

## 重启Ambari-Server

````bash
ambari-server restart
````

## 检查安装是否成功

在Ambari-Server重启后，可以Service列表中看到ElasticSearch，这说明安装成功。

![](https://tva1.sinaimg.cn/large/703708dcly1gjw9d4bk1aj226y0zotku.jpg)

# 服务安装

- [ElasticSearch服务安装](INSTALL_ELASTICSEARCH.md)

## 卸载发布包（慎用）
在Ambari-Server上停止ES服务，并删除ES服务，然后在ambari-server节点执行卸载命令
````bash
ambari-server uninstall-mpack --mpack-name=elastic-ambari-mpack -v
````
重启Ambari-Server即可卸载该插件。