# zcoolJob
### 站酷数仓开发实习生日志

数据集成部分选用 aliyun 的 DataWorks + MaxCompute  
MaxCompute + DataWorks + QuickBI 来建设站酷的数据体系  
### 知识点
#### 1.指标体系
1. 基础指标：指表达业务实体原子量化属性的且不可再分的概念集合，如交易笔数、交易金额、交易用户数等。
2. 复合指标：指建立在基础指标之上，通过一定运算规则形成的计算指标集合，如平均用户交易额、资产负债率等。
3. 派生指标：指基础指标或复合指标与维度成员、统计属性、管理属性等相结合产生的指标，如交易金额的完成值、计划值，累计值、同比、环比、占比等。
4. 标准信息：经过标准化处理的实体非量化属性信息，或分段统计信息，省份（北京、广州等）、缴费方式（缴费、充值）渠道（网厅、直充、专区）、消费金额（30元、50元、100元等）。
#### 2.数据指标体系建设
1. 完成核心指标需求的整理，优先关注核心的数据指标和对应的核心维度。
2. 提炼和设计数据体系：业务过程、事实、维度。
3. 梳理业务部门、核心业务过程及各业务关心的核心指标
   - 当前业务关心的核心业务数据有哪些？有哪些潜在的分析需求。
   - 当前业务可以使用的、用来分析的数据源有哪些。
   - 当前业务有哪些数据分析的系统
4. 进行数据规划，提炼核心业务过程、数据分域、核心事实、核心维度。
5. 数据侧技术栈规划：埋点技术选型和后续演进路线、数据集成方案、数仓及BI选型。

2022/9/26 第一天
1. 入职
2. 数据烟囱
3. dataworks
4. 埋点
5. 完成提数需求 
   - 站内全站，90天内登录搜索过「blender」的全部用户UID和手机号
   - 站内全站，一年内发布的全部作品中包含「Blender」关键词的创作者UID和手机号
  
2022/9/27 第二天
1. 完成提数需求
   - 网易游戏JUSTFUN（站酷id：23483081）的粉丝且近60天内登录过的用户UID和手机号；
   - 网易CFun设计中心（站酷id：20333920）的粉丝且近60天内登录过的用户UID和手机号；
   - 梦冥轩（站酷id：12948054）的粉丝且近60天内登录过的用户UID和手机号；
   - ll晓A（站酷id：15534684）的粉丝且近60天内登录过的用户UID和手机号；
   - 在2021.1月起至今，有产生购买过直播课和录播课行为的全部人数+订单数+订单金额
2. 笛卡尔积  
3. mapreduce下的Reduce side Join  


2022/9/28 第三天  
1. 完成push数据看板

2022/9/28 第四天  
1. 优化push数据看板，使用占位符实现自定义筛选uid  

2022/10/8 第六天
1. 对ods_flow_ph进行数据清洗，创建补数据实例，创建dwd层的dwd_zcoolweb_flow_appstart_pd app启动表，清洗空字段。  

2022/10/9 -2022/10/10 第八天
1. 完成需求
   - 【站酷APP-有奖话题】sql数据需求
2. 完成数据同步，从mysql同步到数仓ODS层
