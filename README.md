# 商丘工学院新闻网

### 1、前言
&emsp;&emsp;`sqgxy-xxydz-news`是在大四参加的web大赛的一个项目，与我的队友协同开发，在此过程中收获颇多。

------

### 2、介绍

&emsp;&emsp;商丘工学院新闻官网（信息与电子工程学院）包括前台新闻展示系统及后台管理系统，基于SpringBoot+Vue+MyBatis-Plus实现。前台商城系统包括首页（轮播图、通知公告、工作动态、学院动态）走进信电、学风建设、信电之星、学科竞赛、党史学习、归德书院、学校首页、联系我们、校园地图等模块。后台管理系统包括普通管理员管理、新闻管理（一级标题和二级标题绑定）、系统数据分析、待办事项、文件管理、信电之星管理、联系方式管理、关于我们、关于本站等模块。本系统UI布局严格统一，代码规范，注释到位。

----

### 3、技术选型

技术选项说明（前后端分离）

- 后端：SpringBoot、Mybatis-Plus、Apache  Shiro、Echart、百度高德地图API
- 前端：Vue、Element-UI、Vue-quill-editor（富文本编辑器）

----

### 4、项目演示

##### 1、后台管理系统

后端项目`sqgxy-xxydz-news-backed`地址：https://github.com/xmpjava/sqgxy-xxydz-news/tree/main/sqgxy-xxydz-news-backend
项目演示地址： http://180.76.56.118/#/login

##### 2、后台接口

后端项目`swagger`地址：http://180.76.56.118:10086/swagger-ui.html

项目演示地址： http://180.76.56.118:10086/swagger-ui.html

##### 3、前台新闻系统

前端项目`sqgxy-xxydz-news-fronted`地址：https://github.com/xmpjava/sqgxy-xxydz-news/tree/main/sqgxy-xxydz-news-frontend

项目演示地址：http://180.76.56.118/

---

### 5、项目部署

- 前端
- - 进入到根目录执行`npm install`，再执行`npm run serve`

- 后端
- - 修改`application.yml`中的数据库信息，然后运行即可。

---

### 6、预览图片

- 前台界面

<img src="preview/Snipaste_2022-11-25_23-00-07.png"/>
<img src="preview/Snipaste_2022-11-25_23-02-16.png"/>
<img src="preview/Snipaste_2022-11-25_23-02-55.png"/>
<img src="preview/Snipaste_2022-11-25_23-01-30.png"/>
<img src="preview/Snipaste_2022-11-30_22-57-00.png"/>
<img src="preview/Snipaste_2022-11-30_22-57-58.png"/>

- 管理员界面

<img src="preview/Snipaste_2022-11-25_23-04-38.png"/>
<img src="preview/Snipaste_2022-11-25_23-07-21.png"/>
<img src="preview/Snipaste_2022-11-30_22-59-17.png"/>
<img src="preview/Snipaste_2022-11-30_22-59-24.png"/>
<img src="preview/Snipaste_2022-11-30_22-59-32.png"/>
