## centos 安装环境

安装 Node.js，<a target="_blank" href="https://nodejs.org/en/download/package-manager/">官方安装方法</a>
```bash
# On RHEL, CentOS or Fedora, for Node.js v8 LTS:
curl --silent --location https://rpm.nodesource.com/setup_8.x | sudo bash -
# Alternatively for Node.js 9:
curl --silent --location https://rpm.nodesource.com/setup_9.x | sudo bash -
# 安装 Node.js
sudo yum -y install nodejs
# Enterprise Linux（RHEL和CentOS）用户可以使用EPEL存储库中的Node.js和npm包。
# 为您的版本安装相应的epel-release RPM（在EPEL存储库主页上找到），然后运行：
sudo yum install nodejs npm --enablerepo=epel
```

安装构建工具，要从npm编译和安装本地插件，您可能还需要安装构建工具：

```bash
sudo yum install gcc-c++ make
# or: sudo yum groupinstall 'Development Tools'
```

安装 MongoDB，首先创建源，创建 `mongodb.repo` 文件, 
<a target="_blank" href="https://docs.mongodb.com/manual/tutorial/install-mongodb-on-red-hat/">官方安装方法</a>

```bash
# 在/etc/yum.repos.d/目录下创建文件mongodb.repo，它包含MongoDB仓库的配置信息，内容如下：
# 复制代码, 代码如下:
[mongodb]
name=MongoDB Repository
baseurl=http://downloads-distro.mongodb.org/repo/redhat/os/x86_64/
gpgcheck=0
enabled=1
```

yum 安装 MongoDB 

```
sudo yum install mongodb-org
```

启动 mongodb

```
sudo service mongod start
```

yum 安装 git

```
sudo yum install git
```
