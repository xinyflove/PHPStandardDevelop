# PHP开发规范

## 1. 前言

为了有利于项目维护、增强代码可读性、提升 Code Review 效率以及规范团队PHP开发，故提出以下PHP开发规范，仅供参考。
如有更好建议，欢迎到 GitHub 提 issue，相互交流。

## 2. PSR规范

PSR 是 PHP Standard Recommendations 的简写，由 PHP FIG 组织制定的 PHP 规范，是 PHP 开发的实践标准。
了解更多关于PSR规范[https://psr.phphub.org/](https://psr.phphub.org/)

## 3. 命名规范

例如有一个项目MyApp，目录结构如下：

```
MyApp/
  ├── MyClass.php
  ├── Controller/
  |   ├── UserInfo.php
  |   └── UserPoint.php
  └── Model/
      ├── Info.php
      └── Point.php
```

**1. 类名和文件名采用首字母大写的驼峰式命名**  
类文件名称必须与文件内部类名相同，以便自动加载。例如：  
```
class UserInfo
{
...
```

**2. 使用命名空间**

命名空间名字与目录路径对应，并以开发者的项目根目录为基准。  
例如项目MyApp/，类文件MyApp/MyClass.php因为在项目根目录，所以命名空间省略。  
类文件MyApp/Controller/UserInfo.php因为UserInfo.php在MyApp项目的Controller目录下，所以要加上命名空间 namespace Controller;，如下：
```
namespace Controller;
class UserInfo
{
....
```

**3. 类的pubilc成员和类的pubilc方法采用首字母小写的驼峰形式**  
例如：
```
pubilc $connectionList = array();
pubilc function getConnectionList()
{
....
```

**4. 类的protected成员和类的protected方法采用一个下划线加首字母小写的驼峰形式**  
例如：
```
protected $_connectionList = array();
protected function _getConnectionList()
{
....
```

**5. 类的private成员和类的private方法采用两个下划线加首字母小写的驼峰形式**  
例如：
```
private $__connectionList = array();
protected function __getConnectionList()
{
....
```

**6. 普通函数及变量名采用小写加下划线方式**
例如：
```
$connection_list = array();
function get_connection_list()
{
....
```

**7. 类的参数和类方法的参数采用小写加下划线方式**
例如：
```
pubilc function __construct($one_param, $tow_param)
{
....
pubilc function getConnectionList($one_param, $tow_param)
{
....
```
