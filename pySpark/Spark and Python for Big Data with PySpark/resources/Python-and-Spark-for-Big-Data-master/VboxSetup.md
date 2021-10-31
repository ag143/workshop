# setup python
```sudo apt install python3-pip```

```pip3 install jupyter```

```jupyter``    // open jupyter

```quite()``    //close python

```ctrl + c```  //shutdown jupyter

```sudo apt-get update```   ///update 'GET' mechanism

```sudo apt-get install default-jre```

```sudo apt-get install scala```

```pip3 install py4j``` 

```sudo tar -zxvf fName.tgz```

```export SPARK_HOME='home/ubuntu/spark-2.1.0-bin-hadoop2.7' ```
```export PATH=$SPARK_HOME:$PATH```
```export PYTHONPATH=$SPARK_HOME:$PATH/PYTHON:$PYTHONPATH```

```export PYSPARK_DRIVER_PYTHON="jupyter" ```
```export PYSPARK_DRIVER_PYTHON_OPTS="notebook" ```
```export PYSPARK_PYTHON=python3 ```

```sudo chmod 777 spark-2.1.0-bin-hadoop2.7```

# setup pyspark
1. go to pyspark folder to start python

2. in home folder:
    - ```pip3 install findspark```
    - <!-- in Python -->
```
import findspark
findspark.init('/home/[user]/spark-2.1.0-bin-hadoop2.7')
import pyspark
```