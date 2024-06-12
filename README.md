# Сурмач Андрей Андреевич
# Replication-and-scaling
# Задание_1
master-slave
Один узел – master, остальные – slaves.
Информация попадает в master, после чего сразу или через некоторое время вычитывается подчинёнными узлами.

При этом запись может происходить только в master, из slave доступно только чтение.

master-master
Все узлы – master.

Запись может осуществляться во все из них, а изменения вычитываются другими master'ами.

Итого
Основное различие – количество доступных для записи узлов. В случае master-slave, запись ведётся только на один узел и затем расходится по read-only подчинённым. В случае master-master все узлы доступны для чтения-записи и обмениваются информацией о внесённых изменениях.

# Задание_2
Master
my.cfg:

![1](https://github.com/Aid1986/Replication-and-scaling/blob/main/1.png)

status:

![2](https://github.com/Aid1986/Replication-and-scaling/blob/main/2.png)

Slave
my.cfg


![3](https://github.com/Aid1986/Replication-and-scaling/blob/main/3.png)


status


![4](https://github.com/Aid1986/Replication-and-scaling/blob/main/4.png)

![5](https://github.com/Aid1986/Replication-and-scaling/blob/main/5.png)


База данных, созданная на мастере, отображается на слейве:

Master

![6](https://github.com/Aid1986/Replication-and-scaling/blob/main/6.png)

Slave

![7](https://github.com/Aid1986/Replication-and-scaling/blob/main/7.png)
