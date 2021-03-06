# cat/less/More

##  cat

cat 一次性显示所有的数据
```

1、命令格式
cat [选项]... [文件]...
2、命令功能
将[文件]或标准输入组合输出到标准输出。
<strong>cat主要有三大功能：
1）.一次显示整个文件:cat filename
2）.从键盘创建一个文件:cat &gt; filename 只能创建新文件,不能编辑已有文件.
3）.将几个文件合并为一个文件:cat file1 file2 &gt; file</strong>
3、常用参数列表
  -A, --show-all            等于-vET
 <strong> -b, --number-nonblank 对非空输出行编号</strong>
  -e                        等于-vE
  -E, --show-ends           在每行结束处显示"$"
<strong>  -n, --number          对输出的所有行编号</strong>
  -s, --squeeze-blank       不输出多行空行
  -t                        与-vT 等价
  -T, --show-tabs           将跳格字符显示为^I
  -u                        (被忽略)
  -v, --show-nonprinting    使用^ 和M- 引用，除了LFD和 TAB 之外
      --help                显示此帮助信息并退出<strong>
     </strong> --version             显示版本信息并退出

```


## more
空格下一页，b上一页
more命令，功能类似 cat ，cat命令是整个文件的内容从上到下显示在屏幕上。 more会以一页一页的显示方便使用者逐页阅读，而最基本的指令就是按空白键（space）就往下一页显示，按 b 键就会往回（back）一页显示，而且还有搜寻字串的功能 。more命令从前向后读取文件，因此在启动时就加载整个文件。
```

1、命令格式
 more [-dlfpcsu] [-num] [+/pattern] [+linenum] [file ...]
2、命令功能
more命令和cat的功能一样都是查看文件里的内容，但有所不同的是more可以按页来查看文件的内容，还支持直接跳转行等功能。
3、常用参数列表
     -num  一次显示的行数
     -d    在每屏的底部显示友好的提示信息
     -l    忽略 Ctrl+l （换页符）。如果没有给出这个选项，则more命令在显示了一个包含有 Ctrl+l 字符的行后将暂停显示，并等待接收命令。
     -f     计算行数时，以实际上的行数，而非自动换行过后的行数（有些单行字数太长的会被扩展为两行或两行以上）
     -p     显示下一屏之前先清屏。
     -c    从顶部清屏然后显示。
     -s    文件中连续的空白行压缩成一个空白行显示。
     -u    不显示下划线
     +/    先搜索字符串，然后从字符串之后显示
     +num 从num行开始显示
```

## less
less 工具也是对文件或其它输出进行分页显示的工具，应该说是linux正统查看文件内容的工具，功能极其强大。less 的用法比起 more 更加的有弹性。在 more 的时候，我们并没有办法向前面翻， 只能往后面看，但若使用了 less 时，就可以使用 [pageup] [pagedown] 等按键的功能来往前往后翻看文件，更容易用来查看一个文件的内容！除此之外，在 less 里头可以拥有更多的搜索功能，不止可以向下搜，也可以向上搜。
```

1．命令格式：
less [参数]  文件
2．命令功能：
less 与 more 类似，但使用 less 可以随意浏览文件，而 more 仅能向前移动，却不能向后移动，而且 less 在查看之前不会加载整个文件。
3．命令参数：
-b &lt;缓冲区大小&gt; 设置缓冲区的大小
-e  当文件显示结束后，自动离开
-f  强迫打开特殊文件，例如外围设备代号、目录和二进制文件
-g  只标志最后搜索的关键词
-i  忽略搜索时的大小写
-m  显示类似more命令的百分比
<strong>-N  显示每行的行号</strong>
-o &lt;文件名&gt; 将less 输出的内容在指定文件中保存起来
-Q  不使用警告音
-s  显示连续空行为一行
-S  行过长时间将超出部分舍弃
-x &lt;数字&gt; 将“tab”键显示为规定的数字空格
<strong>/字符串：向下搜索“字符串”的功能
?字符串：向上搜索“字符串”的功能</strong>
n：重复前一个搜索（与 / 或 ? 有关）
N：反向重复前一个搜索（与 / 或 ? 有关）
<strong>b  向后翻一页
d  向后翻半页</strong>
h  显示帮助界面
Q  退出less 命令
u  向前滚动半页
y  向前滚动一行
<strong>空格键 滚动一页
回车键 滚动一行</strong>

```

空格下一页，b上一页


## 总和

### cat more less

三者区别
```
众所周知linux中命令cat、more、less均可用来查看文件内容，主要区别有：
cat是一次性显示整个文件的内容，还可以将多个文件连接起来显示，它常与重定向符号配合使用，适用于文件内容少的情况；
more和less一般用于显示文件内容超过一屏的内容，并且提供翻页的功能。more比cat强大，提供分页显示的功能，less比more更强大，提供翻页，跳转，查找等命令。而且more和less都支持：用空格显示下一页，按键b显示上一页。下面详细介绍这3个命令。
```
