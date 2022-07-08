<h1 align="center">Deep Sea Areas</h1>

## 🙋‍♀️Introduction

```
//do someting
```

## 🌈Contribution GuideLines

### 编码标准
#### 标准说明
* Revit API 扩展 项目所有方法封装以扩展形式体现
* 扩展方法均应以中文进行代码块注释说明（详参考案例1）

#### 案例1
``` C#
/// <summary>
/// 将公制数值转换为英制数值
/// </summary>
/// <param name="number">要转换的公制数值</param>
/// <returns>英制数值结果</returns>
public static double ConvertToFeet(this double number)
{
     return //do someting;
}
```

#### 案例1
``` C#
/// <summary>
/// 为当前文档I/O行为开启一个事务
/// <code>
/// 
/// document.NewTransaction(()=>
/// {
///     //do sometion...
/// })
/// 
/// </code>
/// </summary>
/// <param name="document">要操作的文档</param>
/// <param name="action">事务内容</param>
/// <param name="name">事务名称</param>
public static void NewTransaction(this Document document, Action action = null, string name = "Default Transaction Name")
{
    using Transaction ts = new Transaction(document, name);
    ts.Start();
    action?.Invoke();
    ts.Commit();
}
```

## 🍿Join Wechat

<p style="text-align:center">
<img style="border-radius:2%!important" 
     width="256px" 
     alt="deepseaareas" 
     src="./WeChatCode.jpg">
</p>
