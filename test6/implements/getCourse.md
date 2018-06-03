<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：getStudents  [返回](../README.md)
用例： [课程列表](../usecase/课程列表.md)

- 权限：
    访客：不能看到课程列表

- 功能：
    返回所有课程的列表。

- API请求地址：
   接口基本地址/v1/api/getCourse

- 请求方式 ：
    GET
    
- 请求参数说明：

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |term_id|学期编号|

- 返回实例：

        {
            "status": true,
            "info": null,
            "total": 121,
            "data": [
                {
                    "COURSE_ID":课程编号,
                    "COURSE_NAME":课程名称,
                },
                {
                ...其他课程
                }
            ]
        }

- 返回参数说明：

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|
  |total|返回课程数|
  |data|所有课程的数组|