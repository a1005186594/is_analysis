<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：getTerm  [返回](../README.md)
用例： [学期列表](../用例/学期列表.md)

- 权限：
    访客：不能看到学期列表

- 功能：
    返回所有学期的列表。

- API请求地址：
   接口基本地址/v1/api/getTerm

- 请求方式 ：
    GET

- 返回实例：

        {
            "status": true,
            "info": null,
            "total": 121,
            "data": [
                {
                    "COURSE_ID":学期编号,
                    "COURSE_NAME":学期名称,
                },
                {
                ...其他学期
                }
            ]
        }

- 返回参数说明：

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|
  |total|返回学期数|
  |data|所有学期的数组|