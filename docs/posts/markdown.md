# Markdown语法

`一级标题用：# 标题内容`

## 多级标题

`二级标题用：## 标题内容`

### 三级标题

`三级标题用：### 标题内容`

`以此类推，但markdown最多可有六级标题`

## 字体

`字体加粗用：**字体内容**`

**hello world！**

`字体斜体用：*字体内容*`

*hello world！*

`字体加粗且斜体用：***字体内容***`

***hello world！***

`字体删除横杠用：~~字体内容~~`

~~hello world！~~

`字体加下划线用：<u>hello world!</u>`

<u>hello world!</u>

`字体下标表示用：H~2~o`

H~2~o

`字体上标表示用：n^2^`

n^2^

`字体高亮用：==字体内容==`

==hello world!==

## 表情符号

`常用表情符号：:smile: :laughing: :dizzy_face: :sob: :cold_sweat: :sweat_smile:  :cry: :triumph: :heart_eyes: :relaxed: :sunglasses: :weary:`

`:+1: :-1: :100: :clap: :bell: :gift: :question: :bomb: :heart: :coffee: :cyclone: :bow: :kiss: :pray: :sweat_drops: :hankey: :exclamation: :anger:`

:smile: :laughing: :dizzy_face: :sob: :cold_sweat: :sweat_smile:  :cry: :triumph: :heart_eyes: :relaxed: :sunglasses: :weary:

:+1: :-1: :100: :clap: :bell: :gift: :question: :bomb: :heart: :coffee: :cyclone: :bow: :kiss: :pray: :sweat_drops: :hankey: :exclamation: :anger:

## 引用

`引用内容用：> 内容`

`二级引用用：>> 内容`

`两次enter键跳出引用`

> 我的第一篇博客
>
> > 二级引用

## 分割线

`常用的分割线用：---或者***回车即可`

___

***

## 图片

`插入本地图片用：![图片名字](图片地址绝对路径)`

![本地图片](../assets/t_1.jpg)



`插入网络图片用：![图片名字](图片地址图片链接)`

![网络图片](../assets/t_2.jpg)

`本地地址和网络上图片地址可能会由于本地的更改删除或者网络图片出处的删除，而导致图片无效而显示不出来，建议大家把需要的图片上传到自己创建的图床里。`

## 超链接

`超链接用：[链接名字](链接地址)`

[点击跳转到我的主页](https://ruheyun.github.io/)

`自动链接用：<链接地址url或者邮箱>`

<https://ruheyun.github.io/>

## 列表

`有序列表用：1. 内容`

1. a
2. b
3. c

`无序列表用：- 内容`

- a
- b
- c

## 表格

`插入表格最简单方法，直接鼠标右键选插入>表格即可`

| 名字 | 性别 | 生日      |
| ---- | ---- | --------- |
| 如何 | 男   | 2022.6.18 |

`插入表格第二种方式需要用格式：`

`|属性|属性|属性|`

`|--|--|--|`

`|内容|内容|内容|`

| 名字 | 性别 | 生日      |
| ---- | ---- | --------- |
| 如何 | 男   | 2022.6.18 |

## 代码块

`编写代码用：```语言名称回车即可`

```java
public class HelloWorld {
	public static void main(String[] args) {
		System.out.println("Hello World!");
	}
}
```

`行内代码用：``两点内书写内容`

## Html

`Markdown语法，同样支持Html语法，所以如果想要更丰富的格式，则可以借助Html、CSS、JS等实现。`


> 2022.6.18是我第一天注册博客园开始学习写文章，为了完成属于自己的第一篇博客，我熬夜写到半夜才完成。虽然有很多地方不足，但是我很开心。也希望自己可以在接下来学习过程中坚持写博客，不放弃，希望可以让自己在学习过程中与大家一起讨论，分享总结。最后，祝各位朋友心想事成！
