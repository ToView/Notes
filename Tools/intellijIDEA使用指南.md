# intelliJ IDEA 常用设置使用指南  

### 1. 下载

[https://www.jetbrains.com/idea/](https://www.jetbrains.com/idea/ "https://www.jetbrains.com/idea/")  

### 2. 激活/破解  

[Jetbrains系列产品2019.3.3最新激活方法[持续更新]](https://zhile.io/2018/08/25/jetbrains-license-server-crack.html "https://zhile.io/2018/08/25/jetbrains-license-server-crack.html")  

破解文件&说明备用下载:  

链接:https://pan.baidu.com/s/1An57LD065JicTtf6efB6jQ  密码:6g9x  

### 3. 教程  

#### 3.1 教程文档  

[IntelliJ IDEA 简体中文专题教程](https://github.com/judasn/IntelliJ-IDEA-Tutorial "https://github.com/judasn/IntelliJ-IDEA-Tutorial")  

#### 3.2 快捷键  

进入快捷键设置: file -- settings -- Keymap  

**在删除原来的快捷键之后,强制新增，如果有冲突,会移除冲突的快捷键**  

代码提示: 搜索"show intention actions" -- 删除原来的快捷键,添加 `Alt` + `/`    

撤销: 搜索 `Undo` --- 删除原来的快捷键,新增 `Ctrl` + `Z`  

恢复: 搜索 `Redo` --- 删除原来的快捷键，新增 `Ctrl` + `Y`  

删除一行: 搜索 `Delete Line` --- 删除原来的快捷键,新增 `Ctrl` + `D`  

关闭当前编辑窗口: 搜索 `Close` --- 删除原来的快捷键,新增 `Ctrl` + `W`  

**其他常用快捷键:**  

打开设置(`settings`): `Ctrl` + `Alt` + `S`  

上/下移动代码: 选中代码,然后按 `Atl` + `Shift` + `Up/Down`  

窗口切换: `Ctrl` + `Tab`  

`try-catch`: 选中代码,然后按 `Ctrl` + `Alt` + `T`  

`setter && getter` : `Alt` + `Ins(ert)`,该快捷键也可用于新建对象  

### 4. 其他设置  

- 设置主题  

  `settings`  ---  `Appearance & Behaiver`  --- `Appearance`  --- `Theme` 选项 (`Darcula`: 酷黑色,`Intellij`: 白色)  

- 设置创建 `class` 等文件的头部提示信息  

  `settings`  ---  `Editor`  --- `File and Code Templates` --- 选择 `class` / `interface` / `Enum` 等文件  

  效果: 

  ```java
  /**
   * @Description: ${DESCRIPTION}
   * @Author: junqiang.lu
   * @Date: ${DATE}
   */
  public class ${NAME} {
  }
  ```

- 关闭自动更新

  `settings`  ---  `Appearance & Behavior`  ---  `System Settings`  ---  `Updates`  --- 取消 `Automatically check updates for ...`  选项  ---  `Apply`  

- 设置本地 `maven`  

  `Settings`  ---  `Build,Execution,Development`  ---  `Build Tools`  ---  `Maven`  ---   
  `Maven home directory` : 选择本地 `Maven` 的地址  
  (eg: `D:/develop/software/apache-maven-3.5.3`)  
  `Use settings file`: 选择本地 `Maven` 的设置文件`settings.xml`,同时勾选后边的 `Override`  
  (eg: `D:\develop\software\apache-maven-3.5.3\conf\settings.xml`)  

- 代码提示不区分大小写  

  1. `Settings`  ---  `Editor`  ---  `Code Completion`  ---  `Case sensitive completion`  ---  选择 `NONE`  
  2. `Settings`  --- 搜索 `sensitive`  ---  `Case sensitive completion` 选择 `NONE`  

- 自动导包  

  `Settings`  ---  `Editor`  ---  `General`  ---  `Auto Import`  -- 选中 `Add unambiguous implorts to fly` 和  

  `Optimize imports on the fly(for current project)`  

- 鼠标放在方法上边显示具体参数  

  `Settings`  ---  `Editor`  ---  `General`  ---  `Other(Show quick documentation on mouse move )` 选中即可，时间可以设置为 `100ms`  

- Java 类实现 `Serializable` 接口，生成 `seriaVersionUID`  

  `Setting` --- 搜索 `Serializable`  ---  在展开的 `Serialization issues` 下拉列表下边选择 `Serializable class without 'seriaVersionUID'` ，勾选即可  

- 添加 `Jrebel`  插件  (**已经失效**)

  ~~`Settings` ---  `Plugins`  --- 选择 `Browse repositories` ， 从应用市场中安装 --- 在弹出的窗口中搜索 `Jrebel`~~  

  ~~`Jrebel` 个人免费激活码网站: [https://my.jrebel.com/](https://my.jrebel.com/ "https://my.jrebel.com/")~~  

  ~~(用Facebook账号登录这个网站，就能获得一个免费的激活码,**需要饭蔷**)~~  

- 设置 `Tomcat` 热部署  

  关键点: 在 `Tomcat` 设置界面,`On 'Update' action` 和 `On frame deaction` 选项选择 `Update classes and resources` ,然后使用 `Debug 模式启动`(如果有`Jrebel` 插件,使用 `Jrebel`的 `Debug` 模式)  

- 设置 文件/工作空间 编码格式  

  设置当前项目的文件编码格式:  

  File --- Settings --- Editor --- File Encodings ,将所有编码文件编码格式都设置为 `utf-8`,BOM for new UTF-8 files 选择 `with no BOM`  

  设置 其他/新建 项目的文件编码格式:  

  File --- Other Settings --- Default Settings --- Editor --- File encodings,格式设置同上  

   

### 5 插件安装  

#### 5.1 Jrebel  

jrebel 是一款 java 热部署插件,功能强大,开发必备,唯一不好，收费太贵  

- 安装:  

File --- Settings --- Plugins --- Browse respositories --- 搜索「Jrebel」 --- 选择「Jrebel for IntelliJ」  

点击「install」 进行安装(安装之后需要对 intellij 进行重启)  

- 破解:  

(1)在安装之后,设置中会有 「jrebel」选项, File --- Settings --- Jrebel --- 点击「change license」 --- 出现激活面板  

(2)下载激活工具(反代理工具),根据不同的系统，下载对应的版本,windows 系统下载 `ReverseProxy_windows_386.exe`  

或者 `ReverseProxy_windows_amd64.exe`  

下载地址: [https://github.com/ilanyu/ReverseProxy/releases](https://github.com/ilanyu/ReverseProxy/releases)  

**注意**: Mac 用户下载 `ReverseProxy_darwin_amd64` ,使用 safari 浏览器下载会保留`.dms` 后缀,使用 Chrome 浏览器下载 会将后缀名 `.dms` 去掉,不过不影响使用(Linux/Unix 系统执行程序不区分后缀名)   

下载之后通过命令行(terminal.app)执行以下操作:  

```bash
# 赋予该文件可执行权限
chmod 777 ReverseProxy_darwin_amd64
```

修改权限之后,就可以双击打开程序了  

(3)打开反代理工具,直接双击下载的 `.exe` 文件,打开之后**窗口不要关闭**，否则无法进行激活  

(4)生成一个 `GUID`  

在线生成 `GUID` 地址:   

[https://www.guidgen.com/](https://www.guidgen.com/)  

[https://1024tools.com/uuid](https://1024tools.com/uuid)  

(5)激活,在 Jrebel 激活面板下边选中 「Co在nnect to License Server」  

第一行填入本地反代理地址: [http://127.0.0.1:8888/24d0606a-606b-48c2-b39d-83ed43b3463f](http://127.0.0.1:8888/24d0606a-606b-48c2-b39d-83ed43b3463f)  

第二行填入邮箱(符合邮箱规则即可,可以随意写)  

关于地址和端口,都是可以修改的,在反代理工具的 Github 中都有说明，以上为在本机进行反代理设置,也可以在搭建本地服务器用于激活    

填好之后点击「chenge license」(这个时候,反代理工具窗口会有一些激活信息输出)  

此时, Jrebel 已经被激活,但是 **关闭反代理窗口,则激活失效**  

因此，**在激活之后，在 Jrebel 的选项面板选择 `Work offline` ，开启离线模式之后,可以有 180天(半年)的有效时间，半年之后可以用同样的方法再进行激活**  

在开启离线模式之后,可以关闭反代理工具的窗口了，关闭之后 Jrebel 仍然可以使用(如果是通过本地内网服务器进行激活，则不需要开启离线模式，只要服务器开着就可以了)  

至此,破解工作结束  

破解教程(原创作者):  

[撸了个反代工具, 可用于激活JRebel](http://blog.lanyus.com/archives/317.html)  

[JRebel 2018.1使用反代失败解决](http://blog.lanyus.com/archives/337.html)  

(6) jrebel maven plugin  

在**最外层父项目的 `pom.xml` 文件中**添加一下配置  

```xml
<plugin>
  <groupId>org.zeroturnaround</groupId>
  <artifactId>jrebel-maven-plugin</artifactId>
  <version>1.1.8</version>
  <executions>
    <execution>
      <id>generate-rebel-xml</id>
      <phase>process-resources</phase>
      <goals>
        <goal>generate</goal>
      </goals>
    </execution>
  </executions>
</plugin>
```

官方文档地址: [https://manuals.zeroturnaround.com/jrebel/standalone/maven.html](https://manuals.zeroturnaround.com/jrebel/standalone/maven.html)  

#### 5.2 Lombok  

Lombok 是一款用于简写Java bean 的插件，如使用 `@Setter` 注解即相当于类中的属性写了 `Setter` 方法，Java 开发者必备插件之一  

- 安装:  

File --- Settings --- Plugins --- Browse respositories --- 搜索「Lombok」 --- 选择「Lombok」安装即可  

#### 5.3 Albaba Java Coding Guidelines  

Albaba Java Coding Guidelines 功能正如其名，是阿里的 Java 代码规范插件，使用这个插件作为辅助，能够轻松写出规范的 Java 代码  

- 安装:  

File --- Settings --- Plugins --- Browse respositories --- 搜索「Albaba」 --- 选择「Albaba Java Coding Guidelines」安装即可   

#### 5.4 RestfulToolKit  

RestfulToolKit 是一套集成了 Restful 服务的辅助开发工具，可以实现通过 URL 定位到具体的 Controller,也能够实现基本的 Http 请求(类似 Postman 的功能)  

- 安装:  

File --- Settings --- Plugins --- Browse respositories --- 搜索「Restful」 --- 选择「RestfulToolKit」安装即可 