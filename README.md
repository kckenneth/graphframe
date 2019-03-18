# GraphFrame

Making GraphFrame work in jupyter notebook

### Install Spark 
<a href=“https://medium.freecodecamp.org/installing-scala-and-apache-spark-on-mac-os-837ae57d283f”>Source</a> 

### Install pyspark
<a href=” https://www.dataquest.io/blog/pyspark-installation-guide”>Source</a> 

Download the graphframe jar file <a href=” https://spark-packages.org/package/graphframes/graphframes”>Here</a> 

### Install GraphFrame 
<a href=” https://github.com/graphframes/graphframes/issues/172”>Source</a>

I download the jar `0.3.0` version. The latest version didn’t seem to work with my Spark `2.4.0` version. 

```
graphframes-0.3.0-spark2.0-s_2.11.jar
```
From the terminal 
```
jar xf graphframes-0.3.0-spark2.0-s_2.11.jar
```
This will unzip the jar into `graphframes` folder with 4 files: `__init__.py`, `examples.py`, `graphframe.py` and `tests.py`. 
You need to zip all those files 
```
zip graphframes.zip -r *
```
You need to copy two files 
1. graphframes-0.3.0-spark2.0-s_2.11.jar → /usr/local/Cellar/apache-spark/2.4.0/libexec/jars/ 
2. graphframes.zip → /usr/local/Cellar/apache-spark/2.4.0/libexec/python/ 

Environment variable setup 
```
vi ~/.bash_profile
```
Add those lines
```
export SPARK_HOME=/usr/local/Cellar/apache-spark/2.4.0/libexec
export PYTHONPATH=/usr/local/Cellar/apache-spark/2.4.0/libexec/python/:$PYTHONP$
export PYTHONPATH=/usr/local/Cellar/apache-spark/2.4.0/libexec/python/graphframes.zip:$PYTHONP$
```
I don’t know in details which steps are most important. After following all the steps from different websites, I think those are the steps that leads me to working graphframe in jupyter notebook. 

