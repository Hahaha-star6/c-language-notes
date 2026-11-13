# <span style="color:#202124">C 语言学后总结</span>

## <span style="color:#AE8F5F">前言</span>

很高兴你愿意花时间打开这份文件。这份文件，是我学习 C 语言过程中遇到的错题和对知识的疑惑的总结，主要分为五个部分：错题、我提过的问题、函数速查、不容易背的硬知识、常见刷题题型与解法。

它更适合已经学过一遍 C 语言、但知识点不扎实、想快速补漏的人——能帮你迅速定位一些常见语法错误和知识疑惑。不过我不能担保它囊括了所有知识，这些只是我目前遇到过的那些。所以我更希望，当你接手这本笔记时，也把你的错误、你的理解补进去，让它成为一份属于你自己的笔记。

希望对你的学习有帮助。

——花自飘零水自流。

---

## <span style="color:#6B7280">📑 目录（点一下直接跳转）</span> <a id="sec0"></a>

<span style="color:#B87A5C">■ 错题</span>　<span style="color:#6E93B5">■ 我提过的问题</span>　<span style="color:#7FA182">■ 函数速查</span>　<span style="color:#9A87B5">■ 硬知识</span>　<span style="color:#6E8A8A">■ 刷题题型</span>

<table style="width:100%;border-collapse:collapse;font-size:14px">

<tr><td colspan="4" style="border-left:3px solid #B87A5C;border-top:1px solid rgba(128,128,128,.22);padding:14px 10px 6px 10px"><b style="color:#B87A5C;font-size:14.5px">第一部分　错题清单</b>　<span style="color:#8b9199;font-weight:400">我踩过的坑：症状 → 病因 → 药方</span></td></tr>
<tr>
<td style="padding:5px 10px"><a href="#p1-1" style="color:#6E7681;text-decoration:none">1.1 语法与符号</a></td>
<td style="padding:5px 10px"><a href="#p1-2" style="color:#6E7681;text-decoration:none">1.2 输入输出</a></td>
<td style="padding:5px 10px"><a href="#p1-3" style="color:#6E7681;text-decoration:none">1.3 数组·字符串·变量</a></td>
<td style="padding:5px 10px"><a href="#p1-4" style="color:#6E7681;text-decoration:none">1.4 循环</a></td>
</tr>
<tr>
<td style="padding:5px 10px"><a href="#p1-5" style="color:#6E7681;text-decoration:none">1.5 程序结构与编译环境</a></td>
<td style="padding:5px 10px"><a href="#p1-6" style="color:#6E7681;text-decoration:none">1.6 思维方式</a></td>
<td style="padding:5px 10px"><a href="#p1-7" style="color:#6E7681;text-decoration:none">1.7 文件与二进制专项</a></td>
<td style="padding:5px 10px"><a href="#p1-8" style="color:#6E7681;text-decoration:none">1.8 高频复发榜</a></td>
</tr>
<tr>
<td style="padding:5px 10px"><a href="#p1-9" style="color:#6E7681;text-decoration:none">1.9 我的弯路档案（真实踩坑实录）</a></td>
<td style="padding:5px 10px"></td>
<td style="padding:5px 10px"></td>
<td style="padding:5px 10px"></td>
</tr>

<tr><td colspan="4" style="border-left:3px solid #6E93B5;border-top:1px solid rgba(128,128,128,.22);padding:14px 10px 6px 10px"><b style="color:#6E93B5;font-size:14.5px">第二部分　我提过的问题（Q&amp;A）</b>　<span style="color:#8b9199;font-weight:400">11 类 · Q1–Q111，按知识主线排列</span></td></tr>
<tr>
<td style="padding:5px 10px"><a href="#p2-1" style="color:#6E7681;text-decoration:none">2.1 输入输出</a></td>
<td style="padding:5px 10px"><a href="#p2-2" style="color:#6E7681;text-decoration:none">2.2 数组与字符串</a></td>
<td style="padding:5px 10px"><a href="#p2-3" style="color:#6E7681;text-decoration:none">2.3 指针</a></td>
<td style="padding:5px 10px"><a href="#p2-4" style="color:#6E7681;text-decoration:none">2.4 函数与递归</a></td>
</tr>
<tr>
<td style="padding:5px 10px"><a href="#p2-5" style="color:#6E7681;text-decoration:none">2.5 结构体与自定义类型</a></td>
<td style="padding:5px 10px"><a href="#p2-6" style="color:#6E7681;text-decoration:none">2.6 动态内存与内存布局</a></td>
<td style="padding:5px 10px"><a href="#p2-7" style="color:#6E7681;text-decoration:none">2.7 文件与二进制</a></td>
<td style="padding:5px 10px"><a href="#p2-8" style="color:#6E7681;text-decoration:none">2.8 运算符与表达式</a></td>
</tr>
<tr>
<td style="padding:5px 10px"><a href="#p2-9" style="color:#6E7681;text-decoration:none">2.9 控制流程与跳转</a></td>
<td style="padding:5px 10px"><a href="#p2-10" style="color:#6E7681;text-decoration:none">2.10 预处理与宏</a></td>
<td style="padding:5px 10px"><a href="#p2-11" style="color:#6E7681;text-decoration:none">2.11 类型与标准库工具</a></td>
<td style="padding:5px 10px"></td>
</tr>

<tr><td colspan="4" style="border-left:3px solid #7FA182;border-top:1px solid rgba(128,128,128,.22);padding:14px 10px 6px 10px"><b style="color:#7FA182;font-size:14.5px">第三部分　函数速查</b>　<span style="color:#8b9199;font-weight:400">与《C易错点与函数速查》第三部分完全一致</span></td></tr>
<tr>
<td style="padding:5px 10px"><a href="#sec53" style="color:#6E7681;text-decoration:none">先背这些（高频必会）</a></td>
<td style="padding:5px 10px"><a href="#sec54" style="color:#6E7681;text-decoration:none">1. stdio.h</a></td>
<td style="padding:5px 10px"><a href="#sec55" style="color:#6E7681;text-decoration:none">2. string.h</a></td>
<td style="padding:5px 10px"><a href="#sec56" style="color:#6E7681;text-decoration:none">3. math.h</a></td>
</tr>
<tr>
<td style="padding:5px 10px"><a href="#sec57" style="color:#6E7681;text-decoration:none">4. stdlib.h</a></td>
<td style="padding:5px 10px"><a href="#sec82" style="color:#6E7681;text-decoration:none">5. ctype.h</a></td>
<td style="padding:5px 10px"><a href="#sec83" style="color:#6E7681;text-decoration:none">6. time.h</a></td>
<td style="padding:5px 10px"><a href="#sec84" style="color:#6E7681;text-decoration:none">7. assert / limits / errno</a></td>
</tr>
<tr>
<td style="padding:5px 10px"><a href="#sec85" style="color:#6E7681;text-decoration:none">8. 头文件地图</a></td>
<td style="padding:5px 10px"></td>
<td style="padding:5px 10px"></td>
<td style="padding:5px 10px"></td>
</tr>

<tr><td colspan="4" style="border-left:3px solid #9A87B5;border-top:1px solid rgba(128,128,128,.22);padding:14px 10px 6px 10px"><b style="color:#9A87B5;font-size:14.5px">第四部分　常用但不容易背的知识点</b>　<span style="color:#8b9199;font-weight:400">背不下来但必须会的硬知识</span></td></tr>
<tr>
<td style="padding:5px 10px"><a href="#p4-1" style="color:#6E7681;text-decoration:none">4.1 格式说明符 %</a></td>
<td style="padding:5px 10px"><a href="#p4-2" style="color:#6E7681;text-decoration:none">4.2 转义字符</a></td>
<td style="padding:5px 10px"><a href="#p4-3" style="color:#6E7681;text-decoration:none">4.3 ASCII</a></td>
<td style="padding:5px 10px"><a href="#p4-4" style="color:#6E7681;text-decoration:none">4.4 类型与范围</a></td>
</tr>
<tr>
<td style="padding:5px 10px"><a href="#p4-5" style="color:#6E7681;text-decoration:none">4.5 运算符优先级</a></td>
<td style="padding:5px 10px"><a href="#p4-6" style="color:#6E7681;text-decoration:none">4.6 位运算技巧</a></td>
<td style="padding:5px 10px"><a href="#p4-7" style="color:#6E7681;text-decoration:none">4.7 返回值与宏约定</a></td>
<td style="padding:5px 10px"><a href="#p4-8" style="color:#6E7681;text-decoration:none">4.8 编译错误码</a></td>
</tr>
<tr>
<td style="padding:5px 10px"><a href="#p4-9" style="color:#6E7681;text-decoration:none">4.9 复杂声明读法</a></td>
<td style="padding:5px 10px"><a href="#p4-10" style="color:#6E7681;text-decoration:none">4.10 结构体对齐</a></td>
<td style="padding:5px 10px"><a href="#p4-11" style="color:#6E7681;text-decoration:none">4.11 输出格式技巧</a></td>
<td style="padding:5px 10px"><a href="#p4-12" style="color:#6E7681;text-decoration:none">4.12 补码·大小端·IEEE 754</a></td>
</tr>
<tr>
<td style="padding:5px 10px"><a href="#p4-13" style="color:#6E7681;text-decoration:none">4.13 预处理</a></td>
<td style="padding:5px 10px"><a href="#p4-14" style="color:#6E7681;text-decoration:none">4.14 存储类别与内存分区</a></td>
<td style="padding:5px 10px"><a href="#p4-15" style="color:#6E7681;text-decoration:none">4.15 类型转换三步</a></td>
<td style="padding:5px 10px"><a href="#p4-16" style="color:#6E7681;text-decoration:none">4.16 struct / 位段 / enum / union</a></td>
</tr>
<tr>
<td style="padding:5px 10px"><a href="#p4-17" style="color:#6E7681;text-decoration:none">4.17 排序与查找</a></td>
<td style="padding:5px 10px"><a href="#p4-18" style="color:#6E7681;text-decoration:none">4.18 刷题套路速查</a></td>
<td style="padding:5px 10px"><a href="#p4-19" style="color:#6E7681;text-decoration:none">4.19 VS 调试六件套</a></td>
<td style="padding:5px 10px"><a href="#p4-20" style="color:#6E7681;text-decoration:none">4.20 十组对照表</a></td>
</tr>
<tr>
<td style="padding:5px 10px"><a href="#p4-21" style="color:#6E7681;text-decoration:none">4.21 一个 .c 怎么变成 .exe</a></td>
<td style="padding:5px 10px"><a href="#p4-22" style="color:#6E7681;text-decoration:none">4.22 文件模式与返回值</a></td>
<td style="padding:5px 10px"><a href="#p4-23" style="color:#6E7681;text-decoration:none">4.23 switch / goto</a></td>
<td style="padding:5px 10px"><a href="#p4-24" style="color:#6E7681;text-decoration:none">4.24 内存到变量</a></td>
</tr>
<tr><td colspan="4" style="border-left:3px solid #6E8A8A;border-top:1px solid rgba(128,128,128,.22);padding:14px 10px 6px 10px"><b style="color:#6E8A8A;font-size:14.5px">第五部分　常见刷题题型与解法</b>　<span style="color:#8b9199;font-weight:400">10 类题型 · 覆盖 T1–T85</span></td></tr>
<tr>
<td style="padding:5px 10px"><a href="#p5-1" style="color:#6E7681;text-decoration:none">5.1 字符串与字符数组</a></td>
<td style="padding:5px 10px"><a href="#p5-2" style="color:#6E7681;text-decoration:none">5.2 双指针与对称</a></td>
<td style="padding:5px 10px"><a href="#p5-3" style="color:#6E7681;text-decoration:none">5.3 循环分支与运算</a></td>
<td style="padding:5px 10px"><a href="#p5-4" style="color:#6E7681;text-decoration:none">5.4 函数与递归</a></td>
</tr>
<tr>
<td style="padding:5px 10px"><a href="#p5-5" style="color:#6E7681;text-decoration:none">5.5 数组算法与排序</a></td>
<td style="padding:5px 10px"><a href="#p5-6" style="color:#6E7681;text-decoration:none">5.6 指针与内存函数</a></td>
<td style="padding:5px 10px"><a href="#p5-7" style="color:#6E7681;text-decoration:none">5.7 结构体与自定义类型</a></td>
<td style="padding:5px 10px"><a href="#p5-8" style="color:#6E7681;text-decoration:none">5.8 动态内存</a></td>
</tr>
<tr>
<td style="padding:5px 10px"><a href="#p5-9" style="color:#6E7681;text-decoration:none">5.9 文件读写与错误处理</a></td>
<td style="padding:5px 10px"><a href="#p5-10" style="color:#6E7681;text-decoration:none">5.10 项目实战</a></td>
<td style="padding:5px 10px"></td>
<td style="padding:5px 10px"></td>
</tr>

</table>

> 💡 颜色只在**支持 HTML 的预览**里显示（VS Code 预览、Typora）。GitHub 会去掉颜色，但**链接照样能跳**。

---

# <span style="color:#B87A5C">第一部分　错题清单</span>

> 每条格式都是 **症状（看到什么）→ 病因（为什么）→ 药方（怎么写）**。完整版见《C易错点与函数速查》第一部分。

## <span style="color:#B87A5C">1.1 语法与符号</span> <a id="p1-1"></a>

| 症状 | 病因 | 药方 |
| --- | --- | --- |
| `if (x = 5)` 永远为真 | `=` 是"存进去"，不是"问是不是" | 用 `==`；常量写左边 `if (5 == x)`，写错编译器直接拦 |
| 两数交换后纹丝不动，报 C4553 | 把赋值写成 `c == a;`——问完答案就扔 | 赋值用 `=`：`c = a; a = b; b = c;` |
| `if (suzu[j] = suzu[i])` 导致 count 恒为 n、数组被改坏 | 右边是变量时 VS 常常不报警，赋值既恒真又覆盖数据 | 比较一律 `==`；写完内层循环检查"有没有改到不该改的数组" |
| `arr[0][0] == arr[0][1] == arr[0][2]` 判三连永远失败 | `==` 从左往右：先得 0/1，再拿 0/1 和字符编码比，几乎恒假 | 两两比较 + `&&`：`a == b && b == c && a != ' '` |
| `if (a < b < c)` 结果诡异 | 先算 `a < b` 得 0/1，再和 c 比 | `a < b && b < c` |
| 两个条件"同时成立"写了逗号 | 逗号表达式只取**最后一个**的值，前半句被丢掉 | 用 `&&`；`for` 三段之间才是分号 |
| `for (a, a < 10, a++)` 报"应输入 ;" | `for` 括号里**必须两个分号** | `for (a = 0; a < 10; a++)` |
| `if (...);` 或 `for (...);` 后面多一个分号 | 那个分号把语句体变成空语句，后面的语句已不属于它 | 删掉；`if`/`for`/`while` 条件后要么 `{`，要么直接写语句 |
| `5 / 2` 得 2 | 两个整数相除，小数被砍 | `5.0 / 2` 或 `(double)a / b` |
| `5 ^ 3` 以为等于 125 | `^` 是**按位异或**，C 没有次方运算符 | 次方用 `pow(5,3)` 或循环累乘 |
| 对 `float` 用 `%` 取余，报 C2296 | `%` 只收整数，"余数"只在整数世界有定义 | 先转整型：`int n = (int)(a * 10 + 0.5);` 再 `%`；浮点用 `fmod` |
| `suzu[b] = 'suzu[b]-32';` 输出怪字符 | 单引号只能包**一个字符**，包表达式变成"多字符常量"→ 垃圾值 | `suzu[b] = suzu[b] - 32;` |
| `strcspn(a, '\n')` / `strtok(b, ' ')` 报 C4047 | 这类函数要 `const char*`，`'\n'` 是 `char`（一个字节的小整数） | 改**双引号**：`strcspn(a, "\n")`、`strtok(b, " ")` |
| `*p[2]` 想取第 2 个元素却崩溃 | `[ ]` 优先级高于 `*`：先取住客，再把这个数当地址敲门 | 下标自带解引用，直接 `p[2]` 或 `*(p+2)` |
| `a[i] > 'a' && a[i] < 'z'` 判字母漏端点 | 严格不等号把 `'a'`、`'z'` 排除在外 | `>= 'a' && <= 'z'`，两端都要带等号 |
| 报 C2106「= 左操作数必须为左值」 | 优先级：`=` 低于 `\|\|`，句子被"粘"成 `(A \|\| B) = ...` | 每个比较都写完整运算符，补回漏掉的 `!` |
| 报 C2001「常量中有换行符」 | 字符串里直接按了回车 | 换行写 `\n`，字符串必须一行写完 |
| 报 C4819 代码页 936 | 文件编码与 VS 代码页不匹配 | 高级保存选项 → UTF-8 带 BOM |
| 报错但代码"看起来没错" | 中文输入法打了全角 `；（） ，` | 切英文输入法，逐字符检查半角 |
| 函数头附近一次报 4 个 E0852「表达式必须是指向完整对象类型的指针」 | 结构体标签**大小写不一致**：定义 `struct Stu`，形参写 `struct stu` → 变成"不完整类型" | 全文件统一 `struct Stu`；或 `typedef struct Stu Stu;` 后只写 `Stu` |
| 声明 `char suzu[0];` 程序行为诡异 | 申请 0 格等于没空间，一写就溢出 | 元素个数必须是正数 |
| `if (y > m) f(x, m+1, y-1);` 后面三条交换也执行了 | `if` 不加大括号时**只买得起一条**语句 | 多条语句加 `{}`；递归终点用 `if (...) return;` |
| `float e = a*10/10 % 100;` 报 C2296 | `%` 与 `/` 同级左结合，先算除法再取余，且 `%` 不收浮点 | 先转整型再拆位：`int n = (int)(a*10+0.5);` |
| 写 `my_memcpy` 时 `(char*)dst + i = ...` 报"左操作数必须是左值" | **强转只作用于紧跟的那个表达式**：`(char*)dst + i` 先把 `dst` 转成 `char*` 再偏移，偏移结果是临时值，不能赋值 | 先赋给变量再偏移：`char* d = (char*)dst; d[i] = ...;` |
| 逐字节搬的时候只走了 `n` 个字节，int 数组却只搬了 1/4 | `memcpy` 的 `n` 是**字节数**，元素个数要乘 `sizeof` | `memcpy(d, s, n * sizeof(int));` |
| 循环写 `i <= n`，多搬一格把邻居踩了 | 字节数下标的合法范围是 `0 ~ n-1` | `for (i = 0; i < n; i++)` |
| `szieof(a)` / `pintf` 拼错 → C3861 / E0020 / C4013 | 手滑把 `sizeof`、`printf` 拼错，编译器不认识这个名字 | 逐字母核对：`sizeof`、`printf`、`strlen`、`strcmp` |
| `printf("%d", 3.14)` 输出怪数字 | 格式符与类型不匹配（`%d` 按 4 字节 int 读 double 的位模式） | `%d` 配整数、`%f` 配浮点、`%c` 配字符、`%s` 配字符串 |
| 看不懂 `if (!found)` | `!` 是逻辑非，把真假翻转（`!0`→1，`!非0`→0） | 读作"如果没有找到"，等价 `found == 0` |
| 逻辑判断结果怪怪的 | 把按位 `&` `\|` 和逻辑 `&&` `\|\|` 搞混了 | 判断逻辑一律用 `! && \|\|`；单个 `&`、`\|` 是位运算 |
| `if suzu[b]:` 编译报错 | ① `if` 条件必须圆括号；② 不能用冒号结尾；③ 括号里必须是完整比较式 | `if (suzu[b] >= '0' && suzu[b] <= '9')` |
| `suzu[b] = L;` 报"L 未定义" | `L` 不加引号就是**变量名**；字符必须加单引号 | `suzu[b] = 'L';` |
| 程序毫无提示直接闪退，报 `0xC0000094: Integer division by zero`，编译零警告 | 分母为 0，CPU 触发硬件异常；编译器只查类型、不知道运行时值 | 凡 `/` 或 `%` 先问"分母会不会是 0"，入口处拦：`if (b == 0) return 0;` |

## <span style="color:#B87A5C">1.2 输入输出</span> <a id="p1-2"></a>

| 症状 | 病因 | 药方 |
| --- | --- | --- |
| 程序崩 / 变量是乱值 / 弹 Debug Assertion Failed | 漏 `&`，把变量的**值**当地址（0 就是 NULL） | `scanf("%d", &n);`——数组名例外 |
| `scanf("%d", arr[i]);` 报 C4477、运行崩 | `arr[i]` 是 int 值，不是地址 | `scanf("%d", &arr[i]);`（二维：`&n[i][j]`，双层循环最易漏） |
| `%s` 输出乱码 / 程序访问冲突 0xC0000005 | `%s` 要**地址**；传了单个字符或整数，那个数被当地址读 | 单字符用 `%c`，整数用 `%d`；`%s` 只配数组名/指针 |
| `printf("%d %s", ret);` 报 C4473 | 占位符比参数多，多出来的去读栈上野地址 | 数一遍：`%` 几个，逗号后就几个值 |
| 比值永远差一点、判断总不对 | 两个 int 相除**先截断再存**，左边是 double 也救不回 | 先转再除：`(double)a / b` |
| `printf("%d", c/19)` 而 c 是 float，输出天文数字 | 格式符是"取件凭证"，`%d` 按 4 字节 int 读 8 字节 double | `%f`；要整数就 `(int)(c/19)` |
| `printf("%f", 4.321)` 输出 `4.321000` | `%f` 默认 6 位小数 | `%.3f` 控制位数，或 `%g` 自动去 0 |
| `(int)(a*10)` 末位少 1（123.4 → 1233） | float 存不准（1233.9999），`(int)` 向 0 截断 | 先四舍五入：`(int)(a*10 + 0.5)` |
| 前面的输入"吃掉"了后面的字符 | 上次留下的回车被 `%c` 接走 | `scanf(" %c", &c);`（前面加空格） |
| 用 `%d` 读字符串 `scanf("%d", c);` | 格式符的"户口"和变量类型不一致 | 字符串只用 `%s` |
| `printf` 没写 `\n`，输出时有时无/崩溃时全消失 | printf 先进缓冲区，遇 `\n` 或正常退出才上屏 | 普通输出一律带 `\n`；只有输入提示可控 |
| 用 `printf` 读入：`printf("请输入%d", &x);` | `printf` 只会"说"不会"听"，它把地址打了出来 | 提示用 `printf`、读入用 `scanf`，分两行 |
| 报 C4996 `scanf` 不安全 | 微软认为它不查长度 | 文件**第一行** `#define _CRT_SECURE_NO_WARNINGS` |
| `scanf_s` 在比赛平台编译失败 | 微软私有函数，gcc 不认 | 统一标准 `scanf` + 顶部宏 |
| 换回 `scanf` 后多写了一个大小参数 | `scanf_s` 才要大小，标准 `scanf` 不要 | `scanf("%s", s);` |
| `scanf("%s", 小数组)` 输入过长崩 | `%s` 不限长度，它不知道数组多大 | 数组开够；或 `scanf("%100s", s);`（数组 ≥ 101） |
| `scanf` 格式串末尾多一个空格 → 程序像卡死 | 空格 = "跳过空白直到非空白"，必须等你再输一个字符才返回 | 格式串**两头都不留空格**；`"\n"` 结尾同病 |
| `printf` 参数把逗号打成 `&` → 乱码 +「烫烫烫」 | `&` 是**按位与**，把两个值合成一个整数，`%c` 没参数可读 | 参数之间一律逗号；`&` 只出现在要地址的地方 |
| `double` 用 `%f` 读 → 得到 `-9.25e+61` | `%f` 只写 4 字节，高 4 字节还是 `0xCC` | **`scanf` 里 double 必须 `%lf`**；`printf` 里 `%f` 就行 |
| `fgets` 后写 `if (a == NULL)` 等于没判 | 数组名是常量地址，永远不等于 NULL；返回值也没接 | `if (fgets(a, sizeof a, stdin) == NULL) return 0;` |
| `fgets` 调用两次（写完又放进 if） | 每调用一次消费一份输入 | 一个流程里只调一次，把返回值接住 |
| `struct stu s[3];` 没初始化 → 一屏「烫」 | 栈上内存填 `0xCC`，`%s` 一路读到 `'\0'` 才停 | 声明就 `= { 0 }`；根治是查"为什么没读进去" |
| 报 C6031「返回值被忽略: scanf」 | `scanf` 有返回值（读到几项），静态分析提示你丢了线索 | `if (scanf("%d,%d", &a, &b) != 2) {...}` 或 `(void)scanf(...)` |
| `printf( % d, b);` 报 expected expression before '%' | 格式串忘加双引号，裸露的 `%` 被当成取余；`%` 与 `d` 之间也不能有空格 | `printf("%d", b);` |
| `scanf_s("%s", suzu);` 运行时访问冲突 | `scanf_s` 对 `%s`/`%c` **强制**多传一个缓冲区大小；少写就抓一个垃圾值当长度，疯狂往外写 | 补参数，或**干脆换回 `scanf`** + 顶部宏 |
| `scanf("%s", &suzu);` 多写了 `&` | 数组名本身就是地址 | `scanf("%s", suzu);`——口诀"数组名不加 `&`，其它都加" |
| `strlen(arr)` 只测出 1（读进 5 个字符） | 循环写成 `scanf("%c", &arr);`——**漏了 `[i]`**，每轮都写进 `arr[0]`；两个地址数值相同，不报不崩 | `scanf("%c", &arr[i]);`——`&` 后面必须跟"名字[下标]" |
| 为了让末尾是 `'\0'` 多读一格（`m+1`），结果整串右移、`arr[0]` 变回车 | `%c` 不会补 `'\0'`；补它的是 `= {0}`。多读的那格正好是上次残留的回车 | 逐格读 `m` 个就够，右下标写 `m-1`，`arr[m]` 天然是 0 |
| 想用 `char` 数组读"一串带空格的整数"，只读进 1 个/读到空格就停 | `%c` 一次读 1 个字符；`%s` 遇空格停；`'3'` 的码是 51 不是 3 | 一串整数用 `int` 数组 + 循环 `%d`；一个单词用 `%s`；整行用 `fgets` |
| 统计题只印了数字，漏了对应字母（要 `a 2` 却只出 `2`） | 桶的下标是数字，字母要用 `'a' + i` 还原 | `printf("%c %d\n", 'a' + i, cnt[i]);` |

## <span style="color:#B87A5C">1.3 数组·字符串·变量</span> <a id="p1-3"></a>

| 症状 | 病因 | 药方 |
| --- | --- | --- |
| `a[10]` 越界读到乱值 | 10 格的合法下标是 0~9 | 下标 `< len`，不是 `<= len` |
| 用 `==` 比较两个字符串永远不等 | `==` 比的是**地址**，不是内容 | `if (strcmp(a, b) == 0)`——相等返回 0 |
| `if (strcmp(...))` 把"不等"当成真 | `strcmp` 返回**差值**，0 才是相等 | 记法：它是"减法算出的差" |
| 变量第一次用就是乱码 | 没初始化，里面是垃圾值 | 声明时随手 `= 0` / `= 1` |
| `int i, a = 0;` 以为两个都归零 | 逗号声明时 `=` 只贴紧邻的那一个 | `int i = 0, a = 0;` |
| 用 `int` 数组装字符串，`strlen` 永远算出 1 | int 每格 4 字节，字符后面跟着 3 个 `0x00`，`strlen` 走到第一个 0 就停 | 装文字一律 `char`；int 数组的长度自己拿变量存 |
| 剪尾巴和取长度顺序反了，长度多 1 | `fgets` 的串还带着 `'\n'` | **先剪、后量**：`a[strcspn(a,"\n")]='\0';` 再 `strlen` |
| 复制完字符串末尾多一个旧字符 | 结束符写成了 `dest[i+1]`，跳过一格 | `dest[i] = '\0';`——循环停在哪就写哪 |
| `strcpy(a, b)` 方向写反，数据静静消失 | `strcpy(目标, 源)`，左边是"倒进去的杯子" | 记法：`strcpy(要改的, 不要改的)` |
| 循环体内又重新 `char* w = strtok(...)` → 死循环 | 花括号里再写 `char*` 是**新变量**，遮住了外层 | 去掉 `char*`，只赋值（C4456 提示的正是它） |
| `p - a` 跨数组相减，输出天文数字 | 指针相减只在同一块连续内存内才有意义 | 在哪个数组里查就减哪个：`p - b` |
| 桶数组 `int cnt[26];` 输出一堆怪数字 | 局部数组不清零，桶里全是垃圾 | `int cnt[26] = {0};` |
| 算出答案却没打印（打印了别的变量） | `printf` 里写错变量名（`max` 写成 `count`） | 输出前念一遍："哪个变量装的是答案？" |
| 想通过指针改原变量，写成 `&x = 20` | `&`/`*` 方向贴反：门牌号不能往里塞值 | `*q = 20;`——要地址用 `&`，要改值用 `*` |
| 大数组写在 `main` 里，程序莫名崩 | 局部变量在栈上，栈只有几 MB | 大数组放 `main` 外面（全局）或 `malloc` |
| `int suzu[0];` 编译器居然不报错 | 零长度数组是 GCC 扩展，MSVC 直接报错 | 元素个数必须是正数 |
| `int a[] = (1, 2, 3);` 报错 | 数组初始化必须花括号 | `int a[] = {1, 2, 3};` |
| 二维数组传参报一串 C4133 / C2109 / E0142 | 形参没写全（漏 `char`、漏第二维） | `void f(char arr[][3])`——第一维可省，**第二维必须写** |
| 结构体数组读姓名 `scanf("%s", &s[i].name)` | `name` 是数组，本身就是地址 | `scanf("%d %s", &s[i].score, s[i].name);` |
| 循环里写 `s[1].name` / `s.name[i]` | 下标写死；或"袋"和"项"的顺序反了 | 一律 `s[i].name`——先挑袋 `[i]`，再翻项 `.成员` |
| `max` 既当分数又当下标 → 最高分总是最后一个 | `int max = 0;` 本意是分数，却 `max = i;` 存下标，再拿 `s[max].score` 用 | 改名 `maxIdx`；一个变量只存一种东西 |
| `sum / 5` 求平均，小数被截断 | 两个 int 相除是整数除法（80.8 → 80） | `(double)sum / count` + `%.1f` |
| `p - a` 跨数组相减 | 指针相减只在同一块连续内存内有意义 | 在哪个数组查就减哪个 |
| `doors[i][j] = (i+1)*(j+1);` 写成 `doors[i+1][j+1]`（下标整体偏移） | 把"人的编号"当"下标"用，`[i+1]` 已经越界 | 下标从 0、编号从 1，两者**不要混着写** |
| 声明 `int n[11][2];`，读入却用 `n[i][2]` | 两列的合法下标只有 0、1；`n[i][2]` 已走到**下一行第 0 格**（行优先平铺），不报错 | 声明 / 读入 / 使用三处的**列数必须一模一样** |
| 数组开小，输入一长就崩 | 题目说"不超过 10⁶"就要开 10⁶ + 1 以上 | 按上限开，再留几个富余（`+5`） |
| `sizeof(suzu)/sizeof(suzu[0])` 算出 0 | 数组声明成了 `suzu[0]`（0 个格子） | 先把数组开够；`sizeof` 算的是**容量**，不是实际长度 |
| 复制字符串只抄 `len` 个字符，末尾没抄 `'\0'` | 循环写 `a < strlen(s)`，漏了结束符（靠全局数组补 0 侥幸） | 用 `strcpy`，或循环写 `<= strlen(s)` |
| 把字符存进 `int` 数组（`scanf("%s", intArr)`） | `%s` 按 1 字符 1 字节写，而 int 一格 4 字节 → 拼成天文数字、桶越界 | 装字符一律 `char` 数组 |
| 内层又声明同名 `int b`，外层那个从没用过（C4101） | 变量重名**遮蔽**，两个是不相干的盒子 | 删掉没用的外层变量；内层临时变量改名 |
| `a[i+1] = '\0';` 补结束符补错位置 | 循环退出时 `i` 正好停在"最后一个字符的下一格"；靠 `= {0}` 兜住才没露馅 | 写 `a[i] = '\0';`——**循环停在哪，结束符就写哪** |
| 数组只读进 1 个数，其余全是垃圾值 | `scanf("%d", suzu)` 一次只吃一个整数，只填第 0 格 | 读一批数必须循环逐格：`for (i=0;i<n;i++) scanf("%d", &a[i]);` |
| 算阶乘结果不对甚至停不下来 | 一个变量既当输入又当累乘结果，循环体改了条件里的数 | 输入、结果分开：`int r = 1;` 再 `for (i=1;i<=n;i++) r *= i;` |
| 求和/求阶乘结果像随机数 | 累加器没初始化（加法从 0、乘法从 1 出发） | `int sum = 0;` / `int r = 1;` |
| 二分查找死循环 | 没找到时不收缩区间，`mid` 永远同一个值 | 每轮必须二选一：`right = mid-1;` 或 `left = mid+1;` |
| 二分查找读到 `a[10]` 越界值 | 10 个元素最大下标是 9；`left = 1` 起步会算出 mid = 10 | `left = 0; right = n - 1;` |
| 循环用 `sizeof` 算的上限，把没输入的格子也处理了 | `sizeof` 给的是**容量**（1000005），不是实际长度 | 上限用 `strlen` 得到的**实际长度** |
| `strlen(suzu)` / `suzu[0]` 算出来总是 0 | **顺序错了**：写在 `scanf` 之前（全局数组那时全是 0）——**头号惯性盲区，已复发 3 次** | 凡"依赖输入内容"的语句，一律写在 `scanf` 之后 |
| 调 `strlen` 报"未声明的标识符" | 它住在 `<string.h>` | 顶部 `#include <string.h>` |
| `char s[5] = "hello";` 编译告警 | `"hello"` 实际占 6 格（5 字母 + `'\0'`） | `char s[6] = "hello";` |
| 数组只用几个，程序却占很多内存 | 声明那一刻就一次性分配整块，用不完也占着 | 按题目上限开，别随手开几亿 |
| 在循环里 `struct stu j; scanf(...)`，一个都留不住 | 变量寿命只到它所在的大括号，每轮新建、本轮销毁 | 用结构体数组 `struct stu s[105];` 在循环外声明 |
| 复制完字符串末尾多一个旧字符（`hhhnihaor`） | 结束符写成 `dest[i+1]`，跳过一格，那格留着旧值 | `dest[i] = '\0';` |
| 写完 `my_strcpy` 直接 `return 0`，没打印就说"跑通了" | 字符串错误是"沉默型"的，不打印看不见 | 每次复制完 `printf("[%s] %zu\n", a, strlen(a));` 再比 `strcmp` |
| `my_strcat` 写完目标串一点没变 | 两个游标串了：条件是 `yuan[i]`（目标位置去量源串），源早结束 | `i` 管目标、`j` 管源；**"还有没有内容"要问源** |

## <span style="color:#B87A5C">1.4 循环</span> <a id="p1-4"></a>

| 症状 | 病因 | 药方 |
| --- | --- | --- |
| `while (i < 10)` 死循环 | 忘了 `i++` | 检查循环变量每轮是否变化 |
| `i++` 关进 `if` 里 → 死循环 | 条件不成立时下标不动 | 步进与 `if` 平级；用 `for` 写在头上最保险 |
| 步进写在 `continue` 后面 → 死循环 | `continue` 跳过本轮剩下的全部语句 | 步进必须写在 `break`/`continue` 之前 |
| 循环一次都不跑 | 条件是永远不成立的式子（`j < 0`） | 把具体值代进去验算一遍 |
| `for (i = 0; i <= a; i++)` 读到了 `s[a]` 垃圾值 | n 个元素合法下标是 `0 ~ n-1` | 上界一律 `i < n`；读入/遍历/打擂台三处边界一致 |
| 遍历条件写成 `arr[i] == '\n'` | 循环条件写的是"继续的理由"，不是"停下的理由" | `arr[i] != '\0'` 或 `i < len` |
| 终点站认错：`scanf("%s")` 的串里没有 `'\n'` | 回车留在缓冲区，数组末尾是 `'\0'` | 终点写 `'\0'`；`fgets` 才含回车 |
| 想倒着走却写了 `b++` | 步进方向和目标方向不一致 | 从右往左 → `b--` |
| 重试循环卡死 | 循环体内没重新读入，条件一直是旧值 | `while(1){ scanf(...); if (合法) break; }` |
| `break` 后面还写语句 | 那行是死代码，永远执行不到 | 要输出的挪到循环外 |
| `while (b <= c) return 0;` 循环形同虚设 | 无花括号时循环体只有紧跟一条语句，而它是 `return` | 循环体用 `{}`；`return` 不进循环 |
| 斐波那契滚动变量越滚越离谱：`a = x+y; y = a; x = y;` | 顺序错：先把旧 y 覆盖了，x 抄到的是新值 | `c = x+y; x = y; y = c;`——先挪旧、后填新 |
| 非 `void` 函数某条路没 `return` → 垃圾值 | 算进局部变量 ≠ 交货 | 每条路都 `return`；最好最后一行无条件 `return` |
| `printf` 循环里写了 `return 0;` | `return` 关的是整个函数/程序 | 跳过本轮用 `continue`，结束循环用 `break` |
| `do { ... } while (b < len)` 报错 | `do-while` 末尾的 `while(条件)` 后面**必须加分号** | `do { ... } while (b < len);` |
| 循环条件里 `\|\|` 连接，少写一个 `!` → C2106 | 优先级把句子粘歪：`A \|\| b = c` 被读成 `(A \|\| b) = c` | 每个比较写完整；看 C2106 先问"`=` 左边是变量还是表达式结果" |
| 嵌套循环结束后用 `suzu[j]` 打印，拿到垃圾值 | 内层退出时 `j` 已 `++` 成 n（出局值） | 要打印外层的数用 `suzu[i]` |
| 找"只出现一次的数"判据写 `count == 0`，永远没输出 | 每个数至少和它自己匹配一次，count 最小是 1 | 判据写 `count == 1` |
| 循环只跑了一次就结束了 | `do-while` 是"先执行后判断"，至少跑一次 | 先想清楚是"至少做一次"还是"可能一次都不做"；后者用 `for`/`while` |
| 输入空串时循环越界乱跑 | `do-while` 无条件先执行一次，第 0 格 `'\0'` 被改掉，失去边界 | 用 `for (i=0; i<len; i++)` 或 `while (s[i] != '\0')`，对空串都安全 |
| 循环里只处理了第一个字符 | `if/else` 写在了循环**外面**，只对 `s[0]` 判断一次 | 循环套 `if`（嵌套），不是并列 |
| 把 `break` 当"状态复位"用 → 循环被提前掐死 | `break` 是彻底跳出循环，不是"这一轮结束" | 非字母时只 `in_word = 0`；**全程不需要 `break`** |

## <span style="color:#B87A5C">1.5 程序结构与编译环境</span> <a id="p1-5"></a>

| 症状 | 病因 | 药方 |
| --- | --- | --- |
| 在 `main` 外直接写 `scanf` / `srand`，报 E0077+C4430+C2365 | 文件顶部是"户口簿"，只登记；干活语句必须在 `{}` 里 | 执行语句进 `main` |
| 菜单输 1 什么都不发生 | 把函数**调用**写成了**声明**（`void game();`） | 要它干活就写 `game();` |
| 头文件声明与 `.c` 定义参数对不上 | 招牌与门店不一致 | 声明和定义**一字不差**，改参数同步改 `.h` |
| `int fibonacci(...)` 报 C2601「局部函数定义」 | 函数套进了另一个函数内部 | 函数平铺在文件里；要提前调用就先写原型 |
| 同一个 `main` 里 `int b = ...` 写三次，报 C2374 | 同一作用域变量只能声明一次 | 一次只跑一条路线；或分文件 |
| 报 C4715「不是所有控件路径都返回值」 | 赋值不是交货，走到末尾没有 `return` | `return x + sum(x-1);` |
| 输入校验只写了 `printf("输入错误")` | 提示不是拦截，喊完照样往下跑 → 递归到栈溢出 | 校验分支里必须 `return`；函数里也兜底 |
| `s(arr,a,b); if (s == 1)` | 返回值没人接，拿函数名（地址）和 1 比 | `int r = s(...); if (r == 1)` |
| `if` 后面没花括号，后面三条语句全脱出控制 | `if` 不加大括号时只买得起**一条**语句 | 多条语句必须 `{}`；递归终点写 `if (...) return;` |
| 报 LNK1168 / LNK1104 无法写入 exe | 旧 exe 还在运行，文件被占用 | 关黑框 / 任务管理器结束进程 / Shift+F5 |
| `source.txt` 放 `.sln` 旁边却 fopen 失败 | VS 调试的当前工作目录是**工程目录**（`.vcxproj` 所在），不是 `.sln` | 文件放工程目录；或打印 `_getcwd` 确认 |
| 输字母给 `scanf("%d")` → 疯狂刷屏 | 读失败时字符赖在缓冲区，下一轮再失败 | 检查返回值 + 清空缓冲：`while ((ch=getchar()) != '\n' && ch != EOF);` |
| 结尾写 `lp == NULL;`，没有任何效果 | `==` 是比较，算完 0/1 就扔 | 置空写 `lp = NULL;` |
| 同一作用域第二次写 `FILE* dp = ...;` → 重定义 | 类型只在声明时写一次 | 第二次只写 `dp = fopen(...);` |
| `fclose(NULL)` 崩溃 | 对没打开成功的文件也关了 | `fclose` 只关"确实打开成功"的；失败分支先关已开的再 return |
| 大数组 + 递归 → 0xC00000FD 栈溢出 | 局部变量都在栈上，栈只有几 MB | 大数组改全局/`malloc`；递归深度检查 |
| 改完字符串却没看到输出 | 漏了 `printf`——**算了不等于输出了** | 收尾自查：题目要的每样东西都有一条输出语句吗？ |
| 同一个头文件 `#include` 写两遍 / 引了用不到的头 | 重复不报错但冗余；多余头文件让意图不清 | 只留用得到的，每个一次 |
| `#define _CRT_SECURE_NO_WARNINGS` 写了仍报 C4996 | 位置错了：必须在**所有 `#include` 之前** | 挪到文件第一行 |
| 函数里用 `scanf` 读坐标，回到 `main` 变量还是 0 | **值传递**：形参是副本，改副本不影响原件 | 要改外面的变量就递地址（`int* px` + `&x`）；或干脆别往外传，在函数内部声明 |
| `if/else` 缩进一样深，以为 `return i;` 也在 `else` 里 | C 不认缩进：不加大括号时 `else` 只买一条语句（本例靠前面的 `return` 挡住才侥幸对） | 分支里多条语句必须加 `{}`；更好是 `return f(a-1) + f(a-2);` 一行收口 |
| 忘了给结构体/函数补 `;` 或漏 `#include`（柔性数组题） | 声明末尾漏分号 → 报错跑到下一行；漏 include → C4013 | 每个 `struct { };` 结尾补 `;`；用到谁先想它住哪个头文件 |

## <span style="color:#B87A5C">1.6 思维方式</span> <a id="p1-6"></a>

| 症状 | 病因 | 药方 |
| --- | --- | --- |
| 玩家输入的 1~3 直接当数组下标 | 人话编号和数组下标差 1，越界还不报错 | 输入 1~3 内部 `-1`，或输入 0~2 直接用 |
| 三子棋判赢判不出 / 一开局就赢 | 漏了三列、没排除空格、硬编码棋子符号 | 三行 + 三列 + 两条对角共 8 条；三条都要"相等 **且** 非空格"；返回胜方而不是打印 |
| 不知道逻辑写循环里还是循环外 | 没分清"搬运"和"判断"的角色 | 循环是搬运工，`if` 是翻译官——**嵌套**关系 |
| `if/else` 两个分支贴反了 | 条件对了，内容贴反 | 写完用中文念一遍："如果它是数字，那就换成___" |
| 两个分支条件一字不差（复制没改） | 第二个条件永远不成立，成了死分支 | 把两个条件并排念一遍 |
| 字符串反转写出来和输入一模一样 | 把"反转"当"复制"——改的是**位置** | 问自己："我要改位置还是内容？"改位置必须**交换** |
| 一种解法跑通就以为任务结束 | 只求"能跑"，没想"有没有更省" | 跑通后多问一句："还有没有更省内存、更短的写法？" |
| `i = -1` 时 `if (i > sizeof(i))` 居然成立 | `sizeof` 返回 `size_t`（无符号），`-1` 变成 4294967295 | `(int)sizeof(i)`，或先存进 int |
| 题目要"找不到输出 not found"，代码没兜底 | 只写了"找到时做什么" | 找到就 `return`/`break`，循环后写兜底；或用 `found` 标志 |
| 边界总出错（0、最后一个、空输入） | 只想着正常情况 | 写完自问：输入 0 会怎样？只有一个字符呢？最后一个越界吗？ |

## <span style="color:#B87A5C">1.7 文件与二进制专项</span> <a id="p1-7"></a>

> 文件是最后学的、也是坑最密集的一章（T79–T85）。这里单独成节。

| 症状 | 病因 | 药方 |
| --- | --- | --- |
| 复制"反着跑"，源文件被清空 | `"r"`=文件→程序、`"w"`=程序→文件**且先清空**；把源用 `"w"` 打开等于先清空再读 | 源 `"r"`、目标 `"w"`；**永远不给源文件 `"w"`** |
| 文件名写错一字符（`scoure, txt` / `dest. txt`）→ 读端 NULL、闪退或多出一个怪文件 | 文件名是**精确字符串**；`fopen` 不报拼写错，只会"新建"或"返回 NULL" | 全程复用一个变量：`const char* SRC = "source.txt";` |
| 两个 `fopen` 只判了一个，`perror` 后没 `return` → 崩 | 两个都可能失败；`perror` 只是喊一声，不会停 | 两个都判，失败就 `return`；目标失败先关源 |
| `int ch;` 写在两条语句之后 | 旧标准要求声明在块开头 | 声明统一放函数开头 |
| `"a"` 打开后直接 `fgets` 读不到任何东西 | `"a"`/`"w"` 是**只写流** | 写完 `fclose`，再用 `"r"` 重新打开 |
| `fputs` 写完两行粘在一起 | `fputs` **不自动加换行** | `fprintf(fp, "%s\n", s)` 或补 `fputc('\n', fp)` |
| `fputs(ch, fp) != EOF;` 单独一行 | 是**比较表达式**，算完就扔 | 要检查就 `if (fputs(...) == EOF) {...}`；不检查就只写调用 |
| 文件里每行之间多一个空行 | `fgets` 已把 `'\n'` 读进 `ch`，再补一个就两个 | 二选一：直接 `fputs(ch, fp)`；或先剪 `ch[strcspn(ch,"\n")]='\0'` 再 `fprintf("%s\n")` |
| 先写再剪换行 → 还是两条换行 | 顺序错：`fputs` 已经把 `\n` 写进去了 | **先剪 → 再写 → 再补** |
| 只调一次 `fgets` 就想读整个文件 → 只打印第一行 | `fgets` 一次只读一行 | `while (fgets(ch, sizeof ch, fp) != NULL) { ... }` |
| `fread` 套在 `for (i<5)` 里，只有第一次拿到数据 | `fread` 一次就搬 count 份，后面已到文件尾返回 0 | 只调一次：`size_t got = fread(...); for (i=0;i<got;i++)` |
| `ftell` 求大小少 1 | 先 `fseek(fp, -1, SEEK_END)` 再 `ftell`，拿到的是 size-1 | `fseek(fp, 0, SEEK_END); long size = ftell(fp);` |
| `l * sizeof(char)` 想换算字节 | `sizeof(char)` 恒为 1，`ftell` 本身已是字节 | 直接 `long size = ftell(fp);`，用 `%ld` |
| 二进制数据写进 `"stu.txt"` | `.txt` 是文本约定，`"wb"` 写的是原始字节，还毁掉了 T81 的文本文件 | 二进制用 `"stu.dat"` + `"wb"/"rb"` |
| `printf("%d", t)` 而 `t` 是 `size_t` | `%d` 只读 4 字节，`size_t` 在 x64 是 8 字节 | `%zu`，或 `(int)t` |
| `for (i=0; i<t; i++)` 中 `i` 是 int、`t` 是 size_t | 有符号/无符号比较，负数会变成巨大正数 | `i < (int)t`，或把 `i` 声明成 `size_t` |
| `free(fp)` 释放 `FILE*` | `free` 只放堆内存，`FILE*` 要靠 `fclose` | `fclose(fp); fp = NULL;` |
| 对数组 `s` 写 `s->name` | `s->name` 等于 `s[0].name`，只处理第 0 个 | 数组元素用 `s[i].name`；只有指针 `p` 才用 `p->name` |
| `fscanf(fp, "%s %d", s->name, s->score)` 少 `&` | `%d` 要 `int*`，`score` 是 int | `fscanf(fp, "%s %d", s[i].name, &s[i].score)` |
| 读文件用 `for (i<5)` 且不判返回值 | 文件不足 5 条时读到垃圾/旧值 | `while (fscanf(fp, "%s %d", name, &score) == 2) i++;` |
| `remove("hh. txt")` 少写字母 → 删除失败还继续 | 文件名手打不一致；返回值没检查 | 打印 `remove` 返回值；名字复用变量 |
| 只验证改名后的新文件，没验证旧文件消失 | 验收不完整 | 改名 = **旧名 fopen 为 NULL + 新名能打开** |
| `"w"` 打开失败 ≠ 清空失败 | 失败返回 `NULL`，文件根本没打开，谈不上清空 | 先看返回值，别猜 |

## <span style="color:#B87A5C">1.8 高频复发榜</span> <a id="p1-8"></a>

> 按复发次数排，这是最该盯的八条。

| 排名 | 坑 | 次数 | 一句话药方 |
| --- | --- | --- | --- |
| 1 | `=` 与 `==` 混用 | 6+ | 每写 `if` 先问"提问还是做事"；常量写左边 |
| 2 | `scanf` 漏 `&`（尤其 `arr[i]`、`n[i][j]`） | 5+ | 传"名字"不加、传"名字[下标]"必须加 |
| 3 | 依赖输入的语句写在 `scanf` 之前 | 3+ | 先读入，再 `strlen` / 取 `s[0]` |
| 4 | 非 `void` 函数漏 `return`（C4715） | 3+ | 每条路都要 `return`，最好末尾无条件一条 |
| 5 | `if` 少花括号，后续语句脱出控制 | 2+ | `if` 只管一条语句；要管两件事就加 `{}` |
| 6 | 区间判断用 `>` `<` 漏端点 | 2+ | 一律 `>=` `<=` |
| 7 | 返回值被丢弃（`strtok`/`scanf`/`fgets` 裸调用） | 2+ | 用变量接住，或放进 `if` 条件 |
| 8 | 文件名写错一字符（空格/逗号/拼写） | 2+ | 全程复用同一个字符串变量 |

## <span style="color:#B87A5C">1.9 我的弯路档案（真实踩坑实录）</span> <a id="p1-9"></a>

> 前面 1.1–1.8 是"按坑分类的浓缩表"，这一节是"**按当时怎么错的**"的原始记录：哪一版、错成什么样、当时为什么会那么想。
>
> 想看完整过程（第几版、批改记录），去《每日刷题日志》对应题目卡片下的「我的弯路」与「批改历程」。

### 一、输入与字符串

- **T76 第 2 版**：用 `int a[100]` 装字符 → 内存变成 `'h' 00 00 00 'e'…`，`strlen` 撞上第一个 `0x00` 就停，**输入多长都只算出 1**。
- **T76**：`if (a == NULL)` 判数组名——数组名是常量地址，永远不为空，这个判断毫无意义。
- **T76**：`strcspn(a, '\n')` 用了**单引号**——形参要的是 `const char*`，必须写 `"\n"`。
- **T76**：先 `strlen` 再剪换行 → 长度永远多 1；**顺序必须是"先 `fgets` → 再剪 → 最后才量"**。
- **T76**：`a[i + 1] = '\0'` —— 结束符要写在 `i` 的位置，不是 `i+1`。
- **T76**：三条读行路线挤在同一个 `main` 里 → 互相抢输入，谁也读不对。
- **T77**：按"字母 + 空格"数接缝 → `hello world  foo` 数出来是 2；应该"数进门的那一次"。
- **T77**：`a[i] > 'a' && a[i] < 'z'` 漏端点 → `banana` 数成 3；区间一律 `>=` `<=`。
- **T77**：`else` 里写了 `break` → 一遇到非字母，整个循环被掐死。
- **T77**：`szieof` 拼错 → C3861「找不到标识符」，找半天以为是头文件问题。
- **T51**：以为 `%c` 不补 `'\0'` 所以要"多读一格结束符" → 实际读到的是上次残留的**回车**，整串右移，首尾比较第一步就失败。
  - 补 `'\0'` 靠的是 `char arr[100] = { 0 };`，不是多读一格。
- **T51**：`if (s == 1)` 拿**函数名**当返回值 → 永远不成立，永远输出 `no`。
- **T78**：`printf("%d", count)` 打印错变量 → 这个坑第 3 次犯，输出前必须再确认"哪个变量装着答案"。

### 二、循环与下标

- **T5 第 1 版**：步进方向写反（该 `right--` 写成 `++`）。
- **T5 第 1 版**：循环条件恒假（`b < 0`）→ 一次都不跑。
- **T5 第 2 版**：自创"借第二个数组复制"版 → 跑通了，但**忘抄 `'\0'`** 是隐患，还多开一块内存。
- **T78**：`if (max < cur)` 放在每轮开头 → 靠最后一个 `'\n'` 多跑一轮才侥幸正确。
- **T36**：把 1~3 当 0~2 用（下标从 1 开始）→ 越界，还少算了第一个。
- **T17**：重试循环里不重新读输入 → 输入没刷新，直接死循环。
- **T37**：循环条件写成 `j < 0`（恒假）→ 棋盘没清空，打印一片乱码。

### 三、函数与结构

- **T43**：整个函数被写进 `main` 的花括号里 → **C2601「局部函数定义」**，函数名和 `{` 全画红波浪线。
- **T46**：函数定义末尾多写一个分号 → 一次报 6 条错，根因只有这一个。
- **T45**：打擂台只记了值、没记下标 → "我知道最高分是 90，但不知道是谁"。
- **T45**：`scanf("%s", &s[i].name)` 多写 `&`（数组成员本身就是地址）。
- **T45**：`printf("%d %s", ret)` —— 两个占位符只给了一个参数。
- **T52**：`for (k; k > 2; k--)` 初始化部分留空 → 能编过，但极容易看错，建议写全。
- **T37**：**形参连续三轮都没写全**（`void dayin(arr[][])` → `void dayin(arr)`）→ C4133、E0142 一窝报错。
- **T37**：`hhh.h` 缺 `#pragma once`，`game.c` 漏 `#include "hhh.h"` → C4013「函数未定义，假定返回 int」。
- **T37**：**招牌和门店不一致**——头文件里声明 `void dayin();`，定义却带参数。

### 四、项目实战（三子棋）

- **T37**：`printf("请输入坐标%d %d", &x, &y)` —— 把 `printf` 当成 `scanf` 用，`x`/`y` 根本没被赋值。
- **T37**：`a == b == c` 连写比较 → `==` 左结合，先算出 0/1 再和第三个比，**判赢永远不触发**。
- **T37**：`if (...);` 多写一个分号 → 分支变成空语句，后面的代码无条件执行。
- **T37**：判赢三漏洞——漏查三列、没排除"三空格"（一开局就判赢）、`'x'` 与 `'X'` 大小写混用。
- **T37**：`srand` 写进"取随机数"的函数里 → 每次调用都重置种子，电脑永远下同一步。
- **T37**：`return x = rand() % 3;` —— `x` 根本没声明。
- **T37**：字符串里直接按回车 → C2001 + C2146；文件编码不符 → C4819。

> **共性**：这些弯路里，真正"不会算法"的很少，绝大多数是 **符号（`=` / `==` / `;` / `&`）**、**顺序（先读后量）**、**归属（花括号、形参）** 三类问题。写代码时按这三类自查，能挡掉大半。

---

# <span style="color:#6E93B5">第二部分　我提过的问题（Q&A）</span>

> 都是学习过程中真实问过的。**Q** 是当时的疑问，**A** 是一句话答案（细节去《C易错点与函数速查》对应小节）。
>
> **分类逻辑（11 类 · Q1–Q111）**：沿着「数据从哪来 → 怎么存 → 怎么算 → 怎么控制 → 怎么落地」的主线排，同一主题的问题一定挨在一起；编号连续，方便以后直接引用「Q37」。

## <span style="color:#6E93B5">2.1 输入输出（Q1–Q15）</span> <a id="p2-1"></a>

> scanf / printf / fgets / 缓冲区

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q1：为什么 `scanf` 不用报大小，`scanf_s` 却要？**</span>

**答**：`scanf` 只拿到数组的**首地址**——数组名传参时长度信息就丢了，它想检查也无从查起。`scanf_s` 是微软的加固版，强制你多传一个"最多写几格"，把责任压回给调用者。

- 代价：`scanf_s` 是**微软私有**，gcc / 蓝桥杯平台不认，写了直接编译失败。
- 所以统一用标准 `scanf` + 文件顶部 `#define _CRT_SECURE_NO_WARNINGS`，容量由自己保证。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q2：`fgets` 的上限为什么是 `n-1`，不是 `n`？**</span>

**答**：`n` 是**缓冲区总格数**，其中 1 格必须留给结束符 `'\0'`，所以正文最多 `n-1` 个。而回车 `'\n'` **也算在这 `n-1` 个里面**——它会被读进来、存进数组。

- 想最多读 99 个可见字符：数组开 `102`（99 + 回车 + `'\0'` + 1 格保险）最稳。
- 读进来后通常马上用 `line[strcspn(line, "\n")] = '\0';` 把回车剪掉，长度才对。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q3：`fgets` 的第三个参数 `stdin` 是什么？能不能换？**</span>

**答**：`stdin` / `stdout` / `stderr` 是程序启动时自动打开的**三个标准流**，本质都是 `FILE*` 宏——键盘、屏幕、错误输出各占一个。

- 读键盘固定用 `stdin`；读文件就把 `fopen` 返回的 `FILE*` 填进去。
- 不能传文件名字符串（类型不对），也不能写 `&stdin`（它本身就是指针）。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q4：`%[^\n]` 这个用法挺新鲜？**</span>

**答**：这是 `scanf` 的**扫描集**：`[...]` 里写"要读哪些字符"，`[^...]` 反过来——`[^\n]` 就是"除换行以外的全部字符"，所以能读带空格的一整行。

- 必须限长：`%100[^\n]`，否则和 `gets` 一样会溢出。
- 它**不跳前导空白**，上次留下的回车会被第一个读到；解法是在格式串开头加一个空格：`" %100[^\n]"`。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q5：为什么写 `if (scanf(" %99[^\n]", a) != 1)`？**</span>

**答**：`scanf` 返回的是**成功读入的项数**。这里只有一个 `%` 项，正常应得 `1`；`!= 1` 一次性兜住"读到 0 项"和"读到 `EOF`(-1)"两种情况。

- 开头那个空格负责跳过上次残留的回车和空白。
- `99` 是限长：数组开 100，最多写 99 个字符，留 1 格给 `'\0'`。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q6：`scanf` 里的 `a` 不用取地址吗？写了 `&a` 会怎样？**</span>

**答**：`a` 是数组名，本身就是首元素地址（等价于 `&a[0]`），所以不用再加 `&`。

- 写成 `&a` 得到的是"指向整个数组的指针"`char(*)[100]`：**数值一样、类型不对**（C4047 / C4024），能跑纯属侥幸。
- 反过来说，正因为 `scanf` 只拿到地址、不知道长度，它才管不住溢出。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q7：`getchar()` 为什么能数空格，`scanf("%s")` 不能？**</span>

**答**：取决于"取货方式"。`%s` 把空格、换行当**分隔符**，遇到就停并跳过；`getchar` 是**来什么吃什么**，空格、回车、Tab 全都算一个字符。

- 所以统计空格数、字符总数必须用 `getchar` 或 `%c`。
- 接它的变量要声明成 `int`：失败时返回 `EOF`（-1），`char` 可能装不下。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q8：什么时候真的需要清输入缓冲区？**</span>

**答**：`%d` / `%f` / `%s` 会自动跳过前导空白，所以"`scanf` 接 `scanf`"**不必清**；只有后面接 `%c`、`%[`、`fgets`、`getchar` 时才需要——它们不跳空白，会把上一个回车当成输入。

- 免清写法：`scanf(" %c", &c);`（格式串前加一个空格，先跳空白）。
- 输入字母导致格式不匹配时也要清，否则剩下的字符会一直卡在缓冲区。
- **不要用 `fflush(stdin)`**：那是未定义行为，标准 C 不认。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q9：怎么读"一整行"？**</span>

**答**：五种武器，按场景选：

| 写法 | 能读空格 | 能限长 | 说明 |
| --- | --- | --- | --- |
| `%s` | ❌ | 可限 | 遇空白就停 |
| `%[^\n]` | ✅ | 需手写 | 不跳前导空白 |
| **`fgets`** | ✅ | ✅ | **主力**，含回车需剪 |
| `getchar` 循环 | ✅ | ✅ | 手搓，最灵活 |
| `gets` | ✅ | ❌ | **C11 已删除，禁用** |

口诀：**不带空格用 `%s`，读一整行用 `fgets`**。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q10：`fgets` 整行打包和 `getchar` 单字符流水线怎么选？**</span>

**答**：看后面要做什么。

- 要"逐字符分析"（数空格、数单词、转大小写）→ `getchar`，一个字符一个字符流过。
- 要"整行处理"（比较两行、截取子串、拼接）→ `fgets`，先把整行拿稳再操作。
- 两者别混在同一个流程里：一个输入流程只调一次读函数，否则会互相抢字符。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q11：`printf` 不写 `\n` 为什么有时看不到输出？**</span>

**答**：标准输出是**行缓冲**的：内容先进内存缓冲区，遇到 `\n`、缓冲区满或程序正常退出才真正刷到屏幕。

- 程序中途崩掉，缓冲区里没刷出去的字就一起消失——这就是"明明 `printf` 了却没输出"。
- 调试时可以 `fflush(stdout);` 强制刷出，或者养成每个输出都带 `\n` 的习惯。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q12：`%f` 和 `%lf` 到底怎么配？**</span>

**答**：两边规则不一样，这是最容易混的一处。

| 场景 | `float` | `double` |
| --- | --- | --- |
| `printf` | `%f` | `%f`（float 会自动提升为 double） |
| `scanf` | `%f` | **`%lf`** |

- 原因：`printf` 拿到的是**值**，float 会先提升成 double；`scanf` 拿到的是**地址**，必须靠格式符区分"写 4 字节还是 8 字节"。
- `scanf("%f", &d)`（`d` 是 double）只写 4 字节，高位留垃圾 → 输出天文数字或负数。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q13：`scanf` 报 C6031「返回值被忽略」要不要管？**</span>

**答**：它不是语法错误，是静态分析的提醒：你丢掉了"这次读成功没有"的唯一线索。

- 推荐改法：`if (scanf("%d", &n) != 1) { printf("输入有误\n"); return 1; }`
- 确实懒得处理时，可以写 `(void)scanf(...);` 明确表示"我知道我在丢"。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q14：`scanf` 返回值是成功/失败吗？能直接塞进 `if` 吗？**</span>

**答**：不是 0/1，而是**成功读入的项数**——读两个数成功返回 2，读一个返回 1，一个都没读上返回 0，遇到输入结束返回 `EOF`(-1)。

- 所以不能写 `if (scanf(...))`：判断不出"少读了一项"这种情况。
- 正确写法是比较项数：`if (scanf("%d %d", &a, &b) != 2) {...}`。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q15：`printf("%s", 某个整数)` 为什么会崩？**</span>

**答**：`%s` 要求参数是一个**地址**，它从那个地址开始逐字节打印，直到遇见 `'\0'`。

- 传进去一个整数（比如 `printf("%s", 65)`），它会把 `65` 当成地址去读内存 → 要么打印乱码，要么直接访问冲突。
- 正确写法：`printf("%d", n)`（值）或 `printf("%s", s)`（字符串地址）。
- 另一个常见错法：`printf("%s", *p)`——`*p` 已经是字符了，想要字符串应该传 `p`。

---

## <span style="color:#6E93B5">2.2 数组与字符串（Q16–Q36）</span> <a id="p2-2"></a>

> 数组下标、交换、字符串函数、内存函数

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q16：两个数组元素怎么交换？为什么不能只写两行？**</span>

**答**：必须三个动作、一个临时变量：

```c
int t = a[l]; a[l] = a[r]; a[r] = t;
```

- 只写两行（`a[l] = a[r]; a[r] = a[l];`）时，第一步就把 `a[l]` 的旧值覆盖了，第二步拿到的已经是新值，等于两个格子都变成 `a[r]`。
- 这就像两杯水直接对倒——中间必须有个空杯子。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q17：交换要用两个数组吗？**</span>

**答**：不用。`temp` 是**一个格子**，不是一排格子。

- 判断标准很简单：**看有没有 `[]`**——`int t;` 是普通变量（1 格），`int t[10];` 才是数组（10 格）。
- 交换只需要存一个值，所以用普通变量就够。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q18：双下标相遇，循环条件用 `<` 还是 `<=`？**</span>

**答**：结果都正确，但 `<` 更好。

- `<=` 在奇数长度时会多跑一次"自己和自己交换"——不报错，但白干一步。
- 习惯统一写 `while (l < r)`：碰头或交叉就停，语义最清楚。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q19：数组容量该开多大？为什么是 1000005 这种怪数字？**</span>

**答**：题目上限 + 1（给 `'\0'`）+ 几个富余。

- 那个 `5` = 1 个结束符 + 4 个保险位，**没有特殊含义**，只是多开几格防手抖。
- 比赛题务必按题面上限开，开小了会越界，开太大可能超内存限制。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q20：数组占内存吗？只装几个字符也占满吗？**</span>

**答**：占，而且**声明那一刻就一次性分配整块**。

- `char a[1000];` 里只放了 `"hi"`，也照样占 1000 字节，剩下全是垃圾值。
- 这是"容量"和"长度"的区别：`sizeof` 是容量，`strlen` 是实际用了多少。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q21：`int` 数组为什么不能当字符串用？**</span>

**答**：字符串函数靠**逐字节找 `'\0'`** 工作，而 `int` 每格 4 字节。

- `int a[10]; a[0] = 'A';` 内存里是 `41 00 00 00`——紧跟的 3 个 `0x00` 会被 `strlen` 当成结束符，长度永远算出 1。
- 而且 `strlen` 按 1 字节步进，读到第 4 字节才到下一个 int 的开头，位置全错。
- 结论：**装字符就用 `char` 数组**。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q22：`strcpy` 到底复制多少字节？**</span>

**答**：从源首地址逐字节搬，**连 `'\0'` 一起**，遇到 `'\0'` 才停。

- 所以目标空间必须 ≥ `strlen(src) + 1`。
- 它会覆盖目标原有内容，不检查目标够不够大——溢出由你负责。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q23：`strncpy` 和 `strcpy` 有什么坑？**</span>

**答**：`strncpy` 最多搬 `n` 个字节，但两个细节要记牢：

- **源比 `n` 短**：剩下的位置用 `0` 补满（不是 `'\0'` 字符，是数值 0）。
- **源不短于 `n`**：**不会补 `'\0'`**，目标可能不是合法字符串，要自己写 `dst[n] = '\0';`。
- 所以"想安全复制又保证有结束符"，其实 `snprintf` 更省心。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q24：为什么 `strtok` 要传副本？**</span>

**答**：它会**把分隔符改写成 `'\0'`**，直接在原串上动手。

- 想保留原串，先 `strcpy` 一份，用副本去切。
- 第二次起第一个参数必须传 `NULL`，表示"接着上次的位置继续"。
- 分隔符参数是**字符集合**：`" ,\n"` 表示空格、逗号、换行任意一个都算分隔。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q25：`strcspn` 名字怎么记？**</span>

**答**：`c` 是 complement（补集）——数"开头连续**不属于**这个集合"的字符个数。

- 所以 `strcspn(line, "\n")` 正好等于这一行的长度（不含回车），一步就能剪掉换行：`line[strcspn(line, "\n")] = '\0';`
- 找不到目标字符时返回 `strlen(s)`，所以这句**天然安全**，不会越界。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q26：`memcpy` 和 `memmove` 有什么区别？**</span>

**答**：都是按字节搬 `n` 个，区别在**要不要处理重叠**。

- `memcpy` 闷头正着搬，源和目标重叠时会互相覆盖，结果错。
- `memmove` 先判方向（目标在后就倒着搬），重叠也安全，代价是多一次判断。
- 记法：**不确定重不重叠，就用 `memmove`**。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q27：`memset` 能把 int 数组设成 1 吗？**</span>

**答**：不能。它**按字节**设值，`memset(a, 1, sizeof(a))` 会让每个 int 变成 `0x01010101`（十进制 16843009）。

- 只有 0 和 -1 这类"每个字节都一样的值"才安全。
- `int` 数组想全设成某个数，只能老老实实写循环。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q28：`sizeof` 和 `strlen` 有什么本质区别？**</span>

**答**：一个是**容量**，一个是**实际长度**。

| | `sizeof` | `strlen` |
| --- | --- | --- |
| 什么时候算 | 编译期 | 运行期 |
| 数什么 | 占多少字节（含 `'\0'`） | 到 `'\0'` 前有几个字符 |
| 数组传进函数后 | 只剩指针大小（4 或 8） | 正常工作 |

- 所以"数组长度"必须在外面算好再传进去，函数内部 `sizeof` 已经退化。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q29：二维数组怎么传参？**</span>

**答**：`void f(char arr[][3])`——第一维可以省，**第二维必须写**。

- 原因：编译器算 `arr[i][j]` 时要靠第二维知道"每行跨几格"。
- 调用时只写 `f(arr)`，行数单独传（`f(arr, row)`），因为函数里量不出第一维。
- 写成 `void f(char arr[][])` 会报 C4133 类型不兼容。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q30：数组名是地址，那 `arr[i]` 为什么还要 `&`？**</span>

**答**：`arr` 是**首元素地址**（整排的起点），`arr[i]` 是**第 i 格里的值**。

- `scanf` 要的是"往哪写"的地址，所以必须 `&arr[i]`；而 `scanf("%s", arr)` 里 `arr` 本身已是地址，不用 `&`。
- 一句话：**数组名不加 `&`，数组元素必须加 `&`**。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q31：字符串字面量 `char* s = "abc";` 能改吗？**</span>

**答**：不能。字面量住在**只读区**，`s[0] = 'x';` 会直接崩（访问冲突）。

- 要改就写 `char s[] = "abc";`——这是把字面量**复制到可写数组**。
- 两者的差别：`char* p = "abc";` 是"指向只读区"（指针 4/8 字节 + 常量区 4 字节）；`char s[] = "abc";` 是"自己开 4 格并拷贝"。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q32：`strcpy(数组, "zhshdd")` 这样可以复制吗？**</span>

**答**：可以。字面量是**源**（只读，不需要改它），字符数组是**目标**（可写、够大），方向完全正确。

- 危险的是反过来：`char* p = "abc"; strcpy(p, "xyz");` ——往只读区写，直接崩。
- 只要目标够大（≥ 源长度 + 1），`strcpy(arr, "字面量")` 是最常见的初始化方式之一。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q33：`'\0'` 和 `'\n'` 到底谁管什么？**</span>

**答**：两个完全不同的东西，只是长得像。

| | `'\0'` | `'\n'` |
| --- | --- | --- |
| 数值 | 0 | 10 |
| 角色 | **字符串的终点标记** | **一个普通字符**（换行） |
| 谁产生 | 字符串常量/`strcpy`/`fgets` 自动补 | 你按的回车、或 `printf("\n")` |

- 字符串函数（`strlen`、`strcpy`、`printf("%s")`）只认 `'\0'`；
- `fgets` 会把 `'\n'` **当内容存进去**，所以读完通常要手动剪掉。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q34：`'\0'` 是 0 还是空格？**</span>

**答**：是**数值 0**（NUL），不是空格（空格的 ASCII 是 **32**）。

- 两者在屏幕上看起来都"什么都没有"，但值差很多：`'\0'` = 0，`' '` = 32。
- 所以判断字符串结束只能写 `s[i] != '\0'`；写 `s[i] != ' '` 会把空格也当终点，遇到 `"hello world"` 就断在中间。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q35：为什么"先剪再补"还是多出一个换行？**</span>

**答**：顺序反了。正确顺序是 **先 `fgets` 读进来 → 再剪掉它带的 `'\n'` → 最后才补自己的内容**。

- 如果先补内容再剪，`strcspn` 找的是新内容里的换行，位置全错；
- 如果忘了剪就直接 `fputs`，`'\n'` 会原样写回文件 → 每条记录多一个空行。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q36：`strncat` 的 `n` 是"最多追加几个"还是"总长最多多少"？**</span>

**答**：是"**最多再追加几个字符**"，不是总长度。

- `strncat(dst, src, 3)` 表示"从 `src` 取最多 3 个接到 `dst` 末尾"。
- 它**一定会补 `'\0'`**（这一点和 `strncpy` 不同）；目标至少要能装下 `strlen(dst) + n + 1`。
- 和 `strncpy` 对比记：`strncpy` 可能不补结束符，`strncat` 一定补。

## <span style="color:#6E93B5">2.3 指针（Q37–Q47）</span> <a id="p2-3"></a>

> 解引用、指针数组 vs 数组指针、const、多级指针

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q37：`*p++` 和 `(*p)++` 有什么区别？**</span>

**答**：都是"先交出旧值"，区别在**谁加 1**。

- `*p++`：先取 `*p`，然后**指针 `p` 挪到下一格**（`++` 的优先级高于 `*`，实际是 `*(p++)`）。数据没动。
- `(*p)++`：先取 `*p`，然后**那格里的值加 1**，指针不动。
- 记法：括号括住谁，谁就加 1。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q38：想通过指针改值，写成 `&x = 20` 为什么不行？**</span>

**答**：`&` 是"取地址"，拿到的是一个**只读的地址值**，不能往它里面塞东西。

- 就像门牌号是事实，你没法"把门牌号改成 20"，只能"进屋里把东西换成 20"。
- 正确写法：`int* p = &x; *p = 20;`——先用 `*` 找到那间屋子，再赋值。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q39：`*p[2]` 为什么会崩？**</span>

**答**：`[]` 的优先级高于 `*`，所以 `*p[2]` 等于 `*(p[2])`：先取出 `p[2]` 这个值，再把它当地址解引用一次。

- 如果 `p` 是 `int**`，那 `p[2]` 是指针，合法；如果 `p` 只是 `int*`，`p[2]` 就是个整数，拿它当地址就是野指针。
- 想要"第 2 个元素的值"，写 `(*p)[2]`（`p` 是数组指针时），或者直接用 `p[2]`。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q40：值传递的 `Swap` 为什么失败？**</span>

**答**：形参是实参的**副本（复印件）**，函数里改复印件，原件当然不变。

- `void swap(int a, int b)` 里交换的是两个临时变量，函数一返回就销毁。
- 想改原件必须递地址：`void swap(int* a, int* b)`，调用 `swap(&x, &y)`，函数里用 `*a`、`*b` 操作。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q41：`sizeof(int*[5])` 和 `sizeof(int(*)[5])` 差在哪？**</span>

**答**：一个是指针**数组**，一个是**数组指针**。

| 写法 | 是什么 | 大小（32 位 / 64 位） |
| --- | --- | --- |
| `int* a[5]` | 5 个指针组成的数组 | 20 / 40 字节 |
| `int(*p)[5]` | 1 个指针，指向"5 个 int 的数组" | 4 / 8 字节 |

- 口诀：**括号里的是指针，没括号的是数组**；`[]` 优先级高于 `*`。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q42：函数名 `fp` 和 `Add` 有什么区别？**</span>

**答**：`Add` 是**函数名**，它本身就是函数的入口地址；`fp` 是**函数指针变量**，可以指向不同函数。

- `fp = Add;` 之后，`fp(2, 3)` 和 `(*fp)(2, 3)` 完全等价。
- 声明要写返回值类型和参数类型：`int (*fp)(int, int);`。
- 用处：把"要调用哪个函数"当参数传（`qsort` 的比较函数就是这么来的）。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q43：结构体里为什么要用指针？**</span>

**答**：省拷贝、能改原件。

- 传结构体是**整袋复制**（几十上百字节），传指针只递 4/8 字节。
- 更重要的是：想在函数里改原结构体，必须传地址，否则改的是副本。
- 用指针访问成员写 `p->score`，等价 `(*p).score`。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q44：二级指针什么时候必须用？**</span>

**答**：只有一种刚需——**在函数里改"外面的指针本身"**。

- 例子：`void alloc(int** pp) { *pp = malloc(...); }`，调用 `alloc(&p)`。
- 原因：一维指针形参也是副本，想让函数把 `p` 指向新内存，必须把 `p` 的地址递进去。
- 如果只是改指针**指向的内容**，一级指针就够（`void f(int* p) { *p = 1; }`）。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q45：`const int* p`、`int* const p`、`const int* const p` 怎么读？**</span>

**答**：从名字往外读，**`const` 挨着谁就锁谁**。

| 写法 | 能不能改指向 | 能不能通过 p 改值 |
| --- | --- | --- |
| `const int* p` | ✅ 能 | ❌ 不能 |
| `int* const p` | ❌ 不能 | ✅ 能 |
| `const int* const p` | ❌ 不能 | ❌ 不能 |

- 记法：`const` 在 `*` **左边** → 锁数据；在 `*` **右边** → 锁指针。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q46：`char** argv` 是什么？**</span>

**答**：指向"字符串指针"的指针，本质就是**字符串数组**，等价 `char* argv[]`。

- `main(int argc, char** argv)` 里，`argv[0]` 是程序名，`argv[1..]` 是命令行参数，`argc` 是参数个数（含程序名）。
- 从命令行运行 `prog a.txt b.txt`，则 `argc = 3`。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q47：指针到底是"名片"还是"房子"？**</span>

**答**：**指针变量是名片盒，里面放的是门牌号；被指的那块内存才是房子**。这两个角色千万别混。

- `int x = 10; int* p = &x;`：`x` 是房子（4 字节，装 10），`p` 是名片（4/8 字节，装 `x` 的地址）。
- `*p` 是"按门牌号去敲门"，拿到房子里的东西；`p` 本身是"看名片"。
- 所以：`p = &y;` 只是换了张名片（指向变），房子里的东西没动；`*p = 20;` 是进屋改了东西（值变）。

---

## <span style="color:#6E93B5">2.4 函数与递归（Q48–Q56）</span> <a id="p2-4"></a>

> 声明、定义、返回值、递归、传参

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q48：为什么需要函数声明？**</span>

**答**：编译器**从上往下**读代码，遇到没见过的名字就按"返回 `int`、参数随便"来处理。

- 声明（原型）让它提前知道返回类型和参数类型，从而能做类型检查。
- 没有声明就调用，可能报 C4013「未声明的标识符」或隐式返回 `int` 导致的怪问题。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q49：声明、定义、调用怎么分？**</span>

**答**：三个动作三副样子：

| 写法 | 是什么 | 特征 |
| --- | --- | --- |
| `void f();` | 声明 | 有分号、**没有函数体** |
| `void f() { }` | 定义 | **有函数体**、末尾**不能加分号** |
| `f();` | 调用 | 有参数列表、不带返回类型 |

- 类比：声明是"挂招牌"，定义是"开后厨"，调用是"点单"。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q50：函数定义末尾多写一个分号会怎样？**</span>

**答**：定义会被降级成**声明**，后面的 `{ }` 变成一个"文件级游离块"。

- 一次性报 E0169 + C2449 + C2059 三条错误，其实**只有一个根因**：多打了那个分号。
- 看到一串语法错先别慌，从第一条开始找，往往改一处全消。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q51：递归为什么必须写终点？**</span>

**答**：没有基线条件，函数会无限调用自己，每层都占一块栈空间，最终**栈溢出**（0xC00000FD）。

- 三件套：**终点**（`n == 0` / `n < 2` / `*s == '\0'`）+ **拆解**（把大问题变成同类小问题）+ **每条路都 `return`**。
- 终点必须是"能让递归停下来"的条件，且参数每次要**朝终点方向变化**（比如 `n-1`）。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q52：斐波那契用递归还是循环？**</span>

**答**：教学用递归，实战用循环。

- 递归写法直观：`return n < 2 ? n : fib(n-1) + fib(n-2);`，但时间复杂度 `O(2^n)`，`fib(47)` 就超 `int` 范围，且慢到跑不动。
- 循环版滚动三个变量即可，`O(n)`：

```c
int fib(int n) {
    int a = 0, b = 1, c;
    for (int i = 2; i <= n; i++) { c = a + b; a = b; b = c; }
    return n < 2 ? n : c;
}
```

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q53：函数里改了数组，外面能看到吗？**</span>

**答**：能。数组传参传的是**地址**，函数里改的就是同一块内存。

- 但"改指针本身"（让它指向别处）外面看不到——那是改副本。
- 所以排序、反转这类函数直接写 `void sort(int a[], int n)` 就能生效。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q54：函数里 `sizeof(arr)` 为什么不是数组总大小？**</span>

**答**：形参里的数组已经退化成**指针**，`sizeof` 只剩一个指针大小（32 位 4、64 位 8）。

- 所以长度必须从外面成对递：`void f(int a[], int n)`。
- 想在函数里知道长度，只能自己传，或者用"结束标记"（如字符串的 `'\0'`）。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q55：为什么函数里不能定义函数？**</span>

**答**：C 语言不支持嵌套函数，写了会报 C2601「局部函数定义」。

- 函数一律平铺在文件里，要提前调用就先在文件顶部写原型。
- 想要"逻辑上属于某个函数"的效果，可以用 `static` 把函数限制在本文件可见。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q56：`void` 函数没有返回值，怎么提前跳出？**</span>

**答**：写 `return;`（不带值）。

- `return;` 在 `void` 函数里表示"到此结束，返回调用处"，是合法的提前退出。
- 写成 `return 0;` 会报错：`void` 函数不该带回值。
- 常见场景：参数不合法时提前退出——`if (n <= 0) return;`，避免后面继续执行。

## <span style="color:#6E93B5">2.5 结构体与自定义类型（Q57–Q63）</span> <a id="p2-5"></a>

> 对齐、pack、union、typedef

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q57：结构体的内存为什么比字段加起来大？**</span>

**答**：因为**内存对齐**——每个成员必须放在"自己宽度的整数倍"地址上，编译器会在中间塞填充字节。

- `struct { char c; int i; char d; };` 字段和是 6 字节，实际 `sizeof` 是 **12**（`c` 占 1 + 填 3 + `i` 占 4 + `d` 占 1 + 尾部填 3）。
- 原因：CPU 读未对齐的数据要分两次取再拼接，慢；对齐后一次读完。
- 推论：**把大的成员放前面、小的放后面**，能减少填充。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q58：怎么算对齐后的大小？**</span>

**答**：三步走。

1. 从偏移 0 开始，逐字段放：放得下就放，放不下就**跳到下一个对齐点**（补填充）。
2. 每个字段的起始偏移必须是"该字段大小"的整数倍。
3. 总大小还要补齐到"**最大成员宽度**"的整数倍。

- 例：`{char; char; int;}` = 1 + 1 + 填 2 + 4 = **8**；`{char; int; char;}` = 1 + 填 3 + 4 + 1 + 填 3 = **12**。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q59：`#pragma pack(1)` 是什么？**</span>

**答**：取消填充，强制按 1 字节对齐。

- 前面那个 12 字节的结构体会变成 **6** 字节（字段直接拼）。
- 代价：访问变慢（可能跨缓存行），某些平台甚至不允许未对齐访问。
- 什么时候用：**跨平台传二进制数据、按协议打包**，需要和对方约定的布局完全一致时。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q60：`union` 和 `struct` 区别？**</span>

**答**：`struct` 各成员**各占一份**空间；`union` 所有成员**共用同一块**。

| | `struct` | `union` |
| --- | --- | --- |
| 大小 | 字段和 + 填充 | **最大成员**的大小 |
| 同时有效 | 全部 | 只有最后写的那个 |

- 典型用途：用 `union` 看一个 `int` 的四个字节（判断大小端）、或者做"一个变量多种解释"。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q61：`typedef` 和 `#define` 有什么区别？**</span>

**答**：`typedef` 是**给类型起别名**（编译器认得类型）；`#define` 是**文本替换**（预处理器做完就没了）。

- `typedef unsigned int uint;` → `uint` 是真正的类型名，能参与类型检查。
- `#define uint unsigned int` → 只是把字面文本换掉，遇到 `uint* p` 会变成 `unsigned int* p`（还好），但复杂声明就容易翻车。
- 一句话：**类型别名用 `typedef`，常量/宏用 `#define`**。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q62：`.` 和 `->` 什么时候用哪个？**</span>

**答**：看左边是**结构体变量**还是**结构体指针**。

| 左边 | 用 | 例子 |
| --- | --- | --- |
| 结构体变量（实体） | `.` | `s.name`、`s.score` |
| 结构体指针（地址） | `->` | `p->name`、`p->score` |

- `p->name` 完全等价于 `(*p).name`——先解引用拿到实体，再取成员。
- 记住：**点号用于实体，箭头用于指针**；`p.name`（p 是指针）会报 C2228。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q63：结构体传参，值传递、指针、`const` 怎么选？**</span>

**答**：按"要不要改原件"和"结构体多大"来选。

- **只读 + 结构体小**：值传递 `void f(struct Stu s)`，简单但要整份复制。
- **只读 + 结构体大**：`void f(const struct Stu* s)` —— 传地址省拷贝，`const` 保证不改。
- **要改原件**：`void f(struct Stu* s)`，调用 `f(&s)`，函数里 `s->score = ...`。
- 数组形式也可以：`void f(struct Stu s[], int n)`——本质还是指针。

---

## <span style="color:#6E93B5">2.6 动态内存与内存布局（Q64–Q74）</span> <a id="p2-6"></a>

> static、栈堆、malloc/free、大小端、柔性数组

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q64：`static` 修饰局部变量有什么用？**</span>

**答**：让它**只初始化一次，函数返回后仍然保留值**（住在静态区，不在栈上）。

- 普通局部变量每次进函数都重新创建、初值随机；`static` 局部变量第二次进来还是上次的值。
- 常见用途：统计函数被调用了多少次。
- 注意：它**不是线程安全**的，多线程会共享这一份。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q65：怎么判大小端？**</span>

**答**：取一个多字节整数的首地址，按单字节读出来看。

```c
int i = 1;
char* p = (char*)&i;
printf("%d\n", *p);   /* 打印 1 = 小端；0 = 大端 */
```

- 小端：低字节放在低地址（x86、VS 都是）；大端：高字节放低地址（部分 ARM/网络序）。
- 换一种说法：`union { int i; char c[4]; }` 也能看。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q66：`malloc` 之后为什么必须判断是不是 NULL？**</span>

**答**：申请失败会返回 `NULL`，直接往里写就是往地址 0 写，程序立刻崩。

```c
int* p = (int*)malloc(n * sizeof(int));
if (p == NULL) { perror("malloc"); return 1; }
```

- 失败原因：内存不足、请求过大、地址空间碎片。
- 判空后再用，是"先验货再拆快递"。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q67：`realloc` 为什么要用临时指针接？**</span>

**答**：它可能**搬家**——原块后面空间不够时，会新申请一块、把内容拷过去、再释放老块。

- 失败时返回 `NULL`，但**老块还在**。如果写成 `p = realloc(p, n)`，`p` 被覆盖成 `NULL`，老地址彻底丢了 → 内存泄漏。
- 正确写法：

```c
int* t = (int*)realloc(p, new_n * sizeof(int));
if (t == NULL) { free(p); return 1; }   /* 老块还在，要自己释放 */
p = t;
```

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q68：`free` 之后还要做什么？**</span>

**答**：把指针置空：`free(p); p = NULL;`

- `free` 只是把内存还给堆管理器，**不会改指针的值**——它仍指向那块已经不属于你的内存（悬空指针）。
- 置 `NULL` 后再误用会立刻崩，比"悄悄改坏别人的数据"好排查。
- 也**不要重复 `free`**：同一块释放两次会破坏堆结构。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q69：`malloc` 的参数是字节还是比特？**</span>

**答**：**字节**。要放 `n` 个 `int`，必须写 `n * sizeof(int)`。

- 整个 C 语言里只有**位段**和**移位运算**是按位算的，其他所有"大小"都是字节。
- `malloc(n)` 只给你 `n` 个字节，装 `int` 只能装 `n / 4` 个。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q70：`malloc(0)` 会怎样？**</span>

**答**：行为由实现决定——可能返回 `NULL`，也可能返回一块"不能用的小内存"。

- 总之**别写**：数组要装几格就申请几格。
- 如果 `n` 是运行时算出来的，申请前先判断 `if (n <= 0) return;`。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q71：柔性数组是什么？**</span>

**答**：结构体最后一个成员写成不写长度的数组 `int a[];`，它**不占 `sizeof`**，用的时候一次 `malloc` 把"结构体 + 数据"一起申请。

```c
struct S { int n; int a[]; };
struct S* p = (struct S*)malloc(sizeof(struct S) + 10 * sizeof(int));
p->n = 10;
free(p);          /* 只 free 一次，整块一起释放 */
```

- 好处：内存连续、只申请一次、只释放一次。
- 约束：`a[]` 必须在最后，且结构体里不能再有其他成员跟在它后面。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q72：栈和堆有什么区别？**</span>

**答**：栈由系统**自动**分配回收、很小（一般几 MB）；堆由 `malloc/free` **手动**管理、大得多。

| | 栈 | 堆 |
| --- | --- | --- |
| 谁管 | 编译器自动 | 程序员手动 |
| 大小 | 几 MB，容易溢出 | 受限于物理内存 |
| 速度 | 快 | 相对慢 |

- 大数组放全局或堆上，别放 `main` 的栈里（几十万 `int` 就可能栈溢出）。
- 局部变量出了作用域就失效，堆内存不会——所以必须自己 `free`。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q73：`malloc` 前的 `(int*)` 到底要不要写？**</span>

**答**：C 里**可以不写**，C++ 里**必须写**。

- C 允许 `void*` 隐式转成任何指针类型，所以 `int* p = malloc(...)` 能编过。
- 写成 `(int*)malloc(...)` 更显式，也能让同一份代码在 C++ 编译器下通过——**建议写上**。
- 注意别写成 `int* p = (int*)malloc(n)` 却忘了乘 `sizeof(int)`，那才是真错。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q74：`int* arr`、`arr[]`、`arr = tmp` 三问到底差在哪？**</span>

**答**：三句话概括。

- **`int* arr`** 是一个**变量**，里面装地址，可以改指向（`arr = tmp;` 合法）。
- **`int arr[10]`** 是一排**格子**，数组名是**常量地址**，不能重新赋值（`arr = tmp;` 报 C2106）。
- **`arr = tmp`** 只是"把名片上的号码换成新的"，不搬家；真正的搬家是 `realloc` 内部做的（新申请 → 拷贝 → 释放旧块 → 返回新地址）。

## <span style="color:#6E93B5">2.7 文件与二进制（Q75–Q92）</span> <a id="p2-7"></a>

> 打开模式、读写函数、feof/ftell、文本 vs 二进制

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q75：`fopen` 的模式有哪些？**</span>

**答**：模式决定三件事——**不存在时建不建、旧内容清不清、能不能写**。

| 模式 | 含义 | 文件不存在 | 旧内容 |
| --- | --- | --- | --- |
| `"r"` | 只读 | **失败（NULL）** | 保留 |
| `"w"` | 只写 | 新建 | **清空** |
| `"a"` | 追加 | 新建 | 保留，写永远在末尾 |
| `"r+"` | 读写 | **失败** | 保留 |
| `"w+"` | 读写 | 新建 | **清空** |
| `"a+"` | 读写 | 新建 | 保留，写永远在末尾 |
| 加 `b` | 二进制版 | 同上 | 同上 |

- 记法：`+` 只表示"可读可写"，**不代表能任意位置写**。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q76：`.png` 是什么？为什么要拿它测二进制？**</span>

**答**：PNG 是图片格式（无损压缩、支持透明），内容是**二进制字节**。

- 用它测 `"rb"/"wb"` 能验证：文本模式会改动换行、二进制模式原样搬（复制后 MD5 一致）。
- 反过来，用文本模式复制图片，文件会损坏——这正是"模式必须匹配内容"的直观证据。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q77：`fputs` 会自动换行吗？为什么两行粘在一起？**</span>

**答**：不会。它只认 `'\0'` 当终点，`'\n'` 只是个普通字符，照写不误。

- 要换行就自己补：`fputc('\n', fp);` 或 `fprintf(fp, "%s\n", s);`
- "两行变一行"几乎都是漏了这句。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q78：`fgets` 和 `fputs` 怎么配对？**</span>

**答**：`fgets` 读一整行（**含换行**）→ `fputs` 写整串（**含换行**），正好对上。

- 不想带换行，先用 `strcspn` 剪掉，再 `fputs`，然后自己决定加不加 `\n`。
- 这一对是"按行复制文件"的标准写法。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q79：`feof` 能当循环条件吗？**</span>

**答**：不能。它是"**读失败之后**"才置位的标记。

- `while (!feof(fp))` 会多跑一轮：最后一次读已经失败，但 `feof` 那时还是假，于是又用旧数据打了一遍。
- 正确写法是看读函数的返回值：`while (fgets(line, sizeof(line), fp) != NULL)`。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q80：`fread` 的返回值是什么单位？**</span>

**答**：**块数**，不是字节数。

- `fread(buf, size, count, fp)` 一次搬 `count` 块，返回实际读到的**完整块数**（0 ~ count）。
- 字节数 = `返回值 × size`。
- 所以别把它套进 `for (i < 5)`：一次调用就把 5 份读完了。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q81：`ftell` 能求文件大小吗？**</span>

**答**：能，标准三行：

```c
fseek(fp, 0, SEEK_END);
long size = ftell(fp);
rewind(fp);
```

- **别先 `-1`**：`fseek(fp, -1, SEEK_END)` 后再 `ftell` 得到的是 `size-1`。
- 返回 `long`，打印用 `%ld`；文本模式下它是"书签"，按字节跳请用 `"rb"`。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q82：`"w"` 打开失败等于"清空失败"吗？**</span>

**答**：不是。失败是返回 `NULL`，文件**根本没打开**，谈不上清空。

- 所以"以为清空了其实没动"和"以为没动其实清空了"是两回事，判断依据只有返回值。
- 反过来：只要 `fopen` 成功返回非 `NULL`，`"w"` 就已经把文件清空了——**这一步不可逆**。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q83：为什么程序报 `fopen` 失败，但文件明明在？**</span>

**答**：因为路径是相对**当前工作目录**的，不是你看到文件的那一层。

- VS 调试时默认工作目录是**工程目录**，不是 `.sln` 旁边，也不是 `Debug` 目录。
- 排查：`system("cd")` 或 `_getcwd()` 打印一下当前目录，把文件放过去。
- 另外注意文件名里别混空格/全角字符（`"stu. txt"`）。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q84：`fscanf` 读文件为什么不能用 `for (i < 5)` 硬读 5 次？**</span>

**答**：文件里到底有几条记录，你不知道。

```c
while (fscanf(fp, "%s %d", name, &score) == 2) { /* 读满 2 项才继续 */ }
```

- 硬读 5 次：文件只有 3 条时，后两次会拿到重复的最后一条；文件有 8 条时又只读了 5 条。
- 用返回值控制循环，才能"有多少读多少"。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q85：文本模式和二进制模式能混用吗？**</span>

**答**：可以跨族，但**布局必须匹配**。

- 兼容矩阵：文本写 ↔ 文本读 ✅；二进制写 ↔ 二进制读 ✅；交叉一般 ❌。
- 例如 `fwrite(&n, 4, 1, fp)` 写进去的 4 个字节，用 `fscanf(fp, "%d")` 读不出来——一个是原始字节，一个要十进制文本。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q86：文件到底分文本和二进制吗？主要区别是什么？**</span>

**答**：**存储层都是字节**，"文本/二进制"说的是**打开模式**，不是两种文件。

- 文本模式（`"r"/"w"`）会做换行转换（Windows 下 `\n` ↔ `\r\n`），有时还做编码转换。
- 二进制模式（`"rb"/"wb"`）一个字节都不动，原样读写。
- 所以判断依据看内容：能用记事本读懂 → 文本；图片/结构体/音频 → 二进制。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q87："格式化"和"二进制"到底是什么关系？**</span>

**答**：是"**翻译**"和"**复印**"的区别。

- `fprintf`/`fscanf`：把内存里的值翻译成十进制文本（或反过来），**人能读**，但要多一步转换。
- `fwrite`/`fread`：把内存里的字节原样复印到文件，**人看不懂**，但快、体积小、无精度损失。
- 两者不是"文件类型"的区别，而是"要不要翻译"的区别。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q88：编码 ≠ 格式化，`fputc` 为什么不算格式化？**</span>

**答**：把"字符变成字节"叫**编码**，把"数值变成十进制文本"才叫**格式化**。

- `fputc('A', fp)` 写的是 `'A'` 这个字符本身（编码后的 1 个字节 65），没有"翻译数字"的过程。
- `fprintf(fp, "%d", 65)` 会把 `65` 翻译成字符 `'6'` 和 `'5'` 两个字节写出去。
- 所以 `fputc` 是字符 I/O，`fprintf` 才是格式化 I/O。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q89：`fscanf` 读到的东西去哪了？**</span>

**答**：和 `scanf` 完全一样——**按你给的地址写进变量**。

- `fscanf(fp, "%d", &n)` 把读到的整数写进 `n`；
- 返回值是**成功匹配的项数**，不是数据本身；
- `name` 是数组不用 `&`，`score` 是 `int` 必须 `&`。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q90：为什么"打开不存在的文件"不会自动新建？**</span>

**答**：只有 `"w"`、`"a"`、`"w+"`、`"a+"` 这四种模式会新建文件。

- `"r"` 和 `"r+"` 的语义是"**打开已存在的文件来读**"，文件不存在就返回 `NULL`。
- 这就是"读文件前必须先确保它有"的原因；想边读边建，用 `"w+"`（但会清空）或 `"a+"`（不清空、写在末尾）。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q91：`r+` / `w+` / `a+` 都是读写，区别在哪？**</span>

**答**：问三件事——不存在建不建、旧内容清不清、写能不能到中间。

| 模式 | 不存在时 | 旧内容 | 写的位置 |
| --- | --- | --- | --- |
| `"r+"` | **失败** | 保留 | 任意（配合 `fseek`） |
| `"w+"` | 新建 | **清空** | 任意 |
| `"a+"` | 新建 | 保留 | **永远末尾** |

- `+` 只表示"可读可写"，**不代表能任意位置写**；`"a+"` 的写永远追加。
- 更新流里"读↔写"切换前要 `fflush` 或 `fseek`，最省心是关掉重开。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q92：`fseek` / `ftell` / `rewind` 只能二进制用吗？**</span>

**答**：不是，文本模式也能用，只是**受限**。

- `rewind(fp)` **永远安全**：等价于"回到开头 + 清标志"。
- `fseek` 在文本模式下，`offset` 只能是 **0** 或 **`ftell` 的返回值**，基点用 `SEEK_SET`——因为文本模式的 `ftell` 返回的是"书签"，不是纯字节偏移。
- 要按字节随便跳、要求文件大小，请用 `"rb"` 打开。

---

## <span style="color:#6E93B5">2.8 运算符与表达式（Q93–Q96）</span> <a id="p2-8"></a>

> sizeof、自增自减、三目

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q93：`sizeof` 是函数吗？**</span>

**答**：不是，是**运算符**——编译期就求值，括号里的表达式**不会被执行**。

- 所以 `sizeof(int)` 的括号是可选的，写成 `sizeof int` 也合法（但不推荐）。
- 因为编译期算，`sizeof(arr)` 在函数里只剩指针大小——数组已经退化了。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q94：`i++` 和 `++i` 有什么区别？**</span>

**答**：`i++` 交出**旧值**再 +1；`++i` 先 +1 再交出**新值**。

```c
int i = 1, a, b;
a = i++;   /* a = 1, i = 2 */
b = ++i;   /* i = 3, b = 3 */
```

- 单独成句时两者没区别，只有在表达式里才分新旧。
- **同一表达式里对同一变量又读又改两次是未定义行为**（`i = i++`），别写。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q95：`a < b ? a : b` 怎么读？**</span>

**答**：三目运算符：条件为真取冒号**左边**，为假取**右边**。

- 等价于 `if (a < b) min = a; else min = b;`，但能直接当值用。
- 两个分支的类型会自动统一（`int` 和 `double` 混用会提升成 `double`）。
- 别嵌套太多层，可读性会崩。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q96：`%zu` 和它的一家人（`%d` / `%u` / `%ld` / `%lld`）怎么配？**</span>

**答**：格式符要和**变量类型**严格对应。

| 类型 | 格式符 | 典型来源 |
| --- | --- | --- |
| `int` | `%d` | 普通整数 |
| `unsigned` | `%u` | 无符号 |
| `long` | `%ld` | `ftell` 返回值 |
| `long long` | `%lld` | 大整数 |
| `size_t` | **`%zu`** | `strlen`、`fread/fwrite` 返回值 |

- `sizeof`、`strlen`、`fread` 都返回 `size_t`，用 `%d` 会报警告（C4477），64 位下还可能打印错。
- 记法：**`z` 前缀 = size_t**。

---

## <span style="color:#6E93B5">2.9 控制流程与跳转（Q97–Q103）</span> <a id="p2-9"></a>

> return/break、for、flag、switch、goto、空串

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q97：`return` 和 `break` 有什么区别？**</span>

**答**：作用范围完全不同。

- `break` 只跳出**当前这一层**循环或 `switch`，后面的代码继续执行。
- `return` 直接**结束整个函数**（在 `main` 里就是结束程序），后面的语句全不执行。
- 想跳出多层循环：用 `return`、用 `goto`、或者用 flag 配合。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q98：为什么遍历默认用 `for`？**</span>

**答**：三段（初始化 / 条件 / 步进）都写在头上，**步进不容易漏**，作用域也更小。

- `while` 的步进写在循环体里，一旦 `continue` 就容易被跳过 → 死循环。
- `do-while` 的主场是"至少执行一次"：读输入、重试、菜单。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q99：要不要经常考虑"空串"？**</span>

**答**：看循环体**会不会改动内容**——会改就必须考虑。

- 空串时第 0 格就是 `'\0'`，如果代码往 `s[0]` 写东西，就会把结束符改掉，后面的函数全乱。
- 例：反转空串、删除首字符、`strcat` 到空串，都要先判 `len == 0`。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q100：怎么知道循环是"正常结束"还是"被 break 打断"？**</span>

**答**：两种办法。

- **flag 开关**：命中时 `found = 1; break;`，循环后判断 `if (found)`。
- **看下标**：循环结束后 `i` 是否等于 `n`——等于说明跑完了，小于说明中途 `break` 了。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q101：`break` 和 `continue` 的区别？**</span>

**答**：`break` 跳出整个循环；`continue` 只结束**本轮**，直接进入下一轮。

- 危险点：`continue` 会跳过它后面的语句，**步进语句千万别写在它后面**，否则死循环。
- `for` 的步进写在头部，所以 `continue` 相对安全；`while` 要特别小心。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q102：`switch` 里忘了 `break` 会怎样？**</span>

**答**：会**穿透**（fall through）到下一个 `case` 继续执行，直到遇到 `break` 或结束。

- 每个 `case` 后面都要 `break`（除非故意合并多个条件）。
- `case` 后面只能是**常量**，不能写变量或范围；末尾加 `default` 兜底。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q103：`goto` 还能用吗？**</span>

**答**：能用，但只推荐一种场合：**从多层嵌套循环一次性跳出**。

- 其他情况一律用 `break` / `return` / 函数拆分。
- 滥用 `goto` 会让控制流变成"面条"，调试困难。

---

## <span style="color:#6E93B5">2.10 预处理与宏（Q104–Q105）</span> <a id="p2-10"></a>

> 函数宏、do-while(0)

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q104：`#define SQUARE(x) x*x` 有什么问题？**</span>

**答**：`SQUARE(1+1)` 会展开成 `1+1*1+1` = **3**，不是 4。

- 宏是**纯文本替换**，不认优先级。
- 正确写法：每个参数和整体都加括号 → `#define SQUARE(x) ((x)*(x))`
- 更稳的做法是用 `static inline` 函数，有类型检查。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q105：多语句宏为什么必须 `do { ... } while (0)`？**</span>

**答**：宏是文本替换，普通的 `{ }` 会在 `if/else` 里"断句"。

```c
#define INIT() { a = 1; b = 2; }
if (x) INIT(); else ...;      /* 展开后 else 找不到 if → 编译错误 */
```

- 用 `do { ... } while (0)` 包起来，它是一个**完整语句**，末尾分号正好收尾，无论放在哪里都安全。

---

## <span style="color:#6E93B5">2.11 类型与标准库工具（Q106–Q111）</span> <a id="p2-11"></a>

> 随机数、char 符号、字符 vs 字符串、VLA

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q106：随机数的正确写法？**</span>

**答**：三件套，`srand` 只在 `main` 开头调一次。

```c
srand((unsigned)time(NULL));
int x = rand() % 100;              /* 0 ~ 99 */
int y = 10 + rand() % 91;          /* 10 ~ 100 */
```

- `rand()` 返回 0 ~ `RAND_MAX`（至少 32767）。
- 要区间 `[a, b]`：`a + rand() % (b - a + 1)`。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q107：为什么 `srand` 调两次会让两个随机数一样？**</span>

**答**：同一秒内 `time(NULL)` 返回相同的秒数 → 种子相同 → 伪随机序列相同 → 两次 `rand()` 的第一个值一样。

- 所以播种**只做一次**，放在程序开头。
- 这也解释了"两次运行结果完全相同"的现象。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q108：`char` 是有符号还是无符号？**</span>

**答**：**不定**，由实现决定；VS 下是有符号的 `signed char`。

- 所以 `char c = 200;` 会溢出成 **-56**。
- 要存 0 ~ 255 就明确写 `unsigned char`；要做字节运算也建议用它。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q109：`'A'` 和 `"A"` 有什么区别？**</span>

**答**：一个是**字符常量**，一个是**字符串**。

| 写法 | 类型 | 大小 | 内容 |
| --- | --- | --- | --- |
| `'A'` | `int`（字符常量） | 1 字节（存 char 时） | 65 |
| `"A"` | `char[2]` | **2 字节** | `'A'` + `'\0'` |

- `sizeof("A")` 是 2，`sizeof('A')` 在 C 里是 4（`int` 大小）——这个差异常考。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q110：`const int n = 100; int a[n];` 为什么不行？**</span>

**答**：C 里 `const` 是"**只读变量**"，不是**常量表达式**。

- `a[n]` 会变成**变长数组（VLA）**：C99 支持但部分编译器/平台不支持，且不能初始化。
- 要真正的常量，用 `#define N 100` 或 `enum { N = 100 };`。
- C++ 里 `const int` 可以当常量（编译期值），所以这条是 C 和 C++ 的差异点。

<span style="display:block;font-size:17.5px;color:#6E93B5;font-weight:700;border-left:3px solid #6E93B5;padding-left:10px;margin-top:26px">**Q111：`assert` 是什么？什么时候用？**</span>

**答**：开发期的"自检哨兵"：断言为假时，立刻打印文件名、行号并终止程序。

```c
#include <assert.h>
assert(p != NULL);          /* p 为空就立刻停在这行 */
```

- 用途：抓"本不该发生"的内部错误（空指针、数组越界前提不成立）。
- 正式发布时用 `#define NDEBUG` 可以把所有 `assert` 变成空语句，不占性能。
- 它**不适合**处理用户输入错误——那应该用 `if` 提示，而不是让程序崩掉。

---

# <span style="color:#7FA182">第三部分　函数速查</span> <a id="sec52"></a>

> **每个家族怎么读**：先看**速查表**（函数 + 原型 + 掌握度）定位，再到下面「**逐个说明**」看这个函数的**完整使用流程**（带编号注释的代码，一步一行）和**注意事项**。
>
> **代码颜色**：全文代码块都标了语言（C 代码标 `c`、示意图标 `text`）。用 **VS Code / Trae 的 Markdown 预览**（`Ctrl+Shift+V`）、Typora 或 GitHub 打开时，会自动按 C 语法上色——**关键字蓝、注释绿、字符串棕**，和 VS 基本一致；直接在编辑器里看源码则不保证上色。
>
> **找不到某个函数**：`Ctrl+F` 搜函数名，或用 `Ctrl+Shift+O` 打开大纲，每个函数都是独立标题。
>
> **怎么读一行原型**：`返回类型 函数名(参数类型1, 参数类型2, …);`
> - **左边看返回类型**：`int` 是个数、`size_t` 是无符号长度、`char*` 是字符串指针、`void` 不返回、`void*` 是"万能指针"；
> - **中间看函数名**：调用时就写它；
> - **右边看参数**：每个参数的类型就是**你该递进去的东西**；
> - **`const` 是承诺**：`const char*` = "我只读、不改"，`char*` = "我要写，你得给可写、够大的内存"。

**参数单位速记（最容易搞混的一张表）**：C 里这些 `n` **从来不是"比特（bit）"**，只有位段和移位才按位算。

| 函数 | 那个数字是什么 | 记法 |
| --- | --- | --- |
| `malloc(n)` | **字节数** | 要 n 个 int 必须写 `n * sizeof(int)` |
| `calloc(n, size)` | `n` 是**元素个数**，`size` 是**每个元素字节数** | 两个数相乘才是字节 |
| `realloc(p, n)` | **调整后的总字节数**（不是增量） | 也别忘乘 `sizeof` |
| [`fread`](#fn-fread) / `fwrite(buf, size, count, fp)` | `size` **每块字节数**，`count` **块数** | 总字节 = size × count |
| `fgets(s, n, fp)` | **缓冲区字节数**（含结束符位置） | 最多读 `n-1` 个字符 |
| `snprintf(buf, n, ...)` | **缓冲区字节数**（含结束符） | 最多写 `n-1` 个字符 |
| [`memcpy`](#fn-memcpy) / [`memmove`](#fn-memmove) / [`memset`](#fn-memset) / `memcmp(..., n)` | **字节数** | 元素个数要乘 `sizeof` |
| [`strncpy`](#fn-strncpy) / [`strncat`](#fn-strncat) / `strncmp(..., n)` | **字符个数** | 单位是 char，1 个就是 1 字节 |
| [`qsort`](#fn-qsort) / `bsearch(base, n, size, cmp)` | `n` **元素个数**，`size` **每个元素字节数** | 两个都要给 |
| `fseek(fp, offset, origin)` | `offset` 是**字节偏移** | 不是第几个元素 |

> **核心心法**：函数不是背单词，是"认亲戚"。
> **第一轮（2026-10 之前）**只要求"熟 4 个家族里最常用的十几个"；**现在（T1–T66 之后）**按**真实使用频次**分三档：✅ 闭眼写、⚪ 查一眼、⬜ 先别学。**清单会随刷题自动升级**——某列里用够 3 次就往上挪一格。

## <span style="color:#7FA182">先背这些（高频必会）</span> <a id="sec53"></a>

> **掌握度标记**：✅ 亲手写通 ≥3 次（闭眼能写）｜⚪ 写过 / 讲过 1–2 次（查一眼就能用）｜⬜ 还没用过
> **依据**：截至 2026-11-04，按《每日刷题日志》T1–T66 的真实出现次数统计。

| 现在就该闭眼会写（✅） | 会用、细节要查（⚪） | 待解锁（⬜） |
| --- | --- | --- |
| `printf`（129 次）、`scanf`（84 次） | `fgets`、`fprintf`、`fscanf`、`fgetc`、`fputc` | `fputs`、`rewind`、`sscanf` |
| `getchar`、`putchar` | `strncpy`、`strncat`、`strncmp`（T63–T66 刚练） | `strerror` + `errno` |
| `strlen`（33）、`strcmp`（33） | `strstr`、`strtok`（T65 分词） | `strcoll`、`strxfrm` |
| `strcpy`、`strcat` | `memcpy`、`memmove`、`memcmp` | `memset`（只听过） |
| `rand`（43）、`srand`（22）、`time` | `malloc`、`realloc`、`free`（T46 版通讯录） | `calloc`、`qsort` 的写法 |
| `sqrt`（T44 判素数） | `pow`、`fabs`、`ceil`、`floor` | `fmod`、`round` |
| `abs`（整数绝对值） | `atoi`、`exit`、`system` | `atof`、`strtol`、`bsearch` |
| `time`（time.h，随机种子） | `clock`（计时） | `difftime`、`strftime` |
| `isdigit`、`isalpha`（ctype.h） | `toupper`、`tolower`、`isspace` | `isalnum`、`ispunct`、`isxdigit` |

- <span style="color:#5F7F63;font-weight:700">一句话</span>：✅ 那一列是你现在就该"闭眼写对"的 20 个；⚪ 那一列允许查；**⬜ 先别学**，等题里真用到再补。
- **判断标准**：合上书 3 分钟能默写出签名 + 一句话作用 + 一个例子 = 真会；写不出 = 还在 ⚪ 那一列。

## <span style="color:#7FA182">1. stdio.h —— 输入输出家族</span> <a id="sec54"></a>

| 函数 | 原型（返回类型 + 参数类型） | 掌握 |
| --- | --- | --- |
| [`printf`](#fn-printf) | `int printf(const char*, ...);` | ✅ |
| [`scanf`](#fn-scanf) | `int scanf(const char*, ...);` | ✅ |
| [`getchar`](#fn-getchar) | `int getchar(void);` | ✅ |
| [`putchar`](#fn-putchar) | `int putchar(int c);` | ✅ |
| [`puts`](#fn-puts) | `int puts(const char* s);` | ⚪ |
| [`fgets`](#fn-fgets) | `char* fgets(char* s, int n, FILE* fp);` | ⚪ |
| [`fputs`](#fn-fputs) | `int fputs(const char* s, FILE* fp);` | ⬜ |
| [`gets`](#fn-gets) | `char* gets(char* s);` | ❌ |
| [`sprintf`](#fn-sprintf) | `int sprintf(char* buf, const char*, ...);` | ⚪ |
| [`snprintf`](#fn-snprintf) | `int snprintf(char* buf, size_t n, const char*, ...);` | ⬜ |
| [`sscanf`](#fn-sscanf) | `int sscanf(const char* s, const char*, ...);` | ⬜ |
| [`fprintf`](#fn-fprintf) | `int fprintf(FILE* fp, const char*, ...);` | ⚪ |
| [`fscanf`](#fn-fscanf) | `int fscanf(FILE* fp, const char*, ...);` | ⚪ |
| [`fgetc`](#fn-fgetc) | `int fgetc(FILE* fp);` | ⚪ |
| [`fputc`](#fn-fputc) | `int fputc(int c, FILE* fp);` | ⚪ |
| [`fread`](#fn-fread) | `size_t fread(void* buf, size_t size, size_t n, FILE* fp);` | ⚪ |
| [`fwrite`](#fn-fwrite) | `size_t fwrite(const void* buf, size_t size, size_t n, FILE* fp);` | ⚪ |
| [`fopen`](#fn-fopen) | `FILE* fopen(const char* path, const char* mode);` | ⚪ |
| [`fclose`](#fn-fclose) | `int fclose(FILE* fp);` | ⚪ |
| [`fseek`](#fn-fseek) | `int fseek(FILE* fp, long offset, int origin);` | ⬜ |
| [`ftell`](#fn-ftell) | `long ftell(FILE* fp);` | ⬜ |
| [`rewind`](#fn-rewind) | `void rewind(FILE* fp);` | ⬜ |
| [`feof`](#fn-feof) | `int feof(FILE* fp);` | ⚪ |
| [`ferror`](#fn-ferror) | `int ferror(FILE* fp);` | ⚪ |
| [`perror`](#fn-perror) | `void perror(const char* s);` | ⚪ |
| [`remove`](#fn-remove) | `int remove(const char* path);` | ⬜ |
| [`rename`](#fn-rename) | `int rename(const char* oldname, const char* newname);` | ⬜ |
| [`fflush`](#fn-fflush) | `int fflush(FILE* fp);` | ⬜ |

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`printf` —— 按格式输出</span> <a id="fn-printf"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：把各个变量的值按格式串拼成一段文字，送到标准输出（屏幕）。

<span style="color:#5F7F63;font-weight:700">原型</span>：`int printf(const char* format, ...);`（`#include <stdio.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`int` 是**返回类型** → 成功返回写出的字符数，失败返回负数｜`printf` 是**函数名**｜`const char* format` 是**参数** → 格式串，`const` 表示只读、函数不会改它｜`...` 是**变参** → 按格式串里 `%` 出现的顺序逐个填值，类型必须与 `%` 对应

| 项目 | 说明 |
| --- | --- |
| 参数 | `format` 格式串；`...` 按 `%` 出现顺序逐个填的值 |
| 返回 | 成功：写出的**字符数**（`int`）；出错：负数 |
| 失败场景 | 磁盘满、输出流被关闭，日常几乎不检查 |
| 何时上屏 | 先进缓冲区，遇 `\n` / 缓冲满 / 程序正常结束才真正写出 |

<span style="color:#5F7F63;font-weight:700">原理</span>：它把格式串当作一张**指令单**逐字符扫描：普通字符原样进缓冲，遇到 `%` 就接着读格式说明（宽度、精度、`d/f/s` 等），据此决定「从参数里取几个字节、怎么转成文字」。变参是靠调用约定传的，参数依次放进寄存器/栈，`printf` 只按格式串顺序去取，它**无法验证类型**，所以 `%d` 打 `double` 会读出乱码。拼好的字符先写进 `stdout` 的缓冲区（`FILE` 结构里的数组 + 两个指针），并不立刻调系统调用；只有缓冲区满、遇到 `\n`（行缓冲）、`fflush` 或正常退出时，才真正 `write` 到屏幕。返回值是这一路**累计写出的字符数**，出错返回负数。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
int n = 42;
double area = 3.14159 * 2 * 2;
printf("n = %d，面积 = %.2f\n", n, area);   /* ① 格式串 ② 按序填值 ③ 末尾 \n */
printf("进度 100%%\n");                     /* ④ 想输出 % 就写 %% */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **格式符和参数类型必须对齐**：`int` 用 `%d`、`double` 用 `%f`、字符串用 `%s`；`%d` 打 `double` 会读出乱码。
- **`%f` 默认 6 位小数**，要两位得写 `%.2f`。
- **忘写 `\n`**：输出留在缓冲区，崩溃时全丢；多次输出还会粘成一行。
- **`printf` 里 `%f` 通吃 `float`/`double`**（float 会自动提升为 double），但 `scanf` 不是这样——那边 double 必须 `%lf`。
- **`%` 本身要写 `%%`**，单个 `%` 后面跟字母会被当成格式符，轻则乱码重则崩溃。
- **格式串忘加双引号**：`printf("%d\n", n)` 写成 `printf(%d\n, n)` 直接编译不过。
- **全角符号混进格式串**（中文引号、全角冒号）→ 运行时 Debug Assertion Failed。
- **返回值是"打印了多少个字符"**，可以接住算宽度，但日常不用管。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **输出到底去了哪？** 先进 stdout 缓冲区，遇 `\n`、缓冲满或程序正常退出才真正写出；中途崩溃，缓冲区里的字一起消失——这就是"有时看不到输出"的机制。
- **返回值有什么用？** 本次写出的字符数：`printf("%d", printf("ab"))` 会先打 `ab` 再打 `2`（T23 链式访问）。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：`printf` = print + formatted，**"印"**；`f` 在名字里表示 formatted，不是 file。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`scanf` —— 按格式读入</span> <a id="fn-scanf"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：从标准输入（键盘）按格式串取值，按地址写进变量。

<span style="color:#5F7F63;font-weight:700">原型</span>：`int scanf(const char* format, ...);`（`#include <stdio.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`int` → 返回**成功读入的项数**（0 = 一项没读到，EOF = 输入结束）｜`scanf` 函数名｜`const char* format` → 格式串（只读）｜`...` → **变量的地址**（普通变量 `&x`，数组名直接写）

| 项目 | 说明 |
| --- | --- |
| 参数 | `format` 格式串；后面是**变量的地址**（普通变量 `&x`，数组名不用 `&`） |
| 返回 | **成功读入的项数**；一个都没读到时返回 `0`；遇到输入结束返回 `EOF`（-1） |
| 失败场景 | 格式不匹配（输入字母给了 `%d`）会提前返回，剩下的字符留在缓冲区 |

<span style="color:#5F7F63;font-weight:700">原理</span>：它是 `printf` 的逆过程：按格式串逐项匹配，从 `stdin` 的**输入缓冲区**取字符（缓冲空了才触发一次 `read`）。多数字符 `%d`/`%f`/`%s` 会**先跳过空白**再取值，取到不该出现的字符就停下，并把这个字符**退回缓冲区**留给下次；转换完的值按你给的**地址**写进内存——这也是普通变量必须 `&`、数组名不用的原因。每成功匹配一项计数加一，所以返回值是「项数」而不是 0/1；一个都没匹配上返回 0，输入直接结束返回 `EOF`。它只拿到地址、拿不到长度，因此对数组溢出完全无能为力。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
int n; double x; char name[20];
scanf("%d", &n);                 /* ① 普通变量必须 & */
scanf("%lf", &x);                /* ② double 必须 %lf */
scanf("%19s", name);             /* ③ 数组名不写 &，且要限长 */
printf("%d %f %s\n", n, x, name);

if (scanf("%d", &n) != 1) {      /* ④ 判断项数，别直接 if(scanf(...)) */
    printf("输入有误\n");
}
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **漏 `&`**：变量初值为 0 时等于传了空指针 → `Debug Assertion Failed`；初值是垃圾值时 → C4477 + C4700 一串报错。
- **`double` 写 `%f`**：`scanf` 靠格式串决定写几字节，`%f` 只写 4 字节，double 高位变垃圾（天文数字或负数）。
- **数组名再加 `&`**：`&name` 类型变成 `char(*)[20]`，数值一样但类型不对（C4047）。
- **返回值不是 0/1**，是**读到的项数**：两项要写 `!= 2`，不能写 `if (scanf(...))`。
- **缓冲区残留**：`scanf` 不读走换行，后面接 `%c` / `fgets` 会读到这个换行；解法是 `scanf(" %c", &c)`（前导空格）或提前清空。
- **`%s` 遇空格就停**，读不了"带空格的一整行"，那种要用 `fgets`。
- **不要用 `scanf_s`**：微软私有，要额外传缓冲区大小，比赛平台不认，会报 0x00000005。
- **格式串末尾别加空格**：`"%d "` 会要求你再多输入一个非空白字符才返回。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **为什么它不知道数组多大？** 数组名传参会退化成首元素地址，长度信息丢了，`scanf` 无从检查；`scanf_s` 正是为补这个才强制多传一个大小。
- **什么时候必须清缓冲区？** 只有后面接 `%c` / `%[` / `fgets` / `getchar` 时才要；接 `%d`/`%s` 会自动跳空白，不必清。
- **C6031 要不要管？** 它不是语法错误，是静态分析提醒你"丢掉了唯一的成功线索"，改成判断项数即可。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：`scanf` = scan + formatted，**"扫"**；扫的是地址，所以 `&` 不能少。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`getchar` —— 读一个字符</span> <a id="fn-getchar"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：从标准输入取**一个**字符，什么都吃（空格、回车都算）。

<span style="color:#5F7F63;font-weight:700">原型</span>：`int getchar(void);`（`#include <stdio.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`int` → 返回读到的字符（0~255）；`EOF`(-1) 表示结束或出错｜`getchar` 函数名｜`void` → **没有参数**，括号里写 `void` 表示"明确不接收任何东西"

| 项目 | 说明 |
| --- | --- |
| 参数 | 无 |
| 返回 | 成功：字符的 ASCII 码（`int`）；输入结束或出错：`EOF`（-1） |
| 失败场景 | 读到文件尾、键盘 Ctrl+Z 时返回 `EOF` |

<span style="color:#5F7F63;font-weight:700">原理</span>：它就是 `fgetc(stdin)`：从标准输入的缓冲里**取走一个字节**，缓冲区空了就触发一次系统 `read` 把数据灌进来。返回时把字节**提升成 `int`**（0~255），这样 `EOF`（-1）才能和「真正读到 0xFF」区分开——这正是必须用 `int` 接的原因。它不做任何空白跳过，来什么给什么。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
int ch;                                  /* ① 必须 int，不是 char */
while ((ch = getchar()) != '\n' && ch != EOF) {
    /* 逐字符处理：数空格、转大写、存进数组 */
}
getchar();                               /* ② 只吃掉一个残留换行 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **用 `char` 接**：`char` 装不下 -1，`EOF` 判断永远不成立，循环停不下来。
- **以为它能跳过空白**：它不跳，空格和回车照吃——这是优点，也是"多读一个回车"的来源。
- **循环里调两次**：`while (getchar() != '\n') { ch = getchar(); }` 会跳过一半字符。
- **和 `scanf` 混用**：`scanf` 留下的换行会被它当第一个字符吃掉，表现为"程序直接跳过输入"。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **为什么它能数空格？** `%s` 把空格当分隔符跳过，`getchar` 来什么吃什么，空格和回车都算字符。
- **它和 `fgets` 怎么选？** 要逐字符分析（数空格、转大小写）用 `getchar`；要整行比较、截取用 `fgets`。
- **为什么接口返回 `int`？** 因为要能表示 `EOF`（-1），这是它和 `char` 最本质的区别。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：`getchar` = get one **char**，**来什么吃什么**，所以能数空格。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`putchar` —— 输出一个字符</span> <a id="fn-putchar"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：把一个字符写到屏幕。

<span style="color:#5F7F63;font-weight:700">原型</span>：`int putchar(int c);`（`#include <stdio.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`int` → 返回写出的那个字符；`EOF` 表示失败｜`putchar` 函数名｜`int c` → 要输出的字符（传 `char` 会自动提升成 `int`，实际只取低 8 位）

| 项目 | 说明 |
| --- | --- |
| 参数 | `c` 要输出的字符（传 `char` 会被提升成 `int`） |
| 返回 | 成功：写出的那个字符；失败：`EOF` |
| 失败场景 | 输出流出错时返回 `EOF` |

<span style="color:#5F7F63;font-weight:700">原理</span>：等价于 `fputc(c, stdout)`：把 `c` 的低 8 位当作**一个字节**写进输出缓冲区，缓冲区满或遇到换行才真正落盘。它不理解字符集、不做编码转换，只负责「放一个字节出去」。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
putchar('A');
putchar('\n');                   /* 打一个换行，比 printf("\n") 短 */
for (i = 0; s[i]; i++) putchar(s[i]);   /* 逐字符输出 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **传字符串**：`putchar("A")` 传的是地址，会输出乱码/崩溃，单个字符要用单引号。
- **它不加换行**：要换行得自己再 `putchar('\n')`。
- **参数是 int**：传超出 0~255 的值只保留低 8 位。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **它和 `printf("%c", c)` 有区别吗？** 等价，`putchar` 更短更快，但不能格式化。
- **为什么参数是 `int`？** 和 `getchar` 对称，接口统一用 `int`，实际只取低 8 位写成 1 字节。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：`put` + `char`，**"放一个字符出去"**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`puts` —— 输出一行</span> <a id="fn-puts"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：输出一个字符串，**自动补一个换行**。

<span style="color:#5F7F63;font-weight:700">原型</span>：`int puts(const char* s);`（`#include <stdio.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`int` → 成功返回非负数，失败返回 `EOF`｜`puts` 函数名｜`const char* s` → 要输出的字符串（只读），函数写完后**自动补一个换行**

| 项目 | 说明 |
| --- | --- |
| 参数 | `s` 要输出的字符串（以 `'\0'` 结尾） |
| 返回 | 成功：非负数；失败：`EOF` |
| 失败场景 | 输出流出错 |

<span style="color:#5F7F63;font-weight:700">原理</span>：先 `fputs(s, stdout)` 把字符串逐字符写到 `'\0'` 为止，**再额外写一个 `'\n'`**——所以它是「输出 + 换行」的组合动作。正因为多写了这一下，返回值只表示「非负 / 失败」，不表示写了几个字符。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
puts("hello world");             /* 输出 hello world 并换行 */
puts("");                        /* 只输出一个空行 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **它会自动换行**，想控制空行就少打一个 `\n`，别再手写。
- **不能格式化**：没有 `%d`，要拼值请用 `printf`。
- **参数必须以 `'\0'` 结尾**，传没结束符的数组会越界读。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **它和 `fputs` 有什么区别？** `puts` 固定写 `stdout` 且**自动补换行**；`fputs` 能指定任意流且**不补换行**。
- **它和 `printf` 怎么分工？** 只输出一整串并要换行用 `puts`；要拼变量、控制格式就用 `printf`。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：`puts` = put **s**tring，**"放一整串 + 自带回车"**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`fgets` —— 安全读一整行</span> <a id="fn-fgets"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：从流里最多读 `n-1` 个字符，遇到换行就停，**换行会读进来**。

<span style="color:#5F7F63;font-weight:700">原型</span>：`char* fgets(char* s, int n, FILE* fp);`（`#include <stdio.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`char*` → 成功返回 **`s` 本身**（方便链式使用），读到末尾/出错返回 `NULL`｜`char* s` → 存放结果的缓冲区（**可写**、够大）｜`int n` → 缓冲区**总字节数**（最多读 `n-1` 个字符）｜`FILE* fp` → 数据来源流（键盘写 `stdin`）

| 项目 | 说明 |
| --- | --- |
| 参数 | `s` 缓冲区；`n` 缓冲区**总字节数**；`fp` 流（键盘用 `stdin`，文件用 `fopen` 返回值） |
| 返回 | 成功：`s` 本身；读到末尾或出错：`NULL` |
| 失败场景 | 一开头就遇 EOF、流出错 → 返回 `NULL`（不会返回空串） |

<span style="color:#5F7F63;font-weight:700">原理</span>：内部是循环 `fgetc`：每读一个字符就检查三件事——是不是 `'\n'`（是就把它也存进去并停止）、是不是已经存了 `n-1` 个（满了就停止）、是不是遇到 `EOF`（停止）。三种情况都会在末尾补上 `'\0'` 收尾，然后返回 `s`。**一个字符都没读到**（一上来就 EOF）时才是 `NULL`，所以空行返回的是 `"\n\0"` 这个合法字符串，而不是 `NULL`。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
char line[100];
while (fgets(line, sizeof(line), stdin) != NULL) {   /* ① 失败返回 NULL */
    line[strcspn(line, "\n")] = '\0';                /* ② 剪掉尾巴的换行 */
    printf("[%s]\n", line);
}
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **上限是 `n-1` 不是 `n`**：`n` 格里有 1 格必须留给 `'\0'`；回车也占这 `n-1` 的名额。
- **会带 `'\n'`**：不剪的话长度多 1，`strcmp` 比较会失败。标准剪法是 `strcspn`。
- **第三参数不能传文件名**，要传 `FILE*`（键盘就是 `stdin`）；也不能写 `&stdin`。
- **输入超长会截断**：一行超过 `n-1` 时，剩下的字符留在缓冲区，下一次 `fgets` 接着读。
- **返回 `NULL` 不等于空行**：空行返回的是一个只含 `"\n"` 的有效字符串。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **读一整行到底有几种办法？** 五种：`%s`（读不了空格）、`%[^\n]`（能读整行但不限长）、**`fgets`（主力）**、`getchar` 循环（手搓）、`gets`（C11 已删除）。
- **它和 `getchar` 怎么选？** 看"要不要留下整行"：逐字符分析用 `getchar`，整行比较/截取用 `fgets`。
- **它为什么和 `fputs` 天生一对？** `fgets` 把 `'\n'` 一起存进数组，`fputs` 又只认 `'\0'` 原样写出，一读一写正好保持原格式。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：`f` + `gets`，**"从 file 拿一串，自带回车，自己剪"**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`fputs` —— 输出一行到流</span> <a id="fn-fputs"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：把一个字符串原样写进流，**不加换行**。

<span style="color:#5F7F63;font-weight:700">原型</span>：`int fputs(const char* s, FILE* fp);`（`#include <stdio.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`int` → 成功非负，失败 `EOF`｜`fputs` 函数名｜`const char* s` → 要写的字符串（只读，写到 `'\0'` 停）｜`FILE* fp` → 目标流（屏幕写 `stdout`）

| 项目 | 说明 |
| --- | --- |
| 参数 | `s` 要写的串；`fp` 目标流（屏幕用 `stdout`） |
| 返回 | 成功：非负数；失败：`EOF` |
| 失败场景 | 流不可写、磁盘满 |

<span style="color:#5F7F63;font-weight:700">原理</span>：从 `s` 开始逐字符往流里写，**只把 `'\0'` 当终止符**，`'\n'` 和其他字符一样照写。它不跟踪行边界、不补换行，所以「按行」这件事完全由调用者决定。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
fputs("hello", stdout);          /* 只写 hello，不换行 */
fputs("hello\n", stdout);        /* 要换行就自己写进去 */

FILE* fp = fopen("log.txt", "a");
fputs("一行日志\n", fp);         /* ① 内容带 \n，写文件才分得开 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **不会自动换行**：连续两次 `fputs` 会粘成一行，这是"两行变一行"的最常见原因。
- **和 `fgets` 配对最顺**：`fgets` 读进来的 `'\n'` 原样写回，正好保持原格式。
- **`stdout` 也是 `FILE*`**：屏幕和文件用同一个函数，只是流的参数不同。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **写文件时换行由谁负责？** 由你——要么串里自带 `'\n'`，要么再 `fputc('\n', fp)`；函数本身不补。
- **它和 `puts` 怎么选？** 写文件必须用 `fputs`；只往屏幕打一行可以图省事用 `puts`。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：`fputs` 只认 `'\0'`，**"写到结尾就停，不管换行"**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`gets` —— ❌ 永远别用</span> <a id="fn-gets"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：读一整行，但**完全不检查长度**，是 C 语言里最危险的函数之一。

<span style="color:#5F7F63;font-weight:700">原型</span>：`char* gets(char* s);`（C11 已从标准中删除）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`char*` → 成功返回 `s`，失败 `NULL`｜`gets` 函数名｜`char* s` → 缓冲区——**注意它没有长度参数**，这正是它被删除的原因

| 项目 | 说明 |
| --- | --- |
| 参数 | `s` 缓冲区（多大都不管） |
| 返回 | 成功：`s`；失败：`NULL` |
| 失败场景 | 读到 EOF |

<span style="color:#5F7F63;font-weight:700">原理</span>：从输入读字符直到 `'\n'`，把换行替换成 `'\0'` 后返回。它**没有第二个参数**，也就没有任何长度上限——写多少算多少，溢出时直接踩坏相邻的栈变量或返回地址，这是它被 C11 删除的根本原因。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
/* 不要写这个 */
char buf[10];
gets(buf);            /* 输入 20 个字符 → 越界，栈被破坏 */

/* 替代方案 */
fgets(buf, sizeof(buf), stdin);
buf[strcspn(buf, "\n")] = '\0';
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **缓冲区溢出**：C11 已把它删掉，VS 会直接报 C4996 错误。
- **编译器给的最简单改法往往还是错的**（如提示换成 `gets_s`），正确替代是 `fgets`。
- **比赛平台可能仍能编过**，但结果不可控，永远别用。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **标准替代怎么写？** `fgets(buf, sizeof(buf), stdin)` 再 `buf[strcspn(buf, "\n")] = '\0';` 剪掉换行，长度就由 `sizeof(buf)` 兜住了。
- **编译器提示的 `gets_s` 能用吗？** 那是微软扩展，比赛平台不认，还是用 `fgets` 最稳。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`gets` = 没有刹车的车**，能开，但随时翻。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`sprintf` —— 把格式化的结果写进字符数组</span> <a id="fn-sprintf"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：和 `printf` 一模一样，只是输出到**字符数组**而不是屏幕。

<span style="color:#5F7F63;font-weight:700">原型</span>：`int sprintf(char* buf, const char* format, ...);`（`#include <stdio.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`int` → 返回写入的字符数（不含 `'\0'`）｜`sprintf` 函数名｜`char* buf` → 目标数组（**可写**，函数不管它多大）｜`const char* format` → 格式串｜`...` → 按 `%` 顺序填的值

| 项目 | 说明 |
| --- | --- |
| 参数 | `buf` 目标字符数组；`format` 格式串；后面是值 |
| 返回 | 成功：写入的**字符数**（不含 `'\0'`）；失败：负数 |
| 风险 | **没有任何长度限制**，写超了直接踩内存 |

<span style="color:#5F7F63;font-weight:700">原理</span>：和 `printf` 共用同一套格式解析，只是把「输出目标」从 `stdout` 换成了**你给的数组**：拼好的字符逐字节写进 `buf`，最后补 `'\0'`，返回写入的字符数。它不知道 `buf` 有多大，所以**缓冲区够不够完全由调用者负责**。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
char buf[100];
int n = 42; double x = 3.5;
sprintf(buf, "%d-%.1f", n, x);        /* buf = "42-3.5" */
printf("%s\n", buf);
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **不知道目标多大** → 拼出来的串超过容量就溢出，优先用 `snprintf`。
- **返回值是"本该写多少字符"**，不是"写了多少"，不能用来判断是否截断（那要用 `snprintf`）。
- **目标必须是可写数组**，不能是字符串字面量。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **它和 `printf` 是什么关系？** 同一套格式解析，只是把"写屏幕"换成"写进字符数组"。
- **典型用途？** 把数字拼成字符串，如文件名 `"img_%d.jpg"`、把多个字段拼成一行。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：`sprintf` 的 `s` = **string 目标**，把屏幕换成数组。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`snprintf` —— 限长版的 `sprintf`</span> <a id="fn-snprintf"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：同 `sprintf`，但**最多只写 `n-1` 个字符**，安全。

<span style="color:#5F7F63;font-weight:700">原型</span>：`int snprintf(char* buf, size_t n, const char* format, ...);`（`#include <stdio.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`int` → 返回**本该写入的长度**（≥ `n` 表示被截断）｜`snprintf` 函数名｜`char* buf` → 目标数组｜`size_t n` → 缓冲区**总字节数**（含 `'\0'`，所以最多写 `n-1` 个）｜其余同 `sprintf`

| 项目 | 说明 |
| --- | --- |
| 参数 | `buf` 目标；`n` 缓冲区**总字节数**（含 `'\0'`）；`format` 格式串 |
| 返回 | **本该写入的长度**（不含 `'\0'`）；若 ≥ `n` 说明被截断了 |
| 失败场景 | 编码错误等返回负数 |

<span style="color:#5F7F63;font-weight:700">原理</span>：格式解析与 `sprintf` 相同，但多了一道「闸门」：最多只写 `n-1` 个字符，写满就**停止写入**，并保证末尾有 `'\0'`。关键设计是：**被截断的部分仍然计数**，所以返回值可能 ≥ `n`——这正是判断「有没有被截断」的依据。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
char buf[10];
int ret = snprintf(buf, sizeof(buf), "%s-%d", "abcdef", 123);
if (ret >= (int)sizeof(buf)) printf("被截断了，需要 %d 字节\n", ret + 1);
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **`n` 含 `'\0'`**：想装 10 个字符，`n` 要写 11。
- **返回值可能大于 `n`**：那正是"被截断"的信号，不是错误。
- **和 `strncpy` 不同**：`snprintf` 一定补 `'\0'`，`strncpy` 不一定。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **怎么判断有没有被截断？** 看返回值：`ret >= n` 就说明放不下，此时 `buf` 里是"截断后的串"。
- **它和 `strncpy` 的区别？** `snprintf` 一定补 `'\0'`；`strncpy` 在"源不短于 n"时不补，要自己补。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：`s` + `n`，**"string 版，带 n 就有刹车"**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`sscanf` —— 从字符串里取数据</span> <a id="fn-sscanf"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：把 `scanf` 的对象从键盘换成**一个字符串**，从里面按格式取数据。

<span style="color:#5F7F63;font-weight:700">原型</span>：`int sscanf(const char* s, const char* format, ...);`（`#include <stdio.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`int` → 返回成功解析的**项数**｜`sscanf` 函数名｜`const char* s` → 源字符串（只读，不会被改动）｜`const char* format` → 格式串｜`...` → 变量的地址

| 项目 | 说明 |
| --- | --- |
| 参数 | `s` 源字符串；`format` 格式串；后面是**变量地址** |
| 返回 | **成功解析的项数**；一个都没匹配返回 `0`；源串读完返回 `EOF` |
| 失败场景 | 格式与内容不符时提前返回 |

<span style="color:#5F7F63;font-weight:700">原理</span>：把第一个参数当成「已经读好的输入行」，其余逻辑与 `scanf` 完全一致：跳空白、按格式转换、按地址写内存、返回值是匹配项数。区别只在**数据来源是内存**，所以不会动输入缓冲区，也不会被残留换行干扰。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
char line[] = "Tom 90 85";
char name[20]; int a, b;
if (sscanf(line, "%s %d %d", name, &a, &b) == 3) {
    printf("%s %d %d\n", name, a, b);
}
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **返回值是项数**，不是成功/失败，判断要写 `== 3`。
- **普通变量仍要 `&`**，数组名不用。
- **不修改源串**：它只读，和 `strtok` 不同。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **它和 `scanf` 的区别？** 数据来源不同：`scanf` 从键盘缓冲区取，`sscanf` 从内存里的字符串取。
- **什么时候用它更稳？** 先用 `fgets` 读一整行，再用 `sscanf` 拆字段——输入出错也不会污染缓冲区。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`s` + `scanf` = 从 string 里扫**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`fprintf` —— 格式化写入文件</span> <a id="fn-fprintf"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：`printf` 的文件版，把格式化结果写进文件。

<span style="color:#5F7F63;font-weight:700">原型</span>：`int fprintf(FILE* fp, const char* format, ...);`（`#include <stdio.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`int` → 返回写出的字符数｜`fprintf` 函数名｜`FILE* fp` → 目标文件流（第一参数从"格式串"换成了"流"）｜其余与 `printf` 相同

| 项目 | 说明 |
| --- | --- |
| 参数 | `fp` 目标流；`format` 格式串；后面按序填值 |
| 返回 | 成功：写出的字符数；失败：负数 |
| 失败场景 | 文件只读、磁盘满 |

<span style="color:#5F7F63;font-weight:700">原理</span>：格式解析同 `printf`，写入目标换成 `fp` 指向的文件缓冲。文件缓冲通常是**全缓冲**（不是行缓冲），要等缓冲满、`fflush` 或 `fclose` 才真正写盘——这就是「写完不关文件可能读不到」的原因。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
FILE* fp = fopen("stu.txt", "w");
if (fp == NULL) { perror("open"); return 1; }
fprintf(fp, "%s %d\n", "Tom", 90);       /* ① 每行自己补 \n */
fclose(fp);                              /* ② 不关 = 可能没写进去 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **不自带换行**：格式串里要自己写 `\n`，否则所有记录连成一行。
- **`fclose` 前数据可能还在缓冲区**：不关文件，程序异常退出会丢数据。
- **`"w"` 会先清空文件**，想追加用 `"a"`。
- **文件名带空格/全角逗号**（`"stu. txt"`）→ `fopen` 返回 NULL。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **它和 `fwrite` 怎么选？** 要人能看懂、记事本能打开用 `fprintf`（文本）；要原样存二进制、读写快用 `fwrite`。
- **它和 `printf` 的关系？** 同一套格式串，目标从屏幕换成文件。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：`f` + `printf` = **f**ile 版格式化输出。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`fscanf` —— 从文件按格式读</span> <a id="fn-fscanf"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：`scanf` 的文件版，按格式从文件里取值。

<span style="color:#5F7F63;font-weight:700">原型</span>：`int fscanf(FILE* fp, const char* format, ...);`（`#include <stdio.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`int` → 返回成功读到的项数；`EOF` 表示到文件尾｜`fscanf` 函数名｜`FILE* fp` → 源文件流｜`...` → 变量地址（`name` 不加 `&`，`score` 要加）

| 项目 | 说明 |
| --- | --- |
| 参数 | `fp` 源文件；`format` 格式串；后面是变量地址 |
| 返回 | **成功读到的项数**；读到文件尾返回 `EOF` |
| 失败场景 | 格式与内容不符、遇到 EOF |

<span style="color:#5F7F63;font-weight:700">原理</span>：解析逻辑同 `scanf`，但数据来自 `fp` 的**文件缓冲**，缓冲空了由库自动 `read` 补齐。返回值是成功匹配的项数；读到文件尾返回 `EOF`。它不会告诉你「文件里还剩几条」，所以循环必须靠返回值控制。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
char name[20]; int score;
while (fscanf(fp, "%s %d", name, &score) == 2) {   /* ① 读满 2 项才继续 */
    printf("%s %d\n", name, score);
}
/* 循环结束后可用 feof(fp) 判断是"正常读完"还是"格式出错" */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **不能 `for (i = 0; i < 5; i++)` 硬读 5 次**：文件里未必有 5 条，多读会拿到重复的最后一条。
- **`fscanf` 的 `%s` 遇空白就停**，读不了带空格的名字。
- **`name` 不加 `&`、`score` 必须加**。
- **返回 `EOF` 或小于项数**都表示没读满，靠 `== 2` 统一兜住。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **它和 `fgets` 怎么选？** 记录规整、字段用空白分隔用 `fscanf`；要整行原样读、自己再解析用 `fgets`。
- **循环结束后怎么知道是读完了还是格式错了？** 配合 `feof(fp)` 与 `ferror(fp)` 分开判断。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：`f` + `scanf`，**从 file 扫，看项数停**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`fgetc` —— 读一个字符（文件）</span> <a id="fn-fgetc"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：从文件里读**一个字节**，文件版 `getchar`。

<span style="color:#5F7F63;font-weight:700">原型</span>：`int fgetc(FILE* fp);`（`#include <stdio.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`int` → 返回读到的字节（0~255）；`EOF` 表示末尾或出错｜`fgetc` 函数名｜`FILE* fp` → 源流

| 项目 | 说明 |
| --- | --- |
| 参数 | `fp` 源文件流 |
| 返回 | 成功：该字节（0~255，提升为 `int`）；文件尾或出错：`EOF` |
| 失败场景 | 读到文件尾、流出错（两者都返回 `EOF`，要区分用 `feof`/`ferror`） |

<span style="color:#5F7F63;font-weight:700">原理</span>：从 `FILE` 的内部缓冲取一个字节，缓冲空了就触发一次系统 `read` 填充。返回时提升成 `int`（0~255），文件尾或出错返回 `EOF`——两者都是 -1，要靠 `feof`/`ferror` 事后区分。文本模式下库会**悄悄处理 `\r\n` 转换**，二进制模式原样返回。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
int ch;                       /* ① 必须 int */
while ((ch = fgetc(fp)) != EOF) {
    fputc(ch, out);           /* 逐字节复制 */
}
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **用 `char` 接**：遇到 0xFF 的字节会被当成 -1，循环提前结束（二进制文件尤其明显）。
- **`EOF` 不能当字符判断**：`char` 装不下，只能 `int`。
- **文本模式读到的 `\r\n` 会被转换**，二进制模式原样。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **它和 `getchar` 是什么关系？** `getchar()` 等价于 `fgetc(stdin)`，区别只是读哪个流。
- **它怎么复制图片？** 图片是二进制字节，用它逐字节读写并配 `"rb"/"wb"`，才能一个字节都不差。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：`f` + `getc`，**按字节取，用 int 接**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`fputc` —— 写一个字符（文件）</span> <a id="fn-fputc"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：把一个字节写进文件，文件版 `putchar`。

<span style="color:#5F7F63;font-weight:700">原型</span>：`int fputc(int c, FILE* fp);`（`#include <stdio.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`int` → 返回写出的字节；`EOF` 失败｜`fputc` 函数名｜`int c` → 要写的字符（只取低 8 位）｜`FILE* fp` → 目标流

| 项目 | 说明 |
| --- | --- |
| 参数 | `c` 要写的字符；`fp` 目标流 |
| 返回 | 成功：写出的字节；失败：`EOF` |
| 失败场景 | 流不可写、磁盘满 |

<span style="color:#5F7F63;font-weight:700">原理</span>：把字节写进 `FILE` 的输出缓冲，缓冲满、遇换行（行缓冲）或 `fflush` 时才落盘。文本模式下库可能把 `'\n'` 转成 `\r\n`（Windows），二进制模式原样写。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
while ((ch = fgetc(in)) != EOF)
    fputc(ch, out);           /* 逐字节复制，文本/二进制通用 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **返回值是 int**，写失败返回 `EOF`，可以用于校验。
- **不刷新缓冲**，要立刻落盘得 `fflush(fp)`。
- **和目标文件的模式有关**：`"w"` 文本模式可能转换换行。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **它和 `fwrite` 的区别？** `fputc` 一次一个字节（流式），`fwrite` 一次一整块（批量）。
- **什么时候必须用它？** 字符级复制、逐字节改写文件时最直观。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：`put` + `c` + `f`，**一个字节一个字节地放**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`fread` —— 按块读（二进制）</span> <a id="fn-fread"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：从文件里整块读 `count` 个 `size` 字节的数据。

<span style="color:#5F7F63;font-weight:700">原型</span>：`size_t fread(void* buf, size_t size, size_t count, FILE* fp);`（`#include <stdio.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`size_t` → 返回**实际读到的完整块数**（不是字节数）｜`fread` 函数名｜`void* buf` → 目标内存（"万能指针"，任何类型都能接）｜`size_t size` → **每块多少字节**｜`size_t count` → **要读几块**｜`FILE* fp` → 源流

| 项目 | 说明 |
| --- | --- |
| 参数 | `buf` 目标内存；`size` **每块多少字节**；`count` **读几块**；`fp` 源文件 |
| 返回 | **实际读到的完整块数**（不是字节数） |
| 失败场景 | 文件尾不够 count 块 → 返回小于 count 的数；0 表示一块都没读到 |

<span style="color:#5F7F63;font-weight:700">原理</span>：以 `size` 为单位循环搬运，最多凑满 `count` 块；内部就是「从文件缓冲拷字节到目标内存」，读不够时由库再 `read` 补齐。返回值是**完整块数**（0~count），最后那「不完整的一块」不会被计入——所以判断读没读完常配合 `feof`。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
struct Stu buf[100];
size_t got = fread(buf, sizeof(struct Stu), 100, fp);   /* ① size 是单份大小 */
printf("读到 %zu 份\n", got);
for (i = 0; i < (int)got; i++) { /* 用 buf[i] */ }
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **返回的是块数不是字节数**：字节数 = `got * size`。
- **别套在 `for (i < 5)` 里**：一次 `fread` 已经读 5 份，循环会变成 5 次空读。
- **`size` 和 `count` 写反**反而也能读，但返回值含义就乱了——保持"单份大小, 份数"。
- **返回值是 `size_t`**，打印用 `%zu`，别用 `%d`（C4477）。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **和 `fscanf` 怎么选？** 结构体整块读用 `fread`（快、无格式解析）；文本记录用 `fscanf`。
- **读不满时怎么判断原因？** `feof` 说明读到头了，`ferror` 说明真出错。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：`fread` = **read 若干整块**，返回值是**块数**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`fwrite` —— 按块写（二进制）</span> <a id="fn-fwrite"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：把内存里的一块数据整份写进文件。

<span style="color:#5F7F63;font-weight:700">原型</span>：`size_t fwrite(const void* buf, size_t size, size_t count, FILE* fp);`（`#include <stdio.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`size_t` → 返回**实际写出的完整块数**｜`fwrite` 函数名｜`const void* buf` → 源内存（只读）｜`size_t size` / `size_t count` 含义同 `fread`｜`FILE* fp` → 目标流

| 项目 | 说明 |
| --- | --- |
| 参数 | `buf` 源内存；`size` 每块字节；`count` 块数；`fp` 目标文件 |
| 返回 | **实际写出的完整块数**（正常时应等于 count） |
| 失败场景 | 磁盘满、流不可写 |

<span style="color:#5F7F63;font-weight:700">原理</span>：以 `size` 为单位把内存字节写进文件缓冲，缓冲满了由库 `write` 到磁盘；返回**成功写出的完整块数**。它完全不理解类型，结构体的填充字节也会照写，所以「文件比字段总和大」是正常现象。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
FILE* fp = fopen("stu.dat", "wb");          /* ① 二进制模式 */
if (!fp) { perror("open"); return 1; }
size_t n = fwrite(s, sizeof(struct Stu), 5, fp);   /* ② 一次写 5 份 */
printf("写出 %zu 份\n", n);
fclose(fp);
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **文本模式 `"w"` 写二进制会被转换换行**，必须 `"wb"`。
- **扩展名不等于格式**：存成 `.txt` 也还是二进制字节，改名字不改内容。
- **结构体有填充字节**（padding），跨平台读会错位。
- **返回值要看**：写满才说明成功。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **为什么文件比"字段加起来"大？** 结构体有内存对齐的**填充字节**，`fwrite` 会连填充一起写出去。
- **它和 `fprintf` 怎么选？** 给人看用 `fprintf`，给程序读、要紧凑用 `fwrite`。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`fwrite` 是搬运工，不懂类型，只认字节**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`fopen` —— 打开文件</span> <a id="fn-fopen"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：按模式打开文件，返回一个流指针；失败返回 `NULL`。

<span style="color:#5F7F63;font-weight:700">原型</span>：`FILE* fopen(const char* path, const char* mode);`（`#include <stdio.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`FILE*` → 成功返回**流指针**，失败返回 `NULL`（必须判空）｜`fopen` 函数名｜`const char* path` → 文件路径（相对当前工作目录）｜`const char* mode` → 模式字符串 `"r"/"w"/"a"/"rb"…`

| 项目 | 说明 |
| --- | --- |
| 参数 | `path` 文件路径；`mode` 模式字符串 |
| 返回 | 成功：`FILE*` 流指针；失败：`NULL` |
| 失败场景 | 文件不存在（读模式）、无权限、路径错误、文件被占用 |

<span style="color:#5F7F63;font-weight:700">原理</span>：向操作系统请求「打开 / 创建」某个路径，成功后由 C 库**分配一个 `FILE` 结构**——里面装着文件描述符、缓冲区、当前位置、读写模式和各种标志位，返回的就是它的地址。模式字符串同时决定三件事：不存在时建不建、旧内容清不清、读写权限。任何一步失败都返回 `NULL`，并把原因记进全局变量 `errno`。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
FILE* fp = fopen("data.txt", "r");
if (fp == NULL) {                       /* ① 必须判空 */
    perror("fopen");                    /* ② 打印失败原因 */
    return 1;                           /* ③ 立刻退出，别继续用 */
}
/* ... 读写 ... */
fclose(fp);
```

**模式速查**

| 模式 | 含义 | 文件不存在 | 旧内容 |
| --- | --- | --- | --- |
| `"r"` | 只读 | **失败（NULL）** | 保留 |
| `"w"` | 只写 | 新建 | **清空** |
| `"a"` | 追加 | 新建 | 保留，写在末尾 |
| `"r+"` | 读写 | **失败** | 保留 |
| `"w+"` | 读写 | 新建 | **清空** |
| `"a+"` | 读写 | 新建 | 保留，写永远在末尾 |
| `"rb"/"wb"/"ab"` | 二进制版 | 同上 | 同上 |

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **不判 `NULL` 就用**：`fgetc(NULL)` 直接崩（0xC0000005）。
- **想读却用了 `"w"`**：文件先被清空，源数据当场没了。
- **以为 `"r"` 会新建文件**：不会，不存在就失败。
- **路径是相对"当前工作目录"**：VS 调试时是工程目录，不是 `.sln` 旁边，也不是 `Debug`。
- **文件名里混进空格**（`"stu. txt"`）→ 永远打不开。
- **`"a"` 模式写不到中间**：`fseek` 只影响读位置，写永远追加到末尾。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **`"w"` 打开失败等于"清空失败"吗？** 不是——失败是返回 `NULL`，文件**根本没打开**，谈不上清空。
- **`+` 是什么意思？** 只表示"可读可写"，不代表能任意位置写；写的位置还受模式和 `fseek` 约束。
- **`"r"` 和 `"r+"` 会新建文件吗？** 都不会，不存在直接返回 `NULL`；只有 `"w"/"a"/"w+"/"a+"` 才新建。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：`fopen` = **file open**，**打开就要验货（判 NULL）**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`fclose` —— 关闭文件</span> <a id="fn-fclose"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：把缓冲区里没写完的数据刷出去，然后断开文件连接。

<span style="color:#5F7F63;font-weight:700">原型</span>：`int fclose(FILE* fp);`（`#include <stdio.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`int` → 成功返回 **0**，失败返回 `EOF`｜`fclose` 函数名｜`FILE* fp` → 要关闭的流

| 项目 | 说明 |
| --- | --- |
| 参数 | `fp` 要关闭的流 |
| 返回 | 成功：`0`；失败：`EOF`（-1） |
| 失败场景 | 缓冲区写盘失败（磁盘满） |

<span style="color:#5F7F63;font-weight:700">原理</span>：先对输出流做一次 `fflush`（把缓冲里的数据写盘），再通知系统关闭文件描述符，最后释放 `FILE` 结构和缓冲区。**顺序很重要**：直接关而不刷，缓冲区里没写出去的数据就丢了。成功返回 0，写盘失败返回 `EOF`。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
FILE* fp = fopen("a.txt", "w");
if (!fp) return 1;
fputs("hello\n", fp);
fclose(fp);                     /* ① 写完立刻关，数据才算落地 */

fp = fopen("a.txt", "r");       /* ② 要换个方向读写，关掉重开最稳 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **不关文件**：缓冲区数据可能丢失；文件句柄泄漏。
- **关完还继续用**：`fclose` 后指针失效，再用是未定义行为。
- **同一流关两次**：会破坏内部结构，直接崩。
- **想立刻读自己刚写的内容**：先 `fflush` 或直接 `fclose` 再重开。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **为什么它一调用，数据就保证落盘？** 它内部先做一次 `fflush` 把缓冲区写出去，再释放流对象。
- **不关文件会怎样？** 缓冲区数据可能丢、文件句柄泄漏，程序异常退出时最明显。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`fclose` = 结账走人**，走之前把账（缓冲区）结清。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`fseek` —— 定位读写位置</span> <a id="fn-fseek"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：把文件读写指针挪到指定位置。

<span style="color:#5F7F63;font-weight:700">原型</span>：`int fseek(FILE* fp, long offset, int origin);`（`#include <stdio.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`int` → 成功返回 **0**，失败返回非 0｜`fseek` 函数名｜`FILE* fp` → 流｜`long offset` → **字节偏移**（可正可负）｜`int origin` → 基点：`SEEK_SET`(0 开头)/`SEEK_CUR`(1 当前)/`SEEK_END`(2 末尾)

| 项目 | 说明 |
| --- | --- |
| 参数 | `fp` 流；`offset` **字节偏移**（可负）；`origin` 基点：`SEEK_SET`(0 开头)、`SEEK_CUR`(1 当前)、`SEEK_END`(2 末尾) |
| 返回 | 成功：`0`；失败：非 0 |
| 失败场景 | 偏移非法、文本模式下不支持的跳转 |

<span style="color:#5F7F63;font-weight:700">原理</span>：直接修改 `FILE` 里记录的**位置偏移**，必要时丢弃「预读」的缓冲内容，免得下次读到的还是旧位置的数据；同时会**清掉 `EOF` 标志**（因为已经不在末尾了）。它只移动「笔尖」，不搬动任何数据，所以后续的写是**覆盖**。文本模式下因为存在 `\r\n` 转换，位置和字节数不能一一对应，标准只保证「0 和 `ftell` 返回过的值」是合法的。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
fseek(fp, 0, SEEK_END);         /* ① 跳到末尾 */
long size = ftell(fp);          /* ② 求文件大小 */
rewind(fp);                     /* ③ 回到开头 */

fseek(fp, 4, SEEK_SET);         /* ④ 第 5 个字节（偏移从 0 数） */
fputc('X', fp);                 /* ⑤ 覆盖那个字节，不是插入 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **偏移从 0 开始**：第 5 个字节的偏移是 **4**。
- **求大小时别先 `-1`**：`fseek(-1, SEEK_END)` 后再 `ftell` 得到的是 `size-1`。
- **文本模式下 `offset` 只能是 0 或 `ftell` 的返回值**，基点用 `SEEK_SET`；要按字节随便跳，用 `"rb"`。
- **覆盖不是插入**：想在中间插入内容，只能读到新文件再写回。
- **`fseek` 会清掉已经置位的 `EOF` 标志**。
- **追加模式 `"a"` 下 `fseek` 管不住写**：写永远落在末尾。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **三个基点怎么选？** `SEEK_SET` 从开头算、`SEEK_CUR` 从当前位置算、`SEEK_END` 从末尾算（末尾偏移用负数往回退）。
- **想"不动位置"只查当前位置怎么办？** `fseek(fp, 0, SEEK_CUR)` 就是个空操作，位置不变。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：`seek` = **找**，**挪笔尖，不改纸**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`ftell` —— 当前在哪</span> <a id="fn-ftell"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：告诉你读写指针距离文件头有多少字节。

<span style="color:#5F7F63;font-weight:700">原型</span>：`long ftell(FILE* fp);`（`#include <stdio.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`long` → 返回当前位置距文件头的字节数，失败返回 `-1L`｜`ftell` 函数名｜`FILE* fp` → 流（返回类型是 `long`，所以打印用 `%ld`）

| 项目 | 说明 |
| --- | --- |
| 参数 | `fp` 流 |
| 返回 | 成功：当前偏移（**字节**，`long`）；失败：`-1L` |
| 失败场景 | 流不可定位 |

<span style="color:#5F7F63;font-weight:700">原理</span>：读取 `FILE` 里那个**位置计数器**的当前值并返回 `long`。二进制模式下它就是「从文件头数起的字节数」；文本模式下因为库做过换行转换，计数器记录的是「流里走过多少字节」，和磁盘上的实际字节数可能不一致——所以只能当「书签」原样还给 `fseek`。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
fseek(fp, 0, SEEK_END);
long size = ftell(fp);          /* ① 文件总字节数 */
printf("大小：%ld 字节\n", size);   /* ② long 用 %ld */

long pos = ftell(fp);           /* ③ 随时取当前位置，做"书签" */
fseek(fp, pos, SEEK_SET);       /* ④ 之后再回到这里 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **返回值是 `long`**：用 `int` 接会截断（文件 > 2GB 更明显），打印用 `%ld`。
- **文本模式下它返回的是"书签"不是纯字节数**（Windows 的 `\r\n` 会算两位），拿它当偏移必须原样放回。
- **没先 `fseek` 到末尾就 `ftell`**，得到的是当前位置，不是文件大小。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **怎么把它当"书签"用？** 先 `long pos = ftell(fp);` 记住位置，乱跳之后再 `fseek(fp, pos, SEEK_SET)` 回来。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：`tell` = **告诉我笔尖在哪**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`rewind` —— 回开头</span> <a id="fn-rewind"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：把指针挪回文件开头，并清掉错误/EOF 标志。

<span style="color:#5F7F63;font-weight:700">原型</span>：`void rewind(FILE* fp);`（`#include <stdio.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`void` → **没有返回值**，失败了也看不出来｜`rewind` 函数名｜`FILE* fp` → 流（回开头并清 `EOF`/错误标志）

| 项目 | 说明 |
| --- | --- |
| 参数 | `fp` 流 |
| 返回 | 无 |
| 副作用 | 清 `EOF` 标志和 `ferror` 标志 |

<span style="color:#5F7F63;font-weight:700">原理</span>：等价于 `fseek(fp, 0, SEEK_SET)` **再加** `clearerr(fp)`：既把位置归零，又把「已到末尾」和「出过错」两个标志一起清掉。它没有返回值，所以不会有失败提示。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
while (fgets(line, sizeof(line), fp)) { /* 第一遍读 */ }
rewind(fp);                              /* ① 回到开头再读一遍 */
while (fgets(line, sizeof(line), fp)) { /* 第二遍读 */ }
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **它不关闭文件**，只是把位置归零。
- **文本 / 二进制模式都安全**，这是它比 `fseek` 省心的地方。
- **`rewind` 后标志被清**，`feof` 会重新变回 0。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **什么时候需要读两遍？** 第一遍统计行数/最大值，第二遍才输出——中间用 `rewind` 回到开头。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：`rewind` = **倒带**，回到第一帧。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`feof` —— 是否到末尾</span> <a id="fn-feof"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：判断上一次读操作是不是**因为读到文件尾而失败**。

<span style="color:#5F7F63;font-weight:700">原型</span>：`int feof(FILE* fp);`（`#include <stdio.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`int` → 返回非 0 表示已到文件尾，返回 0 表示没到｜`feof` 函数名｜`FILE* fp` → 流（只是读标志，不会移动位置）

| 项目 | 说明 |
| --- | --- |
| 参数 | `fp` 流 |
| 返回 | 已到末尾：非 0；否则：`0` |
| 关键点 | 它是**事后标记**，不是预告 |

<span style="color:#5F7F63;font-weight:700">原理</span>：它不预测未来，只**读一个标志位**：这个标志只有某次读操作**真正尝试越过文件尾并失败**之后才会被置起。所以「刚读完最后一条」的那一刻它还是假，必须再读一次、失败一次，它才变真——这就是「拿它当循环条件会多跑一轮」的根本原因。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
/* ❌ 错误：会多跑一轮 */
while (!feof(fp)) {
    fgets(line, sizeof(line), fp);
    printf("%s", line);           /* 最后会多打一次旧数据 */
}

/* ✅ 正确：看读函数的返回值 */
while (fgets(line, sizeof(line), fp) != NULL) {
    printf("%s", line);
}

/* 循环结束后想知道"为什么停" */
if (feof(fp))      printf("正常读完\n");
else if (ferror(fp)) printf("出错了\n");
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **不能当循环条件**：会多执行一轮，输出重复的最后一条。
- **`feof` 为真时文件指针已越界**，不能再用。
- **必须 `clearerr` 或 `rewind`/`fseek` 才能复位**。
- **它只说"到末尾"，不说"为什么停"**，出错要看 `ferror`。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **循环结束后怎么判断"为什么停"？** 用 `feof` 和 `ferror` 组合：`feof=1, ferror=0` 是正常读完；`feof=0, ferror=1` 是真出错。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：`feof` = **file end of file**，**"已经撞墙了才告诉你"**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`ferror` —— 是否出错</span> <a id="fn-ferror"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：判断这个流上有没有发生过**真正的读写错误**。

<span style="color:#5F7F63;font-weight:700">原型</span>：`int ferror(FILE* fp);`（`#include <stdio.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`int` → 返回非 0 表示出过错，0 表示没出错｜`ferror` 函数名｜`FILE* fp` → 流

| 项目 | 说明 |
| --- | --- |
| 参数 | `fp` 流 |
| 返回 | 出过错：非 0；否则：`0` |
| 复位 | `clearerr(fp)` 清除 |

<span style="color:#5F7F63;font-weight:700">原理</span>：I/O 过程中一旦发生真实错误（磁盘故障、权限、管道断开），库就在 `FILE` 里**置起错误标志**；`ferror` 只负责读这个标志。它和 EOF 标志是两个独立的位：正常读完是 `feof=1, ferror=0`，真出错是 `feof=0, ferror=1`。标志是**粘性**的，只能用 `clearerr` 清。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
size_t got = fread(buf, 1, 100, fp);
if (got < 100) {
    if (ferror(fp))       printf("读出错\n");
    else if (feof(fp))    printf("正常读完\n");
}
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **`feof` 和 `ferror` 要分开判断**：读完正常是 `feof=1, ferror=0`；真出错是 `feof=0, ferror=1`。
- **标志是粘性的**：一旦置位不会自动清，要 `clearerr`。
- **它不告诉你具体错误**，需要 `errno` + `strerror`/`perror`。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **它和 `feof` 是两个独立的位？** 对，互不影响；两个都查才能区分"正常读完"和"读到一半坏了"。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：`ferror` = **file error**，**"出过事没有"**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`perror` —— 打印错误原因</span> <a id="fn-perror"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：把当前 `errno` 翻译成一句人话，前面加上你给的提示。

<span style="color:#5F7F63;font-weight:700">原型</span>：`void perror(const char* s);`（`#include <stdio.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`void` → **没有返回值**，只负责打印｜`perror` 函数名｜`const char* s` → 自定义前缀（可传 `NULL` 只打描述）

| 项目 | 说明 |
| --- | --- |
| 参数 | `s` 自定义前缀（可为 `NULL`） |
| 返回 | 无 |
| 输出去向 | 标准错误 `stderr` |

<span style="color:#5F7F63;font-weight:700">原理</span>：读取全局变量 `errno` 当前的值，去一张错误码表里查出对应的英文描述，再按「你的前缀: 描述」的格式**写到 `stderr`**。它不返回任何值，也不会清 `errno`——所以必须在出错后**立刻**调用，中间再调别的库函数可能就把 `errno` 覆盖了。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
FILE* fp = fopen("no_such.txt", "r");
if (fp == NULL) {
    perror("fopen");            /* 输出：fopen: No such file or directory */
    return 1;
}
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **必须在出错后立刻调用**：后面的库函数可能覆盖 `errno`。
- **输出到 stderr 不是 stdout**，重定向时要注意。
- **它不会清 `errno`**，也不返回值。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **它和 `strerror` 有什么区别？** `perror` 直接打印到 stderr；`strerror(errno)` 返回字符串，想怎么排版自己决定。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：`perror` = **print error**，**把错误码翻译成人话**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`remove` —— 删除文件</span> <a id="fn-remove"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：删除指定路径的文件。

<span style="color:#5F7F63;font-weight:700">原型</span>：`int remove(const char* path);`（`#include <stdio.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`int` → 成功返回 **0**，失败返回非 0｜`remove` 函数名｜`const char* path` → 要删除的文件路径

| 项目 | 说明 |
| --- | --- |
| 参数 | `path` 文件路径 |
| 返回 | 成功：`0`；失败：非 0 |
| 失败场景 | 文件不存在、只读、正被打开、无权限 |

<span style="color:#5F7F63;font-weight:700">原理</span>：调用操作系统的删除接口，把目录项标记为可删除。失败时返回非 0 并设置 `errno`；Windows 下如果文件还有打开的句柄，删除会**直接失败**（这是它最常见的失败原因）。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
if (remove("tmp.txt") == 0) printf("删除成功\n");
else perror("remove");          /* ① 失败时看原因 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **返回 0 才是成功**，非 0 是失败（和很多函数相反）。
- **文件还被打开着**（`fopen` 没 `fclose`）→ 删除失败。
- **删了不能恢复**，测试前先备份。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **它和 `fopen("w")` 清空有什么区别？** `remove` 删掉整个文件；`"w"` 只是把内容清空、文件还在。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`remove` = 0 才是"办成了"**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`rename` —— 改名 / 移动</span> <a id="fn-rename"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：把文件从旧名字改成新名字（同一磁盘内也等于移动）。

<span style="color:#5F7F63;font-weight:700">原型</span>：`int rename(const char* oldname, const char* newname);`（`#include <stdio.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`int` → 成功返回 **0**，失败返回非 0｜`rename` 函数名｜`const char* oldname` → 原路径｜`const char* newname` → 新路径

| 项目 | 说明 |
| --- | --- |
| 参数 | `oldname` 旧路径；`newname` 新路径 |
| 返回 | 成功：`0`；失败：非 0 |
| 失败场景 | 源不存在、目标已存在（部分系统）、跨磁盘、文件被打开 |

<span style="color:#5F7F63;font-weight:700">原理</span>：本质是**修改目录项**：把旧名字的条目改成新名字，文件内容一个字节都不动，所以非常快。同一分区内相当于「移动」；跨分区需要真的复制，因此会失败。目标已存在时的行为依平台而定。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
if (rename("a.txt", "b.txt") == 0) printf("改名成功\n");
else perror("rename");
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **同样是 0 才成功**。
- **目标文件已存在时行为依平台而定**，可能覆盖也可能失败。
- **跨盘移动会失败**（不是同一文件系统）。
- **改名后旧名字就没了**，验证时要检查旧名是否还能打开。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **它怎么和 `remove` 配合做"移动"？** 先把文件改名到新目录，原路径就没了，效果等价于移动。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：`rename` = **re-name**，**换名牌，不动货**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`fflush` —— 刷新缓冲区</span> <a id="fn-fflush"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：把输出缓冲区里攒着的数据立刻推到底层（写盘/上屏）。

<span style="color:#5F7F63;font-weight:700">原型</span>：`int fflush(FILE* fp);`（`#include <stdio.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`int` → 成功返回 **0**，失败返回 `EOF`｜`fflush` 函数名｜`FILE* fp` → 要刷新的**输出流**（传 `NULL` 表示刷新所有输出流）

| 项目 | 说明 |
| --- | --- |
| 参数 | `fp` 要刷新的输出流；`NULL` 表示刷新所有输出流 |
| 返回 | 成功：`0`；失败：`EOF` |
| 注意 | **`fflush(stdin)` 是未定义行为**，标准 C 不支持 |

<span style="color:#5F7F63;font-weight:700">原理</span>：把输出缓冲区里**还没写出去的内容**立刻 `write` 到底层，然后清空缓冲。标准只对**输出流**定义了行为；`fflush(stdin)` 属于未定义行为，不同平台表现不一，不能用来清输入。它不关闭流，之后还能继续写。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
FILE* fp = fopen("log.txt", "w");
fputs("hello\n", fp);
fflush(fp);                     /* ① 立刻落盘，不关文件也能读到 */
/* ... 用另一个流去读这个文件 ... */
fclose(fp);
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **`fflush(stdin)` 不是"清输入缓冲区"的标准做法**，是 UB；清输入要用 `getchar` 循环或 `scanf(" %c")`。
- **只对输出流有效**，输入流的刷新行为未定义。
- **刷新 ≠ 关闭**：文件句柄还开着，最后仍要 `fclose`。
- **不 `fflush` 又不 `fclose`**，程序崩溃时数据全丢。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **什么时候必须手动刷新？** 写完马上要用另一个流读同一个文件、或写日志怕程序崩时。
- **它和 `fclose` 的区别？** `fflush` 只落盘、流还开着；`fclose` 落盘并关闭。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：`flush` = **冲水**，把缓冲池里的水一次冲下去。

#### <span style="color:#7FA182">printf / scanf 格式符对照表</span>

| 格式符 | 对应类型 | 例子 |
| --- | --- | --- |
| `%d` | int | `printf("%d", 42);` |
| `%f` | float / double（printf 通用） | `printf("%.2f", 3.14159);` → `3.14` |
| `%lf` | double（scanf 里必须用 `%lf`） | `scanf("%lf", &x);` |
| `%c` | char | `printf("%c", 'A');` |
| `%s` | 字符串 | `printf("%s", name);` |
| `%%` | 输出一个百分号 | `printf("100%%");` → `100%` |
| `%zu` | `size_t`（`strlen`、`sizeof` 的返回值） | `printf("%zu", strlen(s));` |
| `%u` | `unsigned`（无符号整数） | `printf("%u", n);` |
| `%p` | 指针（打印地址） | `printf("%p", (void*)p);` |

> `%.2f` 表示保留两位小数；`%f` 默认保留 6 位。

## <span style="color:#7FA182">2. string.h —— 字符串家族</span> <a id="sec55"></a>

> 使用前记得 `#include <string.h>`。

| 函数 | 原型（返回类型 + 参数类型） | 掌握 |
| --- | --- | --- |
| [`strlen`](#fn-strlen) | `size_t strlen(const char* s);` | ✅ |
| [`strcpy`](#fn-strcpy) | `char* strcpy(char* dst, const char* src);` | ✅ |
| [`strcmp`](#fn-strcmp) | `int strcmp(const char* a, const char* b);` | ✅ |
| [`strcat`](#fn-strcat) | `char* strcat(char* dst, const char* src);` | ✅ |
| [`strchr`](#fn-strchr) | `char* strchr(const char* s, int c);` | ⚪ |
| [`strrchr`](#fn-strrchr) | `char* strrchr(const char* s, int c);` | ⚪ |
| [`strstr`](#fn-strstr) | `char* strstr(const char* s, const char* sub);` | ⚪ |
| [`strncpy`](#fn-strncpy) | `char* strncpy(char* dst, const char* src, size_t n);` | ⚪ |
| [`strncat`](#fn-strncat) | `char* strncat(char* dst, const char* src, size_t n);` | ⚪ |
| [`strncmp`](#fn-strncmp) | `int strncmp(const char* a, const char* b, size_t n);` | ⚪ |
| [`strtok`](#fn-strtok) | `char* strtok(char* s, const char* delim);` | ⚪ |
| [`strspn`](#fn-strspn) | `size_t strspn(const char* s, const char* set);` | ⬜ |
| [`strcspn`](#fn-strcspn) | `size_t strcspn(const char* s, const char* set);` | ⬜ |
| [`memcpy`](#fn-memcpy) | `void* memcpy(void* dst, const void* src, size_t n);` | ⚪ |
| [`memmove`](#fn-memmove) | `void* memmove(void* dst, const void* src, size_t n);` | ⚪ |
| [`memcmp`](#fn-memcmp) | `int memcmp(const void* a, const void* b, size_t n);` | ⚪ |
| [`memset`](#fn-memset) | `void* memset(void* dst, int value, size_t n);` | ⬜ |
| [`strerror`](#fn-strerror) | `char* strerror(int errnum);` | ⬜ |

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`strlen` —— 求实际长度</span> <a id="fn-strlen"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：从字符串开头数到 `'\0'`，告诉你里面**实际有几个字符**（不含结束符）。

<span style="color:#5F7F63;font-weight:700">原型</span>：`size_t strlen(const char* s);`（`#include <string.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`size_t` 是**返回类型** → 无符号的"长度"，打印用 `%zu`｜`strlen` 是**函数名**｜`const char* s` 是**参数** → 要量的字符串，`const` 表示只读、函数不会改它

| 项目 | 说明 |
| --- | --- |
| 参数 | `s` 必须以 `'\0'` 结尾的字符串 |
| 返回 | 到 `'\0'` 之前的字符个数（**不含** `'\0'`） |
| 失败场景 | 没有失败返回；传 `NULL` 或没有结束符的数组会直接崩 |
| 复杂度 | `O(n)`——每次调用都从头数一遍，不做缓存 |

<span style="color:#5F7F63;font-weight:700">原理</span>：它是一个"数到句号为止"的循环：从 `s[0]` 开始逐字节比较，不等于 `0` 就把计数器加一并前进一格，读到 `'\0'`（数值 0）立刻停下并返回计数。因为**按字节**走，`int` 数组里的 `0x00` 也会被当成结束符；因为没有缓存，同一串量两次就要数两遍。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
char s[100] = "hello";
size_t len = strlen(s);            /* ① 5，不含 '\0' */
printf("长度：%zu\n", len);          /* ② size_t 用 %zu */

fgets(s, sizeof(s), stdin);         /* ③ 先读入 */
s[strcspn(s, "\n")] = '\0';         /* ④ 先剪换行 */
printf("%zu\n", strlen(s));         /* ⑤ 最后才量 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **`sizeof` 当长度用**：`sizeof(s)` 是容量（100），`strlen(s)` 才是实际长度（5）。
- **写在 `scanf` / `fgets` 之前**：那时数组里还是垃圾值，量出来毫无意义——**必须先读入再量**。
- **传 `NULL`**：直接崩溃，用前先判空。
- **`int` 数组当字符串**：每格 4 字节，紧跟的 `0x00` 会被当成结束符，永远算出 1。
- **返回 `size_t`（无符号）**：`strlen(s) - 1` 在空串时变成天文数字；和 `int` 比较会有警告（C4018）。
- **没有 `'\0'` 的数组**：会一路读出去，直到碰巧遇到 0 才停。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **`sizeof` 和 `strlen` 有什么本质区别？** `sizeof` 是编译期算的**容量**（含 `'\0'`）；`strlen` 是运行期数的**实际长度**。数组传进函数后 `sizeof` 只剩指针大小，`strlen` 仍然正常工作。
- **为什么返回值不用 `int`？** 长度不可能为负，用无符号的 `size_t` 语义更准，也方便处理超大字符串。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：`str` + `len` = **string length**，"数到句号为止"。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`strcpy` —— 复制字符串</span> <a id="fn-strcpy"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：把源字符串**连 `'\0'` 一起**搬到目标数组。

<span style="color:#5F7F63;font-weight:700">原型</span>：`char* strcpy(char* dst, const char* src);`（`#include <string.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`char*` 是**返回类型** → 返回 `dst` 本身，方便链式使用｜`strcpy` 函数名｜`char* dst` 参数 → **目标**（可写、够大）｜`const char* src` 参数 → **源**（只读）

| 项目 | 说明 |
| --- | --- |
| 参数 | `dst` 目标数组；`src` 源字符串 |
| 返回 | 成功：`dst`；没有"失败"返回值 |
| 失败场景 | 目标不够大 → 越界写，不报错但会踩坏内存 |
| 关键点 | **不检查长度**，容量完全由你保证 |

<span style="color:#5F7F63;font-weight:700">原理</span>：一个"赋值式循环"：`dst[i] = src[i]` 逐字节复制，直到把 `'\0'` 也复制过去才停。它不知道 `dst` 有多大，也不知道两块内存是否重叠——所以目标容量必须 ≥ `strlen(src) + 1`，否则直接写穿。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
char dst[20];
strcpy(dst, "hello");              /* ① 目标够大就行 */
printf("%s\n", dst);

char buf[100];
strcpy(buf, "copy_");              /* ② 返回 dst，可以链式 */
strcat(buf, "me");
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **目标空间不足**：`char dst[5]; strcpy(dst, "hello");` 少的那 1 格是 `'\0'`，直接溢出。
- **目标是字符串字面量**：`char* p = "abc"; strcpy(p, "xyz");` 往只读区写，直接崩。
- **目标自己没结束符**：`strcpy` 只认 `src` 的 `'\0'`，不关心 `dst` 原来是什么。
- **重叠复制**：源和目标在同一块内存里重叠，结果未定义，要用 `memmove`。
- **以为它会检查长度**：它和 `gets` 一样"胆子大"，安全版本是 `snprintf(dst, sizeof(dst), "%s", src)`。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **`strcpy(数组, "zhshdd")` 这样可以复制吗？** 可以——字面量是**源**（只读，不用改），数组是**目标**（可写）。危险的是反过来往字面量写。
- **它和 `strncpy` 的区别？** `strcpy` 保证复制 `'\0'`；`strncpy` 在"源不短于 n"时**不补** `'\0'`，要自己补。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**"连句号一起搬"**——少搬了 `'\0'` 就不是字符串了。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`strcmp` —— 比较字符串</span> <a id="fn-strcmp"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：按字典序比较两个字符串，返回"差多少"，**相等返回 0**。

<span style="color:#5F7F63;font-weight:700">原型</span>：`int strcmp(const char* a, const char* b);`（`#include <string.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`int` 是**返回类型** → 负数 / 0 / 正数｜`strcmp` 函数名｜`const char* a`、`const char* b` 两个参数都是**只读**字符串

| 项目 | 说明 |
| --- | --- |
| 参数 | `a`、`b` 两个待比较的字符串 |
| 返回 | `a < b` 返回负数；`==` 返回 **0**；`a > b` 返回正数 |
| 失败场景 | 传 `NULL` 会崩；没有错误码 |
| 比较规则 | 逐字节比 ASCII 码，第一个不同就返回差值 |

<span style="color:#5F7F63;font-weight:700">原理</span>：从第一个字符开始逐字节相减：`a[i] - b[i]`，只要差不为 0 就立刻返回这个差值；如果一路相等，遇到两个 `'\0'` 时返回 0。所以它关心的是"第一个不同点"，而不是长度——`"abc"` 和 `"abd"` 在第三个字符分出胜负。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
if (strcmp(name, "Tom") == 0)      /* ① 判等必须写 == 0 */
    printf("找到 Tom\n");

if (strcmp(a, b) < 0)              /* ② 字典序：a 在前 */
    printf("%s 排在前面\n", a);
```

<span style="color:#B87A5A;font-weight:700">易错点</span>

- **判等写成 `if (strcmp(a, b))`**：相等时返回 0（假），不相等才进分支——**逻辑正好反了**。
- **拿返回值当 0/1**：它返回的是"差值"，可能是 -32 或 7，只保证正负。
- **大小写敏感**：`"Tom"` 和 `"tom"` 不相等；要忽略大小写得先统一转换。
- **比较地址而不是内容**：`if (s1 == s2)` 比的是两个指针，几乎永远不等。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **密码/用户名为什么必须用 `strcmp`？** 因为 `==` 比的是地址，两个不同数组的地址永远不同。
- **只比前 n 个字符怎么办？** 用 `strncmp(a, b, n)`，返回规则完全一样。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**"cmp 返回差，相等才是 0"**——看到 `== 0` 才是"相等"。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`strcat` —— 拼接</span> <a id="fn-strcat"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：把 `src` 接到 `dst` 的**末尾**（覆盖掉 `dst` 原来的 `'\0'`）。

<span style="color:#5F7F63;font-weight:700">原型</span>：`char* strcat(char* dst, const char* src);`（`#include <string.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`char*` 返回 → `dst` 本身｜`strcat` 函数名｜`char* dst` → 目标（可写、且**已有合法字符串**）｜`const char* src` → 追加内容（只读）

| 项目 | 说明 |
| --- | --- |
| 参数 | `dst` 已有字符串；`src` 要接上去的串 |
| 返回 | `dst` 本身 |
| 失败场景 | 目标剩余空间不足 → 越界 |
| 容量要求 | `strlen(dst) + strlen(src) + 1` |

<span style="color:#5F7F63;font-weight:700">原理</span>：分两步走——先用 `strlen` 式的循环**找到 `dst` 末尾的 `'\0'`**，然后从这个位置开始，把 `src` 逐字节（含它自己的 `'\0'`）复制过去。所以 `dst` 必须是**已经初始化好的字符串**，否则它会一路找到野内存里的 0 才停。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
char dst[50] = "hello";            /* ① 必须先有内容 */
strcat(dst, " world");             /* ② dst = "hello world" */
printf("%s\n", dst);

char buf[100] = { 0 };             /* ③ 想从空串开始，先清零 */
strcat(buf, "abc");
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **目标没初始化**：`char dst[50]; strcat(dst, "abc");` 会把 `dst` 里的垃圾当字符串找结尾，写飞。
- **空间算少**：忘了 `'\0'`，少开 1 格就溢出。
- **自己拼自己**：`strcat(s, s)` 是未定义行为（源和目标重叠）。
- **目标是字面量**：往只读区写，直接崩。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **它和 `strncat` 的区别？** `strcat` 不限长度；`strncat(dst, src, n)` 最多追加 `n` 个，且**自动补 `'\0'`**。
- **为什么手写 `my_strcat` 要"两个游标"？** 一个游标先在 `dst` 走到末尾，第二个再从那里接上 `src`。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**cat = 猫尾巴接上去**——先找到尾巴尖（`'\0'`），再接新的。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`strchr` —— 找某个字符（第一次）</span> <a id="fn-strchr"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：在字符串里找某个字符**第一次出现的位置**。

<span style="color:#5F7F63;font-weight:700">原型</span>：`char* strchr(const char* s, int c);`（`#include <string.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`char*` 返回 → 找到返回**地址**，找不到返回 `NULL`｜`strchr` 函数名｜`const char* s` → 源串（只读）｜`int c` → 要找的字符（用 `int` 是为了能传 `EOF`）

| 项目 | 说明 |
| --- | --- |
| 参数 | `s` 源字符串；`c` 要找的字符（`'a'` 或 97 都行） |
| 返回 | 首次出现的**地址**；找不到返回 `NULL` |
| 失败场景 | 找 `'\0'` 会返回指向结束符的地址（合法） |
| 求下标 | `p - s` 得到位置 |

<span style="color:#5F7F63;font-weight:700">原理</span>：从 `s[0]` 起逐字节和 `c` 比较，命中就返回当前地址；走到 `'\0'` 还没命中则返回 `NULL`。注意它**返回的是指针不是下标**，所以要用 `p - s` 换算成位置，或者直接用指针继续往下走。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
char s[] = "hello world";
char* p = strchr(s, 'o');          /* ① 找到第一个 o */
if (p != NULL)                     /* ② 必须先判空 */
    printf("下标 = %d\n", (int)(p - s));   /* ③ 指针相减得下标 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **不判空就用**：找不到返回 `NULL`，直接 `*p` 会崩。
- **把返回值当字符**：它返回的是**地址**，想取值要 `*p`。
- **想找最后一次却用了它**：找最后一个用 `strrchr`。
- **拿返回值和字符比较**：`if (strchr(s, 'o') == 'o')` 类型都不对。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **它和 `strstr` 的区别？** `strchr` 找**单个字符**，`strstr` 找**子串**。
- **怎么找某个字符出现的所有位置？** 循环：找到后 `p = strchr(p + 1, c)`，直到 `NULL`。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：`chr` = character，"找字符"，返回的是**门牌号**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`strrchr` —— 找某个字符（最后一次）</span> <a id="fn-strrchr"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：和 `strchr` 一样，但找的是**最后一次**出现的位置。

<span style="color:#5F7F63;font-weight:700">原型</span>：`char* strrchr(const char* s, int c);`（`#include <string.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`char*` 返回 → 地址或 `NULL`｜`strrchr` 函数名（`r` = reverse，从后往前）｜`const char* s` → 源串｜`int c` → 目标字符

| 项目 | 说明 |
| --- | --- |
| 参数 | 同 `strchr` |
| 返回 | **最后**一次出现的地址；找不到 `NULL` |
| 典型用途 | 找路径里的最后一个 `/` 或 `.`（取文件名、扩展名） |

<span style="color:#5F7F63;font-weight:700">原理</span>：内部先走到字符串末尾，再从后往前找（或记录"最近一次命中"），所以拿到的是最后那个。其余行为与 `strchr` 一致：返回地址、找不到返回 `NULL`。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
char path[] = "dir/sub/file.txt";
char* dot = strrchr(path, '.');    /* ① 找最后一个点 */
if (dot != NULL) printf("扩展名：%s\n", dot + 1);   /* ② txt */
char* slash = strrchr(path, '/');  /* ③ 最后一个斜杠 → 文件名 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **同样要判空**：没有该字符时返回 `NULL`。
- **和 `strchr` 混用**：找第一个用 `strchr`，找最后一个用 `strrchr`（多一个 `r`）。
- **返回地址不是下标**：同样要 `p - s` 换算。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **`r` 是什么意思？** reverse——从右往左找，所以是"最后一个"。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`strchr` 多一个 `r`，就是"反着找"**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`strstr` —— 找子串</span> <a id="fn-strstr"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：在一个字符串里找**另一个字符串**第一次出现的位置。

<span style="color:#5F7F63;font-weight:700">原型</span>：`char* strstr(const char* s, const char* sub);`（`#include <string.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`char*` 返回 → 子串首次出现的**首地址**，找不到 `NULL`｜`strstr` 函数名｜`const char* s` → 主串（只读）｜`const char* sub` → 要找的子串（只读）

| 项目 | 说明 |
| --- | --- |
| 参数 | `s` 主串；`sub` 子串（空串会直接返回 `s`） |
| 返回 | 子串首地址；找不到 `NULL` |
| 失败场景 | 参数 `NULL` 崩；找不到返回 `NULL` |
| 求下标 | `p - s` |

<span style="color:#5F7F63;font-weight:700">原理</span>：对 `s` 的每个位置都尝试"从这里开始能不能匹配整个 `sub`"，能就返回这个起点，不能就把起点后移一格重试。本质是两层循环（外层起点、内层逐字符比对），所以最坏是 `O(n*m)`。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
char s[] = "a cat and a cat";
char* p = strstr(s, "cat");        /* ① 第一次出现的地址 */
while (p != NULL) {                /* ② 循环找所有 */
    printf("下标 %d\n", (int)(p - s));
    p = strstr(p + 1, "cat");
}
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **不判空**：找不到返回 `NULL`，紧接着 `*p` 就崩。
- **循环里不推进指针**：写成 `p = strstr(p, sub)` 会原地死循环，要 `p + 1`。
- **分不清地址和下标**：要位置得 `p - s`。
- **大小写敏感**：`"Cat"` 和 `"cat"` 不算匹配。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **它和 `strchr` 的区别？** 一个找子串、一个找单字符；返回值规则一样（地址或 `NULL`）。
- **为什么循环替换要用它 + `strncmp`？** 先 `strstr` 定位，再判断从该位置起是否匹配模式串，最后决定"等长覆盖"还是"另开缓冲"。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：`strstr` = **string in string**，"串里找串"。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`strncpy` —— 限长复制</span> <a id="fn-strncpy"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：最多复制 `n` 个字符，但**可能不给你补 `'\0'`**。

<span style="color:#5F7F63;font-weight:700">原型</span>：`char* strncpy(char* dst, const char* src, size_t n);`（`#include <string.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`char*` 返回 → `dst`｜`strncpy` 函数名｜`char* dst` → 目标｜`const char* src` → 源｜`size_t n` → **最多复制几个字符**

| 项目 | 说明 |
| --- | --- |
| 参数 | `dst` 目标；`src` 源；`n` 上限 |
| 返回 | `dst` |
| 源比 n 短 | 剩余位置用 `0` 补满 |
| 源 ≥ n | **不补 `'\0'`**，目标可能不是合法字符串 |
| 关键点 | 想安全，必须自己 `dst[n] = '\0';` |

<span style="color:#5F7F63;font-weight:700">原理</span>：逐字节复制，最多复制 `n` 个。如果 `src` 在 `n` 之前就结束了，它会把剩下的位置**全部填 0**（填满 `n` 个）；如果 `src` 长度 ≥ `n`，复制满 `n` 个就停——此时根本没有地方放 `'\0'`，目标末尾是"截断的半截字符串"。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
char dst[10];
strncpy(dst, "abcdefghijk", 9);    /* ① 源比 n 长 */
dst[9] = '\0';                      /* ② 必须自己补结束符 */
printf("%s\n", dst);                /* abcdefghi */

strncpy(dst, "abc", 9);             /* ③ 源短：后面补满 0，天然有 '\0' */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **源≥n 时忘补 `'\0'`**：`printf("%s")` 会一直打印到野内存里的 0。
- **`n` 写成源长度**：`strncpy(dst, src, strlen(src))` 恰好不复制 `'\0'`。
- **以为它会自动加结束符**：它只在"源短于 n"时才顺带补 0。
- **`n` 超过目标容量**：照样溢出，它不检查 `dst` 大小。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **它和 `snprintf` 的区别？** `snprintf` **一定**补 `'\0'`；`strncpy` 不一定，所以更推荐 `snprintf(dst, sizeof(dst), "%s", src)`。
- **为什么说它"半安全"？** 它防住了"写超 n"，但没保证结果是合法字符串。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`n` 是刹车，不是"保证有句号"**——停得太急就没了结尾。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`strncat` —— 限长追加</span> <a id="fn-strncat"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：最多再追加 `n` 个字符，**并且一定补 `'\0'`**。

<span style="color:#5F7F63;font-weight:700">原型</span>：`char* strncat(char* dst, const char* src, size_t n);`（`#include <string.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`char*` 返回 → `dst`｜`strncat` 函数名｜`char* dst` → 目标（已有字符串）｜`const char* src` → 追加内容｜`size_t n` → **最多再追加几个字符**

| 项目 | 说明 |
| --- | --- |
| 参数 | `n` 是"再追加几个"，**不是总长度** |
| 返回 | `dst` |
| 容量要求 | `strlen(dst) + n + 1` |
| 关键点 | **一定**在末尾补 `'\0'`（比 `strncpy` 友好） |

<span style="color:#5F7F63;font-weight:700">原理</span>：先走到 `dst` 的 `'\0'`，然后从 `src` 开头最多复制 `n` 个字符，复制完**无条件补一个 `'\0'`**。所以它最多只动 `n+1` 个字节（追加内容 + 结束符），目标需要预留 `strlen(dst) + n + 1`。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
char dst[20] = "hello";
strncat(dst, " world!!!", 6);      /* ① 只接 " world" 6 个 */
printf("%s\n", dst);                /* hello world，自动补 '\0' */

strncat(dst, "xyz", 3);             /* ② 接满 3 个也 OK */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **把 `n` 当总长度**：它是"**再**追加几个"，不是"目标总长"。
- **容量算少**：`strlen(dst) + n + 1`，少算 1 就溢出。
- **目标是未初始化数组**：和 `strcat` 一样，会从野内存里找 `'\0'`。
- **以为它和 `strncpy` 一样不补结束符**：**恰恰相反**，它一定补。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **`strncat` 的 `n` 是"最多追加几个"还是"总长最多多少"？** 是**最多再追加几个**；`strncat(dst, src, 3)` = 从 `src` 取最多 3 个接到 `dst` 末尾。
- **它和 `strncpy` 的关键差别？** `strncpy` 可能不补 `'\0'`，`strncat` 一定补。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`n` 管"接几个"，句号它自己补**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`strncmp` —— 只比前 n 个</span> <a id="fn-strncmp"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：只比较两个字符串的**前 `n` 个字符**，返回规则和 `strcmp` 一样。

<span style="color:#5F7F63;font-weight:700">原型</span>：`int strncmp(const char* a, const char* b, size_t n);`（`#include <string.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`int` 返回 → 负 / 0 / 正｜`strncmp` 函数名｜`const char* a`、`const char* b` → 待比较的两个串｜`size_t n` → 最多比几个字符

| 项目 | 说明 |
| --- | --- |
| 参数 | `a`、`b` 两个串；`n` 比较长度上限 |
| 返回 | 负数 / **0（前 n 个相等）** / 正数 |
| 提前结束 | 任一个提前遇到 `'\0'` 也会停 |
| 典型用途 | 判断"是不是以某前缀开头" |

<span style="color:#5F7F63;font-weight:700">原理</span>：和 `strcmp` 相同的逐字节相减，只是多了一个计数器：比满 `n` 个就停，返回 0；或者中途遇到 `'\0'` 或不同字符，提前返回差值。所以它是"只看前 `n` 个字符"的局部比较。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
if (strncmp(s, "abc", 3) == 0)     /* ① 判断前缀 */
    printf("以 abc 开头\n");

if (strncmp(line, "#", 1) == 0)    /* ② 判断是不是注释行 */
    printf("注释：%s\n", line);
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **判等仍要 `== 0`**：返回值不是 0/1。
- **`n` 超过短串长度**：会在 `'\0'` 处提前结束，不会越界读。
- **用 `strcmp` 判前缀**：长度不同会立刻不等，必须用 `strncmp`。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **为什么替换句子时必须用 `strncmp`？** 因为要判断"从这个位置开始的前 3 个字符是不是 cat"，`strcmp` 会连后面整句一起比，必然不等。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`n` 是"只比到第几个"**，前缀判断专用。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`strtok` —— 按分隔符切分</span> <a id="fn-strtok"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：按分隔符把字符串切成一个个"词"，每次调用返回一个词。

<span style="color:#5F7F63;font-weight:700">原型</span>：`char* strtok(char* s, const char* delim);`（`#include <string.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`char*` 返回 → 下一个词的**首地址**，没有了返回 `NULL`｜`strtok` 函数名｜`char* s` → **第一次传原串，之后传 `NULL`**｜`const char* delim` → 分隔符**集合**（每个字符都算分隔符）

| 项目 | 说明 |
| --- | --- |
| 参数 | 第一次 `s` 传原串，后续传 `NULL`；`delim` 是字符集合 |
| 返回 | 下一个词；切完返回 `NULL` |
| 副作用 | **会把原串里的分隔符改写成 `'\0'`** |
| 失败场景 | 传 `NULL` 结束；不可重入（内部有静态指针） |

<span style="color:#5F7F63;font-weight:700">原理</span>：它内部用一个**静态指针记住上次切到哪**。每次调用：跳过开头的分隔符 → 记住这段的起点 → 一路走到下一个分隔符，并把它**改写成 `'\0'`**（这样这段就成独立字符串）→ 返回起点。所以原串会被"打碎"，且第二次起必须传 `NULL` 让它接着上次的位置。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
char line[] = "Tom,90,abc";        /* ① 必须可写 */
char copy[100];
strcpy(copy, line);                 /* ② 想留原串就先复制 */

char* w = strtok(copy, ",");        /* ③ 第一次传副本 */
while (w != NULL) {                 /* ④ 循环里先算后用 */
    printf("[%s]\n", w);
    w = strtok(NULL, ",");          /* ⑤ 之后传 NULL */
}
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **传只读字面量**：`strtok("a,b", ",")` 会崩（它要改内容）。
- **循环里写成 `char* w = strtok(...)`**：变量重复声明，编译错。
- **第二次还传原串**：会从头再切一遍，死循环。
- **分隔符理解成"整个字符串"**：`" ,"` 表示空格和逗号**任意一个**都算分隔，不是"空格逗号"这个整体。
- **多线程/嵌套使用**：内部静态指针会互相干扰。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **为什么它要传副本？** 因为它把分隔符改写成 `'\0'`，直接切原串。
- **`strstr` 和它怎么分工？** `strstr` 找子串（不改原串），`strtok` 按字符集合切词（改原串）。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`tok` = token，"切一次给你一个词"**，第一次给原串、以后给 `NULL`。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`strspn` —— 开头连续"属于某集合"的长度</span> <a id="fn-strspn"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：从开头数，**连续有多少个字符属于给定集合**。

<span style="color:#5F7F63;font-weight:700">原型</span>：`size_t strspn(const char* s, const char* set);`（`#include <string.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`size_t` 返回 → 连续的个数｜`strspn` 函数名｜`const char* s` → 源串｜`const char* set` → **字符集合**（不是子串）

| 项目 | 说明 |
| --- | --- |
| 参数 | `s` 源串；`set` 允许的字符集合 |
| 返回 | 开头连续属于 `set` 的字符个数 |
| 中途遇不属于 | 立刻停，返回已数到的个数 |
| 典型用途 | 跳过前缀（如跳过所有空格） |

<span style="color:#5F7F63;font-weight:700">原理</span>：从 `s[0]` 开始，每个字符都去 `set` 里查一遍"在不在里面"，在就计数加一继续，不在就停。它只数**开头那一段**，中间断开就结束。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
char s[] = "aaabbbccc";
int k = strspn(s, "ab");           /* ① 'a','a','a','b' 都属于 → 4 */
printf("%d\n", k);

char* p = s + strspn(s, " ");      /* ② 跳过开头的空格 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **以为它数"某个子串出现几次"**：它数的是**开头连续**的字符数。
- **`set` 传成子串**：`set` 是"字符的集合"，顺序无关、重复无所谓。
- **返回 `size_t`**：打印用 `%zu`。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **它和 `strcspn` 什么关系？** 一个数"属于"的长度，一个数"不属于"的长度，互为反义。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：`spn` = span（跨度），**"符合的连续跨度"**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`strcspn` —— 开头连续"不属于某集合"的长度</span> <a id="fn-strcspn"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：从开头数，**连续有多少个字符不属于给定集合**——剪换行神器。

<span style="color:#5F7F63;font-weight:700">原型</span>：`size_t strcspn(const char* s, const char* set);`（`#include <string.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`size_t` 返回 → 连续的个数｜`strcspn` 函数名（`c` = complement，补集）｜`const char* s` → 源串｜`const char* set` → **禁止出现的字符集合**

| 项目 | 说明 |
| --- | --- |
| 参数 | `s` 源串；`set` 遇到即停的字符集合 |
| 返回 | 开头连续**不属于** `set` 的字符个数 |
| 找不到 | 返回 `strlen(s)`（天然安全） |
| 典型用途 | `line[strcspn(line, "\n")] = '\0';` |

<span style="color:#5F7F63;font-weight:700">原理</span>：从 `s[0]` 开始逐字符检查"在不在 `set` 里"，**不在**就计数加一继续，一旦**在**就立刻停。所以它正好给出"第一个分隔符之前的长度"——剪换行就是利用这个位置直接写 `'\0'`。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
char line[100];
fgets(line, sizeof(line), stdin);
line[strcspn(line, "\n")] = '\0';   /* ① 找到换行的位置，直接改成 '\0' */

size_t n = strcspn(s, "abc");       /* ② 数"到第一个 a/b/c 之前的长度" */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **`c` 的意思记反**：它是 **c**omplement（补集），数的是"不属于"。
- **集合写单引号**：`strcspn(s, '\n')` 类型不对，要写 `"\n"`。
- **以为没找到会出错**：没找到返回 `strlen(s)`，这个位置正好是 `'\0'`，赋值天然安全。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **`strcspn` 名字怎么记？** `c` = complement（补集）——数"连续**不属于**集合"的字符个数；所以 `strcspn(line, "\n")` 正好是这一行的长度。
- **它和 `strlen` 的关系？** 没有换行时两者相等；有换行时它少 1（不含换行）。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`c` 就是"反过来"**——`strspn` 数属于，`strcspn` 数不属于。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`memcpy` —— 按字节复制（不管重叠）</span> <a id="fn-memcpy"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：把一块内存的 `n` 个**字节**原样搬到另一块。

<span style="color:#5F7F63;font-weight:700">原型</span>：`void* memcpy(void* dst, const void* src, size_t n);`（`#include <string.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`void*` 返回 → 返回 `dst`（"万能指针"，用时强转）｜`memcpy` 函数名｜`void* dst` → 目标内存｜`const void* src` → 源内存（只读）｜`size_t n` → **字节数**

| 项目 | 说明 |
| --- | --- |
| 参数 | `dst` 目标；`src` 源；`n` **字节数**（不是元素个数） |
| 返回 | `dst` |
| 失败场景 | 目标不够大 → 越界；**重叠 → 结果错误** |
| 关键点 | 与类型无关，纯字节搬运 |

<span style="color:#5F7F63;font-weight:700">原理</span>：内部把两个指针都转成 `unsigned char*`，然后逐字节 `*d++ = *s++`，重复 `n` 次。它**不判断两块内存是否重叠**：如果目标起点落在源的范围内，前面写进去的字节可能已经把"还没搬的源数据"覆盖了，于是复制出错——这种场合必须用 `memmove`。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
int a[5] = { 1, 2, 3, 4, 5 };
int b[5];
memcpy(b, a, sizeof(a));           /* ① 第三个参数是字节数 */
printf("%d\n", b[4]);              /* 5 */

struct Stu s1 = { "Tom", 90 }, s2;
memcpy(&s2, &s1, sizeof(struct Stu));   /* ② 结构体整块复制 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **`n` 写成元素个数**：复制 `int` 数组要 `n * sizeof(int)`。
- **重叠时用它**：结果未定义，必须 `memmove`。
- **跨类型副本想当然**：`int` 和 `float` 的字节布局不同，读出来是"按位重解释"。
- **返回值不用就丢**：它返回 `dst`，可以链式。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **它和 `strcpy` 的区别？** `strcpy` 只认字符串（抄到 `'\0'` 停）；`memcpy` 不管内容，按字节抄固定长度。
- **`void*` 为什么不能直接 `+1`？** 因为不知道一步多大，必须先转成 `char*`。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：`mem` + `cpy` = **memory copy**，认字节不认类型。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`memmove` —— 按字节复制（处理重叠）</span> <a id="fn-memmove"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：和 `memcpy` 一样按字节搬，但**源和目标重叠也安全**。

<span style="color:#5F7F63;font-weight:700">原型</span>：`void* memmove(void* dst, const void* src, size_t n);`（`#include <string.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`void*` 返回 → `dst`｜`memmove` 函数名（`move` 比 `copy` 多一层"考虑位置关系"）｜参数含义同 `memcpy`

| 项目 | 说明 |
| --- | --- |
| 参数 | 同 `memcpy`（`n` 仍是字节数） |
| 返回 | `dst` |
| 关键点 | 先比较两个地址，决定正着搬还是倒着搬 |
| 代价 | 比 `memcpy` 多一次判断，速度略慢 |

<span style="color:#5F7F63;font-weight:700">原理</span>：它先判断"目标在源的哪一侧"：如果目标在源**前面**，正着搬不会覆盖未搬数据，就正着来；如果目标在源**后面**且两块重叠，就**从尾部倒着搬**——这样被覆盖的永远是"已经搬完的部分"，结果正确。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
char s[20] = "abcdef";
memmove(s + 2, s, 4);              /* ① 源和目标重叠，仍然正确 */
printf("%s\n", s);                  /* ababcd */

/* 在数组中间删一个元素，也是重叠搬移 */
memmove(&a[i], &a[i + 1], (n - i - 1) * sizeof(int));
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **以为它和 `memcpy` 完全一样**：`n` 的含义相同，但重叠行为不同。
- **`n` 又写成元素个数**：同样要乘 `sizeof`。
- **误以为它总会倒着搬**：只在需要时才倒序，正常情况仍正序。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **手写 `my_memmove` 的关键是什么？** 转 `unsigned char*` 逐字节走，**先判断 `dst` 是否落在源区间内**，在就倒序。
- **什么时候必须用它？** 同一数组内前移/后移（删元素、插元素、右移字符串）。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`move` 会看方向**，重叠也不怕。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`memcmp` —— 逐字节比较</span> <a id="fn-memcmp"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：把两块内存的前 `n` 个**字节**逐一比较。

<span style="color:#5F7F63;font-weight:700">原型</span>：`int memcmp(const void* a, const void* b, size_t n);`（`#include <string.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`int` 返回 → 负 / 0 / 正｜`memcmp` 函数名｜`const void* a`、`const void* b` → 两块内存（只读）｜`size_t n` → **比较多少字节**

| 项目 | 说明 |
| --- | --- |
| 参数 | `a`、`b` 两块内存；`n` 字节数 |
| 返回 | 第一个不同字节的差值；全同返回 0 |
| 与 `strcmp` 区别 | **遇 `'\0'` 不停**，比满 n 个 |
| 典型用途 | 判断"是否完全相同" |

<span style="color:#5F7F63;font-weight:700">原理</span>：转成 `unsigned char*` 后逐字节相减，第一个不为 0 的差值直接返回；`n` 个字节全相等则返回 0。它**不把 `'\0'` 当结束符**——这正是它和 `strcmp` 最本质的区别。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
int a[3] = { 1, 2, 3 }, b[3] = { 1, 2, 4 };
if (memcmp(a, b, sizeof(a)) != 0)  /* ① n 是字节数 */
    printf("不相同\n");

char s1[8] = "abc", s2[8] = "abc";
printf("%d\n", memcmp(s1, s2, 8)); /* ② 0：含后面的 0 也一致 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **拿它比字符串**：`memcmp` 会把 `'\0'` 之后的垃圾也一起比，结果不稳定。
- **只是判等却依赖具体差值**：只保证正负，不保证数值。
- **`n` 写成元素个数**：又要乘 `sizeof`。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **它和 `strcmp` 怎么选？** 比字符串（到 `'\0'` 停）用 `strcmp`；比"一整块二进制"用 `memcmp`。
- **为什么结构体比较用它？** 因为结构体里有填充字节，`strcmp` 会提前停。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`mem` 开头 = 看字节，不看句号**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`memset` —— 按字节设值</span> <a id="fn-memset"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：把一块内存的每个**字节**都设成同一个值。

<span style="color:#5F7F63;font-weight:700">原型</span>：`void* memset(void* dst, int value, size_t n);`（`#include <string.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`void*` 返回 → `dst`｜`memset` 函数名｜`void* dst` → 目标内存｜`int value` → 要设的值（**只用低 8 位**）｜`size_t n` → 字节数

| 项目 | 说明 |
| --- | --- |
| 参数 | `dst` 目标；`value` 按字节写入；`n` 字节数 |
| 返回 | `dst` |
| 安全值 | 只有 `0` 和 `-1`（每个字节都一样） |
| 危险 | 对 `int` 数组设非整字节值会得到奇怪结果 |

<span style="color:#5F7F63;font-weight:700">原理</span>：把 `value` **截断成一个字节**，然后对 `dst` 开头 `n` 个字节逐个写入。它完全不理解类型——对 `int` 数组，四个字节都会被写成同一个值，所以 `memset(a, 1, ...)` 得到的是 `0x01010101`（16843009），而不是 1。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
int a[100];
memset(a, 0, sizeof(a));           /* ① 全部清零：最常用 */
char s[50];
memset(s, 0, sizeof(s));           /* ② 字符数组清空 */
struct Stu st;
memset(&st, 0, sizeof(st));        /* ③ 结构体清零 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **拿它给 `int` 数组设 1**：每个元素变成 `0x01010101`，不是 1。
- **`n` 写成元素个数**：必须乘 `sizeof`。
- **以为它能设浮点数**：浮点 0.0 的字节不是全 0，`memset` 不行，要逐个赋值。
- **只清一部分**：`sizeof(a)` 才是整块，`n` 才对。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **为什么只有 0 和 -1 安全？** 因为它们的每个字节都相同（`0x00` 或 `0xFF`），按字节写不会破坏结构。
- **它和 `calloc` 的区别？** `calloc` 申请新内存并清零；`memset` 清已有内存。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**逐字节刷墙**——只有"每层都一样"的颜色才刷得对。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`strerror` —— 错误码翻译成人话</span> <a id="fn-strerror"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：把错误码（通常是 `errno`）翻译成一句英文说明。

<span style="color:#5F7F63;font-weight:700">原型</span>：`char* strerror(int errnum);`（`#include <string.h>`，常配 `#include <errno.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`char*` 返回 → 指向**静态缓冲区**的说明字符串（不用也不能 `free`）｜`strerror` 函数名｜`int errnum` → 错误码，通常直接传 `errno`

| 项目 | 说明 |
| --- | --- |
| 参数 | `errnum` 错误码（`errno`） |
| 返回 | 指向描述字符串的指针（静态，可能被后续调用覆盖） |
| 失败场景 | 未知错误码返回 "Unknown error" |
| 关键点 | **只翻译，不打印** |

<span style="color:#5F7F63;font-weight:700">原理</span>：拿错误码去一张内置表里查对应的英文描述，返回指向表内字符串的指针。因为是静态（或线程局部）缓冲区，**下次调用可能覆盖**上一次的结果，所以要么马上用，要么先复制走。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
#include <errno.h>
FILE* fp = fopen("no.txt", "r");
if (fp == NULL) {
    printf("打开失败：%s\n", strerror(errno));   /* ① 立刻用 */
    return 1;
}
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **`free` 它**：返回的是静态缓冲区，不能释放。
- **存下来晚点用**：中途再调别的库函数，内容可能已被覆盖。
- **和 `perror` 混**：`perror` 直接打印到 stderr；`strerror` 只返回字符串。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **它和 `perror` 怎么选？** 想自己排版（比如拼进 `printf`）用 `strerror`；想一句话打出来用 `perror`。
- **`errno` 是什么？** 全局错误码，库函数失败时自动设置；它不会自动清零，所以要在失败后**立刻**读。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`str` + `error` = "把错误变成字符串"**。

## <span style="color:#7FA182">3. math.h —— 数学家族</span> <a id="sec56"></a>

> 使用前 `#include <math.h>`；返回值都是 double。

| 函数 | 原型（参数与返回都是 double） | 掌握 |
| --- | --- | --- |
| [`sqrt`](#fn-sqrt) | `double sqrt(double x);` | ✅ |
| [`pow`](#fn-pow) | `double pow(double x, double y);` | ⚪ |
| [`fabs`](#fn-fabs) | `double fabs(double x);` | ⚪ |
| [`ceil`](#fn-ceil) | `double ceil(double x);` | ⚪ |
| [`floor`](#fn-floor) | `double floor(double x);` | ⚪ |
| [`round`](#fn-round) | `double round(double x);` | ⬜ |
| [`trunc`](#fn-trunc) | `double trunc(double x);` | ⬜ |
| [`fmod`](#fn-fmod) | `double fmod(double x, double y);` | ⬜ |
| [`fmin`](#fn-fmin) | `double fmin(double x, double y);` | ⬜ |
| [`fmax`](#fn-fmax) | `double fmax(double x, double y);` | ⬜ |
| [`exp`](#fn-exp) | `double exp(double x);` | ⬜ |
| [`log`](#fn-log) | `double log(double x);` | ⬜ |
| `log10` | `double log10(double x);` | ⬜ |

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`sqrt` —— 平方根</span> <a id="fn-sqrt"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：求一个数的平方根。

<span style="color:#5F7F63;font-weight:700">原型</span>：`double sqrt(double x);`（`#include <math.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`double` 返回 → 平方根（浮点）｜`sqrt` 函数名｜`double x` 参数 → 被开方数

| 项目 | 说明 |
| --- | --- |
| 参数 | `x` 非负数 |
| 返回 | 平方根；`x < 0` 返回 **NaN** |
| 失败场景 | 负数、`-0.0` 边界 |
| 关键点 | 判素数时用 `i * i <= n` 比 `sqrt` 更稳 |

<span style="color:#5F7F63;font-weight:700">原理</span>：用牛顿迭代或硬件指令求浮点平方根，返回近似值。因为结果是浮点，取整时可能有 1 的误差（`sqrt(25)` 理论上 5，`(int)` 强转前要加 0.5）。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
printf("%.2f\n", sqrt(16.0));      /* ① 4.00 */
int r = (int)(sqrt(n) + 0.5);       /* ② 要整数结果就四舍五入 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **传整数不加 `.0`**：`sqrt(16)` 虽然会自动转换，但写 `16.0` 更清楚。
- **对负数求**：返回 NaN，后续比较全为假。
- **直接 `(int)sqrt(n)`**：可能因浮点误差少 1，加 `0.5` 再转。
- **忘了链接数学库**：gcc 命令行要加 `-lm`。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **判素数为什么推荐 `i * i <= n`？** 避免浮点误差，也不用引入 `math.h`。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：`sqrt` = square root，**"开方"**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`pow` —— 求幂</span> <a id="fn-pow"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：算 `x` 的 `y` 次方。

<span style="color:#5F7F63;font-weight:700">原型</span>：`double pow(double x, double y);`（`#include <math.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`double` 返回 → 幂值｜`pow` 函数名｜`double x` 底数｜`double y` 指数（可以是小数）

| 项目 | 说明 |
| --- | --- |
| 参数 | 底数、指数 |
| 返回 | `x^y` |
| 失败场景 | 负底数配非整数指数 → NaN |
| 关键点 | 整数幂用循环更快更准 |

<span style="color:#5F7F63;font-weight:700">原理</span>：通过 `exp(y * log(x))` 或专用算法计算；指数可以是任意实数，所以支持"开任意次方"。缺点是浮点误差，整数结果不精确。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
printf("%.0f\n", pow(2, 10));      /* ① 1024 */
double r = pow(x, 0.5);            /* ② 等同于开方 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **拿它算整数幂**：`pow(2,10)` 可能得到 1023.9999，强转就变 1023。
- **以为它返回 `int`**：返回 `double`，打印用 `%f`。
- **底数为负 + 小数指数**：结果 NaN。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **整数次幂怎么写更好？** 循环累乘（或快速幂），避免浮点误差。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`pow` = power，"几次方"**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`fabs` —— 浮点绝对值</span> <a id="fn-fabs"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：取浮点数的绝对值（`abs` 的浮点版）。

<span style="color:#5F7F63;font-weight:700">原型</span>：`double fabs(double x);`（`#include <math.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`double` 返回 → 绝对值｜`fabs` 函数名（f = float）｜`double x` → 任意浮点数

| 项目 | 说明 |
| --- | --- |
| 参数 | 任意 `double` |
| 返回 | 绝对值（非负） |
| 失败场景 | 无 |
| 关键点 | 比 `abs` 多处理小数部分 |

<span style="color:#5F7F63;font-weight:700">原理</span>：直接把 IEEE 754 浮点的**符号位清零**，所以又快又精确，不会引入误差。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
double d = fabs(-3.14);            /* ① 3.14 */
if (fabs(a - b) < 1e-6)            /* ② 浮点判等标准写法 */
    puts("相等");
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **浮点用 `abs`**：会截断成整数，结果错。
- **浮点直接用 `==` 比较**：应该用 `fabs(a-b) < 1e-6`。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **为什么浮点不能直接判等？** 0.1 + 0.2 不等于 0.3，有舍入误差。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`f` = float，浮点专用绝对值**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`ceil` —— 向上取整</span> <a id="fn-ceil"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：向上取整（天花板），返回不小于 `x` 的最小整数。

<span style="color:#5F7F63;font-weight:700">原型</span>：`double ceil(double x);`（`#include <math.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`double` 返回 → 取整后的浮点值｜`ceil` 函数名（ceiling）｜`double x` → 任意浮点

| 项目 | 说明 |
| --- | --- |
| 参数 | 任意 `double` |
| 返回 | 向上取整的**浮点**结果 |
| 失败场景 | 无 |
| 关键点 | 返回仍是 `double`，要整数得强转 |

<span style="color:#5F7F63;font-weight:700">原理</span>：把小数部分直接"进位"——正数舍去小数后加 1（除非本来就是整数），负数舍去小数后保持。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
printf("%.0f\n", ceil(2.1));       /* ① 3 */
printf("%.0f\n", ceil(-2.1));      /* ② -2 */
int n = (int)ceil(7.0 / 2);        /* ③ 向上取整求"需要几页" */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **以为返回 `int`**：返回 `double`，打印要用 `%f`。
- **和 `floor` 记反**：`ceil` 向上、`floor` 向下。
- **负数时想当然**：`ceil(-2.1)` 是 -2（往"大"的方向）。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **"向上取整"和"四舍五入"一样吗？** 不一样，`ceil(2.1)=3`，`round(2.1)=2`。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`ceil` = ceiling = 天花板**，往上顶。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`floor` —— 向下取整</span> <a id="fn-floor"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：向下取整（地板），返回不大于 `x` 的最大整数。

<span style="color:#5F7F63;font-weight:700">原型</span>：`double floor(double x);`（`#include <math.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`double` 返回 → 取整结果｜`floor` 函数名｜`double x` → 任意浮点

| 项目 | 说明 |
| --- | --- |
| 参数 | 任意 `double` |
| 返回 | 向下取整的浮点结果 |
| 失败场景 | 无 |
| 关键点 | 正数时等价于"截断小数" |

<span style="color:#5F7F63;font-weight:700">原理</span>：把小数部分舍去、往小的方向取——正数直接截断，负数还要再减 1。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
printf("%.0f\n", floor(2.9));      /* ① 2 */
printf("%.0f\n", floor(-2.1));     /* ② -3 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **负数时按"截断"理解**：`floor(-2.1)` 是 -3，不是 -2。
- **返回类型当 int 用**：仍是 `double`。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **它和 `(int)` 强转的区别？** 正数一样；负数时 `(int)-2.1` 是 -2，`floor(-2.1)` 是 -3。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`floor` = 地板**，往下踩。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`round` —— 四舍五入</span> <a id="fn-round"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：四舍五入到最近的整数（.5 远离 0）。

<span style="color:#5F7F63;font-weight:700">原型</span>：`double round(double x);`（`#include <math.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`double` 返回 → 取整结果｜`round` 函数名｜`double x` → 任意浮点

| 项目 | 说明 |
| --- | --- |
| 参数 | 任意 `double` |
| 返回 | 四舍五入后的浮点值 |
| 失败场景 | 无 |
| 关键点 | 0.5 时"远离 0"：2.5 → 3，-2.5 → -3 |

<span style="color:#5F7F63;font-weight:700">原理</span>：看小数部分是否 ≥ 0.5，是就向远离 0 的方向进 1，否则舍去。和"银行家舍入"（.5 取偶）不同，这里是传统四舍五入。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
printf("%.0f\n", round(2.4));      /* ① 2 */
printf("%.0f\n", round(2.5));      /* ② 3 */
int n = (int)round(x);              /* ③ 转整数 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **以为 `printf("%.0f")` 就是四舍五入**：显示层面确实会舍入，但变量本身没变。
- **和 `ceil`/`floor` 混**：只有 `round` 看小数位。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **没有 `round` 时怎么写？** `(int)(x + 0.5)`（只对正数成立）。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`round` = 圆整**，四舍五入。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`trunc` —— 截断小数</span> <a id="fn-trunc"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：直接砍掉小数部分，**不四舍五入**。

<span style="color:#5F7F63;font-weight:700">原型</span>：`double trunc(double x);`（`#include <math.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`double` 返回 → 截断结果｜`trunc` 函数名（truncate）｜`double x` → 任意浮点

| 项目 | 说明 |
| --- | --- |
| 参数 | 任意 `double` |
| 返回 | 朝 0 方向截断的结果 |
| 失败场景 | 无 |
| 关键点 | 正负都朝 0 截断 |

<span style="color:#5F7F63;font-weight:700">原理</span>：去掉小数部分，保留整数部分，方向永远是"朝 0"。所以 `trunc(2.9)=2`、`trunc(-2.9)=-2`。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
printf("%.0f\n", trunc(2.9));      /* ① 2 */
printf("%.0f\n", trunc(-2.9));     /* ② -2 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **和 `floor` 混**：负数时不同（`floor(-2.9)=-3`）。
- **以为它会进位**：它只砍不补。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **`trunc` 和 `(int)` 一样吗？** 正数基本一样；超大数强转可能溢出，`trunc` 不会。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`trunc` = truncate = 砍断**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`fmod` —— 浮点取余</span> <a id="fn-fmod"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：浮点数版的取余，结果符号跟被除数。

<span style="color:#5F7F63;font-weight:700">原型</span>：`double fmod(double x, double y);`（`#include <math.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`double` 返回 → 余数｜`fmod` 函数名（float modulo）｜`double x` 被除数｜`double y` 除数

| 项目 | 说明 |
| --- | --- |
| 参数 | 两个浮点 |
| 返回 | `x - trunc(x/y) * y` |
| 失败场景 | `y == 0` → NaN |
| 关键点 | `%` 只能用于整数，浮点必须用它 |

<span style="color:#5F7F63;font-weight:700">原理</span>：先算 `x / y` 的整数部分，再乘回 `y` 从 `x` 里减掉，剩下的就是余数。符号跟随 `x`。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
double r = fmod(7.5, 2.0);         /* ① 1.5 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **对浮点用 `%`**：直接编译错误。
- **除数为 0**：得到 NaN。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **为什么 `%` 不能用于 `float`？** 取模定义在整数上；浮点要用 `fmod`。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`f` + `mod` = 浮点取模**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`fmin` —— 取较小</span> <a id="fn-fmin"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：返回两个浮点数里较小的那个。

<span style="color:#5F7F63;font-weight:700">原型</span>：`double fmin(double x, double y);`（`#include <math.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`double` 返回 → 较小值｜`fmin` 函数名｜`double x`、`double y` → 两个候选

| 项目 | 说明 |
| --- | --- |
| 参数 | 两个浮点 |
| 返回 | 较小者 |
| 失败场景 | 无（遇 NaN 返回另一个） |
| 关键点 | 比手写 `x < y ? x : y` 多处理 NaN |

<span style="color:#5F7F63;font-weight:700">原理</span>：比较两个值，返回小的；若其中一个为 NaN，返回另一个（这是它与三目的区别）。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
double m = fmin(a, b);
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **整数用它**：虽然能编译，但不如 `min` 宏直观。
- **一次只能比两个**：多个值要循环。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **它和 `fmax` 是成对的吗？** 是，一个取小一个取大。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：`min` = 最小。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`fmax` —— 取较大</span> <a id="fn-fmax"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：返回两个浮点数里较大的那个。

<span style="color:#5F7F63;font-weight:700">原型</span>：`double fmax(double x, double y);`（`#include <math.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`double` 返回 → 较大值｜`fmax` 函数名｜两个浮点参数

| 项目 | 说明 |
| --- | --- |
| 参数 | 两个浮点 |
| 返回 | 较大者 |
| 失败场景 | 无（遇 NaN 返回另一个） |
| 关键点 | 与 `fmin` 对称 |

<span style="color:#5F7F63;font-weight:700">原理</span>：比较并返回较大的一个；NaN 被跳过。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
double m = fmax(a, b);
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **和 `fmin` 记反**：`max` 是大。
- **一次只能比两个**。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **求多个数最大值怎么办？** 循环调用或打擂台。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：`max` = 最大。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`exp` —— e 的幂</span> <a id="fn-exp"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：算 `e` 的 `x` 次方。

<span style="color:#5F7F63;font-weight:700">原型</span>：`double exp(double x);`（`#include <math.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`double` 返回 → `e^x`｜`exp` 函数名（exponential）｜`double x` → 指数

| 项目 | 说明 |
| --- | --- |
| 参数 | 任意 `double` |
| 返回 | `e^x` |
| 失败场景 | 太大溢出成 `inf` |
| 关键点 | `e ≈ 2.71828` |

<span style="color:#5F7F63;font-weight:700">原理</span>：用级数展开或专用指令计算自然指数。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
printf("%f\n", exp(1.0));          /* ① 2.718282 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **和 `pow(e, x)` 混**：结果一样，但 `exp` 更快更准。
- **参数过大**：溢出为 `inf`。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **`e` 怎么表示？** 用 `exp(1.0)` 或直接写 `2.718281828`。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`exp` = 指数**，底数固定是 `e`。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`log` —— 自然对数</span> <a id="fn-log"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：求以 `e` 为底的对数（`ln`）。

<span style="color:#5F7F63;font-weight:700">原型</span>：`double log(double x);`（`#include <math.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`double` 返回 → 对数值｜`log` 函数名｜`double x` → **必须大于 0**

| 项目 | 说明 |
| --- | --- |
| 参数 | `x > 0` |
| 返回 | `ln(x)` |
| 失败场景 | `x <= 0` → NaN 或 `-inf` |
| 关键点 | 以 10 为底用 `log10` |

<span style="color:#5F7F63;font-weight:700">原理</span>：与 `exp` 互逆，内部用级数或查表逼近。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
printf("%f\n", log(2.718282));     /* ① ≈ 1.0 */
double bits = log(n) / log(2);      /* ② 换底公式求以 2 为底 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **以为 `log` 是以 10 为底**：它是自然对数，`log10` 才是常用对数。
- **对 0 或负数求**：得到 NaN / `-inf`。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **怎么算任意底的对数？** 换底公式：`log_b(x) = log(x) / log(b)`。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`log` 默认自然对数**，以 10 为底要写 `log10`。

## <span style="color:#7FA182">4. stdlib.h —— 常用工具家族</span> <a id="sec57"></a>

| 函数 | 原型（返回类型 + 参数类型） | 掌握 |
| --- | --- | --- |
| [`abs`](#fn-abs) | `int abs(int n);` | ✅ |
| [`labs`](#fn-labs) | `long labs(long n);` | ⬜ |
| [`rand`](#fn-rand) | `int rand(void);` | ✅ |
| [`srand`](#fn-srand) | `void srand(unsigned seed);` | ✅ |
| [`atoi`](#fn-atoi) | `int atoi(const char* s);` | ⚪ |
| [`atof`](#fn-atof) | `double atof(const char* s);` | ⬜ |
| [`strtol`](#fn-strtol) | `long strtol(const char* s, char** end, int base);` | ⬜ |
| [`exit`](#fn-exit) | `void exit(int status);` | ⚪ |
| [`abort`](#fn-abort) | `void abort(void);` | ⬜ |
| [`system`](#fn-system) | `int system(const char* cmd);` | ⚪ |
| [`malloc`](#fn-malloc) | `void* malloc(size_t n);` | ⚪ |
| [`calloc`](#fn-calloc) | `void* calloc(size_t n, size_t size);` | ⬜ |
| [`realloc`](#fn-realloc) | `void* realloc(void* p, size_t n);` | ⚪ |
| [`free`](#fn-free) | `void free(void* p);` | ⚪ |
| [`qsort`](#fn-qsort) | `void qsort(void* base, size_t n, size_t size, int (*cmp)(const void*, const void*));` | ⬜ |
| [`bsearch`](#fn-bsearch) | `void* bsearch(const void* key, const void* base, size_t n, size_t size, int (*cmp)(const void*, const void*));` | ⬜ |

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`abs` —— 整数绝对值</span> <a id="fn-abs"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：把负整数变成正数，正数原样返回。

<span style="color:#5F7F63;font-weight:700">原型</span>：`int abs(int n);`（`#include <stdlib.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`int` 返回 → 绝对值（仍是 `int`，可能溢出）｜`abs` 函数名｜`int n` 参数 → 要处理的整数

| 项目 | 说明 |
| --- | --- |
| 参数 | `n` 任意 `int` |
| 返回 | `|n|` |
| 失败场景 | `abs(INT_MIN)` 溢出（`-2147483648` 没有对应的正数） |
| 关键点 | 只处理 `int`，`long` 用 `labs`，`double` 用 `fabs` |

<span style="color:#5F7F63;font-weight:700">原理</span>：判断符号位，负数就取反（`-n`），正数直接返回。因为 `int` 的范围是 `-2^31 ~ 2^31-1`，`INT_MIN` 取反后超出上限，结果是未定义（通常还是负数）。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
printf("%d\n", abs(-5));          /* ① 5 */
printf("%d\n", abs(3 - 8));        /* ② 先算再取绝对值 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **对 `double` 用它**：会截断成整数，浮点要用 `fabs`（`math.h`）。
- **对 `INT_MIN` 用它**：溢出，结果不可靠。
- **忘了包含头文件**：`stdlib.h`。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **`abs` / `labs` / `fabs` 怎么选？** `int` 用 `abs`，`long` 用 `labs`，浮点用 `fabs`；名字前缀就是"给谁用"。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：`abs` = absolute，**"取绝对值"**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`labs` —— long 绝对值</span> <a id="fn-labs"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：`abs` 的 `long` 版本。

<span style="color:#5F7F63;font-weight:700">原型</span>：`long labs(long n);`（`#include <stdlib.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`long` 返回 → 绝对值｜`labs` 函数名（`l` = long）｜`long n` → 要处理的 `long`

| 项目 | 说明 |
| --- | --- |
| 参数 | `long` 整数 |
| 返回 | 绝对值（`long`） |
| 失败场景 | `LONG_MIN` 同样溢出 |
| 关键点 | 打印用 `%ld` |

<span style="color:#5F7F63;font-weight:700">原理</span>：与 `abs` 相同，只是处理 64 位（或 32 位，看平台）的 `long`。范围更大，但 `LONG_MIN` 依然没有对应的正数。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
long x = -123456789L;
printf("%ld\n", labs(x));          /* ① %ld */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **参数传 `int`**：会被提升，结果对但类型易混。
- **打印用 `%d`**：`long` 要 `%ld`（C4477）。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **什么时候必须用 `labs`？** 变量声明成 `long`、且可能超出 `int` 范围时。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`l` 开头 = long 专用**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`rand` —— 伪随机数</span> <a id="fn-rand"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：返回一个 0 ~ `RAND_MAX` 之间的**伪**随机整数。

<span style="color:#5F7F63;font-weight:700">原型</span>：`int rand(void);`（`#include <stdlib.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`int` 返回 → 0 ~ `RAND_MAX`（至少 32767）｜`rand` 函数名｜`void` → **不需要参数**

| 项目 | 说明 |
| --- | --- |
| 参数 | 无 |
| 返回 | 0 ~ `RAND_MAX` 的整数 |
| 失败场景 | 没有失败返回 |
| 关键点 | 默认种子固定，所以**每次运行序列相同** |

<span style="color:#5F7F63;font-weight:700">原理</span>：内部是一个**线性同余**之类的确定性算法：`下个数 = f(上个数)`，起点由"种子"决定。相同种子必然产生相同序列，所以它叫"伪随机"——不播种的话，每次运行都从同一个起点开始。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
srand((unsigned)time(NULL));       /* ① 先播种，只播一次 */
int x = rand() % 100;              /* ② 0 ~ 99 */
int y = 10 + rand() % 91;          /* ③ 10 ~ 100 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **不 `srand`**：每次运行结果一模一样。
- **在循环里 `srand`**：同一秒内种子相同，序列重复。
- **`rand() % n` 分布不均**：范围小时偏差明显，但刷题够用。
- **把它当"真随机"**：它是确定性的，可预测。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **随机数三件套是什么？** `srand`（播种）+ `time(NULL)`（种子来源）+ `rand`（取数）。
- **为什么 `srand` 只调一次？** 每次调用都会重置序列起点；同一秒内调用两次，种子相同，随机数就一样。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`rand` 是"按种子排好的队列"**，种子一样，队列就一样。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`srand` —— 播种子</span> <a id="fn-srand"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：给随机数发生器设置"起点"，决定整条随机序列。

<span style="color:#5F7F63;font-weight:700">原型</span>：`void srand(unsigned seed);`（`#include <stdlib.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`void` 返回 → **没有返回值**｜`srand` 函数名｜`unsigned seed` 参数 → 种子，通常传 `(unsigned)time(NULL)`

| 项目 | 说明 |
| --- | --- |
| 参数 | `seed` 种子 |
| 返回 | 无 |
| 失败场景 | 无 |
| 关键点 | **全程序只调一次**，放在 `main` 开头 |

<span style="color:#5F7F63;font-weight:700">原理</span>：把 `seed` 写进内部状态，作为 `rand` 序列的起点。相同 `seed` → 完全相同的序列。用当前时间做种子，是因为每次运行时间不同，序列才会变。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
#include <time.h>
srand((unsigned)time(NULL));       /* ① 只调一次 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **调两次**：同一秒内种子相同，两次随机数一样（T16 踩过）。
- **写进取随机数的函数里**：每次调用都重置，永远返回同一个值。
- **忘了 `time.h`**：`time` 未声明。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **为什么 `srand` 调两次会让两个随机数一样？** 同一秒内 `time(NULL)` 相同 → 种子相同 → 序列相同。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`s` = seed，"播种一次，收一整季"**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`atoi` —— 字符串转整数</span> <a id="fn-atoi"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：把 `"123"` 这样的字符串转成整数 `123`。

<span style="color:#5F7F63;font-weight:700">原型</span>：`int atoi(const char* s);`（`#include <stdlib.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`int` 返回 → 转换结果，**失败也返回 0**｜`atoi` 函数名（ASCII to integer）｜`const char* s` 参数 → 数字字符串（只读）

| 项目 | 说明 |
| --- | --- |
| 参数 | `s` 以数字开头的字符串 |
| 返回 | 转换出的 `int`；无法转换返回 **0** |
| 失败场景 | **不报错、不区分"0"和"转换失败"** |
| 关键点 | 遇到非数字字符就停 |

<span style="color:#5F7F63;font-weight:700">原理</span>：跳过前导空白后，逐字符把 `'0'~'9'` 换算成数值（`c - '0'`），每读一位就把结果乘 10 再加这一位；遇到第一个非数字字符立刻停止并返回已累计的值。所以 `"12abc"` 得到 12，`"abc"` 得到 0。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
int n = atoi("123");               /* ① 123 */
int m = atoi("12abc");             /* ② 12，遇到 a 停 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **拿它判断输入合法性**：失败返回 0，无法和真正的 0 区分。
- **溢出没有提示**：超出 `int` 范围是未定义行为。
- **以为它认小数**：`atoi("3.14")` 得到 3，小数用 `atof`。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **要检查转换是否成功怎么办？** 用 `strtol`，它通过 `endptr` 告诉你"停在哪"，还能查溢出。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`a` = ASCII，"把字符数字变成真数字"**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`atof` —— 字符串转 double</span> <a id="fn-atof"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：把 `"3.14"` 转成 `double` 的 3.14。

<span style="color:#5F7F63;font-weight:700">原型</span>：`double atof(const char* s);`（`#include <stdlib.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`double` 返回 → 浮点结果，失败返回 0.0｜`atof` 函数名｜`const char* s` → 数字字符串

| 项目 | 说明 |
| --- | --- |
| 参数 | `s` 数字字符串（可含小数点、指数） |
| 返回 | `double`；失败返回 0.0 |
| 失败场景 | 同样不报错 |
| 关键点 | 打印用 `%f` |

<span style="color:#5F7F63;font-weight:700">原理</span>：解析可选符号、整数部分、小数点、小数部分、指数部分，逐段累加成 `double`；遇到无法识别的字符就停。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
double x = atof("3.14");           /* ① 3.14 */
printf("%.2f\n", x);
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **拿它判错**：失败返回 0.0，和真 0 分不清。
- **用 `atoi` 转小数**：会截断成整数。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **它和 `strtod` 的区别？** `strtod` 能通过 `endptr` 报告解析到哪、还能查溢出；`atof` 什么都不告诉你。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`f` = float，"ASCII 转浮点"**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`strtol` —— 字符串转 long（可指定进制）</span> <a id="fn-strtol"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：比 `atoi` 强的版本——能指定进制，还能告诉你"解析到哪、有没有溢出"。

<span style="color:#5F7F63;font-weight:700">原型</span>：`long strtol(const char* s, char** endptr, int base);`（`#include <stdlib.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`long` 返回 → 转换结果｜`strtol` 函数名（string to long）｜`const char* s` → 源字符串｜`char** endptr` → 二级指针，用来**回传"停在哪"**（可传 `NULL` 不关心）｜`int base` → 进制（10、16、2；传 0 表示自动判断）

| 项目 | 说明 |
| --- | --- |
| 参数 | `s` 源串；`endptr` 停在哪；`base` 进制 |
| 返回 | 转换出的 `long` |
| 失败场景 | 溢出返回 `LONG_MAX`/`LONG_MIN` 并设 `errno`；完全没转换返回 0 且 `*endptr == s` |
| 关键点 | 能可靠判断"是否转换成功" |

<span style="color:#5F7F63;font-weight:700">原理</span>：按 `base` 指定的进制逐位累加，遇到不合法字符就停；停下时把当前位置写进 `*endptr`。调用者通过比较 `endptr` 是否等于原串开头，就能判断"一个字符都没转换成功"。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
char* end;
long n = strtol("ff", &end, 16);   /* ① 十六进制 → 255 */
if (end != NULL && *end == '\0')   /* ② 整串都转换成功 */
    printf("合法数字：%ld\n", n);
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **`endptr` 类型写错**：必须是 `char**`，传 `&end`。
- **不检查 `endptr`**：就失去了它相对 `atoi` 的唯一优势。
- **进制传错**：`base` 不写默认当 10。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **为什么它比 `atoi` 安全？** 因为能通过 `endptr` 和 `errno` 区分"转换失败"与"真的等于 0"。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**多两个参数 = 多两双眼睛**（停在哪、几进制）。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`exit` —— 结束程序</span> <a id="fn-exit"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：立刻结束整个程序，并把所有打开的流刷新关闭。

<span style="color:#5F7F63;font-weight:700">原型</span>：`void exit(int status);`（`#include <stdlib.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`void` 返回 → 不返回｜`exit` 函数名｜`int status` → 退出码（0 表示正常，非 0 表示异常）

| 项目 | 说明 |
| --- | --- |
| 参数 | `status` 退出码（`EXIT_SUCCESS` / `EXIT_FAILURE`） |
| 返回 | **不返回** |
| 副作用 | 刷新并关闭所有流、调用 `atexit` 注册的函数 |
| 和 `return` 区别 | `exit` 结束**整个程序**，`return` 只结束当前函数 |

<span style="color:#5F7F63;font-weight:700">原理</span>：它触发"正常退出"流程：先按注册的逆序调用 `atexit` 函数，然后刷新所有输出缓冲区、关闭所有流，最后把 `status` 交给操作系统。因为是正常退出，**缓冲区里的数据会被写出去**。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
if (fp == NULL) {
    printf("打开失败\n");
    exit(EXIT_FAILURE);            /* ① 异常退出 */
}
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **在 `main` 里用它当 `return`**：效果类似，但可读性差。
- **以为它会立刻停**：它还会冲刷缓冲、跑 `atexit`。
- **和 `abort` 混**：`abort` 不刷新、不清理。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **`exit(0)` 和 `return 0` 有区别吗？** 在 `main` 里等价；在别的函数里 `exit` 会直接结束程序，`return` 只是返回。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`exit` = 出厂**，走之前把东西收拾好（刷缓冲）。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`abort` —— 异常终止</span> <a id="fn-abort"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：立刻异常终止程序，**不刷缓冲、不做清理**。

<span style="color:#5F7F63;font-weight:700">原型</span>：`void abort(void);`（`#include <stdlib.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`void` 返回 → 不返回｜`abort` 函数名｜`void` → 无参数

| 项目 | 说明 |
| --- | --- |
| 参数 | 无 |
| 返回 | 不返回 |
| 副作用 | 可能生成 core dump；**不刷新流** |
| 典型用途 | `assert` 失败时内部调用它 |

<span style="color:#5F7F63;font-weight:700">原理</span>：直接向系统发"异常终止"信号（`SIGABRT`），不走正常退出流程，所以输出缓冲区里的内容可能丢失。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
if (p == NULL) abort();            /* ① 严重错误，立即终止 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **用它做正常退出**：数据可能没写盘，应该用 `exit`。
- **调试时没输出**：正是因为它不刷缓冲。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **`exit` 和 `abort` 怎么选？** 正常结束用 `exit`；检测到"程序已经不可信"时用 `abort`。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`abort` = 紧急刹车**，不管后面的事。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`system` —— 调用系统命令</span> <a id="fn-system"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：在程序里执行一条操作系统命令。

<span style="color:#5F7F63;font-weight:700">原型</span>：`int system(const char* cmd);`（`#include <stdlib.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`int` 返回 → 命令的退出状态（0 通常表示成功）｜`system` 函数名｜`const char* cmd` → 命令行字符串

| 项目 | 说明 |
| --- | --- |
| 参数 | `cmd` 系统命令（如 `"cls"`、`"dir"`） |
| 返回 | 命令退出码；`cmd` 为 `NULL` 时返回"是否有命令行环境" |
| 失败场景 | 命令不存在、无权限 |
| 平台差异 | `cls`/`dir` 是 Windows，Linux 是 `clear`/`ls` |

<span style="color:#5F7F63;font-weight:700">原理</span>：把字符串交给系统的命令解释器执行，等它跑完再返回退出状态。它不是 C 标准 I/O，只是"借道"操作系统的 shell。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
system("cls");                     /* ① Windows 清屏 */
system("pause");                   /* ② 暂停等按键 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **跨平台不通用**：`cls` 在 Linux 上无效。
- **返回值含义不统一**：不同系统编码不同，只能大致判断。
- **比赛/在线评测可能禁用**：不可移植。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **T17 的关机程序为什么用 `system`？** 它只是调用系统命令，和 C 语言本身无关。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`system` = 借系统的嘴说话**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`malloc` —— 申请内存</span> <a id="fn-malloc"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：在**堆**上要一块 `n` 字节的内存，返回它的首地址。

<span style="color:#5F7F63;font-weight:700">原型</span>：`void* malloc(size_t n);`（`#include <stdlib.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`void*` 返回 → 内存首地址（"万能指针"，用时强转）｜`malloc` 函数名（memory allocate）｜`size_t n` → **字节数**

| 项目 | 说明 |
| --- | --- |
| 参数 | `n` 字节数（要自己乘 `sizeof`） |
| 返回 | 成功：地址；失败：`NULL` |
| 失败场景 | 内存不足、请求过大 |
| 关键点 | **内容不初始化**，是上次留下的垃圾 |

<span style="color:#5F7F63;font-weight:700">原理</span>：在堆的空闲块链表里找一块至少 `n` 字节的内存，切分后把用户区地址返回（块头里记着大小）；找不到就向系统申请扩展堆。因为复用的是别人用过的内存，内容不会清零。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
int n = 10;
int* p = (int*)malloc(n * sizeof(int));   /* ① 乘 sizeof */
if (p == NULL) return 1;                   /* ② 必须验货 */
for (int i = 0; i < n; i++) p[i] = i;      /* ③ 内容要自己填 */
free(p); p = NULL;                          /* ④ 用完释放 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **参数字节数写成元素个数**：`malloc(n)` 装不下 `n` 个 `int`。
- **不判 `NULL`**：失败后直接写就是往地址 0 写。
- **以为内容清零**：要用 `calloc` 或自己 `memset`。
- **忘记 `free`**：内存泄漏。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **`malloc` 前的 `(int*)` 要不要写？** C 里可省，C++ 必须写；建议写上有助于移植。
- **它和 `new` 的区别？** C 没有 `new`；`malloc` 只给原始内存，不调用构造函数。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`malloc` 只给地皮，不装修**（不清零）。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`calloc` —— 申请并清零</span> <a id="fn-calloc"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：申请 `n × size` 字节，**并全部清零**。

<span style="color:#5F7F63;font-weight:700">原型</span>：`void* calloc(size_t n, size_t size);`（`#include <stdlib.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`void*` 返回 → 首地址或 `NULL`｜`calloc` 函数名（clear + allocate）｜`size_t n` → **元素个数**｜`size_t size` → **每个元素多少字节**

| 项目 | 说明 |
| --- | --- |
| 参数 | `n` 个数、`size` 每个多大（两个数相乘才是字节） |
| 返回 | 成功：地址；失败：`NULL` |
| 失败场景 | 内存不足 |
| 关键点 | **自动清零**，比 `malloc` 省一次 `memset` |

<span style="color:#5F7F63;font-weight:700">原理</span>：内部按 `n × size` 申请，然后把整块内存**逐字节置 0**（可能拿到系统已清零的页，也可能内部 `memset`）。因此对整数、指针、浮点数组都安全地得到"全 0 初值"。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
int* p = (int*)calloc(n, sizeof(int));    /* ① 全是 0 */
struct Stu* s = (struct Stu*)calloc(5, sizeof(struct Stu));  /* ② 结构体数组清零 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **两个参数顺序搞反**：`calloc(sizeof(int), n)` 字节数一样，但语义混乱。
- **以为它和 `malloc` 参数相同**：`malloc` 一个字节数参数，`calloc` 两个。
- **忘了 `free`**。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **它和 `malloc` 怎么选？** 想要全 0 初值用 `calloc`；要大块且马上会覆盖用 `malloc`。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`c` = clear**，"先铺地皮再扫干净"。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`realloc` —— 扩容 / 缩容</span> <a id="fn-realloc"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：把已经申请的内存改成新的大小，**可能搬家**。

<span style="color:#5F7F63;font-weight:700">原型</span>：`void* realloc(void* p, size_t n);`（`#include <stdlib.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`void*` 返回 → **新地址**（可能和旧地址不同）｜`realloc` 函数名｜`void* p` → 原来申请的地址｜`size_t n` → **调整后的总字节数**（不是增量）

| 项目 | 说明 |
| --- | --- |
| 参数 | `p` 旧地址；`n` 新总字节数 |
| 返回 | 成功：新地址；失败：`NULL`（**老块还在**） |
| 失败场景 | 内存不足 |
| 关键点 | **必须用临时指针接** |

<span style="color:#5F7F63;font-weight:700">原理</span>：如果原块后面有足够空闲，就**原地扩大**；否则新申请一块、把老内容拷过去、释放老块，返回新地址。失败时返回 `NULL` 且**原块原封不动**——所以直接写 `p = realloc(p, ...)` 会在失败时丢掉老地址。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
int* t = (int*)realloc(p, (n + m) * sizeof(int));  /* ① 临时指针接 */
if (t == NULL) { free(p); return 1; }               /* ② 失败先释放老块 */
p = t;                                               /* ③ 成功才换 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **`p = realloc(p, ...)`**：失败时老地址丢失，内存泄漏。
- **把 `n` 当增量**：它是"调整后的总数"。
- **忘乘 `sizeof`**：字节数要自己算。
- **以为新扩的部分清零**：不清零，是垃圾值。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **为什么要用临时指针？** 因为它可能搬家；失败时老块还在，需要保留地址去释放。
- **新扩出来的部分是什么？** 未初始化，不能假设是 0。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`realloc` = 换房子**，可能换门牌号，家具由它搬。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`free` —— 释放</span> <a id="fn-free"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：把 `malloc`/`calloc`/`realloc` 申请的内存还给堆。

<span style="color:#5F7F63;font-weight:700">原型</span>：`void free(void* p);`（`#include <stdlib.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`void` 返回 → 无返回值｜`free` 函数名｜`void* p` → **申请时返回的那个地址**（不能是中间地址）

| 项目 | 说明 |
| --- | --- |
| 参数 | `p` 申请函数返回的原始地址；可为 `NULL`（安全） |
| 返回 | 无 |
| 失败场景 | 传非堆地址、重复释放 → 破坏堆 |
| 关键点 | **不会把指针置空**，要自己 `p = NULL` |

<span style="color:#5F7F63;font-weight:700">原理</span>：用块头里记录的信息找到这块内存，标记为空闲并尝试与相邻空闲块合并，交还给堆管理器。它**无法验证**指针合法性——重复释放或释放栈/全局内存会破坏堆结构，往往在后续 `malloc` 时才崩。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
free(p);
p = NULL;                          /* ① 防悬空指针 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **释放后继续用**：悬空指针，行为未定义。
- **重复 `free`**：破坏堆。
- **释放中间地址**：`free(p + 1)` 非法。
- **`free` 后不置空**：下次误用时很难排查。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **`free(NULL)` 会崩吗？** 不会，标准规定它什么也不做。
- **`free` 会把内存清零吗？** 不会，只是标记为空闲。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`free` = 退房**，房卡（指针）要自己作废。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`qsort` —— 快速排序</span> <a id="fn-qsort"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：标准库自带的通用排序，任何类型都能排，只要你提供比较函数。

<span style="color:#5F7F63;font-weight:700">原型</span>：`void qsort(void* base, size_t n, size_t size, int (*cmp)(const void*, const void*));`（`#include <stdlib.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`void` 返回 → 无返回值，**直接改原数组**｜`qsort` 函数名｜`void* base` → 数组首地址｜`size_t n` → 元素个数｜`size_t size` → 每个元素字节数｜`int (*cmp)(...)` → **函数指针**，比较规则

| 项目 | 说明 |
| --- | --- |
| 参数 | 首地址 / 个数 / 单元素大小 / 比较函数 |
| 返回 | 无（原地排序） |
| 失败场景 | 比较函数写错 → 结果乱序 |
| 关键点 | `cmp` 返回 **负 / 0 / 正** |

<span style="color:#5F7F63;font-weight:700">原理</span>：它不知道元素类型，只知道"每个元素 `size` 字节"和"怎么比较"。内部用快排算法不断调用 `cmp(a, b)` 决定顺序，需要交换时按 `size` 字节整块搬。所以同一份 `qsort` 能排 `int`、结构体、字符串。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
int cmp_int(const void* a, const void* b) {
    int x = *(const int*)a, y = *(const int*)b;
    return (x > y) - (x < y);       /* ① 避免相减溢出 */
}
qsort(arr, n, sizeof(int), cmp_int);

int cmp_stu(const void* a, const void* b) {   /* ② 结构体按分数降序 */
    return ((const struct Stu*)b)->score - ((const struct Stu*)a)->score;
}
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **`cmp` 写成 `return a - b;`（指针相减）**：比的是地址，不是值。
- **`size` 写错**：写成元素个数会导致整块错位。
- **`cmp` 返回布尔值**：必须有负/0/正三种。
- **降序忘了反过来**：`a - b` 是升序，降序要 `b - a`。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **`cmp` 里为什么要强转**：`void*` 不知道类型，要转成实际类型再取值。
- **和手写冒泡的关系？** 都是排序，`qsort` 是库实现，更快更省事。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`q` = quick**，你只负责"谁大谁小"，它负责搬。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`bsearch` —— 二分查找</span> <a id="fn-bsearch"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：在**已排好序**的数组里二分查找，返回命中元素的地址。

<span style="color:#5F7F63;font-weight:700">原型</span>：`void* bsearch(const void* key, const void* base, size_t n, size_t size, int (*cmp)(const void*, const void*));`（`#include <stdlib.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`void*` 返回 → 命中元素的地址，没找到 `NULL`｜`bsearch` 函数名｜`const void* key` → 要找的值的地址｜`base/n/size` → 数组首地址、个数、单元素大小｜`cmp` → 比较函数（规则同 `qsort`）

| 项目 | 说明 |
| --- | --- |
| 参数 | 目标值地址 + 数组描述 + 比较函数 |
| 返回 | 命中：元素地址；未命中：`NULL` |
| 失败场景 | **数组没排序 → 结果不可靠** |
| 关键点 | 必须和排序用**同一个** `cmp` |

<span style="color:#5F7F63;font-weight:700">原理</span>：维护 `left/right` 两个下标，每次取中点调用 `cmp`：目标小就往左半找，大就往右半找，相等就返回该地址。每轮排除一半，所以是 `O(log n)`——前提是数组**有序**。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
int key = 42;
int* p = (int*)bsearch(&key, arr, n, sizeof(int), cmp_int);
if (p != NULL)
    printf("找到了，下标 %d\n", (int)(p - arr));
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **数组没排序就用**：结果随机。
- **传值而不是地址**：第一个参数要 `&key`。
- **`cmp` 和排序时不一致**：顺序和查找规则不同，必然找不到。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **它和手写二分的关系？** 算法一样，`bsearch` 是通用版，省去自己写循环和边界。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**先 `qsort` 再 `bsearch`**，一对搭档。

## <span style="color:#7FA182">5. ctype.h —— 字符分类与大小写转换</span> <a id="sec82"></a>

> `#include <ctype.h>`；所有函数**返回 `int`**（0 = 假，非 0 = 真），参数传 `unsigned char` 或 `EOF`。

| 函数 | 原型（全是 `int (int)`） | 掌握 |
| --- | --- | --- |
| [`isalpha`](#fn-isalpha) | `int isalpha(int c);` | ⚪ |
| [`isdigit`](#fn-isdigit) | `int isdigit(int c);` | ⚪ |
| [`isalnum`](#fn-isalnum) | `int isalnum(int c);` | ⬜ |
| [`isspace`](#fn-isspace) | `int isspace(int c);` | ⚪ |
| [`isupper`](#fn-isupper) | `int isupper(int c);` | ⬜ |
| [`islower`](#fn-islower) | `int islower(int c);` | ⬜ |
| [`ispunct`](#fn-ispunct) | `int ispunct(int c);` | ⬜ |
| [`isxdigit`](#fn-isxdigit) | `int isxdigit(int c);` | ⬜ |
| [`toupper`](#fn-toupper) | `int toupper(int c);` | ⚪ |
| [`tolower`](#fn-tolower) | `int tolower(int c);` | ⚪ |

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`isalpha` —— 是不是字母</span> <a id="fn-isalpha"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：判断一个字符是不是 `a~z` 或 `A~Z`。

<span style="color:#5F7F63;font-weight:700">原型</span>：`int isalpha(int c);`（`#include <ctype.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`int` 返回 → **非 0 为真、0 为假**（不是 0/1）｜`isalpha` 函数名｜`int c` → 要判断的字符（传 `char` 会被提升）

| 项目 | 说明 |
| --- | --- |
| 参数 | `c` 字符的 ASCII 值，或 `EOF` |
| 返回 | 是字母返回非 0；不是返回 0 |
| 失败场景 | 传负数（非 `EOF`）是未定义行为 |
| 关键点 | 返回值别和 1 比较，只当"真/假"用 |

<span style="color:#5F7F63;font-weight:700">原理</span>：内部查表或做范围比较（`c >= 'a' && c <= 'z' || c >= 'A' && c <= 'Z'`），命中返回一个非 0 常量，否则返回 0。用查表实现是为了避免区域设置（locale）差异。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
if (isalpha(ch))                   /* ① 直接当条件 */
    words++;
if (!isalpha((unsigned char)ch))   /* ② 保险写法：先转无符号 */
    break;
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **`if (isalpha(ch) == 1)`**：返回值只保证"非 0"，不保证等于 1。
- **直接传负的 `char`**：未定义行为，标准写法是 `(unsigned char)ch`。
- **用它判断中文**：只认 ASCII 字母，中文会返回假。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **为什么参数是 `int` 不是 `char`？** 因为要能接收 `EOF`（-1），`char` 可能装不下。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：`is` + `alpha` = "**是不是字母**"，返回非 0 即真。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`isdigit` —— 是不是数字字符</span> <a id="fn-isdigit"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：判断一个字符是不是 `'0'~'9'`。

<span style="color:#5F7F63;font-weight:700">原型</span>：`int isdigit(int c);`（`#include <ctype.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`int` 返回 → 非 0 真 / 0 假｜`isdigit` 函数名｜`int c` → 字符值

| 项目 | 说明 |
| --- | --- |
| 参数 | 字符 ASCII 或 `EOF` |
| 返回 | 数字字符返回非 0 |
| 失败场景 | 负值非 EOF 是 UB |
| 关键点 | 只认 `'0'~'9'`，不认小数点或负号 |

<span style="color:#5F7F63;font-weight:700">原理</span>：做 `c >= '0' && c <= '9'` 的范围判断（或查表），命中返回非 0。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
if (isdigit(ch))                   /* ① 是数字字符 */
    ndigit++;
int v = ch - '0';                  /* ② 转成数值 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **`isdigit(5)` 想判断数字 5**：它判断的是**字符** `'5'`（53），传 5 得到假。
- **拿来验证整个字符串**：它一次只看一个字符。
- **以为它认 `-` 或 `.`**：都不认。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **字符 `'5'` 和数字 5 有什么区别？** `'5'` 的 ASCII 是 53；`ch - '0'` 才能得到数值 5。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`digit` = 数位**，判断的是字符不是数值。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`isalnum` —— 字母或数字</span> <a id="fn-isalnum"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：字母**或**数字都算真。

<span style="color:#5F7F63;font-weight:700">原型</span>：`int isalnum(int c);`（`#include <ctype.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`int` 返回 → 非 0 真 / 0 假｜`isalnum` 函数名（alpha + number）｜`int c` → 字符值

| 项目 | 说明 |
| --- | --- |
| 参数 | 字符 ASCII 或 `EOF` |
| 返回 | 字母或数字返回非 0 |
| 失败场景 | 负值非 EOF 是 UB |
| 典型用途 | 校验"标识符/用户名"只含字母数字 |

<span style="color:#5F7F63;font-weight:700">原理</span>：等价于 `isalpha(c) || isdigit(c)`，一次判断覆盖两类。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
if (isalnum(ch))                   /* ① 字母或数字 */
    keep++;
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **以为它包含下划线**：不包含，下划线要用 `c == '_'` 单独判断。
- **返回值当 0/1**：只保证非 0。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **它和 `isalpha`/`isdigit` 的关系？** 它俩的并集，省一次 `||`。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`alnum` = alpha + num**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`isspace` —— 是不是空白</span> <a id="fn-isspace"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：判断是不是空格、`\t`、`\n`、`\r`、`\v`、`\f` 之一。

<span style="color:#5F7F63;font-weight:700">原型</span>：`int isspace(int c);`（`#include <ctype.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`int` 返回 → 非 0 真 / 0 假｜`isspace` 函数名｜`int c` → 字符值

| 项目 | 说明 |
| --- | --- |
| 参数 | 字符 ASCII 或 `EOF` |
| 返回 | 空白字符返回非 0 |
| 覆盖范围 | 空格、`\t`、`\n`、`\r`、`\v`、`\f` |
| 典型用途 | 跳过空白、判断"这一行是不是空的" |

<span style="color:#5F7F63;font-weight:700">原理</span>：内部列出六种空白字符逐一比对，命中返回非 0。注意它**包含换行**，所以"跳过空白"常会顺手跳过换行。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
while (isspace(ch)) ch = getchar();   /* ① 跳过所有空白 */
if (isspace(line[0])) puts("以空白开头");
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **以为只判断空格**：`\n`、`\t` 也算。
- **用它跳过空白却不想跳过换行**：要单独写 `ch == ' ' || ch == '\t'`。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **`\n` 算空白吗？** 算——所以 `isspace` 不能用来"只跳空格"。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`space` 泛指所有"看不见的间隔"**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`isupper` —— 是不是大写</span> <a id="fn-isupper"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：判断是不是 `A~Z`。

<span style="color:#5F7F63;font-weight:700">原型</span>：`int isupper(int c);`（`#include <ctype.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`int` 返回 → 非 0 真 / 0 假｜`isupper` 函数名｜`int c` → 字符值

| 项目 | 说明 |
| --- | --- |
| 参数 | 字符 ASCII 或 `EOF` |
| 返回 | 大写字母返回非 0 |
| 失败场景 | 负值非 EOF 是 UB |
| 典型用途 | 统计大写个数、配合 `tolower` 统一大小写 |

<span style="color:#5F7F63;font-weight:700">原理</span>：判断 `c >= 'A' && c <= 'Z'`，命中返回非 0。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
if (isupper(ch)) upper++;
else if (islower(ch)) lower++;
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **和 `islower` 混用**：一个管大写一个管小写。
- **判断的是字符不是字符串**：一次只看一个字符。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **大小写转换怎么配对？** `isupper`/`islower` 判断，`toupper`/`tolower` 转换。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`upper` = 上面 = 大写**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`islower` —— 是不是小写</span> <a id="fn-islower"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：判断是不是 `a~z`。

<span style="color:#5F7F63;font-weight:700">原型</span>：`int islower(int c);`（`#include <ctype.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`int` 返回 → 非 0 真 / 0 假｜`islower` 函数名｜`int c` → 字符值

| 项目 | 说明 |
| --- | --- |
| 参数 | 字符 ASCII 或 `EOF` |
| 返回 | 小写字母返回非 0 |
| 失败场景 | 负值非 EOF 是 UB |
| 典型用途 | 同上 |

<span style="color:#5F7F63;font-weight:700">原理</span>：判断 `c >= 'a' && c <= 'z'`，命中返回非 0。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
if (islower(ch)) lower++;
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **和 `isupper` 记反**：`lower` 是小写。
- **以为数字也算**：不算。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **`islower` 和 `isdigit` 能一起判吗？** 用 `isalnum` 或 `||`。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`lower` = 下面 = 小写**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`ispunct` —— 是不是标点</span> <a id="fn-ispunct"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：判断是不是标点/符号（可打印但既不是字母数字也不是空白）。

<span style="color:#5F7F63;font-weight:700">原型</span>：`int ispunct(int c);`（`#include <ctype.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`int` 返回 → 非 0 真 / 0 假｜`ispunct` 函数名（punct = punctuation）｜`int c` → 字符值

| 项目 | 说明 |
| --- | --- |
| 参数 | 字符 ASCII 或 `EOF` |
| 返回 | 标点符号返回非 0 |
| 覆盖范围 | `,` `.` `!` `?` `;` `:` `-` 等 |
| 典型用途 | 统计标点、清洗文本 |

<span style="color:#5F7F63;font-weight:700">原理</span>：判断"可打印（`isgraph`）且不是字母数字"，命中返回非 0。空格不算标点。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
if (ispunct(ch)) punct++;
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **以为空格算标点**：不算。
- **以为中文标点算**：只认 ASCII。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **统计"纯符号"怎么配合？** `isalpha`/`isdigit`/`isspace` 都不成立时，剩下的基本就是标点。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`punct` = punctuation，"标点"**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`isxdigit` —— 是不是十六进制字符</span> <a id="fn-isxdigit"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：判断是不是 `0~9`、`a~f`、`A~F`。

<span style="color:#5F7F63;font-weight:700">原型</span>：`int isxdigit(int c);`（`#include <ctype.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`int` 返回 → 非 0 真 / 0 假｜`isxdigit` 函数名（x = hex）｜`int c` → 字符值

| 项目 | 说明 |
| --- | --- |
| 参数 | 字符 ASCII 或 `EOF` |
| 返回 | 十六进制字符返回非 0 |
| 覆盖范围 | `0-9`、`a-f`、`A-F` |
| 典型用途 | 校验十六进制字符串 |

<span style="color:#5F7F63;font-weight:700">原理</span>：三段判断——数字、小写 `a~f`、大写 `A~F`，任一命中返回非 0。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
if (isxdigit(ch)) hex_count++;
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **以为 `g~z` 也算**：只到 `f`。
- **和 `isdigit` 混用**：十进制只用 `isdigit`。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **怎么把 `'a'` 转成 10？** 手动判断：`if (ch >= 'a') v = ch - 'a' + 10;`（标准库没有现成函数）。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`x` = hex**，十六进制专用。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`toupper` —— 转大写</span> <a id="fn-toupper"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：把小写字母转成大写，**其它字符原样返回**。

<span style="color:#5F7F63;font-weight:700">原型</span>：`int toupper(int c);`（`#include <ctype.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`int` 返回 → **转换后的字符值**（不是"成功/失败"）｜`toupper` 函数名｜`int c` → 原字符

| 项目 | 说明 |
| --- | --- |
| 参数 | 字符 ASCII 或 `EOF` |
| 返回 | 大写字符；非小写原样返回 |
| 关键点 | **不改原变量，必须赋值** |
| 典型用途 | 统一大小写后再比较 |

<span style="color:#5F7F63;font-weight:700">原理</span>：如果是 `'a'~'z'`，返回 `c - ('a' - 'A')`（即减 32）；否则原样返回 `c`。它是**纯函数**，只返回新值，不动原内存。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
char c = 'a';
c = toupper(c);                    /* ① 必须赋值回去 */
printf("%c\n", c);                 /* A */

for (i = 0; s[i]; i++)
    s[i] = toupper((unsigned char)s[i]);   /* ② 整串转大写 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **`toupper(c);` 不赋值**：返回值被丢掉，原变量没变。
- **以为它只处理字母**：数字、标点会原样返回，不报错。
- **直接传负 `char`**：标准写法是 `(unsigned char)c`。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **字符大小写转换的本质？** 就是 ASCII 码相差 32，`'a'` 是 97、`'A'` 是 65。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`to` 开头 = "转成"，返回新值不改原值**。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`tolower` —— 转小写</span> <a id="fn-tolower"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：把大写字母转成小写，其它字符原样返回。

<span style="color:#5F7F63;font-weight:700">原型</span>：`int tolower(int c);`（`#include <ctype.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`int` 返回 → 转换后的字符值｜`tolower` 函数名｜`int c` → 原字符

| 项目 | 说明 |
| --- | --- |
| 参数 | 字符 ASCII 或 `EOF` |
| 返回 | 小写字符；非大写原样返回 |
| 关键点 | 同样**必须赋值** |
| 典型用途 | 忽略大小写比较 |

<span style="color:#5F7F63;font-weight:700">原理</span>：如果是 `'A'~'Z'`，返回 `c + 32`；否则原样返回。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
char a = 'Q';
a = tolower(a);                    /* ① q */
if (tolower(x) == tolower(y))      /* ② 忽略大小写比较 */
    puts("相同");
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **不赋值**：原变量不变。
- **拿它改字符串常量**：只读区不能写。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **忽略大小写比较要怎么写？** 两边都 `tolower` 后再 `strcmp`，或逐字符比较。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`lower` = 小写**，和 `toupper` 对称。

## <span style="color:#7FA182">6. time.h —— 随机种子的来源 & 计时器</span> <a id="sec83"></a>

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`time` —— 取当前时间（秒数）</span> <a id="fn-time"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：返回从 1970-01-01 00:00:00 到现在的**秒数**，最常用来当随机数种子。

<span style="color:#5F7F63;font-weight:700">原型</span>：`time_t time(time_t* timer);`（`#include <time.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`time_t` 返回 → 秒数（本质是整数类型）｜`time` 函数名｜`time_t* timer` 参数 → 可传 `NULL`（只要返回值）；也可传地址让它顺带写一份

| 项目 | 说明 |
| --- | --- |
| 参数 | `timer` 常传 `NULL` |
| 返回 | 当前时间的秒数（`time_t`） |
| 失败场景 | 极少失败，失败返回 `(time_t)-1` |
| 关键点 | 同一秒内多次调用返回值相同 |

<span style="color:#5F7F63;font-weight:700">原理</span>：向系统读取当前的"日历时间"（Unix 时间戳），换算成秒返回。它只精确到**秒**，所以同一秒内连续调用会拿到同一个数——这正是"两次 `srand` 随机数一样"的根源。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
srand((unsigned)time(NULL));       /* ① 最典型用法：播种 */
time_t now = time(NULL);           /* ② 拿当前时间戳 */
printf("%lld\n", (long long)now);  /* ③ 打印 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **用它做"高精度计时"**：只到秒，测代码耗时要用 `clock`。
- **同一秒内多次取**：值相同，不能用来生成不同种子。
- **打印格式**：`time_t` 可能是 `long long`，用 `%lld` 并强转最稳。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **为什么随机数要用它做种子？** 每次运行时间不同 → 种子不同 → 序列不同。
- **1970 年是什么？** Unix 纪元起点，所有时间戳都相对它计数。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`time` = 时间戳**，精确到秒。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`difftime` —— 两个时间差</span> <a id="fn-difftime"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：算两个 `time_t` 之间差了多少**秒**（浮点）。

<span style="color:#5F7F63;font-weight:700">原型</span>：`double difftime(time_t end, time_t begin);`（`#include <time.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`double` 返回 → 秒差（浮点）｜`difftime` 函数名｜`time_t end` 结束时间｜`time_t begin` 起始时间（**顺序不能反**）

| 项目 | 说明 |
| --- | --- |
| 参数 | 结束、开始（注意顺序） |
| 返回 | `end - begin` 的秒数 |
| 失败场景 | 无 |
| 关键点 | 返回 `double`，可表示小数秒（虽然 `time` 只有整秒） |

<span style="color:#5F7F63;font-weight:700">原理</span>：内部就是 `end - begin`，但用浮点返回，避免不同平台上 `time_t` 类型差异带来的问题。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
time_t t1 = time(NULL);
/* ... 一段耗时操作 ... */
time_t t2 = time(NULL);
printf("耗时 %.0f 秒\n", difftime(t2, t1));   /* ① 结束在前 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **参数顺序反了**：得到负数。
- **用它测短耗时**：`time` 只有秒，小于 1 秒会得到 0。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **测很短的时间用什么？** `clock()`（CPU 时间）或系统高精度计时器。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`difftime` = difference of time**，大减小。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`clock` —— 测代码耗时</span> <a id="fn-clock"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：返回程序消耗的 **CPU 时钟滴答数**，除以 `CLOCKS_PER_SEC` 就是秒。

<span style="color:#5F7F63;font-weight:700">原型</span>：`clock_t clock(void);`（`#include <time.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`clock_t` 返回 → 滴答数（整数）｜`clock` 函数名｜`void` → 无参数

| 项目 | 说明 |
| --- | --- |
| 参数 | 无 |
| 返回 | 从程序启动起消耗的 CPU 滴答数 |
| 换算 | 秒 = `clock() / CLOCKS_PER_SEC` |
| 失败场景 | 不可用时返回 -1 |

<span style="color:#5F7F63;font-weight:700">原理</span>：读的是**进程消耗的 CPU 时间**，不是墙上时钟。所以程序睡眠、等输入时它不走；测算法快慢它比 `time` 精确得多（通常毫秒级）。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
clock_t start = clock();
for (int i = 0; i < 1000000; i++) { /* 被测代码 */ }
clock_t end = clock();
printf("耗时 %.3f 秒\n", (double)(end - start) / CLOCKS_PER_SEC);
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **直接打印 `clock()`**：那是滴答数不是秒，必须除 `CLOCKS_PER_SEC`。
- **拿它测"等待时间"**：等待时 CPU 没干活，它不走。
- **整数除法**：`(end - start) / CLOCKS_PER_SEC` 会先整除，要强转 `double`。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **`clock` 和 `time` 的区别？** `time` 是墙上时间（秒），`clock` 是 CPU 时间（更细）。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`clock` = CPU 的秒表**，只算干活的时间。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`localtime` —— 秒数转年月日</span> <a id="fn-localtime"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：把时间戳拆成年、月、日、时、分、秒。

<span style="color:#5F7F63;font-weight:700">原型</span>：`struct tm* localtime(const time_t* timer);`（`#include <time.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`struct tm*` 返回 → 指向**静态结构体**的指针｜`localtime` 函数名｜`const time_t* timer` 参数 → 时间戳的**地址**（要 `&now`）

| 项目 | 说明 |
| --- | --- |
| 参数 | 时间戳地址（不是值） |
| 返回 | `struct tm*`，成员含 `tm_year`（年份-1900）、`tm_mon`（0~11）等 |
| 失败场景 | 时间超出范围返回 `NULL` |
| 关键点 | **年月都要加偏移**：`tm_year + 1900`、`tm_mon + 1` |

<span style="color:#5F7F63;font-weight:700">原理</span>：把秒数按本地时区换算成日历字段，填进一个**库内部静态**的 `struct tm`，返回它的地址。因为是静态的，下一次调用会覆盖上一次的内容。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
time_t now = time(NULL);
struct tm* t = localtime(&now);    /* ① 传地址 */
printf("%d-%02d-%02d\n", t->tm_year + 1900, t->tm_mon + 1, t->tm_mday);  /* ② 加偏移 */
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **传值不传地址**：`localtime(now)` 类型不对。
- **忘了 `+1900` / `+1`**：年份显示成 126 年，月份少 1。
- **把返回值存起来晚点用**：静态缓冲区会被下次调用覆盖。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **`tm_mon` 为什么从 0 开始？** 历史设计，月份 0~11，所以显示要 `+1`。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**拆时间戳**，年要加 1900、月要加 1。

### <span style="display:block;color:#5F7F63;border-left:3px solid #7FA182;padding-left:10px;margin-top:34px">`strftime` —— 时间格式化</span> <a id="fn-strftime"></a>

<span style="color:#5F7F63;font-weight:700">一句话</span>：把 `struct tm` 按格式串转成字符串。

<span style="color:#5F7F63;font-weight:700">原型</span>：`size_t strftime(char* s, size_t max, const char* format, const struct tm* tm);`（`#include <time.h>`）

<span style="color:#5F7F63;font-weight:700">原型拆解</span>：`size_t` 返回 → 写入了多少字符（0 表示放不下）｜`strftime` 函数名｜`char* s` 输出缓冲｜`size_t max` 缓冲大小｜`const char* format` 格式串（`%Y-%m-%d` 等）｜`const struct tm* tm` 时间结构

| 项目 | 说明 |
| --- | --- |
| 参数 | 缓冲、大小、格式、时间 |
| 返回 | 写入字符数；**0 表示缓冲区不够** |
| 失败场景 | 缓冲太小、格式不认识 |
| 关键点 | 有长度限制，比 `sprintf` 安全 |

<span style="color:#5F7F63;font-weight:700">原理</span>：扫描格式串，把 `%Y`（四位年）、`%m`（月）、`%d`（日）、`%H`（时）等占位符替换成对应字段，写进缓冲并补 `'\0'`。写满 `max` 就停并返回 0。

<span style="color:#5F7F63;font-weight:700">常用写法</span>

```c
char buf[64];
time_t now = time(NULL);
struct tm* t = localtime(&now);
if (strftime(buf, sizeof(buf), "%Y-%m-%d %H:%M:%S", t) > 0)
    printf("%s\n", buf);
```

<span style="color:#B87A5C;font-weight:700">易错点</span>

- **缓冲区太小**：返回 0，且内容不可靠。
- **格式符大小写**：`%m` 是月、`%M` 是分；`%H` 时、`%h` 可能是月名。
- **对 `time_t` 直接格式化**：必须先 `localtime` 转成 `struct tm`。

<span style="color:#6E93B5;font-weight:700">相关知识点 / 我曾问过</span>

- **它和 `sprintf` 的区别？** `strftime` 有缓冲区大小参数，更安全。

<span style="color:#A08050;font-weight:700">记忆钩子</span>：**`strftime` = string format time**，时间版 `sprintf`。

## <span style="color:#7FA182">7. assert.h / limits.h / errno.h —— 三个小头文件</span> <a id="sec84"></a>

| 头文件 | 里面有什么 | 怎么用 |
| --- | --- | --- |
| `assert.h` | `assert(表达式)` | 表达式为假时**打印文件名+行号并终止**；`#define NDEBUG` 可整体关掉（发布版常用） |
| `limits.h` | `INT_MAX` `INT_MIN` `CHAR_MAX` `CHAR_MIN` `SHRT_MAX` `LONG_MAX` `CHAR_BIT` | 判溢出：`if (n > INT_MAX - m)`；`CHAR_BIT` 是"一字节几位"（8） |
| `errno.h` | `errno` + `EDOM`（定义域错）`ERANGE`（超出范围） | 函数失败后查 `errno`，再用 `strerror(errno)` 翻译成人话 |

```c
#include <assert.h>
assert(p != NULL);          /* 调试期：p 为空就当场报"哪个文件第几行" */

#include <limits.h>
if (a > INT_MAX - b) { /* 加法会溢出，提前拦 */ }

#include <errno.h>
#include <string.h>
double d = strtod("1e999", NULL);   /* 超出范围 */
if (errno == ERANGE) printf("超出范围：%s\n", strerror(errno));
```

- `assert` **只在 Debug 生效**（Release 自动失效），所以不能把"必须执行的逻辑"写进 `assert`；
- `SIZE_MAX` 在 `<stdint.h>`；`INT_MAX` 约 21 亿（`2^31-1`）。

---

## <span style="color:#7FA182">8. 头文件地图 & 按需求找函数</span> <a id="sec85"></a>

### <span style="color:#7FA182">8.1 我要做这件事 → 用哪个函数</span>

| 需求 | 函数 | 头文件 |
| --- | --- | --- |
| 读一个整数 / 一行 / 一个单词 | `scanf("%d")` / `fgets` / `scanf("%s")` | stdio.h |
| 输出格式化内容 | `printf` / `fprintf` / `sprintf` | stdio.h |
| 读整行（安全） | `fgets`（记得剪 `\n`） | stdio.h |
| 求长度 / 复制 / 拼接 / 比较 | `strlen` `strcpy` `strcat` `strcmp` | string.h |
| 找子串 / 找字符 / 切分 | `strstr` `strchr` `strtok` | string.h |
| 整块内存清零 / 复制 / 比较 | `memset` `memcpy` `memcmp` | string.h |
| 动态数组 | `malloc` `realloc` `free` | stdlib.h |
| 排序 / 查找 | `qsort` / `bsearch` | stdlib.h |
| 随机数 | `srand` `rand` + `time` | stdlib.h + time.h |
| 绝对值 / 平方根 / 幂 / 取整 | `abs` `sqrt` `pow` `ceil/floor` | stdlib.h / math.h |
| 判字符类型 / 大小写转换 | `isalpha` `isdigit` `toupper` | ctype.h |
| 文件读写 | `fopen` `fclose` `fgetc` `fread` | stdio.h |
| 计时 | `clock` + `CLOCKS_PER_SEC` | time.h |
| 调试断言 / 查极限值 / 查错误码 | `assert` / `INT_MAX` / `errno` | assert.h / limits.h / errno.h |

### <span style="color:#7FA182">8.2 忘 include 会怎样</span>

- **`implicit declaration of function`（C4013）**：编译器没见过这个函数，默认它返回 `int`——参数/返回值一变就出错；
- **`C3861 找不到标识符`**：名字拼错，或头文件没包含；
- **口诀**：**"用到谁，先想它住哪个头文件"**——stdio / string / stdlib / math / ctype / time 六个够用很久。

> [⬆ 回到目录](#sec0)

---
# <span style="color:#9A87B5">第四部分　常用但不容易背的知识点</span>

## <span style="color:#9A87B5">4.1 格式说明符 `%`</span> <a id="p4-1"></a>

> 一条公式：`% [flags] [width] [.precision] [length] 转换字符`

**转换字符**

| 字符 | 打印/读取什么 | 例子 |
| --- | --- | --- |
| `%d` / `%i` | 有符号十进制整数 | `printf("%d", -5)` |
| `%u` | 无符号十进制 | `printf("%u", 4000000000u)` |
| `%o` / `%x` / `%X` | 八进制 / 十六进制（小写/大写） | `printf("%X", 255)` → `FF` |
| `%c` | 单个字符 | `printf("%c", 'A')` |
| `%s` | 字符串（要**地址**） | `printf("%s", name)` |
| `%f` / `%e` / `%g` | 浮点：普通 / 科学计数 / 自动选短 | `printf("%.2f", 3.14159)` |
| `%p` | 指针地址 | `printf("%p", (void*)p)` |
| `%%` | 一个百分号本身 | `printf("100%%")` → `100%` |
| `%n` | 把已输出字符数写回变量 | **禁用**（安全漏洞） |

**scanf 独有的三种写法**

| 写法 | 含义 | 例 |
| --- | --- | --- |
| `%5s` | **最多读 5 个字符**（宽度 = 上限，与 printf 相反） | `char b[6]; scanf("%5s", b);` |
| `%*d` | 读进来但**丢掉**（赋值抑制），不占参数 | `scanf("%*d %d", &b);` 跳过第一个数 |
| `%[^\n]` | **扫描集**：读除换行外的整行 | `scanf(" %99[^\n]", s);` 前导空格跳空白 |

**长度修饰符（决定读/写几字节）**

| 修饰 | 配对类型 | printf | scanf |
| --- | --- | --- | --- |
| `hh` | char | `%hhd` | `%hhd` |
| `h` | short | `%hd` | `%hd` |
| 空 | int / unsigned | `%d` / `%u` | `%d` / `%u` |
| `l` | long（整数）/ double（scanf 浮点） | `%ld`；`%f` 或 `%lf` 都行 | `%ld`；**`%lf` 必须** |
| `ll` | long long | `%lld` / `%llu` | 同左 |
| `z` | **size_t** | **`%zu`** | **`%zu`** |
| `t` | ptrdiff_t | `%td` | `%td` |
| `L` | long double | `%Lf` | `%Lf` |

**printf 与 scanf 最不对称的一处**

| | float | double | long double |
| --- | --- | --- | --- |
| printf | `%f` | `%f`（`%lf` 也行） | `%Lf` |
| scanf | `%f` | **`%lf` 必须** | `%Lf` |

原因：printf 是可变参数，float 会自动提升成 double；scanf 拿的是地址，必须靠格式串区分写 4 还是 8 字节。

## <span style="color:#9A87B5">4.2 转义字符</span> <a id="p4-2"></a>

| 写法 | 含义 | 写法 | 含义 |
| --- | --- | --- | --- |
| `\n` | 换行 | `\\` | 一个反斜杠 |
| `\t` | 制表（对齐） | `\"` | 双引号 |
| `\r` | 回车（回行首） | `\'` | 单引号 |
| `\0` | 空字符（字符串结束符） | `\a` | 响铃 |
| `\b` | 退格 | `\f` | 换页 |
| `\v` | 垂直制表 | `\x41` | 十六进制 0x41 = `'A'` |
| `\101` | 八进制 101 = `'A'` | `%%` | printf 里输出 `%` |

> 路径要写双反斜杠 `"C:\\test\\a.txt"`，或直接用正斜杠 `"C:/test/a.txt"`；`'\0'` 的值是 0，所以 `if ('\0')` 为假。

## <span style="color:#9A87B5">4.3 ASCII 常用值</span> <a id="p4-3"></a>

| 字符 | 编码 | 记法 |
| --- | --- | --- |
| `'\0'` | 0 | 字符串结束符 |
| `'\n'` | 10 | 换行 |
| `' '` | 32 | 空格 |
| `'0'` ~ `'9'` | 48 ~ 57 | 数字字符**连续** 10 个 |
| `'A'` ~ `'Z'` | 65 ~ 90 | 大写连续 |
| `'a'` ~ `'z'` | 97 ~ 122 | 小写连续 |

三条必用结论：
1. 判断数字用 `ch >= '0' && ch <= '9'`（**不能**和整数 0、9 比）；
2. 大小学差 **32**：`ch - 32` 变小写→大写，`ch + 32` 反过来；
3. 数字字符转数值：`ch - '0'`；数值转字符：`n + '0'`。

## <span style="color:#9A87B5">4.4 类型与范围</span> <a id="p4-4"></a>

| 类型 | 典型大小（VS/x64） | 范围 | 格式 |
| --- | --- | --- | --- |
| `char` | 1 | -128 ~ 127（VS 有符号） | `%c` / `%hhd` |
| `unsigned char` | 1 | 0 ~ 255 | `%hhu` |
| `short` | 2 | -32768 ~ 32767 | `%hd` |
| `int` | 4 | -2147483648 ~ 2147483647 | `%d` |
| `unsigned` | 4 | 0 ~ 4294967295 | `%u` |
| `long` | Windows 4 / Linux 8 | 看平台 | `%ld` |
| `long long` | 8 | 约 ±9.2×10¹⁸ | `%lld` |
| `float` | 4 | 约 ±3.4×10³⁸（7 位有效） | `%f` |
| `double` | 8 | 约 ±1.8×10³⁰⁸（15 位有效） | `%lf`（scanf） |
| `size_t` | 4 或 8 | 无符号 | `%zu` |

**溢出规则**
- **有符号溢出是未定义行为**（可能变负数，也可能被优化掉）；
- **无符号溢出是"绕圈"**：`0u - 1` = 4294967295；
- `char c = 127; c = c + 1;` → 整型提升后截断成 -128；
- `-INT_MIN` 还是负数（补码里最小值没有对应正数）；
- **无符号倒序循环是死循环**：`for (unsigned i = n-1; i >= 0; i--)`。

**常见 `sizeof` 结果（32/64 位下都成立的）**

| 表达式 | 结果 |
| --- | --- |
| `sizeof(char)` / `sizeof(unsigned char)` | 1 |
| `sizeof(short)` | 2 |
| `sizeof(int)` / `sizeof(float)` | 4 |
| `sizeof(double)` / `sizeof(long long)` | 8 |
| `sizeof('A')` | **4**（字符常量在 C 里是 int） |
| `sizeof("A")` | **2**（`'A'` + `'\0'`） |
| `sizeof(int[5])` | 20 |
| `sizeof(char[10])` | 10 |
| `sizeof(指针)` | 4 或 8（看平台） |

**一条铁律**：不要背字节数，用 `sizeof` 量。

## <span style="color:#9A87B5">4.5 运算符优先级（够用版）</span> <a id="p4-5"></a>

| 级别 | 运算符 | 结合性 |
| --- | --- | --- |
| 1 | `()` `[]` `.` `->` | 左 |
| 2 | `!` `~` `++`(前置) `--`(前置) `+`(正) `-`(负) `*`(解引用) `&`(取地址) `sizeof` | **右** |
| 3 | `*` `/` `%` | 左 |
| 4 | `+` `-` | 左 |
| 5 | `<<` `>>` | 左 |
| 6 | `<` `<=` `>` `>=` | 左 |
| 7 | `==` `!=` | 左 |
| 8 | `&`（位与） | 左 |
| 9 | `^` | 左 |
| 10 | `\|`（位或） | 左 |
| 11 | `&&` | 左（短路） |
| 12 | `\|\|` | 左（短路） |
| 13 | `?:` | **右** |
| 14 | `=` `+=` `-=` … | **右** |
| 15 | `,` | 左 |

三条实战结论：
- **`*p++` = `*(p++)`**（后置 `++` 比 `*` 高）；
- **`a = b = c` 从右往左**，所以能连等；
- **`if (a = b)` 是赋值**，编译器只给警告（C4553）。

**只有四个顺序点**：`&&`、`||`、`?:`、`,`

```c
printf("%d %d\n", a++, a++);   /* ✗ 未定义行为：同一变量又读又改两次 */
```

**除法与取余的符号**

```c
5 / 2   /* 2   整数除法直接砍小数 */
-7 / 2  /* -3  向零取整 */
-7 % 2  /* -1  余数符号跟被除数走 */
```

## <span style="color:#9A87B5">4.6 位运算技巧</span> <a id="p4-6"></a>

| 运算符 | 含义 | 典型用法 |
| --- | --- | --- |
| `&` | 位与 | `n & 1` 取最低位（判奇偶） |
| `\|` | 位或 | `x \| (1<<k)` 把第 k 位置 1 |
| `^` | 位异或 | 相同得 0、不同得 1；`a^a=0`、`a^0=a` |
| `~` | 按位取反 | `~0` = -1（全 1） |
| `<<` | 左移 | `n << 1` ≈ ×2，右边补 0 |
| `>>` | 右移 | `n >> 1` ≈ ÷2；负数算术右移补符号位 |

**五个常用技巧**

```c
n & 1                  /* 判奇偶：1 奇、0 偶 */
n = n & (n - 1)        /* 消掉最右边那个 1（数 1 的个数） */
n & (n - 1) == 0       /* 判是不是 2 的幂（n > 0） */
a ^= b; b ^= a; a ^= b;/* 不用临时变量交换（同一地址会清零，可读性差） */
x | (1 << k)           /* 把第 k 位置 1；x & ~(1<<k) 清 0 */
```

注意事项：
- 位运算只能用于**整型**（`float` 不行）；
- 移位**不改原变量**，要 `a = a >> 1;`；
- 左移负数、移位数 ≥ 宽度都是未定义行为。

## <span style="color:#9A87B5">4.7 返回值与宏约定</span> <a id="p4-7"></a>

| 记号 | 值 | 谁返回它 |
| --- | --- | --- |
| `EOF` | -1 | `fgetc` / `getchar` / `scanf` 失败 |
| `NULL` | 0（空指针） | `fopen` / `malloc` / `fgets` / `strstr` 失败 |
| `'\0'` | 0 | 字符串结束符 |
| `SEEK_SET / CUR / END` | 0 / 1 / 2 | `fseek` 的基点 |
| `stdin / stdout / stderr` | 三个 `FILE*` 宏 | 标准流 |
| `RAND_MAX` | VS 下 32767 | `rand()` 的上限 |
| `CLOCKS_PER_SEC` | 1000（VS） | `clock()` 换算成秒 |
| `EXIT_SUCCESS / EXIT_FAILURE` | 0 / 非 0 | `exit()` 的规范写法 |
| `BUFSIZ` | 实现定义（常见 512/4096） | 默认缓冲区大小 |
| `INT_MAX / INT_MIN` | 2147483647 / -2147483648 | `<limits.h>` |

**"0" 有三种含义，看函数**

| 返回值 0 表示 | 函数 |
| --- | --- |
| **成功** | `fclose` `fflush` `fseek` `remove` `rename` `strcmp`（相等） |
| 条件不成立 | `feof` `ferror` |
| 一项都没读到 | `fscanf` `fread` |

**常用返回类型速记**
- `strlen` / `sizeof` / `fread` → **无符号**（`%zu`）；
- `strcmp` / `memcmp` → **差值**（判等写 `== 0`）；
- `malloc` / `realloc` / `fopen` / `fgets` / `strstr` → **指针**（失败是 `NULL`）；
- `qsort` / `free` / `srand` → `void`；
- `scanf` / `fscanf` / `sscanf` → **成功项数**。

## <span style="color:#9A87B5">4.8 编译错误码速查</span> <a id="p4-8"></a>

| 编号 | 真实含义 | 先查什么 |
| --- | --- | --- |
| **C4996** | `scanf`/`strcpy` 被判"不安全" | 文件第一行加 `#define _CRT_SECURE_NO_WARNINGS` |
| **C4700** | 使用了未初始化变量 | 声明时 `= 0` |
| **C2133 / C2466** | 数组大小不是常量 | 用 `#define` 或字面量 |
| **E0169 应输入声明** | 上一段结构没闭合 | 往上找第一处不配对 |
| **C2449 / C2059** | 文件范围内出现 `{` / 语法错误 | 函数定义**末尾多了分号** |
| **C3861** | 找不到标识符 | 拼写、没 include、定义在调用之后 |
| **C4553** | `==` 结果没被使用 | `=` 和 `==` 写反了 |
| **C4477 / C4473** | 格式符与参数类型/个数不匹配 | 数占位符 + 对类型 |
| **C4013** | 隐式声明（没见过这个函数） | 没 include、或定义在调用之后 |
| **C4047 / C4024** | 间接级别 / 形参类型不兼容 | 单引号改双引号？数组名多写 `&`？ |
| **C4133** | 类型不兼容（`char*` 传给 `char(*)[N]`） | 数组名多写 `&`？形参第二维漏写？ |
| **C2106 / E0137** | `=` 左边不是左值 | 优先级把 `A \|\| b = c` 粘歪了，补回运算符 |
| **C2296 / C2297** | `%` 操作数类型无效 | 浮点不能用 `%`，先转整型或用 `fmod` |
| **C2374** | 重定义、多次初始化 | 同一作用域同名变量只能声明一次 |
| **C2371 / C2556** | 重定义 / 签名不一致 | 同名函数写了两遍、声明与定义参数不同 |
| **C6385 / C6386** | 读/写越界（静态分析） | 下标上界、`<=` 写成 `<` |
| **C6001** | 使用未初始化内存 | 先清零 |
| **C6262** | 栈用量过大 | 大数组改全局或 `malloc` |
| **C4715** | 不是所有路径都返回值 | 每条路都要 `return` |
| **C2601** | 局部函数定义 | 函数套进别的函数里了 |
| **LNK2019** | 只有声明没有定义 | 函数体写了吗、文件加进工程了吗 |
| **LNK1168 / LNK1104** | 无法写 exe | 旧程序还在运行，结束进程 |
| **0xC00000FD** | 栈溢出 | 递归太深 / 局部数组太大 |
| **0xC0000005** | 访问冲突 | 空指针、野指针、越界、`free` 后再用 |

**读报错三条习惯**
1. **从第一条开始修**（后面的常是连锁反应）；
2. 先看**报错行往上 3 行**；
3. 改完**重新编译**再看列表（列表可能是上一次的残留）。

## <span style="color:#9A87B5">4.9 复杂声明读法</span> <a id="p4-9"></a>

口诀：**从名字往外读，先右后左；括号里的是指针，没括号的是数组。**

| 写法 | 读法 | 大小（32/64 位） |
| --- | --- | --- |
| `int* p[5]` | 指针数组：5 个 `int*` | 20 / 40 |
| `int (*p)[5]` | 数组指针：指向"5 个 int 的数组" | 4 / 8 |
| `int (*pf)(int, int)` | 函数指针 | 4 / 8 |
| `int (*t[2])(int, int)` | 函数指针数组（转移表） | 8 / 16 |
| `char** argv` | 指向"char*"的指针 = 字符串数组 | 4 / 8 |
| `int* (*p)[10]` | `p` 是指针 → 指向"10 个 `int*` 的数组" | 4 / 8 |
| `char* (*p[4])(int)` | `p` 是 4 元素数组 → 每个元素是"参数 int、返回 `char*` 的函数指针" | 16 / 32 |

配套三条：
- **`p + 1` 的跨度 = 去掉一个 `*` 后的类型大小**（`int(*)[5]` 跨 20 字节）；
- **函数名就是地址**：`fp = Add;` 之后 `fp(2,3)` 与 `(*fp)(2,3)` 等价；
- **函数指针数组 = 转移表**，可以替掉长长的 `switch`。

## <span style="color:#9A87B5">4.10 结构体内存对齐</span> <a id="p4-10"></a>

**三条规则**
1. 每个成员的偏移必须是**自身大小**的整数倍，不够就插填充；
2. 结构体总大小必须是**最大成员宽度**的整数倍；
3. 嵌套结构体按它自己内部最大对齐算。

| 声明 | 大小 | 过程 |
| --- | --- | --- |
| `struct { char a; int b; char c; }` | **12** | a@0，填充 3，b@4~7，c@8，补 3 到 12 |
| `struct { char a; char b; int c; }` | **8** | a@0，b@1，填充 2，c@4~7 |
| `struct { int a; char b; }` | **8** | a@0~3，b@4，补 3 到 8 |

**两个扩展**
- `#pragma pack(1)`：取消填充，上面第一个变 6（省空间但可能变慢）；
- `offsetof(struct S, b)`：求成员偏移（`<stddef.h>`），配合"用地址减"可验证对齐。

**省空间技巧**：把**小成员排在前面**、大成员排后面，能少插填充。

## <span style="color:#9A87B5">4.11 输出格式技巧</span> <a id="p4-11"></a>

```c
printf("%5d|", 42);        /* "   42|"   右对齐，总宽 5 */
printf("%-5d|", 42);       /* "42   |"   左对齐 */
printf("%05d|", 42);       /* "00042|"   补 0 */
printf("%+d %+d", 5, -5);  /* "+5 -5"    强制带符号 */
printf("%8.2f|", 3.14159); /* "    3.14|" 总宽 8、2 位小数 */
printf("%.3s|", "hello");  /* "hel|"     只打前 3 个字符 */
printf("%-10s|", "ab");    /* "ab        |" 表格对齐神器 */
```

| 需求 | 写法 | 备注 |
| --- | --- | --- |
| 保留 2 位小数 | `%.2f` | `%f` 默认 6 位 |
| 去掉多余的 0 | `%g` | 4.321 → `4.321` |
| 十六进制大写带前缀 | `%#X` | 255 → `0XFF` |
| 补前导 0 | `%04d` | 7 → `0007` |
| 打印地址 | `%p` | 配合 `(void*)` 更规范 |
| 打印 size_t | `%zu` | 别用 `%d` |
| 表格列对齐 | `%-10s` | 比手打空格稳 |

> **width 是最小宽度**（内容更长就撑破）；`%8.2f` 里的 8 **含小数点**；scanf 里 width 的含义相反——是"最多读几个"（`%5s`）。

---

## <span style="color:#9A87B5">4.12 补码 · 大小端 · IEEE 754</span> <a id="p4-12"></a>

### 补码（整数在内存里长什么样）

| 情况 | 规则 | 例子（8 位） |
| --- | --- | --- |
| 正数 | 原码 = 反码 = 补码 | `5` = `0000 0101` |
| 负数 | 反码 = 符号位不变、其余取反；补码 = 反码 + 1 | `-5`：`1000 0101` → `1111 1010` → `1111 1011` |

- **内存里存的永远是补码**（不是原码）；
- 所以 `char c = 127; c = c + 1;` → **-128**（`0111 1111` + 1 = `1000 0000`）；
- 补码让"减法变成加法"，也让 0 只有一个表示；
- `-INT_MIN` 还是负数（最小值没有对应的正数）。

### 大小端

| 名词 | 含义 | 谁 |
| --- | --- | --- |
| 小端 | **低**字节放**低**地址 | x86 / VS（最常见） |
| 大端 | 高字节放低地址 | 部分嵌入式、网络字节序 |

判断三行（背下来）：

```c
int i = 1;
char* p = (char*)&i;
printf("%d\n", *p);   /* 1 = 小端，0 = 大端 */
```

### IEEE 754（float 怎么存）

```text
float（4 字节）= 1 位符号 S + 8 位阶码 E + 23 位尾数 M

值 = (-1)^S × 1.M × 2^(E-127)
```

手算 `5.5`：

| 步骤 | 结果 |
| --- | --- |
| 5.5 → 二进制 | `101.1` |
| 规格化 | `1.011 × 2²` |
| 阶码 E = 2 + 127 | 129 = `1000 0001` |
| 尾数 M（去掉前导 1） | `0110000…`（补满 23 位） |
| 拼起来 | `0 10000001 0110000…` = **0x40B00000** |
| 小端机器上按字节看 | `00 00 B0 40` |

三条结论：
- **浮点不精确**：0.1、0.4 在二进制里是无限循环，只能存近似值；
- **判等用 `fabs(a-b) < 1e-6`**，不要写 `a == b`；
- `(int)3.9 == 3`（向 0 截断），转整型取位前先 `+0.5` 四舍五入。

## <span style="color:#9A87B5">4.13 预处理</span> <a id="p4-13"></a>

**四个指令**

| 指令 | 作用 |
| --- | --- |
| `#include` | 把另一个文件的内容整段搬进来（纯文本粘贴） |
| `#define` | 宏定义（文本替换），`#undef` 取消 |
| `#if / #ifdef / #ifndef / #else / #elif / #endif` | 条件编译 |
| `#pragma` | 编译器相关（`#pragma once`、`#pragma pack(1)`） |

**`#include <>` 与 `""` 的区别**

| 写法 | 查找顺序 |
| --- | --- |
| `#include <stdio.h>` | 只找**系统/编译器**的头文件目录 |
| `#include "my.h"` | **先找当前目录**，找不到再找系统目录 |

**宏的四条铁律**

```c
#define MAX 100
#define SQUARE(x) ((x)*(x))          /* 参数和整体都要括号 */
#define SWAP(a, b) do { int t = (a); (a) = (b); (b) = t; } while (0)
#define STR(x) #x                    /* # 把参数变字符串 */
#define CAT(a, b) a##b               /* ## 把两个标识符粘成一个 */
```

1. 宏是**文本替换**，没有类型、不做检查；
2. 参数必须加括号：`SQUARE(1+1)` 不加括号会变成 `1+1*1+1` = 3；
3. 多语句宏用 `do { ... } while (0)` 包起来，否则在 `if/else` 里会断句；
4. 宏名习惯全大写，且**末尾不加分号**。

**预定义宏（调试常用）**

| 宏 | 值 |
| --- | --- |
| `__FILE__` | 当前源文件名 |
| `__LINE__` | 当前行号 |
| `__DATE__` / `__TIME__` | 编译日期 / 时间 |
| `__STDC__` | 是否遵循标准 C |

**`offsetof` 宏（自己实现一遍就懂了）**

```c
#define MY_OFFSETOF(type, member) ((size_t)&(((type*)0)->member))
```

思路：假装 0 地址处有一个该结构体，取成员的地址，那个地址就是**偏移量**。

**防重复包含（头文件的标配）**

```c
#ifndef MY_H
#define MY_H
/* 内容 */
#endif
```

## <span style="color:#9A87B5">4.14 存储类别与内存分区</span> <a id="p4-14"></a>

**四种存储类别**

| 关键字 | 位置 | 生命周期 | 说明 |
| --- | --- | --- | --- |
| `auto` | 栈 | 出块即销毁 | 局部变量默认，几乎不写 |
| `static` | 静态区 | **整个程序** | 局部：只初始化一次、值保留；全局：**只在本文件可见** |
| `extern` | — | — | 声明"这个变量/函数在别的文件里定义" |
| `register` | 建议放寄存器 | 出块即销毁 | 只是个建议，现代编译器基本忽略 |

**`static` 的三张脸（最常考）**
1. 修饰**局部变量** → 寿命变长（函数返回后值还在）；
2. 修饰**全局变量** → 作用域缩到本文件；
3. 修饰**函数** → 只能本文件调用。

**内存五区**

| 区 | 放什么 | 谁回收 | 特点 |
| --- | --- | --- | --- |
| 栈 stack | 局部变量、函数参数、返回地址 | 系统自动 | 很小（几 MB），向下生长 |
| 堆 heap | `malloc/calloc/realloc` | **手动 `free`** | 大，向上生长，会碎片化 |
| 静态区（.data/.bss） | 全局变量、`static` 变量 | 程序结束 | 未初始化的在 .bss（自动为 0） |
| 常量区 | 字符串字面量、`const` 全局 | 只读 | 写它会崩（0xC0000005） |
| 代码区 | 编译后的机器指令 | 只读 | — |

推论：
- **大数组别放 `main` 里**（栈装不下 → 0xC00000FD）；
- 全局数组**自动清零**，局部数组**不清零**（垃圾值）；
- `char* s = "abc"; s[0] = 'x';` 崩，因为字面量在常量区。

**函数栈帧（一句话版，够应付面试题）**

| 事实 | 结论 |
| --- | --- |
| 栈向**低地址**生长，`push` 让 `esp` 减 4 | 先压的落在高地址 |
| 参数**从右往左**压 | 第一个形参在 `[ebp+8]`、第二个在 `[ebp+12]` |
| `[ebp]` 存旧 ebp、`[ebp+4]` 存返回地址 | 这两格是"过路费" |
| 局部变量在 `[ebp-4]` 往下 | 所以局部变量的地址比参数小 |
| 函数返回后栈帧销毁，但内存不擦 | 未初始化的局部变量是**上一轮残留**（Debug 版填 `0xCC`） |

**动态内存四件套 + 四类错误**

```c
int* p = malloc(n * sizeof(int));      /* ① 申请 */
if (p == NULL) return 1;               /* ② 验货 */
int* t = realloc(p, 2 * n * sizeof(int));
if (t != NULL) p = t;                  /* ③ 扩容（先接临时指针） */
free(p);  p = NULL;                    /* ④ 释放并置空 */
```

| 错误 | 后果 | 怎么防 |
| --- | --- | --- |
| 忘 `free` | **内存泄漏**（程序越跑越胖） | 每个 `malloc` 配一个 `free` |
| `free` 后继续用 | **悬空指针**（UB，可能崩） | `free(p); p = NULL;` |
| `free` 两次 | 堆结构被破坏（崩溃） | 置空后第二次 `free(NULL)` 才安全 |
| 越界写 | 踩坏别人的数据（最隐蔽） | 下标 `< n`，`malloc` 大小乘 `sizeof` |

## <span style="color:#9A87B5">4.15 类型转换三步</span> <a id="p4-15"></a>

```text
① 整型提升：char / short 先"长成 int"再参加运算
② 寻常算术转换：向"更宽/更高级"的类型看齐
③ 赋值截断：算完再塞回小类型，高位直接砍掉
```

**① 整型提升**

```c
char c = 3 + 127;   /* 3+127=130 → 截断成 char → -126（有符号 char） */
```

有符号按符号位补，无符号补 0——这是 `char c = 200;` 变 -56 的根源。

**② 寻常算术转换的优先级**

```text
long double > double > float > unsigned long long > long long
> unsigned long > long > unsigned int > int
```

关键一条：**`int` 遇到 `unsigned` 会变成 `unsigned`**——这就是 `-1 > sizeof(i)` 成立的机理（`-1` 变成 4294967295）。

**③ 截断与浮点转整**

| 写法 | 结果 |
| --- | --- |
| `(int)3.9` | 3（向 0 截断，不是四舍五入） |
| `int n = 3.9;` | 3（隐式截断，可能给警告） |
| `(int)(x + 0.5)` | 四舍五入的正数写法 |
| `(double)a / b` | 先转再除，结果是小数 |
| `a / b * 1.0` | **错**：除法已经先截断了 |

## <span style="color:#9A87B5">4.16 struct / 位段 / enum / union</span> <a id="p4-16"></a>

| 类型 | 关键字 | 大小 | 访问 | 典型用途 |
| --- | --- | --- | --- | --- |
| 结构体 | `struct` | 各成员之和 + 填充（对齐） | `.` / `->` | 描述"一个东西的多个属性" |
| 位段 | `struct` + `int a:3;` | 按位分配 | 同结构体 | 省空间（协议头、标志位），**不可移植** |
| 枚举 | `enum` | 同 int | 直接用名字 | 给整数起有意义的名字（默认 0,1,2…） |
| 联合 | `union` | **最大成员**的大小 | `.` | 同一块内存"换个角度看"（判大小端、类型双关） |

**关键区别一句话**
- `struct` 各成员**各占一份**；
- `union` 所有成员**共用一块**，同一时刻只有一个有效。

**枚举**

```c
enum Color { RED, GREEN, BLUE };      /* 0, 1, 2 */
enum Flag  { OK = 200, ERR = 404 };   /* 可指定起始值 */
```

**联合判大小端（三行）**

```c
union U { int i; char c; } u;
u.i = 1;
printf("%c", u.c == 1 ? '小' : '大');   /* 小端：低字节在低地址 */
```

**位段**

```c
struct Flags { unsigned a : 1; unsigned b : 3; unsigned c : 4; };  /* 共 1 字节 */
```

注意：位段宽度不能超过类型宽度；不同编译器排布可能不同，**存档/跨平台数据别用位段**。

**结构体的两个必备语法**

```c
struct Node { int val; struct Node* next; };   /* 自引用必须用指针 */
struct Node n;  struct Node* p = &n;
n.val = 1;      /* 变量用 . */
p->val = 1;     /* 指针用 -> */
```

## <span style="color:#9A87B5">4.17 排序与查找</span> <a id="p4-17"></a>

| 算法 | 复杂度 | 稳定性 | 一句话 |
| --- | --- | --- | --- |
| 冒泡 | O(n²) | 稳定 | 相邻比较，大的往后沉，n-1 趟 |
| 选择 | O(n²) | 不稳定 | 每趟选出最小的放到前面 |
| 插入 | O(n²) | 稳定 | 像整理扑克牌，往前插 |
| 二分查找 | O(log n) | — | **必须有序**，每次砍一半 |
| `qsort` | O(n log n) | 不稳定 | 库函数，传比较函数 |

**冒泡（背这个就够）**

```c
for (i = 0; i < n - 1; i++)              /* n-1 趟 */
    for (j = 0; j < n - 1 - i; j++)      /* 每趟少比一个 */
        if (a[j] > a[j + 1]) { int t = a[j]; a[j] = a[j + 1]; a[j + 1] = t; }
```

**二分查找**

```c
int left = 0, right = n - 1;
while (left <= right) {
    int mid = left + (right - left) / 2;   /* 防溢出，别写 (l+r)/2 */
    if (a[mid] == key) return mid;
    else if (a[mid] < key) left = mid + 1;  /* 每轮必须收缩，否则死循环 */
    else right = mid - 1;
}
return -1;
```

**`qsort` 的三种比较函数**

```c
int cmp_int(const void* a, const void* b) {
    return *(const int*)a - *(const int*)b;          /* 升序；b-a 是降序 */
}
int cmp_str(const void* a, const void* b) {
    return strcmp(*(const char**)a, *(const char**)b);
}
int cmp_stu(const void* a, const void* b) {
    const struct Stu* x = a, *y = b;
    return y->score - x->score;                      /* 分数降序 */
}
qsort(arr, n, sizeof(arr[0]), cmp_int);
```

> 比较函数必须返回 **负 / 0 / 正**（别返回布尔值）；`n` 是元素个数、`size` 是每元素字节数。

## <span style="color:#9A87B5">4.18 刷题套路速查</span> <a id="p4-18"></a>

> 十四个模板，写题前先想"这是哪一套"。

**① 打擂台（找最大/最小）**

```c
int max = a[0];                 /* 擂主必须来自数组，别写 0 */
for (i = 1; i < n; i++)
    if (a[i] > max) max = a[i]; /* 结构体版记下标 maxIdx */
```

**② 双下标相向而行（反转 / 回文）**

```c
int l = 0, r = len - 1;
while (l < r) {                 /* 只比较就不交换：回文 */
    char t = s[l]; s[l] = s[r]; s[r] = t;   /* 反转 */
    l++; r--;
}
```

**③ 数组当桶（计数）**

```c
int cnt[26] = { 0 };            /* 必须清零 */
for (i = 0; s[i] != '\0'; i++)
    if (s[i] >= 'a' && s[i] <= 'z') cnt[s[i] - 'a']++;
for (i = 0; i < 26; i++)
    if (cnt[i]) printf("%c %d\n", 'a' + i, cnt[i]);
```

**④ 状态变量数单词（栅栏问题）**

```c
int count = 0, in_word = 0;
for (i = 0; s[i] != '\0'; i++) {
    if (isalpha((unsigned char)s[i])) { if (!in_word) { count++; in_word = 1; } }
    else in_word = 0;           /* 非字母才复位；不要用 break */
}
```

**⑤ 递归四模板**（顺序打印 / strlen / 斐波那契 / 反转 + 汉诺塔）

```c
void print_digits(int n) { if (n > 9) print_digits(n / 10); printf("%d ", n % 10); }
int my_strlen(char* s)   { return *s ? 1 + my_strlen(s + 1) : 0; }
int fib(int n)           { return n < 2 ? n : fib(n - 1) + fib(n - 2); }  /* 实战改迭代 */

void reverse(char* s, int l, int r) {         /* 区间类递归：反转字符串 */
    if (l >= r) return;                        /* 终点：相遇就停 */
    char t = s[l]; s[l] = s[r]; s[r] = t;
    reverse(s, l + 1, r - 1);
}

void hanoi(int n, char a, char b, char c) {   /* 汉诺塔：把 n 个从 a 借 b 挪到 c */
    if (n == 0) return;
    hanoi(n - 1, a, c, b);                     /* 先把上面 n-1 个挪到 b */
    printf("%c -> %c\n", a, c);                /* 把最大的挪到 c */
    hanoi(n - 1, b, a, c);                     /* 再把 n-1 个从 b 挪到 c */
}
```

> 递归三件套：**终点**（`n == 0` / `n < 2` / `*s == '\0'`）、**拆解**（把大问题变成同类小问题）、**每条路都 `return`**。

**⑥ 异或找落单**

```c
int r = 0;
for (i = 0; i < n; i++) r ^= a[i];   /* 成对抵消，剩下那个就是落单的 */
```

**⑦ 按"整个字符串"切分（`strstr`）**

```c
char* p = s;
while ((q = strstr(p, "abb")) != NULL) { /* 打印 [p, q) */ p = q + strlen("abb"); }
/* 剩下的 p 是最后一段 */
```

**⑧ 字符串替换（等长原地 / 变长新缓冲）**

```c
/* 等长：直接覆盖 */
for (i = 0; i + oldlen <= len; ) 
    if (!strncmp(s + i, old, oldlen)) { memcpy(s + i, new, oldlen); i += oldlen; }
    else i++;

/* 变长：另开一个数组，边扫边写，最后补 '\0' */
```

**⑨ 游戏主循环四件套**

```text
初始化 → while (1) { 打印棋盘 → 玩家落子(判合法/判占用) → 判赢/判满 → 电脑落子 → 判赢/判满 }
```

**⑩ 多文件工程骨架**

```
game.h   招牌（#ifndef 防重复包含 + 函数声明 + 宏）
game.c   后厨（#include "game.h" + 函数定义）
test.c   点单（main + 菜单 + 调用）
```

**⑪ 结构体数组 + 计数器（通讯录模型）**

```c
struct Contact { struct PeoInfo data[MAX]; int sz; };   /* 一排格子 + 一个计数器 */
/* 增：data[sz++] = x;   删：后面往前挪 + sz--;   查：遍历比 strcmp */
```

**⑫ 数字拆位（取每一位）**

```c
while (n > 0) {
    int d = n % 10;        /* 取最低位 */
    n /= 10;               /* 砍掉最低位 */
}
/* 要从高位开始？先递归 print_digits(n/10)，再打印 n%10 */
```

**⑬ 辗转相除求最大公约数**

```c
int gcd(int a, int b) {
    while (b) { int t = a % b; a = b; b = t; }   /* 终点：b == 0 */
    return a;
}
```

**⑭ 计数 / 累加 / 累乘三兄弟**

```c
int cnt = 0, sum = 0, prod = 1;   /* 计数和求和的初值是 0，累乘必须是 1 */
```

> 初值口诀：**加法从 0 出发、乘法从 1 出发、擂主从"第一个真数据"出发**。

## <span style="color:#9A87B5">4.19 VS 调试六件套</span> <a id="p4-19"></a>

**六个快捷键**

| 键 | 名字 | 干什么 |
| --- | --- | --- |
| **F9** | 切换断点 | 在光标行下/取消红点 |
| **F5** | 启动调试 | 跑到下一个断点（或结束） |
| **F10** | 逐过程 | 一行一行走，**不进函数** |
| **F11** | 逐语句 | 一行一行走，**进函数内部** |
| **Shift+F5** | 停止调试 | 结束这次调试（卡死时救命） |
| **Ctrl+F5** | 开始执行不调试 | 直接跑，不停断点 |

**五个窗口（调试 → 窗口）**

| 窗口 | 看什么 |
| --- | --- |
| 监视 / 自动 | 变量当前值（可输入表达式） |
| 局部变量 | 当前函数的局部变量 |
| 内存 | 按地址看原始字节（验证大小端、`0xCC`） |
| 调用堆栈 | 谁调用了谁（递归时看层数） |
| 断点 | 管理所有断点 |

**调试四步法**：**复现 → 定位（断点/打印）→ 假设（改哪里）→ 验证（改完重跑）**。

**两个新手常犯**
1. **Debug 与 Release 行为不同**：Release 会优化，未初始化变量、越界读写表现完全不一样——"Release 才对"往往说明代码有 UB；
2. 改完代码**没重新编译**就看错误列表/结果——列表可能是上一次的残留。

**三个"看一眼就定位"的信号**

| 现象 | 多半是 |
| --- | --- |
| 输出「烫烫烫」 | 打印了未初始化（`0xCC`）的内存 / 数据没读进去 |
| 窗口一闪而过，退出码 `0xC0000005` | 空指针、野指针、越界、`free` 后再用 |
| 退出码 `0xC00000FD` | 栈溢出：递归太深 / 局部数组太大 |

## <span style="color:#9A87B5">4.20 十组对照表</span> <a id="p4-20"></a>

**① `sizeof` vs `strlen`**

| | `sizeof` | `strlen` |
| --- | --- | --- |
| 本质 | **运算符**（编译期） | 函数（运行期） |
| 量什么 | **容量**（占多少字节） | **实际长度**（数到 `'\0'`） |
| 含 `'\0'` 吗 | **含** | 不含 |
| 返回类型 | `size_t` | `size_t` |
| 例：`char s[10] = "ab";` | 10 | 2 |

**② 数组名的三张面孔**

| 场合 | 代表 | 例（`int a[5];`） |
| --- | --- | --- |
| `sizeof(a)` | **整个数组** | 20 |
| `&a` | **整个数组的地址** | `&a + 1` 跨 20 字节 |
| 其他所有场合 | **首元素地址** | `a + 1` 跨 4 字节；`f(a)` 退化成指针 |

**③ 二维数组"行优先平铺"**

| 概念 | 说明 |
| --- | --- |
| 内存布局 | `a[0][0] a[0][1] … a[1][0] …` 一整条直线 |
| 行指针 | `int (*p)[4]` 才能跨整行（`p+1` 跨 16 字节） |
| 传参 | `void f(int a[][4])`——第一维可省、**第二维必须写** |

**④ 字符串字面量 vs 字符数组**

| | `char* s = "abc";` | `char s[] = "abc";` |
| --- | --- | --- |
| 住哪 | 常量区（只读） | 栈（可写） |
| 能否改 | **不能**（`s[0]='x'` 崩） | 能 |
| `sizeof` | 4 或 8（指针） | 4（含 `'\0'`） |

**⑤ 值传递 vs 传地址**

| | 值传递 `void f(int x)` | 传地址 `void f(int* p)` |
| --- | --- | --- |
| 收到什么 | 副本（复印件） | 地址（门牌号） |
| 能改外面吗 | **不能** | 能（`*p = 值`） |
| 典型 | 普通计算 | `Swap`、`scanf`、改结构体 |

**⑥ `.` vs `->`**

| 写法 | 左边是什么 | 例 |
| --- | --- | --- |
| `s.name` / `s[i].name` | **结构体变量**（或数组元素） | `struct Stu s; s.name` |
| `p->name` | **结构体指针** | `struct Stu* p = &s; p->name` |

**⑦ 循环三兄弟怎么选**

| 循环 | 先判断还是先执行 | 典型场合 |
| --- | --- | --- |
| `for (i=0; i<n; i++)` | 先判断 | **遍历**（次数已知），步进写在头上最保险 |
| `while (条件)` | 先判断 | 次数未知、可能一次都不做 |
| `do { } while (条件);` | **先执行**，至少一次 | 读输入、重试（"至少做一次"），**末尾必须有分号** |

**⑧ 数组的"类型"和"方括号"什么时候出现**

| 场合 | 写法 | 说明 |
| --- | --- | --- |
| 声明 | `int a[10];` | 类型 + 名字 + **常量**大小 |
| 初始化 | `int a[10] = {0};` | 花括号；不满自动补 0 |
| 形参 | `void f(int a[], int n)` | **方括号可省**（`int* a` 等价），长度另传 |
| 二维形参 | `void f(int a[][4])` | 第一维可省、**第二维必须写** |
| 访问 | `a[i]` | 下标可以是变量，范围 `0 ~ n-1` |
| 传参 | `f(a)` | **只写名字**，不带类型、不带 `[]` |
| 取长度 | `sizeof a / sizeof a[0]` | 只在本作用域有效（传进函数就失效） |

**⑨ `const` 与指针的四种位置**

| 写法 | 谁不能改 | 记忆 |
| --- | --- | --- |
| `const int* p` | 不能通过 `p` 改**值** | `*` 在 `const` 右边 → 值是只读 |
| `int* const p` | `p` 的**指向**不能改 | `const` 紧贴 `p` → 指针自己是常量 |
| `const int* const p` | 值和指向都不能改 | 两个都锁死 |
| `char* const argv[]` | 指针数组的元素不能改 | 常见于 `main` 参数 |

> 读法：**从名字往外、先右后左**，看 `const` 紧贴的是 `p` 还是 `*p`。

**⑩ 结构体传参：传值 vs 传指针**

| | `void f(struct Stu s)` | `void f(struct Stu* p)` |
| --- | --- | --- |
| 复制什么 | **整袋复制**（可能几十字节） | 只复制地址（4/8 字节） |
| 能改原结构体吗 | **不能** | 能（`p->score = 100;`） |
| 访问成员 | `s.score` | `p->score` |
| 什么时候用 | 只读、结构体很小 | 要修改、或结构体较大 |

## <span style="color:#9A87B5">4.21 一个 .c 怎么变成 .exe</span> <a id="p4-21"></a>

**两个环境**：**翻译环境**（编译器把源码变成可执行文件）+ **执行环境**（载入内存 → 调用 `main` → 建栈帧 → 运行 → 终止）。

**翻译环境的四道关**

| 阶段 | 干什么 | 产物 | 这一阶段出错的典型报错 |
| --- | --- | --- | --- |
| **预处理** | 展开 `#include`、替换 `#define`、删注释、处理条件编译 | `.i` | 找不到头文件、宏写错 |
| **编译** | C 代码 → 汇编代码（查语法、类型） | `.s` | 语法错误、C4700、C4553 |
| **汇编** | 汇编 → 机器指令（目标文件） | `.o` / `.obj` | 很少出错 |
| **链接** | 多个 `.o` + 库函数拼起来、解析外部符号 | `.exe` | **LNK2019 无法解析的外部符号**、LNK1168 |

**一句话判据**
- 报"语法错误 / 未定义标识符" → **编译期**；
- 报"LNK2019 / 无法解析的外部符号" → **链接期**（函数只有声明没有定义、或文件没加进工程）；
- 报"LNK1168 无法写入" → 旧 exe 还在跑；
- 编过了但运行时崩 → **运行期**（0xC0000005 / 0xC00000FD）。

## <span style="color:#9A87B5">4.22 文件模式与返回值</span> <a id="p4-22"></a>

**六种打开模式（加 `b` 变二进制）**

| 模式 | 能读 | 能写 | 文件不存在时 | 旧内容 | 写位置 |
| --- | --- | --- | --- | --- | --- |
| `"r"` | ✓ | ✗ | **失败返回 `NULL`** | 保留 | — |
| `"w"` | ✗ | ✓ | **新建** | **清空** | 从头 |
| `"a"` | ✗ | ✓（只追加） | 新建 | 保留 | **永远末尾** |
| `"r+"` | ✓ | ✓ | **失败** | 保留 | 由 `fseek` 决定 |
| `"w+"` | ✓ | ✓ | 新建 | **清空** | 由 `fseek` 决定 |
| `"a+"` | ✓ | ✓（只追加） | 新建 | 保留 | **永远末尾，`fseek` 改不了** |

**三个坑**
1. **`"w+"` 一打开就清空**，哪怕你只想读；
2. **`"a+"` 的 `fseek` 改不了写位置**，写永远追加；
3. **更新流（带 `+`）读写切换前要 `fflush` 或 `fseek`**，否则缓冲区状态未定义——最稳是 `fclose` 再重开。

> 只有 `"w"/"a"/"w+"/"a+"` 会新建文件；读模式要求文件已存在。

**19 个文件函数按七族分组**

| 族 | 函数 | 返回什么 |
| --- | --- | --- |
| 打开关闭 | `fopen` / `fclose` | `FILE*`（失败 `NULL`）/ 0（失败 `EOF`） |
| 字符 | `fgetc` / `fputc` | 读到的字符或 `EOF` / 写入的字符或 `EOF` |
| 行 | `fgets` / `fputs` | `s` 或 `NULL` / 非负或 `EOF` |
| 格式化 | `fprintf` / `fscanf` | 写出的字符数 / **读到的项数** |
| 二进制块 | `fread` / `fwrite` | **成功搬运的块数** |
| 定位 | `fseek` / `ftell` / `rewind` | 0 成功 / **字节位置** / void |
| 状态与管理 | `feof` / `ferror` / `perror` / `remove` / `rename` / `fflush` | 标记 / 标记 / void / 0 成功 / 0 成功 / 0 成功 |

**别把这三类"0"混了**：`fclose/fseek/remove/rename` 的 0 = **成功**；`feof/ferror` 的 0 = **条件不成立**；`fscanf/fread` 的 0 = **一项都没读到**。

## <span style="color:#9A87B5">4.23 switch / goto</span> <a id="p4-23"></a>

**`switch` 的五条规则**

```c
switch (n) {            /* n 只能是整型 / char / enum */
case 1:  printf("一"); break;
case 2:
case 3:  printf("二三"); break;   /* 2 和 3 共用一段 */
default: printf("其他"); break;   /* 位置随意 */
}
```

| 规则 | 说明 |
| --- | --- |
| `case` 后必须是**常量** | `case n:` 不行；`case 1 ... 5:` 是 GCC 扩展，别用 |
| 忘了 `break` 会**穿透** | 初学一律写 `break`，除非明确要共用 |
| `default` 位置随意 | 习惯放最后 |
| `switch` 里不能直接定义变量 | 要加 `{}` 或把声明提到外面 |
| 怎么选 | 判"等于某几个固定值"用 `switch`，判"范围/复合条件"用 `if` |

**`goto` 只推荐一种用法**

```c
for (...) for (...) if (出错) goto cleanup;   /* 一次跳出多层循环 */
cleanup: /* 统一释放资源 */
```

- 只能跳**同一函数内**的标号；
- `break` 只能跳一层，多层嵌套才轮到 `goto`；
- **别用它写正常流程**（面条代码的源头）。

## <span style="color:#9A87B5">4.24 从内存到变量：三句话</span> <a id="p4-24"></a>

| 概念 | 一句话 |
| --- | --- |
| 内存 | 一排有编号的房间，每个房间（字节）住 8 个 0/1 灯泡 |
| bit / byte | 1 bit = 一个灯泡；1 byte = 8 个灯泡 = 256 种状态（ASCII 256 个符号的来历） |
| 变量 | **贴了名字标签的房间**：按类型订房 → 贴标签 → 把值搬进去 |
| `=` | "搬进去"的动作，不是"相等"；赋新值会**覆盖**旧值 |
| 数据类型 | 房型：决定**房间大小**和**能住什么** |
| 字符 | 本质是 ASCII 小整数，所以 `c + 32` 能做大小写转换 |

**推论（后面所有知识的根）**
- `char` 数组装字符串 = 一排小房间 + 末尾 `'\0'`；
- 数组是一排连号房间，所以 `a[i]` 等价 `*(a+i)`；
- 指针是"装着门牌号的名片盒"，`&` 抄门牌、`*` 敲门。

---

> 学完只是"认识"，写出来才算"会"。这份总结建议每周扫一遍第一、二部分（那是你自己的坑和你的疑问），第三、四部分随用随查。
>
> **最后一条建议**：4.18 那十四个套路，每个都亲手默写一遍——**能默写出来的才叫库存，看着眼熟的只是"见过"**。

---

# <span style="color:#6E8A8A">第五部分　常见刷题题型与解法</span> <a id="p5-0"></a>

> 这一部分按**题型**组织，覆盖 T1–T85 全部 85 道题。每类固定五件套：**怎么认 → 四步做 → 骨架 → 代表题 → 易错点**。
>
> 和 4.18 的分工：4.18 是**零件库**（十四个代码模板），这里是**索引**——拿到一道新题，先判断它属于哪一类，再回 4.18 取零件。

## <span style="color:#6E8A8A">拿到题先问三句</span>

| 问题 | 可能答案 | 决定了什么 |
| --- | --- | --- |
| **输入是什么形状？** | 一个数 / 一行字符 / n 条记录 / 一个文件 | `scanf` 还是 `fgets`；要不要开数组 |
| **要输出什么？** | 一个值 / 一串 / 一张表 | 打印放循环内还是循环外 |
| **中间要存吗？** | 不存 / 数组 / 结构体 / 动态 / 文件 | 普通变量、数组、`struct`、`malloc`、`fopen` |

> 三句答完，选型基本就定了；剩下只是套 4.18 的模板。

---

## <span style="color:#6E8A8A">5.1 字符串与字符数组</span> <a id="p5-1"></a>

**怎么认**：题目给你"一个字符串 / 一整行"，要求**替换、统计、查找、切分、读入**。

**四步做**
1. 定**终点站**：C 字符串是 `'\0'`，读入的一行是 `'\n'`（先用 `strcspn` 剪掉）。
2. 定**容器**：原地改（等长替换）/ 另开数组（变长）/ 桶数组（统计）。
3. 写**逐字符循环**，判断和处理都在循环体内。
4. 收尾补 `'\0'`，检查越界。

**骨架**

```c
/* 逐字符遍历 + 原地替换 */
for (i = 0; s[i] != '\0'; i++)
    if (s[i] >= 'a' && s[i] <= 'z') s[i] = 'L';

/* 统计：数组当一排桶（必须清零） */
int cnt[26] = { 0 };
for (i = 0; s[i] != '\0'; i++)
    if (s[i] >= 'a' && s[i] <= 'z') cnt[s[i] - 'a']++;
for (i = 0; i < 26; i++)
    if (cnt[i]) printf("%c %d\n", 'a' + i, cnt[i]);
```

**代表题**：T1 编码替换、T40 统计字母、T63 手写 `strcpy`、T65 `strstr`/`strtok`、T76 读一整行、T77 数单词、T78 最长单词。

**易错点**
- 桶数组忘写 `= {0}`，输出一堆垃圾数（T40）。
- 循环条件写成 `!= '\n'`，字符串里根本没有换行 → 一次都不跑。
- `strncpy` 在"源 ≥ n"时**不补 `'\0'`**，要自己写 `d[n] = '\0';`（T64）。
- `fgets` 读进来带 `\n`，不剪会导致长度多 1（T76）。

---

## <span style="color:#6E8A8A">5.2 双指针与对称问题</span> <a id="p5-2"></a>

**怎么认**：出现**反转、回文、从两端向中间汇聚、去重**这类字眼。

**四步做**
1. 两端下标 `l = 0, r = len - 1`。
2. 循环条件一律 `l < r`（不是 `<=`）。
3. 循环体：**要改就交换，只判就比较**。
4. 步进放循环体末尾：`l++; r--;`。

**骨架**

```c
/* 反转：交换 */
int l = 0, r = len - 1;
while (l < r) { char t = s[l]; s[l] = s[r]; s[r] = t; l++; r--; }

/* 回文：只比较 + flag */
int flag = 1;
for (l = 0, r = len - 1; l < r; l++, r--)
    if (s[l] != s[r]) { flag = 0; break; }
```

**代表题**：T5 字符串反转、T7 判断回文、T14 两端汇聚、T51 递归版回文。

**易错点**
- 写成 `<=`：奇数长度时会多一次"自己和自己换"（无害但白干，T5）。
- 回文只写 `break` 不设 `flag`，跳出后无法判断结果。
- 递归版回文：终点是 `l >= r → 1`，不是 `l > r`（T51）。

---

## <span style="color:#6E8A8A">5.3 循环、分支与基础运算</span> <a id="p5-3"></a>

**怎么认**：数列求和、阶乘、倍数、乘法表、分档计算、数位统计。

**四步做**
1. 定循环变量与范围（`1..n` 还是 `0..n-1`）。
2. 定**累加器初值**：求和从 0、累乘从 1、擂主从第一个真数据。
3. 写循环体，注意**整数除法**与**浮点格式符**。
4. 检查类型：`int/int` 是整除，`double` 必须 `%lf`。

**骨架**

```c
/* 累乘 + 复用 */
long ret = 1, sum = 0;
for (i = 1; i <= 10; i++) { ret *= i; sum += ret; }

/* 分数求和：符号翻转 + 浮点 */
double s = 0; int sign = 1;
for (i = 1; i <= 100; i++) { s += sign * 1.0 / i; sign = -sign; }

/* 数位拆解 */
while (n > 0) { int d = n % 10; n /= 10; /* 用 d */ }
```

**代表题**：T10 阶乘、T11 阶乘和、T31 数 9、T32 分数求和、T34 乘法表、T41 `i > sizeof(i)`、T70 工资分档。

**易错点**
- 累乘器初值写成 0，结果永远是 0。
- `1/i` 写成整数除法，答案恒为 0 或 1（T32）。
- `printf("%d", 浮点变量)` / `scanf("%f", &double变量)`（T70）。
- `sizeof` 返回 `size_t`（无符号），和 `-1` 比较会被提升成天文数字（T41）。

---

## <span style="color:#6E8A8A">5.4 函数与递归</span> <a id="p5-4"></a>

**怎么认**：题目说"**写一个函数**"或"**用递归实现**"。

**四步做**
1. 先定**返回类型**：要带回结果就 `int`/`char*`，只打印就 `void`。
2. 定**参数**：数组一定成对递 `(arr, n)`。
3. 递归写**三件套**：终点、拆解、每条路都 `return`。
4. 自查：所有分支都有返回值吗？终点会不会漏？

**骨架**

```c
/* 递归三件套：求和 */
int sum(int n) {
    if (n == 1) return 1;              /* ① 终点 */
    return n + sum(n - 1);             /* ② 拆解 + ③ 交货 */
}

/* 递归 + 区间收拢：反转 */
void rev(char* s, int l, int r) {
    if (l >= r) return;                /* 终点用 return，不是只写 if */
    char t = s[l]; s[l] = s[r]; s[r] = t;
    rev(s, l + 1, r - 1);
}

/* 判素数：找反例 */
int is_prime(int n) {
    if (n < 2) return 0;
    for (int i = 2; i * i <= n; i++)
        if (n % i == 0) return 0;      /* 抓到约数才否定 */
    return 1;                          /* 循环外兜底 */
}
```

**代表题**：T24 顺序打印、T25 递归 strlen、T49 递归求和、T52 青蛙跳台阶、T53 汉诺塔、T54 递归反转、T44 素数表。

**易错点**
- 忘了终点 → 无限递归 → `0xC00000FD` 栈溢出。
- 算了却没 `return`（`i = x + sum(x-1);`）→ C4715 + 垃圾值（T49）。
- `void` 函数里写 `return 0;`；`int` 函数有分支不返回。
- 递归里 `return` 写进循环，只跑第一轮（T43）。
- `sizeof(arr)` 在函数里只剩指针大小，长度必须外面算好传进来。

---

## <span style="color:#6E8A8A">5.5 数组、算法与排序</span> <a id="p5-5"></a>

**怎么认**：求最大/最小、查找、排序、去重、统计。

**四步做**
1. **读入**：`scanf("%d", &a[i])`——`a` 不加 `&`，`a[i]` 必须加。
2. 定**擂主 / 边界**：擂主要取第一个真数据，且写在循环外。
3. 遍历比较或折半收缩。
4. 输出**答案**，不是中间过程。

**骨架**

```c
/* 打擂台 */
int max = a[0];
for (i = 1; i < n; i++) if (a[i] > max) max = a[i];

/* 二分查找 */
int l = 0, r = n - 1, mid;
while (l <= r) {
    mid = l + (r - l) / 2;
    if (a[mid] == key) break;
    else if (a[mid] < key) l = mid + 1;
    else r = mid - 1;
}

/* 冒泡 */
for (i = 0; i < n - 1; i++)
    for (j = 0; j < n - 1 - i; j++)
        if (a[j] > a[j + 1]) { int t = a[j]; a[j] = a[j + 1]; a[j + 1] = t; }
```

**代表题**：T6 最大字符、T13 二分查找、T30 辗转相除、T36 冒泡、T39 异或找落单、T42 求最大值、T47 二维数组比较。

**易错点**
- 擂主初值写在循环里 → 每轮重置，等于没比（T42）。
- 二分写 `l <= r` 却忘了 `mid ± 1` → 死循环。
- 二维数组列数三处不一致（声明 `[2]` 却用 `[3]`）。
- `int / int` 是整除，比值要先 `(double)`。

---

## <span style="color:#6E8A8A">5.6 指针与内存函数</span> <a id="p5-6"></a>

**怎么认**：要求"**在函数里改外面的变量**"、"按字节复制/设置"。

**四步做**
1. 判断是否需要**传地址**（要改实参就必须）。
2. 形参写 `int*`，调用写 `&x`。
3. 函数里用 `*p` 赋值。
4. 内存函数先转 `unsigned char*` 再逐字节走。

**骨架**

```c
void swap(int* a, int* b) { int t = *a; *a = *b; *b = t; }

void my_memcpy(void* dst, const void* src, size_t n) {
    unsigned char* d = (unsigned char*)dst;
    const unsigned char* s = (const unsigned char*)src;
    while (n--) *d++ = *s++;          /* void* 不能直接 +1 */
}
```

**代表题**：T18 传址交换、T22 调用一次加 1、T67 内存函数边界、T68 手写 `memcpy`/`memmove`。

**易错点**
- 值传递改不了实参（形参是复印件）。
- `void*` 不能直接 `+1`（不知道一步多大），必须转 `char*`。
- `memcpy` 不处理重叠，重叠要用 `memmove`。
- `memset` 按字节，`memset(a, 1, ...)` 得到 `0x01010101`。

---

## <span style="color:#6E8A8A">5.7 结构体与自定义类型</span> <a id="p5-7"></a>

**怎么认**：题目出现"**学生 / 商品 / 联系人**"这类**多条记录**。

**四步做**
1. 定义 `struct`（**末尾分号别丢**）。
2. 开数组：`struct Stu s[105];`。
3. 读入：`&s[i].score`（`int` 要 `&`），`s[i].name`（数组不要 `&`）。
4. 打擂台记**下标**、排序**整体交换**、查找用 `strcmp == 0`。

**骨架**

```c
struct Stu { char name[20]; int score; };
struct Stu s[105];
int best = 0;
for (i = 0; i < n; i++) scanf("%s %d", s[i].name, &s[i].score);
for (i = 1; i < n; i++) if (s[i].score > s[best].score) best = i;
printf("%s\n", s[best].name);         /* 记下标才能回查姓名 */
```

**代表题**：T45/T56 打擂台找最高分、T55 结构体入门、T57 结构体排序、T58 按姓名查找、T60–T62 位段/枚举/联合、T69 清零 + 整块搬运。

**易错点**
- `struct` 定义末尾漏分号，报一串语法错。
- 排序时只换 `score` 不换 `name` → 人和分数**错位**（T57）。
- 打擂台只记值不记下标，最后查不到是谁。
- `&f.a`（位段取地址）非法，C2104。

---

## <span style="color:#6E8A8A">5.8 动态内存</span> <a id="p5-8"></a>

**怎么认**：题目里 **n 是运行时才输入的**，或者要"扩容 / 追加"。

**四步做**
1. 算**字节数**：`n * sizeof(类型)`。
2. 申请后**判 NULL**。
3. 用完 **`free` + 置 NULL**。
4. 扩容用 `realloc`，**必须用临时指针接**。

**骨架**

```c
int* a = (int*)malloc(n * sizeof(int));
if (a == NULL) return 1;
/* ... 使用 ... */
int* tmp = (int*)realloc(a, (n + m) * sizeof(int));
if (tmp == NULL) { free(a); return 1; }
a = tmp;
free(a); a = NULL;
```

**代表题**：T72 六个真相、T73 两段扩容、T74 动态成绩表、T75 柔性数组。

**易错点**
- 字节数写成元素个数（`malloc(n)` 而不是 `n * sizeof(int)`）。
- `p = realloc(p, ...)` 失败时丢掉老地址 → 内存泄漏。
- `free` 后继续用 → 悬空指针；重复 `free` → 破坏堆。
- 柔性数组只能 `free` 一次（结构体整体）。

---

## <span style="color:#6E8A8A">5.9 文件读写与错误处理</span> <a id="p5-9"></a>

**怎么认**：要求"**存到文件 / 从文件读**"。

**四步做**
1. 选模式：读 `"r"`、写 `"w"`（会清空）、追加 `"a"`、二进制加 `b`。
2. `fopen` 后**立刻判 NULL**，用 `perror` / `strerror(errno)` 报错。
3. 读写**看返回值**控制循环（`while (fgets(...))`、`while (fscanf(...) == 2)`）。
4. `fclose` 关掉；要换个方向读写就**关掉重开**。

**骨架**

```c
/* 文本：写 → 关 → 重开读 */
FILE* fp = fopen("stu.txt", "w");
if (fp == NULL) { perror("open"); return 1; }
fprintf(fp, "%s %d\n", s.name, s.score);
fclose(fp);

fp = fopen("stu.txt", "r");
if (fp == NULL) { perror("open"); return 1; }
while (fscanf(fp, "%s %d", name, &score) == 2) { /* ... */ }
fclose(fp);

/* 二进制：整块写 / 整块读 */
fwrite(s, sizeof(struct Stu), n, fp);      /* 返回份数，不是字节 */
size_t got = fread(buf, sizeof(struct Stu), n, fp);
```

**代表题**：T59 通讯录存盘、T66 全句替换 + `strerror`、T79 字符级复制、T81 格式化存盘、T82 二进制整块、T83 定位改写、T84 `perror`/`feof`/`ferror`、T85 `rename`/`remove`。

**易错点**
- 用 `"w"` 打开源文件 → 内容先被清空。
- `while (!feof(fp))` 当循环条件 → 多跑一轮。
- 求文件大小写成 `fseek(-1, END); ftell()` → 得到的少 1。
- 想改写中间内容却用 `"a"` → 追加模式永远写在末尾。
- 文件名里混进空格（`"stu. txt"`）→ `fopen` 失败。

---

## <span style="color:#6E8A8A">5.10 项目实战</span> <a id="p5-10"></a>

**怎么认**：要求做一个**完整的游戏 / 管理系统**，通常带菜单。

**四步做**
1. **画模块**：先分"数据"和"功能"两块（棋盘 + 落子/判赢；通讯录 + 增删查改）。
2. **拆文件**：`game.h` 招牌 / `game.c` 后厨 / `test.c` 点单。
3. **主循环**：`while (1) { 菜单 → switch 分发 → 各功能 }`。
4. **补边界**：越界、占用、满员、输入非法，逐个补。

**骨架**

```text
game.h   #ifndef 防重复 + 宏(ROW/COL) + 函数声明
game.c   #include "game.h" + 各函数定义
test.c   main + 菜单 + 调 game()
```

```c
while (1) {
    menu();
    scanf("%d", &choice);
    switch (choice) {
    case 1: play(); break;
    case 0: return 0;
    default: printf("输入错误\n");
    }
}
```

**代表题**：T16 猜数字、T37 三子棋（多文件 + 宏化 + 输入加固）、T38 扫雷、T46 通讯录。

**易错点**
- 判赢写成"三个格子都等于空格"也算赢（T37）。
- 扫雷不放大棋盘，统计周围雷时越界读取。
- 菜单输错不兜底，程序直接退出。
- 功能没拆函数，`main` 写到几百行。

---

> **用法**：拿到新题 → 先套「三句问」定形状 → 对到 5.x 某一类 → 照四步走 → 写完回易错点自查一遍。**能归类，就不会从零开始。**

---

## <span style="color:#AE8F5F">后言</span>

当你读到这里，我感到非常开心——你可能是为数不多读完全文的人。想必你也发现了，中间的内容是我借助 AI 完成的，但我可以确保：里面每一个错误、每一个问题，都是货真价实的。读完的你，是否也有所收获？

有时我也会翻起这份文件，看到自己曾经以为「scanf 没加 `&`」而犯错，确实有点好笑；回想起刚开始学 C 语言时抓耳挠腮的样子，仍历历在目。现在的你，可能也会因为学不懂 C 语言而困惑，但我想说：很多时候不是你学不会，而是这些东西你还没见过。路要慢慢走，剩下的交给时间吧。

最后想说一句不相干的话：朋友，一定要去看每日的晚霞；哪怕那天没有，也别失落。

