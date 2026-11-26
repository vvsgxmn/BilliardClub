# 基于SpringBoot+Vue的台球俱乐部管理系统

![Spring Boot](https://img.shields.io/badge/-Spring%20Boot-6DB33F?style=flat-square&logo=spring-boot&logoColor=white) ![Vue3](https://img.shields.io/badge/-Vue3-grey?style=flat-square) ![MySQL](https://img.shields.io/badge/-MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white) ![MyBatis](https://img.shields.io/badge/-MyBatis-000000?style=flat-square&logo=mybatis&logoColor=white) 

## 项目介绍

本系统是一款面向台球俱乐部会员与前台运营人员的一体化经营平台，针对球桌档期难统筹、开台计费靠手记、吧台点单与台费结算割裂、教练预约与赛事报名分散、会员消费记录难追溯等问题，把球桌档案与实时状态、在线预约占台、开台计时结算、吧台商品点单、教练课程、赛事活动报名、社区评价以及管理端经营看板整合到同一套前后端分离工程中，形成“预约—开台—消费—结算—评价”的闭环。

系统采用 SpringBoot + Vue 架构，区分会员与管理员：会员端浏览球桌与教练、提交预约与赛事报名、选购吧台商品并管理个人资料；管理端维护球桌类型与档案、收银开台结算、订单与评价审核、赛事发布及公告运营。球桌封面、教练形象与商品图统一落盘 uploads，仪表盘可统计开台率、营收与热门球桌，适合作为毕设、课设与线下球房数字化改造学习参考。

## 主要功能模块

- **统一登录与角色分流**：会员与管理员统一入口登录注册，JWT 鉴权；按角色进入会员大厅或管理后台，路由与接口双重隔离
- **会员首页**：展示可预约球桌、热门赛事、教练推荐与公告资讯，快捷进入开台预约、吧台点单与赛事报名
- **球桌档案与类型**：维护斯诺克、中式八球、九球等桌型单价与封面，实时展示空闲/使用中/维护状态
- **球桌预约**：会员按日期时段提交占台申请，管理员确认或驳回，避免撞档与空置
- **开台结算收银**：前台开台计时、叠加吧台消费，按桌型单价自动汇总台费并完成结账关台
- **吧台点单**：零食饮料与球具商品浏览下单，与开台订单关联结算或独立收银
- **教练管理与约课**：维护教练简介特长与形象照，会员查看并参与相关课程或陪打安排
- **赛事活动**：发布俱乐部内部赛与报名规则，会员在线报名，管理端审核与赛程维护
- **社区评价**：会员对球桌体验与服务打分留言，管理员审核展示
- **经营数据看板**：今日开台、营收、预约待审、热销商品等 KPI，以及桌型占用与订单趋势可视化
- **公告与用户中心**：发布营业通知与活动置顶；会员维护头像资料，管理员启停账号
- **本地文件上传映射**：球桌封面、教练照、商品图与公告配图统一 uploads，对外 /api/uploads/** 访问

## 技术架构

- **后端**：Spring Boot 2.7 + MyBatis-Plus + JWT + Hutool
- **前端**：Vue 3 + TypeScript + Vue Router + Pinia + Element Plus + Vite + ECharts
- **数据库**：MySQL 8.0

<!-- screenshots-start -->
## 系统截图

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/billiardclub/%E7%99%BB%E5%BD%95%E9%A1%B5%E9%9D%A2.png" alt="登录页面" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/billiardclub/%E4%BC%9A%E5%91%98%E9%A6%96%E9%A1%B5.png" alt="会员首页" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/billiardclub/%E7%90%83%E6%A1%8C%E6%A1%A3%E6%A1%88.png" alt="球桌档案" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/billiardclub/%E7%90%83%E6%A1%8C%E9%A2%84%E7%BA%A6.png" alt="球桌预约" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/billiardclub/%E5%BC%80%E5%8F%B0%E7%BB%93%E7%AE%97.png" alt="开台结算" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/billiardclub/%E5%90%A7%E5%8F%B0%E7%82%B9%E5%8D%95.png" alt="吧台点单" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/billiardclub/%E8%B5%9B%E4%BA%8B%E6%B4%BB%E5%8A%A8.png" alt="赛事活动" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/billiardclub/%E7%AE%A1%E7%90%86%E5%91%98%E4%BB%AA%E8%A1%A8%E7%9B%98.png" alt="管理员仪表盘" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/billiardclub/%E8%AE%BA%E6%96%87%E5%9B%BE1.png" alt="论文图1" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/billiardclub/%E8%AE%BA%E6%96%87%E5%9B%BE2.png" alt="论文图2" width="600" />

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/AutoUpload/screenshots/billiardclub/UML%E5%9B%BE%E5%88%97%E8%A1%A8.png" alt="UML图列表" width="600" />

<!-- screenshots-end -->

---

## 接毕业设计和论文

### 作者微信：vvsgxmn  (支持修改、 部署调试、 支持代做毕设)

### 接网站建设、小程序

### 选题+开题报告+任务书+程序定制+安装调试+论文+答辩ppt 都可以做

### 购买地址：[https://www.vvxx.love](https://www.vvxx.love)（vv毕设网）

### 支持 **一键生成 UML 图**：上传项目压缩包即可自动产出功能模块图、用例图、流程图、E-R 图、时序图等全套毕设图表。

### 提供 **免费配套软件下载 + 安装说明 + 部署教程**

![vv毕设网 - 一键画图](https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/uml-draw.png)

<img src="https://fanhua-yingcai.oss-cn-shanghai.aliyuncs.com/image-20260825133349317.png" alt="image-20260825133349317" />

⚠️ Bug添加微信**免费修复**，免费修复。其他平台的私信一律不管（微信方便发送文件）
