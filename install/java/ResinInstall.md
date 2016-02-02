# Resin 安装 Agent

### 1. 获取授权编号

* License Key 获取<br>
 ![](/images/license_keyget01.png)

### 2. 下载
* 下载 Agent
 ![](/images/agent_download01.png)

* JDK 1.6 - 1.8  请下载
```
 wget: https://user.oneapm.com/account/5dad74ffe945c060/agent/java/OneAPM_java_Agent_latest.zip
 ```

* JDK 1.5 请下载
 ```
 wget:https://user.oneapm.com/account/5dad74ffe945c060/agent/java/OneAPM_java_Agent_legacy.zip
  ```

### 3. 安装

* 解压「Agent」至「Resin 的根目录」下
```
 unzip OneAPM_java_Agent_latest.zip -d
 <Application Server Path>/
 ```

* 写入「License Key」至配置文件「OneAPM/oneapm.properties」<br>
 模板如下：<br>
 ![](/images/ailicense_key01.png)

* 注意 license_key配置的时候不能有引号

### Resin 3.1版本之前安装 Agent 方法

* linux /unix > bin/httpd.sh -Xms200m -Xmx1024m -Xloggc:./log/gc.log -XX:MaxNewSize=256m -XX:MaxPermSize=256m -Djava.awt.headless=true

* 编辑 httpd.sh, 如下内容：
```
args='-J-server -Xms200m -Xmx1024m -javaagent:/full/path/to/OneAPM/oneapm.jar -Xloggc:./log/gc.log -XX:MaxNewSize=256m -XX:MaxPermSize=256m -Djava.awt.headless=true'
```

* win>   bin/httpd.exe -Xmn100M -Xms500M -Xmx500M -javaagent:/full/path/to/OneAPM/oneapm.jar

* install win service> bin/httpd.exe -Xmn100M -Xms500M -Xmx500M -javaagent:/full/path/to/OneAPM/oneapm.jar -install -Xss1m.

* 注意 -javaagent:后面跟 oneapm.jar 安装的绝对路径。

### Resin 3.1版本之后安装 Agent 方法

* 只需修改resin.conf,如下配置即可，比如：
```
<jvm-arg>-Xmx2048m</jvm-arg>
<jvm-arg>-Xms1024m</jvm-arg>
<jvm-arg>-javaagent:/full/path/to/OneAPM/oneapm.jar</jvm-arg>
```
* 注意 -javaagent:后面跟 oneapm.jar 安装的绝对路径。





