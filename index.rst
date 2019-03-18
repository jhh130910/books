==============================
Python Handbooks @ by Jinhh 
==============================

1 - Python Core  
-----------

1.1 env + base set
==================

env::

    PYTHONIOENCODING=UTF-8 
    PYTHONUNBUFFERED=1 

2 - Module 
---------------

2.1 argparse
==========

Define: ``argparse`` standard library command line parameter::

Two type，position parameter and option parameter:

parameter demo::

    python xx.py arg_1 arg_2
    python xx.py -g arg_1 

code demo::

    parser=argparse.ArgumentParse()  # create an obj
    parser.add_argument() # add parameter and option
    parser.parse_args() # parse
    
2.2 ConfigParser
============

Config file format::

    [section0] 
    option0 = value0 
    option1 = value1 
    option2 = value2 

    [section1] 
    option0 = value0 
    option1 = value1 
    option2 = value2

- ConfigParser.read(filename)
- ConfigParser.sections()                  # return all sections [list]
- ConfigParser.options(section)：
- ConfigParser.items()                     # return turple(option,value)
- ConfigParser.get(section, option)        # read option value，return str
- ConfigParser.getint(section, option)
- ConfigParser.add_section(section)
- ConfigParser.set(section, option, value) # directly modify option value
- ConfigParser.write(file(filename, 'w'))

2.3 MySQLdb
===========

desc table_xx_name::

    +----------+-------------+------+-----+---------+-------+
    | Field    | Type        | Null | Key | Default | Extra |
    +----------+-------------+------+-----+---------+-------+
    | userid   | int(11)     | NO   | PRI | NULL    |       |
    | username | varchar(20) | YES  |     | NULL    |       |
    +----------+-------------+------+-----+---------+-------+

3 - OOP、decorator、package
-----------------------

3.1 def + class 
==================

def::
    
    - ``functional `` divide job and do it 

class::
    
    - __iter__, __init__

3.2 OOP
=================

XX::

    - ``OOP``apply environment


3.3 Decorator Apply 
===================

decorator::

    - staticmethod ，classmethod
    - self define 

3.4 package
==============

package type::

    - buildin | third party package | self define 

Also See
--------

os::

    import os
    if os.path.exists('/path/obj'):
        print ( "its ok\n" )

