# jenkins_config
wget -O /etc/yum.repos.d/jenkins.repo http://jenkins-ci.org/redhat/jenkins.repo
rpm --import http://pkg.jenkins-ci.org/redhat/jenkins-ci.org.key
yum install jenkins
yum install java

usermod -a -G docker jenkins
service jenkins restart

git tag -a v1.0
git push origin v1.0

Gitlab hook plugins
检查gitlab 代码有更新后自动触发构建

参考文档
https://www.cnblogs.com/kevingrace/p/6479813.ht


gitlab hook
https://blog.csdn.net/a18210148948/article/details/69563290

--------------------------------------------------------------------------------------------------------------------------------------------
jenkins 安装gitlab; gitlab hook;gitlab auth 插件

项目添加webhooks
进入project-setting-Integrations-添加url和token(jenkins: http://gitlab.example.com:8088/project/ansible-playbook-Advanced-Generated获取token)


gitlab_config_outbond
Admin Area-setting - Outbound requests  


after seed  do ops
https://www.cnblogs.com/caoj/p/7815820.html

Build Triggers
Build after other projects are built


build with Parameters

This project is parameterized  	
  Parameter Type -> Tag

-------------------------------------------------------------------------------------------------------------------------------------------

邮件告警配置
- 安装插件Email Extension Plugin
- Manage Jenkins - Configure System - Jenkins Location(添加Jenkins URL 和System Admin e-mail address发件箱)
- 相同结构-配置Extended E-mail Notification 配置SMTP server 和高级配置User Name和密码
- 相同接头-配置E-mail Notification 配置SMTP server 和高级配置User Name和密码 和Extended E-mail Notification 保持一致

- 项目配置-添加Post-build Actions- E-mail Notification 和 Extended E-mail Notification 配置相应参数

参考链接: https://blog.csdn.net/u010798968/article/details/74075021
          https://www.cnblogs.com/huangenai/p/7136093.html



-------------------------------------------------------------------------------------------
备份jenkins配置

参考链接

https://blog.csdn.net/tengdazhang770960436/article/details/62043154

