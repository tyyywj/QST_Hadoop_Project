##方案设计  

方案设计——提交方案，方案中包括系统如何设计，包含哪些模块，为什么选用这些模块。

日志存储系统  
系统设计：使用Hadoop框架进行系统的开发，将日志信息存储在Hbase中，编写MapReduce程序对日志信息进行处理。  
  
统计：  
　1. UV统计：读取日志信息，获取其中的IP地址，统计不重复的IP数量  
　2. PV统计：获取日志信息中所有的IP地址，统计数量  
　3. 留存统计：获取当日/当月的所有IP，并于前一日/月的IP进行对比，统计两日/月间重复出现的IP数量  
　4. 跳转/跳转率： 获取所有从baidu跳转过来的IP，统计数量 
  
查询：  
　1. 实时查询访问数量：将日志信息存储在HBase中，可以进行实时查询  
##项目拆解
项目拆解——把需求安排在一定的时间内完成，给出项目各个阶段和小项目的完成时间。    

- 12.10~12.11  UV统计、PV统计
- 12.12~12.14 留存统计、跳转的PV、跳转率统计
- 12.14 实时查询当前show/musician访问量


