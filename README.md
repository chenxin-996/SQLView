# SQLView
MySQL数据库中视图View详解



### 一、什么是视图

在SQL中，视图是基于SQL语句的结果集的可视化的表。

MySQL是从5.0.1版本开始提供视图功能，视图包含行和列，就像一个真实的表。视图中的字段就是来自一个或多个数据库中的真实的表中的字段。我们可以向视图添加SQL函数、WHERE以及JOIN语句，我们也可以提交数据，就像这些来自于某个单一的表。

通俗的讲，视图就是一条SELECT语句执行后返回的结果集。

### 二、视图的特性

视图是对若干张基本表的引用，是一张虚拟表，是查询语句执行的结果，不存储具体的数据。

基本表数据发生了改变，视图也会跟着改变，数据还是存储在原来的表里，可以跟基本表一样，进行增删改查操作。

一般来说，我们只是利用视图来查询数据，不会通过视图来操作数据。

### 三、视图的作用

1、选取有用的信息，筛选的作用

视图可以隐藏一些数据。

2、操作简单化，所见即所需

可以展现特定的数据，而无需重复设置查询条件，简化操作。

3、保护数据，增加数据的安全性

视图可以只展现数据表的一部分数据，对于我们不希望让用户看到全部数据，只希望用户看到部分数据的时候，可以选择使用视图。

4、提高逻辑的独立性

当真实的数据表结构发生了变化，可以通过视图来屏蔽真实表的结构变化，从而实现了视图的逻辑独立性。

5、简化复杂的SQL操作，不必知道它的查询细节

### 四、视图的使用场景

在开发的过程中，界面的数据需要使用到某一些表的数据，但是存在一些字段（列）的冗余，此时我们并不需要全部数据返回，只需要指定字段数据即可。

例如，权限控制的时候，我们不希望用户访问表中某些含敏感信息的列，关键信息来源于多个复杂关联表，此时就可以创建视图提取我们需要的信息，简化操作。



