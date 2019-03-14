# Markdown纯文本标记语言
> 可以通过简书的Markdown编辑模式进行markdown的练习   
> 开启方式`开启方式：设置->默认编辑器->Markdown编辑器  
> [据说是官方说明](https://daringfireball.net/projects/markdown/syntax)

## Markdown 语法
> 基本符号:  * - + >   
> 基本上所有的markdown标记都是基于这四个符号或组合   
> 以基本符号开头的标记,基本符号后要有一个空格(用于分割标记符和内容)   
> 如果只是想显示这些基本符号建议在基本符号前加反斜杠\(例如\*)  
> **Markdown语法也原生支持HTML语法**   

## 字体
### 1. 斜体
> 语法: 在需要斜体的文字两端用\*包裹起来  
> 例如*这样*(用\*包裹)   
### 2. 粗体   
> 语法: 在需要加粗的文字两端用\*\*包裹起来   
> 比如**这样**(用\*\*包裹)  
### 3. 斜体加粗   
> 语法: 三个\*   
> ***这个就是斜体加粗***(用\*\*\*包裹)   
### 4. 下划线   
> 语法: 用\_包裹需要下划线的文字    
> 例如_这样_(用\_包裹)  
### 5. 删除线   
> 语法: 用\~\~包裹
> 例如~~这样~~(用\~\~包裹) 

## 标题
> 语法: 在一行的开头使用 # 加空格 表示标题,几个#代表几级标题
> # 一级标题 `# 一级标题(相当于大标题)`   
> ## 二级标题 `## 二级标题(相当于中标题)`   
> ### 三级标题 `### 三级标题`   
> #### 四级标题 `#### 四级标题`   
> ##### 五级标题 `##### 五级标题`   
> ###### 六级标题 `###### 六级标题`
> ####### 最多只有六级标题

## 分段   
1. 换行
> * 换一行: 直接敲回车是不行的,必须在换行前至少敲2个空格在换行,或者使用`<br/>`来换行  
> * 多行换行: 同样直接敲出多个换行符也不会只会认为换了一行,要换多行应该多次使用换一行语法  
2. 分割线
> 语法: 在单行用三个\-或者\*
***  

## 列表
### 1. 无序列表:   
> 语法: 使用 * + - 表示无序列表, 例如:
> - 无序列表一(用-表示)
> + 无序列表二(用+表示)
> * 无序列表三(用*表示)   

### 2. 有序列表:   
> 语法: 使用数字和 . 表示有序列表,有序列表是从第一行的数字开始往下排列   
> 4. 有序列表    
> 3. 有序列表   
> 233. 有序列表   
> - 这也算 

### 3. 多重列表
> 语法: 单层列表项后边另起一行并且缩进三个空格就可以往后面叠加子列表
> 1. 首层列表项(有序)   
>    1. 这个是嵌套层(嵌套的列表可以是有序的)  <br/>这个是多行显示
> 2. 第二层列表  
>    - 这个也是嵌套层(也可以是无序的)

### 3. 其他说明
> 1. 列表会为列表内的多行文本自动缩进相同的空格  
> 2. 两个列表项之间有空行的话则每个列表的内容会被\<p>标签包裹

## 引用
> 语法: 使用 > 表示文字引用; 多层引用就是多个 > 叠加
>> 比如这样
>>> 这是三个 >

## 代码   
### 1. 行内代码(内联代码)
> 语法: 在文字左右使用反引号包含（键盘Esc键下面,数字键"1"左边的大波浪号,打出来是 \` )   
> 示例: 例如这段文字的 `这部分` 就是使用的行内代码块 
    
### 2. 定义型代码块(没效果啊,干嘛用的啊)    
> 语法: 冒号 \: 加四个空格(左侧加一个可见的英文冒号和4个不可见的空格)   
> 示例:   
:    这是一个代码块,此行左侧有四个不可见的空格  
    
### 3. 代码块(一整段都是代码)  
   1. 普通代码块
   > 语法: 在代码的前后使用三个\`\`\`  
   > 例如:  
```
        <?xml version="1.0" encoding="UTF-8"?>
        <project xmlns="http://maven.apache.org/POM/4.0.0"
                 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                 xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
            <modelVersion>4.0.0</modelVersion>
        
            <groupId>org.climer.</groupId>
            <artifactId>spring</artifactId>
            <version>1.0-SNAPSHOT</version>
        
            <dependencies>
                <dependency><!-- spring核心依赖 -->
                    <groupId>org.springframework</groupId>
                    <artifactId>spring-core</artifactId>
                    <version>5.1.4.RELEASE</version>
                </dependency>
                <dependency><!-- spring核心组件context -->
                    <groupId>org.springframework</groupId>
                    <artifactId>spring-context</artifactId>
                    <version>5.1.4.RELEASE</version>
                </dependency>
            </dependencies>
        </project>
```
   2. 特定语言的代码块:  
   > 语法: 用法同普通代码块,只不过在代码前的三个\`后边跟上需要标记的语言就可以了
   > 例如: 
```java
@SpringBootApplication
public class Application {

	public static void main(String[] args) {
		SpringApplication.run(Application.class, args);
	}

}  
```  
   3. 类似与git日志那种代码块 
> 语法: 使用三个\`加diff开头,在需要显示删除的行的开头使用- 在需要显示添加的行使用+   
```diff
- 这是删除的代码块
+ 这是添加的代码块
```

## 表格  

 
## 其他
> 1. 连接  
> 语法: \[]()  
> 例子: [这个页面的连接](https://github.com/baldass/gitstudy/blob/master/Markdown%E6%A0%87%E8%AE%B0%E8%AF%AD%E8%A8%80%E8%AF%B4%E6%98%8E.md)  

> 2. 图片  
> 语法:  \!\[]()  
> 例如: ![小喵喵](https://raw.githubusercontent.com/baldass/gitstudy/master/imgs/tx.jpg)  


 