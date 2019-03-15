==============================
Python Handbooks by Jinhh 
==============================

1 - Python 架构
-----------

1.1 环境参数::

    PYTHONIOENCODING=UTF-8 
    PYTHONUNBUFFERED=1 

2 - Python 模块
---------------

:argparse:
==========

定义: ``argparse`` 是python标准库里用来处理命令行参数的库::

命令行参数两种，位置参数和选项参数:

- 位置参数，程序根据该参数出现的位置来确定 如：ls root，root就是位置参数
- 选项参数，程序已经提前定义好的参数， 如：ls -l，-l就是一个选项参数

code demo::

    parser=argparse.ArgumentParse()#创建一个解析对象
    parser.add_argument() #添加命令行参数和选项
    parser.parse_args() #解析
    

:ConfigParser:
==============

Config配置文件格式::

    [section0] 
    option0 = value0 
    option1 = value1 
    option2 = value2 

    [section1] 
    option0 = value0 
    option1 = value1 
    option2 = value2

- ConfigParser.read(filename)：读取配置文件。
- ConfigParser.sections()：返回一个包含所有sections的list。
- ConfigParser.options(section)：返回包含section中所有options的list。
- ConfigParser.items()：返回一个list,其中元素为元组(option,value)。
- ConfigParser.get(section, option)：读取option的具体值，返回str
- ConfigParser.getint(section, option)：以int类型返回option值。
- ConfigParser.add_section(section)
- ConfigParser.set(section, option, value)：可直接修改现有option
- ConfigParser.write(file(filename, 'w'))

3 - 函数式、OOP、装饰器、包
-----------------------

    + 备注：一级，二级标题不可以越级    

XX::

    xxxx

3.1 函数式def联合class
==================

XX::
    
    xxxx

    - ``函数式``编程，分治思想，流程思维


3.2 OOP思想与应用
=================

XX::

    - ``面向对象``编程与应用环境
XX::

    xxxxx


3.3 装饰器的应用
================

XX::

    - ``decorator``，内置装饰器，staticmethod ，classmethod，等与自定义装饰器

XX::

    xxxxx

3.4 包-package
==============
XX::

    - 内置包，第三方包，自定义包

XX::
    
    xxxxx

Also See
--------

os模块举例::

    import os
    if os.path.exists('/path/obj'):
        print ( "its ok\n" )
