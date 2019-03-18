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

CMD::    

    use <db name>; 
    
    show tables; 

    desc <table name>;

    +----------+-------------+------+-----+---------+-------+
    | Field    | Type        | Null | Key | Default | Extra |
    +----------+-------------+------+-----+---------+-------+
    | userid   | int(11)     | NO   | PRI | NULL    |       |
    | username | varchar(20) | YES  |     | NULL    |       |
    +----------+-------------+------+-----+---------+-------+

    DELETE FROM <table> WHERE <EXPR.. id=1..>;
    truncate table; （ can't recovery ）

EXAMPLE 1::
    
    import MySQLdb

    conn=MySQLdb.connect(host='localhost',user='xiaojin',passwd='',db='test',charset='utf8')
    
    cur=conn.cursor()
    
    cur.execute("""
    create table if not EXISTS jinhh1
    (
      userid int(11) PRIMARY KEY ,
      username VARCHAR(20)
    )
    """)
    
    for i in range(1,1000000):
        #print ( " test '{0}','{1}'".format(int(i), 'XX'+str(i) ) )
        cur.execute ( 
            "insert into jinhh(userid,username) values( '{}', '{}' ) ".format( int(i),'Name'+ str(i) )
            )
    
    conn.commit()
    cur.close()
    conn.close()


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

