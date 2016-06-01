# Java Agent 兼容性和安装要求
本文主要针对 OneAPM 的 Java Agent 的兼容性，安装方法，配置进行展开说明。
我们支持的应用服务器和应用框架如下表所示：
<table>
	<thead> 
		<tr>
			<th>平台类型</th>
			<th>支持列表</th>
		</tr> 
	</thead>
	<tbody>
		<tr>
			<th>JDK</th>
			<td>JDK 1.5<br>
				JDK 1.6<br>
				JDK 1.7<br>
				JDK 1.8<br>
			</td>            
        </tr>
		<tr>
			<th>Java 虚拟机</th>
			<td>Oracle Hotspot JVM for Linux, Solaris, Windows, AIX UX<br>
				IBM JVM for Linux (6 - 7)<br>
				OpenJDK(1.6-1.7)<br>
				Oracle JRockit(1.6)<br>
			</td>
		</tr>
		<tr>
			<th>App/Web 服务器				
			</th>
			<td>ColdFusion 10<br>
				Glassfish 3.0 - 4.0<br>
				JBoss 4.0.5 - 7.x<br>
				Jetty 6 - 9.1<br>
				Netty 3.5 - 3.9<br>
				Resin 3.1.9 - 4.0<br>
				Tomcat 5.5 - 7<br>
				TomEE 1.5<br>
				WebLogic 9.2.3 - 12.1<br>
				WebSphere 7.0 - 8.5.5<br>
				WildFly 8<br>
			</td>
		</tr>
		<tr>
			<th>框架	</th>
			<td>CXF<br>
				Grails 1.3.7 - 2.3x<br>
				JSF(Java Server Faces)<br>
				Play 1.2.4<br>
				Play 2.0.3 - 2.3.0<br>
				Spring 3.x - 4.x<br>
				Struts 2<br>
				Hibernate3.x - 4.x<br>
				EJB2<br>
				EJB3<br>
				Jersey<br>
				Dubbo<br>
				HttpClient 3.0.1 - 4.3.0<br>
			</td>
		</tr>
		<tr>
			<th>SQL数据库</th>
			<td>jTDS open source JDBC 3.0 type 4 driver<br>
				MySQL mysql-connector-java-5.1.13-bin<br>
				Oracle ojdbc14, ojdbc5, ojdbc6<br>
				Postgres postgressql-8.4-701.jdbc3, 9.0, 9.1<br>
				SQLServer sqljdbc4<br>
				
				支持通用的JDBC驱动
			</td>
		</tr>
		<tr>
			<th>NoSQL数据库</th>
			<td>Redis<br>
				Mongodb<br>
				Memcached<br>
			</td>
		</tr>
		<tr>
			<th>消息中间件</th>
			<td>RabbitMQ 2.7<br>
				JMS 1.1 and Spring-JMS<br>
			</td>
		</tr>
		<tr>
			<th>JVM语言</th>
			<td>Play 1.2.4<br>
				Play 2.0.3 - 2.3.0<br>
				Grails 1.3.7 - 2.3x<br>
				Scala 2.9 - 2.10 async tracking<br>
			</td>
		</tr>
		<tr>
			<th>Web Services</th>
			<td>CXF</td>
		</tr>
		<tr>
			<th>其他</th>
			<td>Akka 2.0 - 2.1 async tracking<br>
				Amazon Simple Storage Service (Amazon S3)<br>
				java.net (HttpURLConnection)<br>
				JMS 1.1 and Spring-JMS<br>
				JMX<br>
				JSP - Java Server Pages 2.0 - 2.2<br>
				Quartz Job Scheduler 1.8.3 - 2.2.x<br>
				async tracking<br>
				Solr 1.4.0 - 4.0<br>
				Tuxedo<br>
			</td>
		</tr>
	</tbody>
</table>

 