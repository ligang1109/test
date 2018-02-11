# 概述

rigger是一个项目环境搭建工具，用于解决多人开发时的统一环境配置问题

本项目的示例都是用的项目中的[demo](https://github.com/Andals/rigger/tree/master/demo)目录中的内容

# 使用方法

需要[gpm](https://github.com/Andals/gpm)

## 部署

```
git@github.com:Andals/rigger.git
cd rigger
andals-gpm install
./deploy/deploy.sh host1 host2 ...
```

这会将rigger工具安装至目标主机的/usr/local/bin下

## 项目中使用

首先，需要填写指导rigger执行所需要的配置文件，详见：[rigger配置文件](https://github.com/Andals/rigger/wiki/rigger%E9%85%8D%E7%BD%AE%E6%96%87%E4%BB%B6)

示例运行：

```
rigger -rconfDir=/home/ligang/go/src/rigger/demo/conf/rigger/ prjHome=/home/ligang/go/src/rigger/demo
```

示例中的参数说明：

- -rconfDir：必选参数，放置rigger配置文件的目录，请用绝对路径

- prjHome：可选，和项目相关，这里是因为demo的配置文件[var.json](https://github.com/Andals/rigger/wiki/rigger%E9%85%8D%E7%BD%AE%E6%96%87%E4%BB%B6#varjson)中会用到
