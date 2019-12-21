# multiple thread 多线程

{% embed url="https://www.liaoxuefeng.com/wiki/1252599548343744/1255943750561472" %}



##  synchronized

## `wait`and`notify`

\_\_[_https://www.liaoxuefeng.com/wiki/1252599548343744/1306580911915042_](https://www.liaoxuefeng.com/wiki/1252599548343744/1306580911915042)\_\_

`wait`和`notify`用于多线程协调运行：

* 在`synchronized`内部可以调用`wait()`使线程进入等待状态；
* 必须在已获得的锁对象上调用`wait()`方法；
* 在`synchronized`内部可以调用`notify()`或`notifyAll()`唤醒其他等待线程；
* 必须在已获得的锁对象上调用`notify()`或`notifyAll()`方法；
* 已唤醒的线程还需要重新获得锁后才能继续执行。

## ReentrantLock

{% embed url="https://www.liaoxuefeng.com/wiki/1252599548343744/1306580960149538" %}

## `Condition`

\_\_[_https://www.liaoxuefeng.com/wiki/1252599548343744/1306581033549858_](https://www.liaoxuefeng.com/wiki/1252599548343744/1306581033549858)\_\_

`Condition`可以替代`wait`和`notify`；

`Condition`对象必须从`Lock`对象获取。

