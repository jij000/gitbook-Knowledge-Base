# Behavioral Design Pattern

## Chain of Responsibilitiy Pattern 责任链模式

* 为请求创建一个 接收此次请求对象 的链 \(一个请求需要多个对象协作处理\)
* 
![](../.gitbook/assets/image%20%2823%29.png)

## Command Pattern 命令模式

* 将"请求"封装成对象, 以便使用不同的请求
* 解决了应用程序中对象的职责以及它们之间的通信方式

![](../.gitbook/assets/image%20%2810%29.png)

## Interpreter Pattern 解释器模式

* 给定一个语言, 定义它的文法的一种表示, 并定义一个解释器, 这个解释器使用该表示来解释语言中的句子
* 为了解释一种语言, 而为语言创建的解释器

## Iterator Pattern 迭代器模式

* 提供一种方法, 顺序访问一个集合对象中的各个元素, 而又不暴露该对象的内部表示

## Mediator Pattern 中介者模式

* 定义一个 "封装一组对象如何交互" 的对象
* 通过使对象明确的相互引用来促进松散耦合, 并允许独立地改变它们的交互

## Memento Pattern 备忘录模式

* 保存一个对象的某个状态, 以便在适当的时候恢复对象

![](../.gitbook/assets/image%20%2822%29.png)

## Observer Pattern 观察者模式

* 定义了对象之间的一对多依赖, 让多个观察者对象同时监听某一个主题对象, 当主题对象发生变化时, 它的所有依赖者\(观察者\)都会收到通知并更新
* 只要被观察的对象内容发生改变, 就自动调用notifyObservers方法去通知观察者类做更新

![Observer Pattern Class Diagram ](../.gitbook/assets/image%20%283%29.png)

## State Pattern 状态模式

* 允许一个对象在其内部状态改变时, 改变它的行为

![](../.gitbook/assets/image%20%282%29.png)

## Strategy Pattern 策略模式

* 定义了算法家族, 分别封装起来, 让它们之间可以互相替换, 此模式让算法的变化不会影响到使用算法的用户
* 消除大量的if...else...
* 例如做一个促销策略接口, 各种促销类实现该接口, 然后再促销行为是选择合适的促销类来达到不同的促销方式, 常用于促销, 返利业务场景

![Strategy Pattern Class Diagram](../.gitbook/assets/image%20%284%29.png)

## Template Pattern 模板方法模式

* 定义一个算法的骨架, 允许子类去实现其中的步骤
* 可以一次性实现算法的不变部分, 把可变部分留给子类实现

## Vistitor Pattern 访问者模式

* 封装作用于某数据结构\(如List/Set/Map等\)中的各元素的操作
* 可以在不改变各元素的类的前提下, 定义作用于这些元素的操作
* 通俗来说: 对相同的数据做不同的操作

![](../.gitbook/assets/image%20%2819%29.png)

