# 概要说明
* src 里面是源代码 practice
* bin 程序入口
* lib 和程序解耦的一些函数,比如hash计算
* log  程序的日志
* db   程序的数据,比如用户的基本信息,用户的账单信息
* doc  程序相关文档

# 功能
普通用户功能<br>
2. 可取款 <br>
3. 定期还款（每月指定日期还款，如15号）--未实现,能还款,不能定时<br>
4. 可存款<br>
5. 定期出账单<br>
6. 支持多用户登陆，用户间转帐<br>
7. 支持多用户<br><br><br>
管理员功能 <br>
8. 管理员可添加账户、指定用户额度、冻结用户等<br>
1. 指定最大透支额度<br>
这里改变了下,全部通过adduser的逻辑改变

# 测试方式
* 程序入口 dan04.bin.start_atm.py
* 使用admin  123456 登录
* 系统中现在有几个帐号,自己可以建帐号测试
* 输入?,查看帮助,里面的所有功能都支持
* 注意: adduser的步骤中,该输入数字的地方,不要输入其他字符,没有判断,会直接报错,其他地方基本上都又验证的。


# 附加
* 用户密码使用common模块的函数利用md5加密
* 使用了装饰器,验证用户状态,是否为admin,是否被冻结
* 架构设计,不同文件放在不同的目录中
* 利用logging函数来记录日志
* 使用配置文件的概念,不会修改的东西都放在 config/setting.py
* 使用模块之间的调用
* 使用主函数的概念

# 问题
* lib/common.py show_my_log()  会多次打出日志


# 优化
## 20160901
* 拼音的地方修改为了英文
* 优化much
* 优化项目的提示（使用信用卡的时候）