JavaScript
====================

1. ``var``, ``let``, ``const`` 的区别
    a. ``var`` 能重复声明
    #. ``var`` 存在变量提升（声明会提升到作用域最前面）, ``let``, ``const`` 存在暂时性死区（未声明前不能使用）
    #. ``var`` 最小作用域为函数作用域, ``let``, ``const`` 有块作用域
    #. ``const`` 声明的变量不能再次赋值

#. ``null``, ``undefined`` 的区别
    - ``null`` 表示空对象
    - ``undefined`` 表示已经声明但是未赋值

#. JavaScript中的数据类型
    a. JavaScript中的数据类型分为基本类型和引用类型
    #. 基本数据类型: ``String``, ``Number``, ``string``, ``Boolean``, ``Undefined``, ``Symbol``, ``BigInt``, ``Null``.
    #. 引用数据类型: ``Object``, ``Array``, ``Function`` 等

#. 如何判断数据类型
    a. ``typeof`` 是否用于判断除 ``Null`` 外的基本类型和函数
    #. ``instanceof`` 用于检测对象是否是某构造函数的实例（检查原型链）
    #. 通过对象的 ``constructor`` 获取构造函数
    #. Object.prototype.toString.call() 通用且准确

#. ``this`` 指向
    a. 作为对象方法调用时，指向调用对象
    #. 作为构造函数使用，指向新创建的对象实例
    #. 作为普通函数独立调用时，非严格模式指向 ``window``，严格模式为 ``undefined``
    #. ``call``, ``apply``, ``bind`` 为显示绑定，当指定对象不是 ``undefined``, ``null`` 时，为指定对象，否则为 ``window``
    #. 箭头函数中的 ``this`` 继承自外层作用域
