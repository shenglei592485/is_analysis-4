# 接口：getCourses  [返回](../README.md)
用例： [显示课程列表](../用例1/查看课程列表.md)

- 功能：
   根据学期和专业显示学生的课程列表。
    
- 权限：
    学生。    
    
- API请求地址： 
    接口基本地址/v1/api/getCourses

- 请求方式：
    GET

- 请求实例：

        {
            "student_id": "201510414202",
            "semester_data": "2017-2018学年第1学期"
        }
        
- 请求参数说明:        

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |student_id|学生学号|
  |semester_data|学生所修的学期，格式必须固定|
  * 注：只能由"学生"访问该场景。
  
- 返回实例：

        { 
            "status": true,
            "info": null,
            "data": {
                "courses": [{
                    "course_id": "11111",
                    "course_name": "J2EE程序设计",
                    "techer": {
                        "techer_id": "11111",
                        "name": "张三"
                    }
                },{
                    "course_id": "111112",
                    "course_name": " 大学英语（B）",
                    "techer": {
                        "techer_id": "11112",
                        "name": "李四"
                    }
                }]   
            }    
        }

- 返回参数说明：    
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|
  |data|返回主体信息JSON串|
  |courses|返回符合条件的所有课程集合，若空则返回[]|
  |course_id|课程编号|
  |course_name|课程名称|  
  |teacher|老师信息|
  |teacher_id|老师编号|
  |teacher_name|老师姓名|
