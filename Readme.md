# Vuldocker - Your Home Cloud Penetration System

![Vuldocker](./vuldocker.png)
<p align="center">
    <i>A Home Cloud Container Platform Built For Learning Penetration And Network Security</i>
</p>

![Desktop](./Desktop.png)


采用Docker容器搭建渗透测试和漏洞环境，用于记录分享渗透测试学习和代码审计
容器以Appfile的形式安装部署在[CasaOS](https://casaos.io/)上

- **容器中可能包含漏洞，强烈建议不要部署在生产环境**

## 应用列表

*   [x]  [KunLun-M](https://github.com/arch3rPro/Vuldocker/tree/master/Tools/KunLun-M) - 开源的静态白盒扫描工具，支持PHP、JavaScript的语义扫描，基础安全、组件安全扫描，Chrome Ext\Solidity的基础扫描
*   [x]  [Reverse-shell-generator](https://github.com/arch3rPro/Vuldocker/tree/master/Tools/Reverse-shell-generator) - 多功能反弹Shell命令生成器
*   [x]  [Viper](https://github.com/arch3rPro/Vuldocker/tree/master/Tools/Viper) -  图形化Metasploit红队行动辅助平台
*   [x]  [WebMap](https://github.com/arch3rPro/Vuldocker/tree/master/Tools/WebMap) - Nmap 图形化Web版控制台和报告生成工具
*   [x]  [Rips](https://github.com/arch3rPro/Vuldocker/tree/master/Tools/Rips) - 一款不错的静态源代码分析工具，主要用来挖掘 PHP 程序的漏洞
*   [x]  [NPS](https://github.com/arch3rPro/Vuldocker/tree/master/Tools/NPS) - 一款轻量级、高性能、功能强大的内网穿透代理服务器
*   [x]  [Pentest-Collaboration-Framework](https://github.com/arch3rPro/Vuldocker/tree/master/Tools/Pentest-Collaboration-Framework) - 开源、跨平台和便携式工具包，用于在执行各种测试工作时自动化常规流程
*   [x]  [Acunetix](https://github.com/arch3rPro/Vuldocker/tree/master/Tools/Acunetix) - AWVS 快速查找并修复使您的Web应用程序面临攻击风险的漏洞
*   [x]  [Empire](https://github.com/arch3rPro/Vuldocker/tree/master/Tools/Empire) - PowerShsell Empire是一款针对Windows平台的，使用PowerShell脚本作为攻击载荷的渗透攻击框架工具
*   [ ]  [Nemo](https://github.com/hanc00l/nemo_go) Nemo是用来进行自动化信息收集的平台
*   [ ]  [Openvas](https://www.openvas.org/) OpenVAS 是一个全功能的漏洞扫描器。它的功能包括非认证测试、认证测试、各种高水平和低水平的互联网和工业协议、大规模扫描的性能调整和一个强大的内部编程语言来实现任何类型的漏洞测试

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

4. 浏览器输入主机IP可进入CasaOS的UI界面，注册账号即可使用。


### 安装应用

#### 应用市场

CasaOS内置应用商店，可安装官网推荐的精选App，点击App Store，选择需要安装的应用，点击安装即可。

#### 自定义安装

1. CasaOS提供自定义安装APP选项，点击Apps列表右上角加号，选择自定义安装APP。
2. 可自行设置Docker镜像等信息安装应用，也可以点击右上角导入选择Appfile进行安装(本项目使用Appfile安装)
3. 选择AppFile，上传项目Tools目录下的json文件，eg：[Empire.json](https://github.com/arch3rPro/Vuldocker/tree/master/Tools/Empire/AppFile)，提交后确认安装即可。


#### 访问目标

安装成功后，在App列表页点击对应的应用访问目标（部分应用不提供Web页面，可通过API进行连接）


