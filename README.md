# markdown 语法

## markdown 官方语法总结

|     对象     |                      语法                      |                    描述或例子                     |
|--------------|------------------------------------------------|---------------------------------------------------|
| 兼容HTML     | HTML 语法                                      | 直接使用html 标签即可                             |
| Setext标题   | 标题下加 `"="` 、`"-"`                         | 一级加 `"="` ,二级加 `"-"`                        |
| Atx 标题     | # 标题                                         | `"#"`1~6 个代表 H1~H6 标题                        |
| 区块引用     | \> 引用内容                                    | 前加 `>` ,`>` 后可带 markdown语法                 |
| 无序列表     | 前加 `*` 或 `+` 或 `-` 号                      | 列表前加 `*+-` 其一                               |
| 有序列表     | `数字.` 列表                                   | 1. Bird   2.McHale   3.Parish                     |
| 代码区块     | 缩进 4 空格或 1 制表符                         | tab 缩进 或 加4空格                               |
| 分隔线       | `***` 或 `---` 或  `___` 或                    | 中间加1~2个间隔，如 `***` = `* * *`               |
| 行内链接     | `[name](url "title")`                          | `[name](baidu.com "baidu")`                       |
| 参考链接     | `[name][id]` and `[id]:url "title"`            | `[name][id1]`  and  `[id1]:baidu.com "baidu"`     |
| 隐式链接     | `[name][]` and `[urlName]:url "title"`         | `[baidu][]` and `[baidu]:baidu.com  "baidu"`      |
| 强调         | `*` 强调词 `*` 或 `_` 强调词 `_`               | 用 `*` 包起会转为 `<em>` 用 `_` 会转为`<strong>`  |
| 行内代码标记 | \`要标记的段行内代码\`                         | Use the \`printf()\` function.                    |
| 行内图片     | `![alt text](imgUrl "title")`                  | `![myimg](/path/img/jpg "mytile")`                |
| 参考图片     | `![alt text][id]` and `[id]:imgUrl "title"`    | `![myimg][id1] and [id1]:/path/img/jpg "mytile"`  |
| 隐式图片     | `[alt text][] []` and `[alt text]:url "title"` | `![myimg][] and [myimg]:/path/img/jpg "mytile"`   |
| 自动链接     | `<webUrl> or <emil>`                           | `<http://example.com>` or `<example@example.com>` |
| 符号转义     | `\`需要转义的符号                              | \\`                                               |

以上内容为官方文档整理排版。<http://daringfireball.net/projects/markdown/basics>  
Markdown官方网站：<http://daringfireball.net/projects/markdown/>     
在线 Markdown 编辑器：<https://stackedit.io/> 

------------------------------------------------------------------------------------------------------------------

## markdown 支持语法总结

|   对象   |                   语法                   |            描述或例子             |
|----------|------------------------------------------|-----------------------------------|
| 删除线   | `~~content~~`                            | 用 ~~ 包起要删除内容 ~~例子~~   |
| 语法高亮 | \```语言(sql,java,shell...) content \``` | 用\```语言 和 \``` 包起需高亮语言 |
| 表格     | 竖线加中线组成表头。竖线为表边           | markdown 其他支持语法使用详情     |

以上支持语法总结内容为网络收集整理排版

-----------------------------------------------------------------------------------------------------------------

## markdown 其他支持语法使用详情

### 删除线

    ~~删除线~~

~~删除线~~

### 语法高亮

    ```java
    public static void main(String[] args){
        System.out.println("This is the syntax highlighting");
    } 
    ```

```java
public static void main(String[] args){
    System.out.println("This is the syntax highlighting")
}
```

### talbe

可以通过安装单词列表包，然后用 `|` 和 `-` 来创建表格,tab 检测创建行或列

    | aaa | bb |
    |-----|----|
    |  1  | 2  |
    |  3  | 4  |

拷贝创建，用`,` 隔开各列，然后全选，按自定义快捷键，如我的是 Ctrl+t ,然后在第二行加 `|-` > tab

    aaa,bbb        | aaa  |  bbb  |
    1,2       ==>  |  1   |  2    |
    3,4            |  3   |  4    |   

第二行加 `|-` > tab

```
| aaa | bbb |         |  aaa  |  bbb  |
|-               ==>  |---------------|
| 1   | 2   |         |  1    |  2    |
| 3   | 4   |         |  3    |  4    |
```

以下给出 sublime 的 Table Editor 包的安装方式

1. 安装包控制器 package Control   
    <https://packagecontrol.io/>

2. 安装 Table Editor
     1. Preferences > Package Control > Package Control install package > talble editor > install
     2. Preferences > Key Bindings-User > add   
    > { "keys": ["ctrl+t"], "command": "table_editor_csv_to_table", "context":
    > [{ "key": "setting.enable_table_editor", "operator": "equal", "operand": true, "match_all": true }]}

    详见 <https://github.com/vkocubinsky/SublimeTableEditor> 
