# 1-Jenkins安装（war包部署tomcat方式）
1. **环境准备( CentOS Linux release 7.4.1708 )**
<br>
- JDK
- 安装git
2. **下载Jenkins war包**
<br>
[https://jenkins.io/zh/download/](https://jenkins.io/zh/download/)
<br>
<img src="./pic/xiazailujing.png" width="400" />
3. **将Jenkins war包放到tomcat webapps目录下**
![avatar](./pic/jenkins_war.png)
4. **启动tomcat**
<br>
![avatar](./pic/tomcat_start_log.png)
5. **访问ip:8080/jenkins/**
![avatar](./pic/jenkins_startpage.png)
按照提示输入密码并继续，选择推荐插件并安装
![avatar](./pic/chajian.png)
next<br>
如果部分插件安装失败可先忽略，之后再解决
![avatar](./pic/install_errorpage.png)
next<br>
新建一个管理员账号
![avatar](./pic/create_user_page.png)
next<br>
完成安装
![avatar](./pic/config_page.png)
![avatar](./pic/complate_page.png)

