# 3.9 配置中心
配置中心可以用于管理容器的「环境变量」和「配置文件」。
***

## 3.9.1 属性说明
### 3.9.1.1 配置集
「配置集」是多个「配置项」的上层聚类。

**1. 配置集名称：**配置集一旦创建完成，「配置集名称」就不能被修改

!>**命名规则**：2-63位的小写字母、数字或"-"，不能以"-"开头或结尾<br>

**2. 关联服务：**用于显示当前「配置集」被关联到了哪些服务的「配置文件」

**3. 创建时间：**当前「配置集」创建的时间

### 3.9.1.2 配置项
「配置项」是以key-value的形式进行管理。

**1. 配置项名称：**配置项一旦创建完成，「配置项名称」就不能被修改

!>**命名规则**：2-64位的字母、数字、"-"、"."、"_"<br>

**2. 配置内容：**可以是任意字符，且支持随时修改
***

## 3.9.2 如何添加配置集和配置项
操作如下：
**1）点击控制台左边栏的「配置中心」，切换至配置中心页面** 

**2）点击「添加配置集」，完成配置集的添加**

**3）然后有两种方式可以添加配置项：**<br>
第一种是点击目标配置集最右侧的「添加配置项」icon
![重新部署](_figures/user-guide/configmap_add1.jpg)

第二种是点击目标配置集最左侧的「展开」icon，再点击「点击添加」
![重新部署](_figures/user-guide/configmap_add2.jpg)
***

## 3.9.3 如何修改配置项
「配置项」被创建后，只能修改「配置内容」。<br>
操作如下：<br>
**1）点击控制台左边栏的「配置中心」，切换至配置中心页面** 

**2）点击目标配置集最左侧的「展开」icon**

**3）点击目标配置项最右侧的「编辑」icon**
![重新部署](_figures/user-guide/configmap_edit_value.jpg)
***

## 3.9.4 如何在环境变量中应用配置集
「配置项」的「配置内容」能够被关联到多个「环境变量」的「变量值」，实现统一设置和修改，可以有效避免手动输入带来的重复操作以及出错风险。    
先要保证已经创建完成「配置集」以及「配置项」，通过「创建服务」或者「服务升级」对「环境变量」进行添加或修改，接下来操作如下：

**1）选择「环境变量」的「加载方式」为「配置集」**
![重新部署](_figures/user-guide/configmap_env1.jpg)

**2）点击「变量值」进行下拉选择目标「配置项」**
![重新部署](_figures/user-guide/configmap_env2.jpg)
***

## 3.9.5 如何在配置文件中应用配置集
「配置集」除了可以通过「环境变量」的方式注入进容器，还能以「配置文件」的形式挂载到容器内的指定目录，这样就满足了一些应用通过读取文件的方式加载配置。    
先要保证已经创建完成「配置集」以及「配置项」，通过「创建服务」或者「服务升级」对「配置文件」进行添加或修改，接下来操作如下：

**1）填写「配置文件」在容器内部的「挂载路径」**
![重新部署](_figures/user-guide/configmap_file1.jpg)

**2）点击「配置集名称」进行下拉选择目标「配置集」**
![重新部署](_figures/user-guide/configmap_file2.jpg)

?>「配置集」下的每个「配置项」都以一个配置文件挂载到容器内的「挂载路径」，其中「配置项名称」是文件名，「配置内容」是文件内容
***

## 3.9.6 如何删除配置集和配置项
### 3.9.6.1 删除配置项
操作如下：

**1）点击目标配置项最右侧的「删除」icon**
![重新部署](_figures/user-guide/configmap_delete_value1.jpg)

### 3.9.6.2 删除配置集
操作如下：

**1）点击目标配置集最左侧的「选中」icon**

**2）点击「删除配置集」**
![重新部署](_figures/user-guide/configmap_delete_value2.jpg)



