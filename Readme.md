# Vuldocker - Your Home Cloud Penetration System

![Vuldocker](./vuldocker.png)
<p align="center">
    <i>A Home Cloud Container Platform Built For Learning Penetration And Network Security</i>
</p>

![snapshot](./Desktop.png)

采用Docker容器搭建渗透测试和漏洞环境，用于记录分享渗透测试学习和代码审计
容器以Appfile的形式安装部署在[CasaOS](https://casaos.io/)上

- **容器中可能包含漏洞，强烈建议不要部署在生产环境**


## 使用文档

### 安装CasaOS

1. 准备一个X86或ARM架构设备，比如树莓派、玩客云、各种工控机、云服务器等

2. 安装一个相对纯净的系统（支持的操作系统列表如下）


```
官方支持

Debian 11 (✅ Tested, Recommended)
Ubuntu Server 20.04 (✅ Tested)
Raspberry Pi OS (✅ Tested)

社区支持

Elementary 6.1 (✅ Tested)
Armbian 22.04 (✅ Tested)
Alpine (🚧 Not Fully Tested Yet)
OpenWrt (🚧 Not Fully Tested Yet)
ArchLinux (🚧 Not Fully Tested Yet)
```

3. 使用root权限账户后运行下列一键安装脚本，稍等5分钟即可（和网速相关）

```
wget -qO- https://get.casaos.io | sudo bash
```
或者
```
curl -fsSL https://get.casaos.io | sudo bash
```

4. 浏览器输入主机IP可进入CasaOS的UI界面

![](https://bg9ega.cn/wp-content/uploads/2022/03/20220322150338.jpg)

### 安装应用


### Pull镜像

```
docker pull  vuldocker/xxxx
```
- xxxx 为需要pull的镜像名

**每个环境对应的详细使用方法我会写在该环境目录的Readme中**

###  启动容器

```
docker run -d -p 8080:80 --name abc  vuldocker/xxxx
```
-  -d   后台启动 ， -p 指定映射的端口   abc为指定容器名 
-  如果需要容器开机自启，可以加上 --restart always 选项
-  如果pull速度较慢，推荐使用 [中科大 Docker Mirrors](https://lug.ustc.edu.cn/wiki/mirrors/help/docker) 或者使用 [阿里云 Mirrors(加速器)](https://cr.console.aliyun.com/#/accelerator)

### 访问目标

访问 `http://a.b.c.d:8080/` 即可访问目标地址，开始学习相关漏洞了~

### 应用列表
*   [x]  [KunLun-M](https://github.com/arch3rPro/Vuldocker/tree/master/Tools/KunLun-M) - 开源的静态白盒扫描工具，支持PHP、JavaScript的语义扫描，基础安全、组件安全扫描，Chrome Ext\Solidity的基础扫描
*   [x]  [Reverse-shell-generator](https://github.com/arch3rPro/Vuldocker/tree/master/Tools/Reverse-shell-generator) - Hosted Reverse Shell generator with a ton of functionality. -- (Great for CTFs)
*   [x]  [Viper](https://github.com/arch3rPro/Vuldocker/tree/master/Tools/Viper) - Redteam operation platform with webui 图形化红队行动辅助平台
*   [x]  [WebMap](https://github.com/arch3rPro/Vuldocker/tree/master/Tools/WebMap) - Nmap Web Dashboard and Reporting
  
