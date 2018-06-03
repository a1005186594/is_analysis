﻿<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：logout  [返回](../README.md)
用例： [登出](../usecase/登出.md)

- 功能：
    已经登录的用户登出平台。
    
- 权限：
    学生/老师已经登录。    
    
- API请求地址： 
    接口基本地址/v1/api/logout

- 请求方式 ：
    POST

- 请求实例：

        {
            "user_id":324111
        }
        
- 请求参数说明:        

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |user_id|已经登录用户的user_id值，对应表USERS.USER_ID的值|
  
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

