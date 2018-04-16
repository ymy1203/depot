# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...

# 笔记
# 结构

* 控制器位于  app/controllers
* 视图位于   app/views
    
## 模型
* Active Record ： rails 提供的ORM （对象—关系映射）库。

## 视图和控制器
* Action pack  : rails 把视图和控制器捆绑在一起的组件

## 视图
1. 动态内容的三种方式
> - 嵌入式ruby (ERB) 
> - js代码的 ajax
> - XML Builder

## 控制器
* 把外部请求分派到内部动作

# 命令

1. rails generate 创建命令
> 例如： rails generate controller Say hello goobye


# RUBY
## 类型
* nil 是一个对象（ruby），表示什么都没有
## 命名
### 1 变量
1. 局部变量         小写字母下划线开头（单词下划线链接）
2. 实例变量			@开头
3. 类变量			@@开头
4. 全局变量			$开头
### 2 常量、模块名
* 大写字母开头 （驼峰式）
### 3 关键字
* def if else 等等
### 4 方法名 、方法参数
* 遵循局部变量命名规则

## 方法
```
例如：
def say_goodnight(name)
  result = 'Good night, ' + name
  return result
end
```
## 数据类型
### 字符串
* '' 单纯的字符串
*   "" 会编译反斜杠 \ 例如 \n ; 会解析 #{}
* capitalize()  将字符串首字母大写返回

### 数组和散列
#### 数组
* <<() 将值添加到数组末尾
```
ages = []
ages << my.name
a = ['ant','b','c'] 
# 等价于
a = %W{ant b c}
```
取值 a[0] #=>'ant'
#### 散列  
> 由建和值组成  => 左边的是键，右边的是值。键是唯一的

```
inst = {
    :cello              => 'string',
    :clarinet           => 'woodwind',
    :drum               => 'ppp'
}
等同于
inst = {
    cello:             'string',
    clarinet:         'woodwind',
    drum:             'ppp'
}
```

- 取值 a[:cello] #=>'string'

### 正则表达式
1.创建方式
- /pattern/   或者
- %r{pattern}  

2.匹配

- =~  判断是否匹配 
```
if line =~ /pattern/
```
## 控制逻辑
### 控制结构
1. if
```
if a > 10
  puts '大于10'
elsif a == 3
  puts '等于3'
else
  puts 'sb'
end
```
2. while
> 条件不为true时循环执行
```
while a<100 and b<=30
  ......
end
```
3. until
> 一直执行下去直到条件为true、

### 块和迭代器 
> 块指大括号或者do...end之间的代码
```
{ puts 'abc'}               # 这是一个块
do                          # 这也是一个块
  puts 'abc'
  club.enroll(person)
end
```
> 迭代器：逐个返回集合元素的方法
```
animals = %w{ant bee cat dog} #创建数组
animals.each{|animal| put animal} # 便利数组
```
* 在整数N上调用times方法
```
3.times {print "Ho!"} #=> Ho! Ho! Ho!
```
* &前缀运算符可以捕获传递给方法的块，将其作为方法的具名参数
```
def wrap &b
  print "ymy say: "
  3.times(&b)
  print "|n"
end
wrap {print "Ho!"}
```
### 异常
> 异常是Exception的类或者子类的对象
通常把方法或代码块包在begin和end之间，可以通过rescue子句某些类型的异常

## 组织结构

### 类
```
class SayController < ApplicationController
  def hello
    @time = Time.now
    @files = Dir.glob("*")
  end

  def goobye
  end
end
```
class开头，首字母大写

### 模块
作用：
* 作为命名空间，防止冲突
* 在多个类之间实现功能共享

### YAML
> 用于定义数据库的配置，测试数据。。。。

### 对象的序列化




