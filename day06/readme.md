# 面向对象

# 作业

## 实现功能
        People Student Teahcer Course 4个类
        可以创建老师,创建学生,创建课程
        老师上课可以获得课时费
        学生上课可以获得上课内容
        学生可以选课
        学生可以查看已选课程和上课记录  studeng.show()
        学生可以评价课程质量,老师相应的增减资产

## 注意
        作业程序入口 day06/src/course.py
        没有做CMD界面,在文件末尾提供了一大堆测试的函数,可以随便测试
        建议使用现在有的这一个,测试过程可以参考test.md
        使用配置文件概念

## 亮点

        使用了类的继承
        使用了super（Students, self）.__init__(  )
        使用pickle存储数据
        使用配置文件概念
        使用静态方法
        使用一般变量
        使用property , 只是写在那里, 其实最终也没有用
        文件里面存储的是时间戳,显示的时候转换一下,使用字符串的格式
        pickle:   把obj写入文件,和从文件中读出obj ,单独分离出来, 增加代码重用性
        使用了成员修饰符 def __get_courses(self):
        发现一个坑:  foo = property(fget=func1, fget=func2, fdel=func3)  只能通过obj调用,使用Class可以调用,但是不生效
        
## 个人观点
        
        我看了属性,如果不是为了看别人写的代码,直接使用普通方法更加的简单直观
        还有特殊变量中的 __getitem__ __setitem__ __delitem__ 都可以通过普通方法实现
        __str__ 这个我直接写一个自定义的show来替换
