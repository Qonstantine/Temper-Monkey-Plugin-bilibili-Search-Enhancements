**插件介绍**

    实现以下功能:
1. 筛选日期范围内发布的视频
2. 筛选掉播放量少于()的视频
3. 根据(播放,点赞比) ,(播放,投币比),(播放,收藏比)等条件排序视频结果 
4. 结合原本的搜索条件,如分区,视频时长综合筛选 
5. 除了投币,同样的搜索方式套用到专栏上
6. 无缝翻页
7. 根据标题中的关键词去掉视频
8. 根据简介中的关键词去掉视频
---
7.26 - 创建仓库,选择开源协议GPL3.0,开始研究他人代码
1. Bilibili搜索页面筛选增强脚本，增加今年、本月、当日发布筛选，可配合B站原有的综合排序、最多点击、最多弹幕、最多收藏使用。
https://greasyfork.org/zh-CN/scripts/468336-bilibili%E7%AD%9B%E9%80%89%E5%A2%9E%E5%BC%BA/code 


2. add time filter to bilibili search results
https://greasyfork.org/en/scripts/448716-bilibili-search-filter-by-time


3. bilibili官方api
https://github.com/SocialSisterYi/bilibili-API-collect


4. 时光机app,调用b站api
https://github.com/10miaomiao/bilimiao2/tree/master

---
7.31 实现基础功能之**根据投币播放比排序搜索首页结果** - 版本号: v1.0

无缝翻页功能最后做 因为大部分有效搜索结果都在前面

开发:筛选日期内发布的视频功能实现

想法: 用户在看完视频后可以选择点击按钮,好或坏, 
然后脚本会爬取这个视频的信息,获取其点赞收藏播放评论市场等数据,
根据点赞率,投币率,lg时长等参数,以一个越来越小的学习率去修改我的公式中各个值的权重
[视频评分算法]()
---
