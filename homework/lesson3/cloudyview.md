# 第三课 作业

## 流程图
![浏览器与服务器交互过程的流程图](https://github.com/cloudyview/myPhoto/blob/master/cloudyview.png)

图片网址：https://github.com/cloudyview/myPhoto/blob/master/cloudyview.png

## 一、对本节课程序的阅读心得

### 1. name_style.js

好的命名是指，不需要去研究程序，只是看命名就知道该命名的含义和数据类型。

从方法上，首先是要说清楚，不要以为命名说了某个点，就可以了。例如，start就是一个糟糕的命名，可以有无数的理解。但是如果用startCount,我们可以知道这是开始计数，指向就很明确，也知道这是个数据类型是numbetr类型。如果用startTime,那可以推断是表达日期。

我还留意到，如果想表达布尔型，一般是用isStart。

另一个重要的技巧是：不要How,要what！

我的理解是，如何操作这个数据，不需要在命名里说明，这个事情是程序其他部分的命令决定的。真正要说明的是到底这个命名是指向什么东西的，这个不说清楚，大家看程序就会犯晕，程序的可读性就会变得很差。

### 2. statement.js

这个例程里面展示了三种语句，即表达式/赋值语句，条件语句和循环语句。

表达式，赋值这些比较简单，用"="连接，将右侧的数值赋予左侧即可。

条件语句的结构就是 if ... else。这个也好理解，就是如果判断成立，执行if的部分，不成立，就执行else的部分。

switch语句，我的理解大约是如果有N中不同状态，如果在流程图里面画，估计就是那种一个判断，可以得出N种不同结果的情况，例如，爱好？唱歌，跳舞，吃饭，睡觉，游戏，编程，其他，那么就可以swith到这几种状态，然后做相应操作这样。

最后一种语句是循环语句，这个也比较好理解，就是有初始值，然后有一个结束循环的判断条件，然后有一个判断值（游标）本身的计算方法。

while方法，感觉不如for方法来的直接和清晰。

JS的for循环的这种方法，我感觉有一种很大的进步。这种进步就是不容易产生死循环。因为一开始你就要设定一个结束的条件。这种条件很明确的摆在你的面前，跟初始值和游标变化方式放在一起，会让程序员很容易去判断。

当然，应该还是会有死循环的，如果你非要弄的话。例如：
<pre>for (i = 0; i > 3; i--){
    console.log(i);
}
</pre>

**这个循环应该被无限循环下去吧，因为永远也无法达到结束条件。这是我的猜想，结果，我在chrome里面实验的结果是:undefined。。。难道，是JS会检查死循环吗？**

另外，双游标方式，或者多游标方式，表明，一个循环里面，可以针对N组数据进行相应处理，如果使用&&，||等方式对多个游标进行联合判断，应该可以形成更加复杂的逻辑。当然，一切都是看需要。

现在感觉非常渴望能够面对实际的问题来写代码！

## 二、对数据交互过程的理解

前端（客户端）和后端（服务端），各自承担了不同的任务。前端主要满足了用户界面，交互等功能，主要的数据操纵，处理，一般在后端完成。

所以，也可以理解为前端请求服务，后端满足前端请求，提供服务的这样一个过程。

对于数据，前端也不是完全不做处理，前端也会将数据进行一定程度的处理，打包，转化成后端比较容易处理的格式，然后再交给后端进行处理的。

## 三、软件架构与运行环境

软件架构是一个系统的设计图。从这个角度理解，软件架构的产生应该是面对某一类问题，有一些比较通用的解决思路，有人将这种思路总结归纳后，做成一个通行的设计，然后提供给其他人用。那么这个时候，你可以理解这是一个软件架构。

Node.js,并不针对特定问题或者业务，只要符合他的标准，它都可以为程序提供一个可运行的环境，所以，肯定是运行环境，而不是架构。

## 四、数据类型的价值
不同的数据类型，决定了代码的执行效率。效率包括：存储效率，计算效率，传递效率。

选择适合的数据类型，来处理我们的数据，这是一个程序员努力的方向。如何能够提高代码的执行效率，这应该是一个程序员进步的方向。

从课程里，我们可以了解到，数组，对象，这些复合型的数据类型，计算机对其进行处理的步骤是比较繁琐的，会消耗比较多的资源。我们将一组属性封装起来，然后形成一个对象，或者将一组数据直接变成数组的这些封装操作，实际上是方便程序员来编程。对于计算机来说，一定是会降低执行效率的。

一个程序好不好，在都能完成业务需求的前提下，一个重要的衡量维度就是执行效率高不高。

还有一个需要注意的部分，定义就必须要使用。不管是变量，还是数组，或者是函数，都是一样！

如何使用不同的数据类型，这个在书中有详尽的说明。

总的来说，所有的类型都可以转化String类型，包括布尔型，null这些都可以。可以说，字符串是一个万能数据类型，将来变成应该是非常有用的。

其他类型相互之间的转换，只要能理解他们的值在这个类型中是否有意义，就比较容易可以推断了。

例如转化为布尔值，对于布尔值而言，只要有值，就应该为真，没有值的就是假。就容易理解了。

关于命名方面的理解，在刚才已经有描述，所以后面不再继续总结。

这两天的任务就是继续啃书，把基础拿下！

问题：

关于数据类型的操纵方式，有一些用"."，有一些用"()",有的用"[]"。到底什么用点，什么时候用括号呢？这些用法背后的逻辑，或者规律是什么呢？
