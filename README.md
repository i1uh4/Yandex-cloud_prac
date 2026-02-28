# Yandex-cloud\_prac

\# PySpark: Витрина mart\_city\_top\_products



\## Описание

Сборка витрины Top-2 товаров по выручке для каждого города

на основе данных users, orders, products.



\## Стек

\- Apache Spark / PySpark

\- Apache Zeppelin

\- Yandex Cloud Dataproc

\- HDFS / S3



\## Структура проекта

yandex-cloud-pyspark-hw/

├── README.md

└── notebooks/

└── mart\_city\_top\_products.json



\## Шаги решения

1\. Создание исходных данных (users, orders, products)

2\. Вычисление revenue = qty \* price

3\. Join: orders + users + products

4\. Агрегация по (city, product\_id, product\_name)

5\. Top-2 по revenue\_sum через оконную функцию (Window + row\_number)

6\. Запись в HDFS и S3 (parquet, overwrite)

7\. Чтение обратно и отображение результата



\## Результат

Витрина сохранена по пути:

\- HDFS: /tmp/sandbox\_zeppelin/mart\_city\_top\_products/

\- S3: s3a://YOUR\_BUCKET\_NAME/mart\_city\_top\_products/

