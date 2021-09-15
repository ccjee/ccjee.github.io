# 知识管理迭代过程

<!--more-->
# 知识管理迭代过程
## 十进制
### 笔记YAML基本元素
```
Title（标题）:
Link（链接）: 
Author（作者）: 
- 
Date（时间）: 
Tags（标签）: 
- 
```
### 基本结构
<details>
  <summary>点击查看</summary>

	- 收集箱
		- 内容地图
		- TODO
		- 待处理：待处理笔记汇总，编辑总结后，分类至【项目】
	- 项目：进行中的精进方向
		- 管理
		- 实践
		- 课程
		- 工作
		- 个人发展
	- 个人
		- 简历
		- 法律
		- 医疗
		- 住房
		- 事件
	- 兴趣
	- 归档

</details>

### 总结
- 收集箱
	- TODO
		- 问题：每日清单过于细化，部分清单时间跨度大，无法及时清理list
		- 思路：每周为单位
	- 待处理
		- 问题：笔记内容添加太多，未能及时归档
		- 思路：资讯内容收集、阅读、直接归档
- 项目
	- 问题：涵盖的领域多，分类过于笼统，导致笔记分类管理时，需要耗费很大精力
	- 思路：细化分类，关注于进行中的内容
## P.A.R.A第一版
### 基本结构
<details>
  <summary>点击查看</summary>

	- 收集箱
		- 内容MOC
		- TODO
		- 待处理：连接$\dashrightarrow$项目、资源、归档
	- 项目：进行中的精进方向
		- 管理
		- 实践
		- 课程
		- 工作
		- 兴趣
	- 领域：项目内容涉及的领域，【领域】的分类借鉴【中图法】
		- 健康
		- 财务
		- 工作
		- 旅游
		- 爱好
		- 活动
		- 住房
		- 事件
		- 法律
		- 朋友
		- 住房
		- 汽车
		- 生产力
	- 资源：项目内容涉及的资源（文档、视频、音乐等），对应【领域】分类
		- 认知与思维
		- 哲学
		- 经济学
		- 人物
		- 信息收集与整理
		- 新趋势
		- 新观念
		- 协作、组织与管理
		- 历史
		- 技术
		- 习惯养成
		- 项目管理
		- 咖啡
		- 运营
		- 装修
	- 档案：参照项目的文档编辑
		- 参考
			- 书籍
			- 文章
			- 视频
			- 音频
			- 附件
		-  ZK卡片
</details>

### 总结
- 收集箱
	- TODO
		- 问题：任务进行状态分类不详细
		- 思路：笔记内容作为重点，将TODO移至【项目】中，状态分类细化（进行中、待确认、已完成等）
- 领域
	- 大类作为一级类目，细化二级类目
## P.A.R.A第二版
### 基本结构
<details>
  <summary>点击查看</summary>

	- 收集箱
		- 内容地图
		- 待处理
	- 项目
		- 进行中
		- 待确认
		- 计划中
	- Areas领域
		- 重点
			- 工作
			- 软件技能
			- 内容输出
			- 健康
			- 编程
			- 财务
		- 娱乐
			- 影视
			- 阅读
			- 音乐
			- 旅行
			- 资讯
		- 其他
			- 人际
			- 事件
		- 未分类
	- 资源
		- 物品清单
		- 活动
		- 工作
		- 课程
		- 影视
		- 阅读
		- 音乐
		- 工具
		- 未分类
	- 归档
		- 参考
		- ZK卡片

</details>

### 笔记关联
笔记YAML状态关联【标签】+【状态分类】
### 标签
- 工作
- 学习
- 生活
- 娱乐
- 未分类
### 状态分类
- 稍后计划
- 准备进行
- 定期进行
- 当前进行
- 暂时停止
- 未分类
#### 笔记YAML元素
```
---
Title: 
Link: 
Author: 
- 
keywords:
- 
finished:
- 待处理√
- 进行中
- 跟进中
- 已完成
- 已归档
Date: {{Date:YYYYMMDD}}{{time:HHmm}}
Catagories: 
- 
Tags: 
- 
---
```