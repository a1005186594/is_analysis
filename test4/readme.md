# 实验4：图书管理系统顺序图绘制
|学号|班级|姓名|照片|
|:-------:|:-------------: | :----------:|:---:|
|201510414115|软件(本)15-1|倪嘉瑞|![flow1](../test2/touxiang.jpg)|

### 1.维护读者信息

**1.1 维护读者信息用例PlantUML源码**
~~~
@startuml
skinparam backgroundColor #EEEBDC
skinparam handwritten true

hide footbox
title __维护读者信息__ 用例
actor 图书管理员 
boundary 账号判断
control 业务控制
database 数据库


autonumber
group 读者账号合法性验证
activate 账号判断
	图书管理员 -> 账号判断 :  输入读者账号信息
	activate 业务控制
		账号判断 -> 业务控制 : 获取账号信息
deactivate 账号判断
		activate 数据库
			业务控制 -> 数据库 : 比对账号密码合法性
			数据库 --> 业务控制 : 账号合法
end
group 维护读者信息
			图书管理员 -> 业务控制 : 输入读者新信息
			业务控制 -> 数据库 : 修改读者信息
			数据库 -> 业务控制 : 返回操作结果
		deactivate 数据库
	业务控制 -> 图书管理员 : 返回维护读者信息结果
	deactivate 业务控制
	

end

@enduml
~~~
**1.2 维护读者信息用例顺序图**

![维护读者信息](读者信息安全维护.png)

**1.3 维护读者信息用例顺序图说明**
1.参与者：图书管理员(actor)、账号判断(boundary)、业务控制(control)、数据库(database)。
2.消息：(1)读者账号合法性判断：输入读者账号信息->获取账号信息->对比账号密码合法性->账号合法
       (2)维护读者信息：输入读者新信息->修改读者信息->返回操作结果->返回维护读者信息结果

### 2.借出图书

**2.1 借出图书用例PlantUML源码**
~~~
@startuml
skinparam backgroundColor #EEEBDC
skinparam handwritten true


hide footbox
title __借出图书__ 用例
actor 图书管理员 
boundary 账号判断
control 业务控制
database 数据库


autonumber
group 读者账号合法性验证
activate 账号判断
	图书管理员 -> 账号判断 :  输入读者账号信息
	activate 业务控制
		账号判断 -> 业务控制 : 获取账号信息
deactivate 账号判断
		activate 数据库
			业务控制 -> 数据库 : 比对账号密码合法性
			数据库 --> 业务控制 : 账号合法
end
group 借出图书
			图书管理员 -> 业务控制 : 输入借出图书信息
			业务控制 -> 数据库 : 增加借阅信息
			业务控制 -> 数据库 : 修改图书库存
			数据库 -> 业务控制 : 返回操作结果
		deactivate 数据库
	业务控制 -> 图书管理员 : 返回借出结果
	deactivate 业务控制
	

end

@enduml
~~~
**2.2 借出图书用例顺序图**

![借出图书](借出图书.png)

**2.3 借出图书用例顺序图说明**
1.参与者：图书管理员(actor)、账号判断(boundary)、业务控制(control)、数据库(database)。
2.消息：(1)读者账号合法性判断：输入读者账号信息->获取账号信息->对比账号密码合法性->账号合法
       (2)借出图书：输入借出图书信息->增加借阅信息->修改图书库存->返回借出结果


### 3.维护图书

**3.1 维护图书用例PlantUML源码**
~~~
@startuml
skinparam backgroundColor #EEEBDC
skinparam handwritten true


hide footbox
title __维护图书__ 用例
actor 图书管理员 
boundary 图书合法性判断
control 业务控制
database 数据库


autonumber
group 图书信息合法性验证
activate 图书合法性判断
	图书管理员 -> 图书合法性判断 :  输入图书信息
	activate 业务控制
		图书合法性判断 -> 业务控制 : 获取图书信息
deactivate 图书合法性判断
		activate 数据库
			业务控制 -> 数据库 : 图书是否存在
			数据库 --> 业务控制 : 图书存在
end
group 维护图书
			图书管理员 -> 业务控制 : 输入图书新信息
			业务控制 -> 数据库 : 修改图书信息
			数据库 -> 业务控制 : 返回操作结果
		deactivate 数据库
	业务控制 -> 图书管理员 : 返回维护图书结果
	deactivate 业务控制
	

end

@enduml
~~~
**3.2 维护图书用例顺序图**

![维护图书](图书信息维护.png)

**3.3 维护图书用例顺序图说明**
1.参与者：图书管理员(actor)、图书合法性判断(boundary)、业务控制(control)、数据库(database)。
2.消息：(1)图书信息合法性判断：输入图书信息->获取图书信息->图书是否存在->图书存在
       (2)维护图书：输入图书新信息->修改图书信息->返回操作结果->返回维护图书结果


### 4.归还图书

**4.1 归还图书用例PlantUML源码**
~~~
@startuml
skinparam backgroundColor #EEEBDC
skinparam handwritten true

hide footbox
title __归还图书__ 用例
actor 图书管理员 
boundary 账号判断
control 业务控制
database 数据库


autonumber
group 读者账号合法性验证
activate 账号判断
	图书管理员 -> 账号判断 :  输入读者账号信息
	activate 业务控制
		账号判断 -> 业务控制 : 获取账号信息
