# Covid vaccination study
 The goal of this project is to test the hypothesis that there is a correlation between vaccination rate, weather and the spread of Covid-19 (both in new cases and deaths) in Sweden. Specifically, we wanted to 

  1. Prove that vaccines help reduce the spread of Covid-19.
  2. Prove that cold temperatures increase the rate of transmission.

In our project we gathered relevant datasets, preprocessed and analysed the data. We used two methods for testing correlation namely Random Forrest and Chi2 test of independence. Based on our analysis we concluded that both vaccination and temperature are correlated to Covid-19 cases and deaths.


## How to run the code
To run the code first, make sure that HDFS is setup correctly and run:

```bash
$HADOOP_HOME/sbin/hadoop-daemon.sh start namenode
$HADOOP_HOME/sbin/hadoop-daemon.sh start datanode
```
Navigate to the project directory and put datasets to HDFS.

```bash
$HADOOP_HOME/bin/hdfs dfs -mkdir /data
$HADOOP_HOME/bin/hdfs dfs -put covid-data-per-country.csv  /data
$HADOOP_HOME/bin/hdfs dfs -put stockholm_daily_mean_temperature.csv /data
```

Next, install required python libraries using pip in the project directory: 

```bash
pip install -r requirements.txt
```
Lastly, start jupyter notebook:
```bash
jupyter-notebook experiments.ipynb
```
Make sure that port number for localhost and python version in a "setup" section of the notebook are set correctly. 