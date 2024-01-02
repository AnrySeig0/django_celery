# django_celery

# Project base
Django 4.2.8 (LTS) 
Celery v5.3.6 

NOTE: các lib đi kèm khi cài celery
```
amqp-5.2.0
billiard-4.2.0
celery-5.3.6
click-8.1.7
click-didyoumean-0.3.0
click-plugins-1.1.1
click-repl-0.3.0
kombu-5.3.4
prompt-toolkit-3.0.43
python-dateutil-2.8.2
six-1.16.0
tzdata-2023.3
vine-5.1.0
wcwidth-0.2.12
```


# Start Celery Worker
```shell
sh ./run_celery.sh
```


# Running a task
```shell
$ python ./manage.py shell
>>> from demoapp.tasks import add, mul, xsum
>>> res = add.delay(2,3)
>>> res.get()
5
```