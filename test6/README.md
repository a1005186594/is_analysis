<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 基于GitHub的实验管理平台的分析与设计

### 成都大学信息科学与工程学院

|学号|班级|姓名|照片|
|:-------:|:-------------: | :----------:|:---:|
|201510414115|软件(本)15-1|倪嘉瑞|![flow1](../test2/touxiang.jpg)|

## 1. 概述
- 基于GitHub的实验管理平台的作用是在线管理实验成绩的Web应用系统。学生和老师的实验内容均存放在GitHUB
页面上。
- 学生的功能主要有：一是设置自己的GitHub用户名，二是查询自己的实验成绩，三是选择课程。学生的GitHub用户名是公开的，但成绩不公开。
- 老师的功能主要有：一是批改每个学生的成绩，二是查看每个学生的成绩，三是选择课程。
- 老师和学生都能通过本系统的链接方便地跳转到学生的每个GitHUB实验目录，以便批改实验或者查看实验情况。
- 实验成绩按数字分数计算，每项实验的满分为100分，最低为0分。
- 系统自动计算每个学生的所有实验的平均分。
    
## 2. 系统总体结构
![](系统总体结构.png)

界面设计参见：https://a1005186594.github.io/is_analysis/test6/ui/index.html
    
## 3. 用例图设计 [源码](src/UseCase.puml)
![](UseCase.png)

## 4. 类图设计 [源码](src/class.puml)
![](./class.png)

## 5. 数据库设计
- ### [参见数据库设计](./数据库设计.md)

## 6. 用例及界面详细设计
- ### [“学生列表”用例](./usecase/学生列表.md),[界面](https://a1005186594.github.io/is_analysis/test6/ui/index.html)
- ### [“评定成绩”用例](./usecase/评定成绩.md),[界面](https://a1005186594.github.io/is_analysis/test6/ui/评定成绩.html)
- ### [“查看成绩”用例](./usecase/查看成绩.md),[界面](https://a1005186594.github.io/is_analysis/test6/ui/查看成绩.html)
- ### [“修改密码”用例](./usecase/修改密码.md),[界面](https://a1005186594.github.io/is_analysis/test6/ui/顶部菜单.html)
- ### [“修改用户信息”用例](./usecase/修改用户信息.md),[界面](https://a1005186594.github.io/is_analysis/test6/ui/顶部菜单.html)
- ### [“查看用户信息”用例](./usecase/查看用户信息.md),[界面](https://a1005186594.github.io/is_analysis/test6/ui/顶部菜单.html)
- ### [“登出”用例](./usecase/登出.md),[界面](https://a1005186594.github.io/is_analysis/test6/ui/顶部菜单.html)
- ### [“登录”用例](./usecase/登录.md),[界面](https://a1005186594.github.io/is_analysis/test6/ui/登录.html)
- ### [“学生选课”用例](./usecase/学生选课.md),[界面](https://a1005186594.github.io/is_analysis/test6/ui/学生选课.html)
- ### [“老师选课”用例](./usecase/老师选课.md),[界面](https://a1005186594.github.io/is_analysis/test6/ui/老师选课.html)
- ### [“课程列表”用例](./usecase/课程列表.md),无界面，为下拉菜单显示
- ### [“学期列表”用例](./usecase/学期列表.md),无界面，为下拉菜单显示
    
