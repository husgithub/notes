# 2-Jenkins配置（基于github）
### **一.准备**
1. **本地创建git项目并push至github远程仓库**
### **二.相关配置**
1. **配置jdk（全局工具配置）**
![](./pic/javahome_path.png)
![](./pic/jdkconfig.png)
2. **配置Maven**
<br>
![avatar](./pic/maven_home.png)
![avatar](./pic/maven_config_page.png)
3. **配置git**
![avatar](./pic/git_path.png)
![avatar](./pic/gitconfig_page.png)
### **三.在Jenkins中创建工程**
1. **新建任务创建一个工程**
![avatar](./pic/create_project_page.png)
2. **添加github项目地址**
![avatar](./pic/github_proj_path.png)
3. **配置源码管理**
![avatar](./pic/github_pingzheng_add.png)
![avatar](./pic/github_pingzheng.png)
以上要输入github账号和密码
4. **使用maven进行构建**
![avatar](./pic/manen_goujian_page.png)
5. **测试**
<br>
点击立即构建
![avatar](./pic/jenkins_test.png)


