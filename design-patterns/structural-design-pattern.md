# Structural Design Pattern

## Adapter Pattern 适配器模式

* 将一个类的接口转换成客户期望的另一个接口
* 使原本接口不兼容的类可以一起工作
* 不是软件设计阶段考虑的设计模式, 是随着软件维护, 由于不同产品, 不同厂家造成功能类似而接口不相同情况下的解决方案

![&#x5BF9;&#x8C61;&#x9002;&#x914D;&#x5668;\(&#x7EC4;&#x5408;\)](../.gitbook/assets/image%20%2815%29.png)

![&#x7C7B;&#x9002;&#x914D;&#x5668;\(&#x7EE7;&#x627F;\)](../.gitbook/assets/image%20%2860%29.png)

## Bridge Pattern 桥接模式

两个类通过组合的方式连接起来

例子: 银行类中组合进账户类\(抽象类\), 两个类可以自由发展

## Composition Pattern 组合模式

* 将对象组合成树形结构以表示 "部分----整体" 的层次结构
* 使客户端对单个对象和组合对象保持一致的方式处理

![](../.gitbook/assets/image%20%2822%29.png)

## Decorator Pattern 装饰者模式

* 在不改变原有对象的基础上, 将功能附加到对象上
* 提供了比继承更加有弹性的替代方案\(扩展原有对象功能\)

![&#x901A;&#x8FC7;&#x88C5;&#x9970;&#x8005;&#x7C7B;&#x6269;&#x5C55;&#x529F;&#x80FD;](../.gitbook/assets/image%20%2831%29.png)

![](../.gitbook/assets/image%20%2836%29.png)

## Facade Pattern 外观模式

* 又叫门面模式, 提供了一个统一的接口, 用来访问子系统中的一群接口
* 外观模式定义了一个高层接口, 让子系统更容易使用

![](../.gitbook/assets/image%20%2864%29.png)

## Flyweight Pattern 享元模式

* 提供了减少对象数量从而改善应用所需的对象结构的方式
* 运用共享技术有效地支持大量细粒度的对象
* 多用于缓冲池, 连接池
* 要注意线程安全

![EMPLOYEE\_MAP&#x4F5C;&#x4E3A;&#x4E00;&#x4E2A;&#x7F13;&#x51B2;&#x6C60;](../.gitbook/assets/image%20%2849%29.png)

## Proxy Pattern 代理模式

为其他对象提供一种代理, 以控制对这个对象的访问

例子: 房东---中介---租房者



