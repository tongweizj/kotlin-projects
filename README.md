# kotlin_City-Weather

## 版本说明

0.02 分支，实现基本的业务逻辑
## Milestone

- 0.01 init
  基于304课程的kotlin android 的starter，实现了网络等功能。在这个基础上增加自己的业务逻辑
- 0.02 
  - [x] 城市列表独立
  - [x] 导航，进入单城市详情页，无数据
  - [x] 天气预报的api调用走通了
  - [x] 单城市详情页显示天气数据
  - [x] 整理代码
- 0.03 存数据库
  - [x] 接入ROOM
  - [x] 一次性存入城市、天气
  - [x] 收藏城市，取消收藏
  - [x] 页面基本完成 
  - [ ] 重构代码
  - [ ] 

## 页面重构

- citylist 每个城市增加地标建筑的图片
- weather 详情页，地表图，显示在顶部

## 收藏+数据库功能逻辑

APP启动时
1. 从数据库取
   1. 城市数据， 生成城市列表，收藏城市列表
   2. 天气数据

2. 如果数据库没有城市数据
   1. 从本地将城市数据导入
3. 如果没有当天的天气数据，开始更新数据，并存入。

收藏操作
1. 点击fav 页面
   1. 如果没有收藏的城市，显示为空
2. 在城市页面，点击收藏、取消收藏
   1. 在数据库中，修改城市数据的收藏字段
   2. 修改本地缓存：收藏城市列表


数据分为2层
1. 本地缓存 state
2. 数据库

天气数据要带日期
