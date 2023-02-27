## LOCI课题组页面食用手册

### 基本信息

技术选型: Hugo + Github Pages Markdown编写格式
 
链接：https://ujnloci.github.io/zh/

安装hexo:
https://gohugo.io/installation/windows/

添加一个新成员
hugo new content/authors/firstname-lastname


配置页面相关
进入到config/_defaulf/*页面下
config
│
└───_defaulf
│   │   config.yaml 主站点配置，例如en/zh light/night
│   │   languages.yaml 语言配置
│   │   menus.en.yaml 英文页面
│   │   menus.zh.yaml 中文页面
│   │   params.yaml 定制化

成员页面相关
---
title: 欧阳谨
# Username (this should match the folder name)
authors:
  - 欧阳谨
superuser: false
role: 研一
organizations:
  - name: 济南大学
    url: 'https://www.ujn.edu.cn/'
bio: My research interests include distributed robotics.
interests:
  - 人工智能
  - 网络空间安全
education:
  courses:
    - course: 计算机科学与技术 硕士
      institution: 济南大学
      year: 2022
    - course: 计算机科学与技术 学士
      institution: 珠海科技学院
      year: 2018
# Social/Academic Networking
# For available icons, see: https://wowchemy.com/docs/getting-started/page-builder/#icons
social:
  # Email
  - icon: envelope
    icon_pack: fas
    link: 'mailto:test@example.org'
  # Github
  - icon: github
    icon_pack: fab
    link: https://github.com/xxx
	# 你也可以加别的

# 这个不用写
email: 'xxxx'

user_groups:
  - 在读学生
---

这里可以写点你自己想留下的话，支持markdown格式




协同开发

1. 创建个Github账号
2. Fork ujnloci(切记，要把only master分支fork取消掉，我们需要将所有分支fork下来) -> https://github.com/ujnloci/ujnloci.github.io
3. Git clone 你fork下来的本地帐号开始开发
4. cd Directory
5. git branch -a 查看分支
6. git checkout develop 切换到开发分支
7. git checkout -b mydevelop 创建一个属于你自己的工作分支
8. 各种操作~(这里的各种操作指拿到源码后修改生成的Public)
9. git add .
10. git commit -m "update"
11. git checkout develop 切换回开发分支
12. git merge --no-ff mydevelop 合并你的工作分支到开发分支
13. git branch -d mydevelop 删除你的工作分支
14. git push origin develop 推送到自己的远程仓库
15. 提交Pr到ujnloci等待审核合并。（最好提前跟管理员说一下你更改了哪些地方）

答疑相关

有什么问题可以在这里进行留言

Q1：xxx文件？

A1：xxxx
