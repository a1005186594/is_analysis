<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：addStudentsCourse  [返回](../README.md)
用例： [老师选课](../usecase/老师选课.md)

- 功能：
    添加老师所选课程。
    
- 权限：
    老师：选择课程必须先登录。    
    
- API请求地址： 
    接口基本地址/v1/api/setPassword

- 请求方式 ：
    POST

- 请求实例：

        {
            "course_id":1234,
            "coursename":信息系统分析与设计
            "term":2016~2017第一学期
        }
        
- 请求参数说明:        

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |course_id|课程的ID号。对应表COURSE.COURSE_ID的值|
  |coursename|课程名称。不能为空。| 
  |term|课程对应学期。不能为空。| 
  
- 返回实例：

        {         
            "status": true,
            "info": null,    

        }
 
- 返回参数说明： 
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|
