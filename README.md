# Hadoop 3 On Windows
## Step1
### Install Java & set environment variable for Java And Hadoop

Open the command prompt: Press the Windows key + R to open the Run dialog box. Type "cmd" and press Enter to open the command prompt.
Check the Java version: In the command prompt, type the following command and press Enter:

[Java](https://www.oracle.com/java/technologies/javase/javase8-archive-downloads.html)

### You need free account create one

[Login](https://login.oracle.com/mysso/signon.jsp)

### Java

```
java -version
```

```
javac -version
```

```
echo %JAVA_HOME%
```

```JAVA_HOME```
```
C:\Program Files\Java\jdk1.8.0_202
```

```in path```

```System Variables path new ```
```
C:\Program Files\Java\jdk1.8.0_202\bin
```
### Hadoop
```HADOOP_HOME```
```
C:\Program Files\hadoop-3.3.5\bin
```
```
C:\Program Files\hadoop-3.3.5
```



## Step2
### [Download Hadoop Link](https://dlcdn.apache.org/hadoop/common/)

``` core-site.xml ```
```
<property>
 <name>fs.default.name</name>
 <value>hdfs://localhost:9000</value>
</property>
``` 

``` mapred-site.xml ```
```
<property>
 <name>mapreduce.framework.name</name>
 <value>yarn</value>
</property>
```

``` hdfs-site.xml ```
```
<property>
  <name>dfs.replication</name>
  <value>1</value>
 </property>
 <property>
  <name>dfs.namenode.name.dir</name>
  <value>file:///C:/hadoop-3.3.5/data/namenode</value>
 </property>
 <property>
  <name>dfs.datanode.data.dir</name>
  <value>/C:/hadoop-3.3.5/data/datanode</value>
 </property>
```
``` yarn-site.xml ```
```
<property>
 <name>yarn.nodemanager.aux-services</name>
 <value>mapreduce_shuffle</value>
</property>
<property>
  <name>yarn.nodemanager.auxservices.mapreduce.shuffle.class</name>
  <value>org.apache.hadoop.mapred.ShuffleHandler</value>
</property>
```

``` hadoop-env.cmd```
```
set JAVA_HOME=C:\Program Files\Java\jdk1.8.0_202

```
Formate Hadoop
```
hdfs 
```

[7Zip](https://www.7-zip.org/download.html)
cmd command 
```
tar -zxvf hadoop-3.3.5.tar.gz
```
