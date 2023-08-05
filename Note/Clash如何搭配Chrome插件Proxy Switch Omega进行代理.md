---

author: aitx

title: Clash如何搭配Chrome插件Proxy Switch Omega进行代理

time: 2022-10-09 周日

tags: 
  - Clash
  - ProxySwitchOmega
  - Chrome

---

# Proxy Switch Omega 

 Poxy Switch Omega插件是Chrome的一个扩展，用于自定义规则进行代理。但在安装Clash后，出站模式为规则并开启系统代理后，可能会产生冲突，这时可以考虑以下方式解决。

# 启用Clash系统代理

应用（比如Git）已经配置了需要http代理，则必须要开启Clash的系统代理功能，这时需要禁用Proxy Switch Omega插件

![Git已配置代理](https://raw.githubusercontent.com/pvisanhash/PicSiteRepo1/main/note/img/202210070006865.png)
![](https://raw.githubusercontent.com/pvisanhash/PicSiteRepo1/main/note/img/202210070006221.png)

# 启用Proxy Switch Omega插件

如果应用未依赖Clash系统代理，则考虑将Clash的系统代理关闭，开启Proxy Switch Omega插件，这里使用 EXtension Manager插件配置分组以实现不同场景启用不同的插件

![](https://raw.githubusercontent.com/pvisanhash/PicSiteRepo1/main/note/img/202210070010981.png)

# 同时开启系统代理与Proxy Switch Omega

往往我们既需要给其他应用开启系统代理，又需要Chrome浏览器开启Proxy Switch Omega，这时我们可以考虑给Clash 的配置文件加上如下的规则：

打开配置文件夹

![](https://raw.githubusercontent.com/pvisanhash/PicSiteRepo1/main/note/img/202210070017416.png)

选择编辑配置文件

![](https://raw.githubusercontent.com/pvisanhash/PicSiteRepo1/main/note/img/202210070018614.png)

在rules处添加规则

Mac系统：

```yaml
rules:
    - 'PROCESS-NAME,Google Chrome Helper,代理节点配置'
    - 'DOMAIN,www.baidu.com,DIRECT'
```

如果是Windows系统：

```yaml
rules:
    - 'PROCESS-NAME,chrome.exe,代理节点配置'
    - 'DOMAIN,www.baidu.com,DIRECT'
```

注意Chrome中在SwitchyOmega内设置为直连的域名将不经过Clash直接访问，设置为代理的域名将无视Clash规则直接代理