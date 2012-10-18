
## 存在与创造

负数是我们**创造**出来的，它不是客观存在的（例如，负数不能像自然数那样可以用来计数，它们并不"自然"）。
数学家们创造负数是为了在保持算术基本运算的条件下使运算能够自如。
但是，我们**可以**并且**必须**加以证明的是，在这些定义的基础上，算数的交换律、结合律、分配率是保持不变的。

事实也确实如此，自然数的定律同样适用于负数（这不是理所当然的，而是数学家们证明出来的，在未证明之前我们不能把自然数的定律使用在负数上，为了防止某些同学看我博客时睡着，我在此也不写证明过程了）。

计算机中的数，我们都习惯性的称它们为“整数”、“小数”，因为这些概念我们熟悉，其实，
它们的名字是**定点数**(相当于整数)、**浮点数**(相当于小数)。

定点数、浮点数的运算法则和我们数学中的整数、小数一样吗？数学中的定律同样适用定点数、浮点数吗？
作为纯理性派的一员，我坚持的信条是：**任何未经证明的东西我们都不能认为它是理所当然**。
就好比我口袋有个洞，那么隔壁小李口袋也应该有个洞，因为我俩裤子是从一家店买的，显然这是错误的。

## 数学定律

其实，我们习以为常的数学定律在计算机中很容易找到反例。

(A / B) * C 等于 (A * C) / B 吗？

看下面的例子

	0.6 * 10 / 0.2 = 30
	0.6 / 0.2 * 10 = 29.999999999999996

(A + B) * C 等于 (A * C) + (B * C) 吗？

看下面的例子

	(0.2 + 0.4) * 10 = 6.000000000000001
	0.2 * 10 + 0.4 * 10 = 6

再举一个其它例子

	0.3 - 0.2 = 0.09999999999999998
	0.2 - 0.1 = 0.1

在本系列『前言』中，也介绍了一些数学公理在计算机中不存在"普适性"。

## 计算机定律

几百年前数学家们就在讨论，"加法"需要定义吗？如果需要，该如何定义呢？算数的基础是什么？

`2 + 3 = 5` 显然是正确的(除非你被赵大叔给忽悠了)，两个苹果再加上三个苹果就是五个，应该可以当作公理而不需要证明。

罗素在《数理逻辑》一书写道，

> 538346 + 465345 = 1003691 也不需要证明吗？也算是公理吗？我相信任何人都不可能一眼看出它的真伪。

天才的皮诺亚真的构造了一个可以和欧几里德《几何原本》相媲美的算术系统。

皮诺亚的算术系统以后再给大家普及(《[哥德尔、艾舍尔、巴赫书：集异璧之大成](http://t.cn/zOEsu0d)》里面有一章关于皮诺亚系统介绍，读了两遍之后，真是连火星人都能看懂，正在考虑我的博文要不要写皮诺亚了)，计算机的定点数、浮点数也是一个皮诺亚系统，
完善这个系统的就是计算机界的先驱和天才们，阿兰·图灵、冯·诺依曼、库尔特·哥德尔、阿隆左·丘奇… 当然了，别忘了罗素和布尔。

关于计算机中的运算(加、减、乘、除等等)的定义在后续文章中会详细介绍(放在皮诺亚系统之后)，居然上面提到了计算机的天才们，就顺便写点计算机的历史吧。

1930年前后，在第一台电脑问世之前，就有四位大牛对形式化运算系统展开了研究。
他们不是为了发明计算机(电脑)，而是如何让机器思考。
这些天才的数学家们想通过所谓的“形式系统”，来证明一个命题：**可以用简单的数学法则表达现实系统**。
这四位天才就是阿兰·图灵、冯·诺依曼、库尔特·哥德尔、阿隆左·丘奇。

在《[剑桥五重奏：机器能思考吗](http://t.cn/zlQrlUp)》中，作者用一个数学家的丰富想象力虚构了一次特别的晚宴，
晚宴发生在1949年的春夏之交，地点是剑桥大学基督学院的一间房子。
五位世界级的科学名人，品尝着美味佳肴，围绕着“机器能思考吗”这一论题展开了广泛深入的探讨。

1936年，图灵提出了“图灵机”的形式系统。图灵提出并证明了可以通过0、1运算来解决复杂问题。

1939年，阿坦纳索夫研制成功了第一台电子计算机ABC。

1945年，诺依曼等人基于当时计算机系统ENIAC的研究成果，提出了EDVAC体系设计，以及其上的编码程序、
纸带存储和输入。该设计方案被认为是图灵机的一个很完美的实现。诺依曼也顺利当上了“计算机之父”。

我们现在的编程环境，就是构架在诺依曼体系中，该设计包括五大部件: 运算器、逻辑控制器、存储器、输入设备、输出设备。
其中，运算器基于的理论就是0、1运算（最早由数学家布尔提出），其他部件呢？存储器和输入输出设备都是依赖于0、1（你电脑上几个G的苍老师教学视频也都是0和1）。
因此，诺依曼体系就是一个这样的体系：**数据存储在内存或者硬盘，并依赖内存进行运算**。

简单来说就是，**通过修改内存来反映运算的结果**，在冯氏体系中，逻辑控制器的作用就一个“修改内存或者寄存器”。
由此产生了汇编语言、C语言、Java、C#… 这些语言被称为“命令式语言”。

但是，我们应用机器的目的是，**运算，并产生结果**。所以运算才是本质，而“修改内存”只是运算带来的“副作用”。

在冯诺依曼电脑十年之后，约翰·麦卡锡(John McCarthy)教授对阿隆左·丘奇的工作产生了兴趣，并在1959年公布了他的表处理语言Lisp。
该语言其实就是对阿隆左·丘奇的Lambda(希腊字母λ的发音)演算的实现。

保罗·格雷厄姆在总结编程语言时说道：

> 二十年来，开发新编程语言的一个流行的秘诀是：取C语言的计算模式，逐渐地往上加入 lisp 语言的特性，
> 例如运行时类型和无用单元收集。

那些基于Lambda演算的语言通常被称为函数式语言。
**并不是一个语言支持函数就是函数式语言**。

什么是函数式编程语言？仔细看下面的“绕口令”

<ol>
  <li>函数式编程语言的运算元是函数</li>
  <li>函数的参数是函数</li>
  <li>函数的返回值是函数</li>
</ol>

> 函数式编程语言的函数，接受一个或者N个函数作为输入，处理完成后，输出另一个函数。

在这里很多人都存在误解，比如计算 `1 + 2 * 3` 写成函数 `add(1，mul(2，3))` 算是函数是语言吗？
add函数，接收了一个整数参数1，和一个函数mul。

其实，add函数并没有接收mul函数作为他的参数，它*只接收了mul函数处理完成后的返回值，而不是接收了mul函数本身*。
看看add函数的签名(声明、定义)就知道了 `int add(int，int)`，可见add函数的参数是两个整数。

## 做什么 VS 怎么做

待续…

## 逻辑演算

-1乘以-1为什么等于+1?

待续…

## -1乘以-1为什么等于+1

待续…