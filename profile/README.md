<h1 align="center">Deep Sea Areas</h1>

## 🙋‍♀️介绍

> 第一阶段主要以Revit作为开发对象，对Revit的API进行扩展，增加Reivt开发普适性框架，增加UI控件库（WPF）

### 代码仓库
#### Revit Wrapper
* 几何算法
* 视图帮助
* 事务管理
* 事件管理
* 数据查询
* 数据持久化
* GUI绘图

#### Revit Framework
* MVVM模板
* WPF UI Control
* 单元测试
* 帮助文档
* 日志
* 异常捕捉

#### Revit UI Control

#### Revit Lab WebView


## 🌈指南

### 编码标准
#### 标准说明
* Revit API 扩展 项目所有方法封装以扩展形式体现
* 扩展方法均应以中文进行代码块注释说明（详参考案例1）
* 扩展方法宜添加<code>Code</code>段进行使用使用（本条不作强制要求，各自判断，详参考案例2）

#### 命名规范
* 扩展类命名后缀加<code>*Extension.cs</code>
* 特征类命名后缀加<code>*Attribute.cs</code>
* 帮助类命名后缀加<code>*Helper.cs</code>
* 其他参考微软编码命名标准

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

#### 案例2
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

## 🍿加入我们

<p style="text-align:center">
<img style="border-radius:2%!important" 
     width="256px" 
     alt="deepseaareas" 
     src="./WeChatCode.jpg">
</p>
