# 3.12 空间管理
空间管理可以允许用户对跟自己账户相关的空间进行操作，操作的范围跟账户在空间下的「角色」有关。另外，每个账户最多可以存在于3个空间下，这3个空间包括账户自己创建的空间和其他用户的空间。

?>「空间」是Kubernetes的Namespace概念。同一个区域下的多个空间或者多个区域下的同名空间之间资源隔离，进程相互独立。
***

## 3.12.1 属性说明
### <span id="jump1">3.12.1.1 空间属性</span>
空间自身的属性，包含空间名、空间类型、描述信息。

**1. 空间名：**空间一旦创建完成，「空间名」就不能被修改。

!> **命名规则：**2-30位的小写字母、数字或"-"，不能以"-"开头

**2. 空间类型：**当前空间的使用模式，分为简易模式和原生模式，且只能为其中的一种。空间一旦创建完成，不能被修改。

?> **简易模式：**使用平台的可视化简易操作<br>
   **原生模式：**使用kubernetes原生的dashboard和kubectl

**3. 描述信息：**用户自定义的空间描述信息，可以通过「编辑」操作进行修改。

**4. 关联的扣费账户：**当前空间下如果产生费用，将从该账户的余额中扣除。

**空间创建后，如何指定关联的扣费账户？**<br>
空间创建后，会默认指定空间创建人的账户为扣费账户。如果想要更换扣费账户，请发邮件到qcos-pd@qiniu.com，由相关工作人员处理。

### <span id="jump1">3.12.1.2 空间人员属性</span>
空间人员在空间内的属性，包含邮箱、角色。

**1. 邮箱：**账户在平台注册/登入时的邮箱地址。

**2. 角色：**当前空间下账户的角色信息，分为管理员和成员。

?> **管理员：**能够操作空间下组件资源，也能够进行人员管理。一个空间下要保证至少有一名管理员。<br>
   **成员：**能够操作空间下组件资源，但是不能进行人员管理。
***

## 3.12.2 如何创建空间
操作如下：

**1）点击控制台左边栏的「空间管理」，切换至空间管理界面**

**2）点击「新建空间」，开始创建一个新的空间**

!> **每个账户最多可以存在于3个空间下：**如果列表中已经存在3个空间，用户将不能主动创建新的空间和被拉取到他人空间<br>
***

## 3.12.3 如何编辑空间描述信息
操作如下：

**1）点击控制台左边栏的「空间管理」，切换至空间管理界面**

**2）点击目标空间最右侧的「编辑」**
***

## 3.12.4 如何添加人员到空间
只有「管理员」才有权限添加人员到空间，如果你已经是管理员，可以操作如下：

**1）点击控制台左边栏的「空间管理」，切换至空间管理界面**

**2）点击目标空间右侧的「人员管理」，进入人员管理界面**

**3）点击「添加人员」，开始添加一个新的人员到空间**

!> 添加人员之前请一定确保邮箱地址正确，否则可能导致邮箱不存在或者添加了其他人员进入空间。
***

## 3.12.5 如何修改人员角色
当前人员角色分为「管理员」和「成员」。只有「管理员」才能够修改人员角色，如果你已经是管理员，可以操作如下：

**1）点击控制台左边栏的「空间管理」，切换至空间管理界面**

**2）点击目标空间右侧的「人员管理」，进入人员管理界面**

**3）点击目标人员右侧的「角色管理」，就可以对当前人员的角色进行更改**

!> 如果当前空间下有且只有一名管理员时，管理员在指定一名新的管理员之前，不能对自身做角色修改。
***

## 3.12.6 如何将人员移出空间
只有「管理员」才有权限将人员移出空间，如果你已经是管理员，可以操作如下：

**1）点击控制台左边栏的「空间管理」，切换至空间管理界面**

**2）点击目标空间右侧的「人员管理」，进入人员管理界面**

**3）点击目标人员右侧的「移出空间」**

!> 如果当前空间下有且只有一名管理员时，管理员在指定一名新的管理员之前，不能够将自己移出空间。
***