## Установка

Для выполнения задания не требуется устанавливать сервер Spark. При установке пакета
`pyspark` через `pip`, он включает в себя все необходимые Spark-бинарники для локального режима работы. В таком режиме Spark запускается как локальный процесс на  компьютере, и можно использовать все функции Spark без отдельной установки или запуска Spark-кластера. Spark при запуске SparkSession автоматически поднимает локальный Spark-сервер (standalone mode) внутри процесса Python.

```
conda create -n covid-bigdata python=3.10
conda activate covid-bigdata
conda install jupyter pandas matplotlib seaborn
pip install pyspark
```

Установка может занять время(pyspark-4.0.1.tar.gz (434.2 MB) 15 минут).

Spark работает со старой версии джавы, поэтому необходимо еще пару шагов:

```
brew install openjdk@11
export JAVA_HOME="/usr/local/opt/openjdk@11"
export PATH="$JAVA_HOME/bin:$PATH"
```

Далее выбираем в анаконде covid-bigdata environment и запускаем JupiterLab. Убеждаемся что в JupiterNotebook выбрано ядро, соответствующее этому окружению.

Если не поможет можно запустить из консоли где выбрано нужное окружение и java path:
```
jupyter lab
```
