# Практическая работа 1

  - [Отчет по ПР1](https://github.com/savvche/distributedsystems/blob/main/practice/PR_1.pdf).
  
# Практическая работа 2

  - [Отчет по ПР2](https://github.com/savvche/distributedsystems/blob/main/practice/PR_2.pdf).

# Практическая работа 3

  - [Отчет по ПР3](https://github.com/savvche/distributedsystems/blob/main/practice/PR_2.pdf).

# Практическая работа 4

  - [Отчет по ПР4](https://github.com/savvche/distributedsystems/blob/main/practice/PR_3_1.pdf).

chat gpt по заданию 20 дал вот такой ответ и он рабочий:
Для запуска Hadoop в Docker контейнере можно использовать готовый образ, например, sequenceiq/hadoop-docker. Для запуска word count на этом контейнере необходимо выполнить следующие действия:

Запустить контейнер:
docker run -it sequenceiq/hadoop-docker /etc/bootstrap.sh -bash
Проверить, что Hadoop запущен:
hadoop version
Создать входные данные для word count:
echo "hello world" > input.txt
Скопировать входные данные в HDFS:
hadoop fs -mkdir /input
hadoop fs -put input.txt /input
Запустить word count:
hadoop jar $HADOOP_HOME/share/hadoop/mapreduce/hadoop-mapreduce-examples-2.7.1.jar wordcount /input /output
Проверить результат:
hadoop fs -cat /output/*
Теперь вы можете увидеть результат выполнения word count в консоли.
