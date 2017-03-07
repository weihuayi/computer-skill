# Django

## 
```
$ sudo -H pip3 install Django
```

## Models

Models 是你的关于数据的单一, 限定的信息源. 包含数据的基本字段和行为.
一般情况下, 每个字段对应一个单独的数据库表

* 每个 Model 是一个 Python 类, 是 `django.db.models.Model` 的子类.
* 每个 Model 的属性代表一个数据库字段
* Django 自动生成一个数据库访问的API.

### 例子

定义一个 `Person` model, 有两个字段 `first_name` 和 `last_name`

```
from django.db import models

class Person(models.Model):
    first_name = models.CharField(max_length=30)
    last_name = models.CharField(max_length=30)
```

这个 Model 会创建如下的数据库表:

```
CREATE TABLE myapp_person (
    "id" serial NOT NULL PRIMARY KEY,
    "first_name" varchar(30) NOT NULL,
    "last_name" varchar(30) NOT NULL
);
```

* 表名字是自动产生, 但可以修改.
* id 也是自动产生, 但不能被修改.

## 使用 models

## Fields

一个 Model 唯一要求的重要部分是 Field. 一个 model 中的每一个 field
都是一个适当的 Field 类的实例化.

* 数据类型
* 如何显示 widget
* model field reference
* 也可定制自己的 field 

### Field 的选项参数

* null
* blank
* choices
* default
* help_text
* primary_key: 该 Field 是否为主键,i
    + 一般不用认定, Django 会自动生成一个
    + 只读, 如果修改就会创建一个新的对象
* unique: 


### 自动的主键字段
### 字段名字
* 可在创建字段时指定
* 也可默认, 用字段变量名字生成, first_name --> "first name"
* `ForeignKey`, `ManyToManyField`, `OneToOneField` 的第一个参数是一个类对象,
    需要显式指定 `verbose_name=....`
* 名字第一个字母小写


## 关系 Relationship

* Many-to-one relationships
* Many-to-many relationships
    + ManyToManyField 
    + the class to which the model is related
    + Fields 名字建议用复数
    + 需要编辑的类实例才加入这个字段
* One-to-one relationships
    + OneToOneField


## Models across files

其它应用中的 moddels 可以联系在一块

## Field 名字的限制

1. not reserved word
1. not two underscores


## Meta options

1. 一些辅助的信息
1. Django 已经定义了一些 meta options

## Model attributes

1. model 的 objects 属性
1. 它是 Django model 提供的数据库查寻操作的界面, 用来从数据库中重新获得类实例
1. 只能通过类访问, 不能通过类实例访问

## Model method

类实例

1. attribute
1. 
