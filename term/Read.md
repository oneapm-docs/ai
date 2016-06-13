#术语解释
<br>

##OneAPM 常用术语

###Apdex

 - Apdex (Application Performance Index) 是由 Apdex 联盟制定的国际应用性能指数标准，用来量化用户对应用性能的满意程度。

 - Apdex 定义了 3 个用户的满意度区间，即
<table>
	<thead>
		<tr>
			<th>满意程度</th>
			<th>阈值</th>
			<th>评分</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td> 满意 </td>
			<td> < T </td>
			<td> 1.0 </td>
		</tr>
		<tr>
			<td>容忍</td>
			<td>T~4T</td>
			<td> 0.5</td>
		</tr>
		<tr>
			<td>失望</td>
			<td> > 4T</td>
			<td> 0 </td>
		</tr>
	</tbody>
</table>
- 其中，T 为用户自定义的响应时间阈值。	<br>

- Apdex 指数 = (1.0 * 满意样本数 + 0.5 *容忍样本数)/样本总数。这样，抽象的应用性能满意度被量化为 0、1 之间的数值（0 代表没有满意用户，1 则代表所有用户 都满意）。
 
###Web 事务

- 一个事务，表示一个从“用户请求 ->webserver->DB->webserver-> 用户请求”的完整过程。通常表现为一个 HTTP 请求。OneAPM 会把这样一个请求定义为 Web事务。

###后台任务

- 非 Http 请求的，类似于 [1.JCronTab;2.JavaTimer;3.Cron4J;4.Quartz;]在后台定时运行的 Job， OneAPM 会把这样 Job 定义为后台任务。

###DataBase
- OneAPM 数据库的监控主要是帮助开发者找出数据库操作中的慢sql操作并且这个慢sql是由哪个方法执行的并展示其相互关联的调用关系和耗时情况。

###吞吐量

- 应用吞吐量，是指应用程序每分钟被调用的次数（cpm，即 Calls Per Minute）。吞吐量可以反映应用系统对于用户请求的响应能力。

### JVM
- JVM，英文全称为 Java Virtual Machine，是指 Java 虚拟机，OneAPM 的 JVM 监控分为三部分，分别是：[1.内存;2.线程;3.会话;]
 <!--pobiao-->   
1. 内存：Java 的内存通常分为堆内存和非堆内存，堆内存由 Java 对象使用，非堆内存 则用于存放 JNI、Java 线程对象等非 Java 数据。
OneAPM JVM 内存监控会实时展示：

  * Java 堆内存和非堆内存使用情况；
  * GC 每块内存的执行频率和消耗时间；
  * ClassLoad 的使用情况。
	<br>
	<br>
2. 线程：OneAPM 线程监控实时展示 Java 程序中每个线程 的最大值和最小值，以及活跃线程数和非活跃线程数。

3. 会话：OneAPM 会话监控实时展示 Session 创建的次数，以及 Session 的活跃数值和 Session 的过期数值。

###Web External

- OneAPM 把 Http 请求调用的第三方服务接口定义为 Web External。

###错误率

- OneAPM Error 监控会实时展示应用程序返回出错以及抛出异常等异常状况的详细信息，包括错误率图和错误列表这 2 个部分。

###性能剖析

- OneAPM 性能剖析工具可以在不影响用户体验的情况下，监控并分析特定时间内执行的线程执行情况，CPU消耗情况，代码性能消耗情况，有了这项功能您可以：
<!---->
1. 发现代码级别的性能瓶颈

2. 揭开应用程序堆栈的缺陷（虚拟机、应用服务器、集成中间件等）

###拓扑

- OneAPM 拓扑功能实时展现程序间端到端的调用情况，比如，A，B，C，3个节点的调用情况，可以展现各个节点的业务调用逻辑并显示出各个节点相互调用的耗时信息，并可以实现不同节点数据关联打通，比如Java 端和 PHP端的相互调用。

###服务器列表
-  服务器，此处是指应用服务器，区别于一般所说的物理服务器。当一个应用运行在多个应用服务器上时，我们在每一个应用服务器上部署Ai探针，就可以监控应用在不同应用服务器的运行情况及服务器性能指标在服务器列表中展示。


##Data Retention	

- Data retention（数据存储）是指 Application Insight 内置的数据存储功能，系统将会自动保存从 OneAPM 探针接受到的数据。

###存储时间

- Application Insight 免费版用户数据的存储时间为 1 天；专业版用户 Metric Data 存储时间为 30 天， Trace Data 存储时间为 15 天。

- 数据存储时间如下表所示： 

<table>
	<thead>
  		<tr>
    		<th>数据类型</th>
			<th>免费版</th>
    		<th>专业版</th>
 		</tr> 
 	</thead>
	<tbody>
		<tr>
			<td>Metric Data</td>
			<td>1 天</td>
            <td>30 天</td>
        </tr>
		<tr>
			<td>Trace Data</td>
			<td>1 天</td>
            <td>15 天</td>
		</tr>
	</tbody>
</table>



###数据类型
- Application Insight 的数据类型包括 Metric Data 和 Trace Data 两类。
####1. Metric Data
- Metric Data 是指 Application Insight 基于用户数据得出的统计结果。如图中标注的 Apdex、Web 事务响应时间、Web 事务吞吐量和错误率等性能数据。

![](http://i.imgur.com/AeDSQC6.png)

- 主要的 Metric Data 如下表所示：

<table>
	<thead>
		<tr>
			<th>产品</th>
			<th>Metric Data</th>
	   	</tr>
	</thead>
	<tbody>
		<tr>
			<td>Application Insight</td>
			<td>
				Apdex<br>
   				吞吐量<br>
 				响应时间<br>
 			 	错误率<br>
 			 	CPU 使用率<br>
 			 	Memory 使用率<br>
			</td> 
		</tr>
	</tbody>
</table>
####2. Trace Data
- Trace Data 是指 Application Insight 得到的影响用户应用性能的关键信息。
如图中标注的错误列表

![](http://i.imgur.com/RKnE8BN.png)

- Trace Data 包含内容如下表所示： 

<table>
	<thead>
		<tr>
			<th>产品</th>
			<th>Trace Data</th>
	   	</tr>
	</thead>
	<tbody>
		<tr>
			<td>Application Insight</td>
			<td>
				慢事务追踪<br>
   			    最慢组件<br>
 				错误列表<br>
			</td> 
		</tr>
	</tbody>
</table>
###数据展示
- Application Insight 以列表、拓扑图、折线图等多种形式向用户展示数据信息。根据用户查询时间范围选择的不同，提供相应的时间粒度。<br>
####时间选择
- Application Insight 提供不同的时间选择范围。如图所示：

![](http://i.imgur.com/0ycCri7.png)

- 以 Web 事务折线图为例，图中为最近 30 分钟的数据信息，折线图中时间粒度为 1 分钟，即折线图中点间最小时间间隔为 1 分钟。<br>
 
![](http://i.imgur.com/LsVxhmq.png)

##帮助

- 如需更多信息，欢迎访问 [http://support.oneapm.com](http://support.oneapm.com)
