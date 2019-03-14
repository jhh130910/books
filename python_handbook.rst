==============================
Python Handbooks by Jinhh 
==============================

模块介绍
--------

一级标题^^
^^^^^^^^^^

二级标题==
==========

三级标题>>
>>>>>>>>>>

:argparse:

定义: ``argparse`` 是python标准库里用来处理命令行参数的库::

命令行参数两种，位置参数和选项参数:

    位置参数，程序根据该参数出现的位置来确定 如：ls root，root就是位置参数

    选项参数，程序已经提前定义好的参数， 如：ls -l，-l就是一个选项参数

ConfigParser

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

函数式、OOP、装饰器、包
-----------------------

    The simplest way to install the package is via ``easy_install`` or