deactivate 账号判断
		activate 数据库
			业务控制 -> 数据库 : 比对账号密码合法性
			数据库 --> 业务控制 : 账号合法
end
group 归还图书
			图书管理员 -> 业务控制 : 输入归还图书信息
			业务控制 -> 数据库 : 删除借阅信息
			业务控制 -> 数据库 : 修改图书库存
			数据库 -> 业务控制 : 返回操作结果
		deactivate 数据库
	业务控制 -> 图书管理员 : 返回归还结果
	deactivate 业务控制
	

end

@enduml
~~~
**4.2 归还图书用例顺序图**

![归还图书](归还图书.png)

**4.3 归还图书用例顺序图说明**
1.参与者：图书管理员(actor)、账号判断(boundary)、业务控制(control)、数据库(database)。
2.消息：(1)读者账号合法性判断：输入读者账号信息->获取账号信息->对比账号密码合法性->账号合法
       (2)归还图书：输入归还图书信息->删除借阅信息->修改图书库存->返回操作结果->返回归还结果


### 5.维护管理员信息

**5.1 维护管理员信息用例PlantUML源码**
~~~
@startuml
skinparam backgroundColor #EEEBDC
skinparam handwritten true


hide footbox
title __维护管理员信息__ 用例
actor 超级管理员 
boundary 账号判断
control 业务控制
database 数据库


autonumber
group 管理员账号合法性验证
activate 账号判断
	超级管理员 -> 账号判断 :  输入管理员账号信息
	activate 业务控制
		账号判断 -> 业务控制 : 获取账号信息
deactivate 账号判断
		activate 数据库
			业务控制 -> 数据库 : 比对账号密码合法性
			数据库 --> 业务控制 : 账号合法
end
group 维护管理员信息
			超级管理员 -> 业务控制 : 输入管理员新信息
			业务控制 -> 数据库 : 修改管理员信息
			数据库 -> 业务控制 : 返回操作结果
		deactivate 数据库
	业务控制 -> 超级管理员 : 返回维护管理员信息结果
	deactivate 业务控制
	

end

@enduml
~~~
**5.2 维护管理员信息用例顺序图**

![维护管理员信息](管理员维护.png)

**5.3 维护管理员信息用例顺序图说明**
1.参与者：超级管理员(actor)、账号判断(boundary)、业务控制(control)、数据库(database)。
2.消息：(1)管理员账号合法性判断：输入管理员账号信息->获取账号信息->对比账号密码合法性->账号合法
       (2)维护管理员信息：输入归还图书管理员新信息->修改管理员信息->返回操作结果->返回维护管理员信息结果


### 6.查询图书

**6.1 查询图书用例PlantUML源码**
~~~
@startuml
skinparam backgroundColor #EEEBDC
skinparam handwritten true


hide footbox
title __查询图书__ 用例
actor 游客 
control 业务控制
database 数据库
entity 图书信息

autonumber

activate 业务控制
	游客 -> 业务控制 :  输入图书信息
		activate 数据库
			业务控制 -> 数据库 : 根据图书信息查询对应图书
			数据库 -> 业务控制 : 返回查询结果
		deactivate 数据库
		activate 图书信息
			业务控制 -> 图书信息 : 生成图书信息列表
		deactivate 业务控制
			图书信息 -> 游客	: 返回图书信息
		deactivate 图书信息

@enduml
~~~
**6.2 查询图书用例顺序图**

![查询图书](查询图书.png)

**6.3 查询图书用例顺序图说明**
1.参与者：游客(actor)、业务控制(control)、数据库(database)、图书信息(entity)。
2.消息：输入图书信息->根据图书信息查询对应图书->返回查询结果->生成图书信息列表->返回图书信息


### 7.查询借阅信息

**7.1 查询借阅信息用例PlantUML源码**
~~~
@startuml
skinparam backgroundColor #EEEBDC
skinparam handwritten true



hide footbox
title __查询借阅信息__ 用例
actor 读者 
boundary 权限判断
control 业务控制
database 数据库
entity 借书记录

autonumber
group 账号合法性验证
activate 权限判断
	读者 -> 权限判断 :  输入账号信息
	activate 业务控制
		权限判断 -> 业务控制 : 获取账号信息
deactivate 权限判断
		activate 数据库
			业务控制 -> 数据库 : 比对账号密码合法性
			数据库 --> 业务控制 : 账号合法
		
		
		
	

end
group 借书记录查询
	业务控制 -> 数据库 : 查询借阅表
	数据库 -> 业务控制 : 返回查询结果
	deactivate 数据库
	activate 借书记录
		业务控制 -> 借书记录 : 生成借书记录列表
	deactivate 业务控制
		借书记录 -> 读者 : 返回查询结果
	deactivate 借书记录
	

end

@enduml
~~~
**7.2 查询借阅信息用例顺序图**

![查询借阅信息](查询借阅信息.png)

**7.3 查询借阅信息用例顺序图说明**
1.参与者：读者(actor)、权限判断(boundary)、业务控制(control)、数据库(database)、借书记录(entity)。
2.消息：(1)账号合法性判断：输入账号信息->获取账号信息->对比账号密码合法性->账号合法
       (2)借书记录：查询借阅表->返回查询结果->生成借书记录列表->返回查询结果



