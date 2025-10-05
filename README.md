
------

# 项目名称 : k4t v2 manager console 管理控制台（k4m） 试用版 测试版

#### k4m 对标 kubectl

## 项目目的：

本软件目的是:

* 测试

* 公众预览

* 培训教学

### 不得用于生产环境!

------

# k4m 软件：

软件版本： k4m版本必须和 k4t2workerd 版本完全一致。

支持os：支持win，linux。

暂时只发布win+x64版，建议在win虚拟机中使用。

支持cpu：不支持x86，支持x64，支持arm64。

------

# k4m 功能：

* 改写 k4t2 元数据文档。即改写excel文件（*.xlsx）。

注意：你可以使用任意图形界面的程序编辑excel。
如：Libre Office，ms office，wps等。

你可以使用任意，自己开发的，tui、cli界面的程序编辑excel。
如：python开发的命令行，powershell开发的命令行，golang，rust，等。

* 经 sftp 协议和端口，复制 k4t v2 app配置 文件，到 linux k4t v2 worker被控机。

注意：k4t v2使用【k4t2_workers_list.xlsx】文件中定义的 k4t2 worker ip。

默认最优先使用ssh-key-file：k4m参数输入


默认次优先使用ssh-key-file：
win：    c:\Users\<你的win账户名>\.ssh\id_ed25519
linux：  /root/.ssh/id_ed25519


默认3优先使用ssh-key-file：
win：    c:\Users\<你的win账户名>\.ssh\id_rsa
linux：  /root/.ssh/id_rsa

* 在 k4t v2 app 容器应用生命周期中，移动app，删除app。
功能类似于k8s的 【驱逐node】【污点node】等。

------

# k4m 手册位置：

https://gitee.com/chuanjiao10/k4t2/tree/master/docs/k4m命令手册.xlsx

# k4m 用法：

#### 目的：设定k4m输出中文信息

在win，linux，powershell中的动作：
```powershell
$env:LANG = 'zh_CN.UTF-8'
```

#### 目的：设定k4m输出英文信息

在win，linux，powershell中的动作：
```powershell
$env:LANG = 'en_US.UTF-8'
```

#### 目的：应用名为【abc】，设定副本数为3。

在win，linux，powershell中的动作：
```powershell
k4m setapps "abc" copynumber 3
```

应用名支持非英文。中文，及unicode。

#### 目的：部署/编排 应用 【abc】

在win，linux，powershell中的动作：
```powershell
k4m aa deladd "abc"
```

说明：applyapp（aa）-------aa是别名

------

# 名词解释：

【master】法师。k4t v2 admin 管理人员，运维人员，技术人员

【manager】k4t v2 主控机（对标k8s master）

支持单机，主备高可用。k4t v2 主控机不支持，当做worker机执行容器应用。

【worker】k4t v2 节点机（对标k8s node）




------

#  问：谁能免费使用 k4t v2?

答：

https://gitee.com/chuanjiao10/k4t2/blob/master/docs/%E8%AE%A9%E5%85%8D%E8%B4%B9%E7%9A%84k4t%E4%B8%8E%E4%BD%A0%E5%85%B1%E8%A5%84%E7%9B%9B%E4%B8%BE.md

注意： 付费用户不受此限制。

------

# 问：k4t2 如何免费？答：类似于使用免费ai，限制使用速率/频率。

### 免费周期：分为【阳光】，【雨露】，【小绿瓶】，【中绿瓶】，【大绿棒】

#### 享受【阳光】：

每隔3天=72小时，可以使用1次k4m aa命令。

#### 享受【雨露】：

每隔2天=48小时，可以使用1次k4m aa命令。


#### 用【小绿瓶】获取仙液：

每隔1天=24小时，可以使用1次k4m aa命令。


#### 用【中绿瓶】获取仙液：

我给你一个空的【中绿瓶】，中绿瓶容量为1滴仙液。

每隔12小时，你使用【k4m getfree】命令，即可获取一滴仙液，最多保存1滴仙液。


#### 用【大绿棒】获取仙液：

我给你一个空的【大绿棒】，大绿棒容量为2滴仙液。

每隔8小时，你使用【k4m getfree】命令，即可获取一滴仙液，最多保存2滴仙液。


#### 消耗仙液：

每应用1次k4t v2 app，需要消耗1滴仙液。

更改副本数等功能后，再次应用k4t v2 app，还需要再次消耗1滴仙液。

每次停用1次k4t v2 app应用，需要消耗1滴仙液。

#### 注意：

免费用户，不能超过10台worker。cpu核心数不限，cpu频率不限，内存大小不限。付费用户不受此限制。

------

#


------


## 项目协议 LICENSE

1 k4m不开源。在限速的同时，免费使用。

2 配套的，外部的powershell脚本，内部的powershell脚本，shell脚本，yaml，excel配置文件等。除已有著作权之外的，初步考虑采用 **mit** 协议开源。

总结：
整个 k4t2 项目是由众多（开源，或商业）软件产品，组件，搭建、组合而成的。

------





## 免责声明 Disclaimer

* 使用本软件前，用户应该做好充分备份，测试。

* 本软件对用户造成的任何后果、损失，概不负责。

------


## 相关网址

# 手册：https://gitee.com/chuanjiao10/k4t2/tree/master/docs

