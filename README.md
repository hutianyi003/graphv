# About

graphv，一个基于C++和JavaScript的图分析可视化工具

## 功能

### **graphv_algorithm**

核心算法API，包括：

* 最短路
* 最小生成树
* 中心度
* 不同边阈值下的连通分量

### **graphv_visual**

基于D3的可视化组件

### **graphv_creator**

通过数据建图，使用json保存结果

## 开发环境

VS 2017

## 规范

参与需遵循如下代码规范(my partner)

1. 所有类和函数统一放在名称为graphv的命名空间中
1. 不允许*仅仅*使用#pragma once来防止重复引用
1. 对每个类，如果实现了五个default函数中的任意一个或多个，应当显式地对这五个函数的**每一个**进行声明。
    1. 五个函数指拷贝构造、拷贝赋值、移动构造、移动赋值、析构函数
	1. 对仍然采用默认行为的函数，使用 = default
	1. 对禁止进行的操作，使用 = delete
	1. 特别地，对于含有动态资源的类（包括指针和容器等），**显式声明**这五个函数
1. 使用unique\_ptr代替不可共享的指针，shared\_ptr代替可以共享的指针
	1. unique_ptr几乎没有额外开销
	1. 如果使用裸指针，注释说明不使用unique_ptr的原因并说明何时释放资源
1. 使用enum class表示枚举常量
1. 不允许全局使用using namespace

## LICENSE

基于MIT LICENSE