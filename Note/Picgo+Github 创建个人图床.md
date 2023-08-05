---

author: aitx

title: Picgo+Github 创建个人图床

time: 2022-10-09 周日

tags: 
  - 图床
  - Picgo
  - Github
  - Typora
  - Obsidian

---

## Picgo+Github+Typora/Obsidian 创建个人图床

### Github作为图床

#### 选择Github作为图床的原因

单个仓库支持1G的文件储存，不限制总仓库数，免费

#### Github创建图床的步骤

新建个人仓库，公开，初始化仓库添加readme.md，在设置-开发者设置-个人访问token中生成新的token，勾选repo然后点击生成token


![](https://raw.githubusercontent.com/pvisanhash/PicSiteRepo1/main/note/img/202210050027874.png)
![](https://raw.githubusercontent.com/pvisanhash/PicSiteRepo1/main/note/img/202210050029712.png)


### 下载Picgo并配置

下载地址：https://picgo.github.io/PicGo-Doc/

我这里以下载Mac版本的Picgo应用，配置图床

![](https://raw.githubusercontent.com/pvisanhash/PicSiteRepo1/main/note/img/202210050034875.png)

仓库名：用户名/仓库名
分支名：main
设定Token:上步生成的token
指定存储路径：默认为img/
指定自定义域名：默认即可，如果使用CDN则需要自定义

设置Picgo的服务地址，默认即可，如果被修改了，参考下图修改回来

![](https://raw.githubusercontent.com/pvisanhash/PicSiteRepo1/main/note/img/202210050038911.png)

其他设置

![](https://raw.githubusercontent.com/pvisanhash/PicSiteRepo1/main/note/img/202210050039015.png)

时间戳重命名：可以解决相同文件名的图片上传失败
上传后自动复制URL：打开，可以用作粘贴

### 软件集成Picgo

#### Typora集成Picgo

Typora设置插入图片时的动作与上传服务设定

![](https://raw.githubusercontent.com/pvisanhash/PicSiteRepo1/main/note/img/202210050043381.png)

#### Obsidian设置Picgo

下载第三方插件：Image auto upload Plugin

![](https://raw.githubusercontent.com/pvisanhash/PicSiteRepo1/main/note/img/202210050045675.png)

 选项设定
 
![](https://raw.githubusercontent.com/pvisanhash/PicSiteRepo1/main/note/img/202210050047388.png)
