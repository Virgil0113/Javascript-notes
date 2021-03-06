## JavaScript DOM 编程艺术 Chapter 6 循环语句

关键词：while 循环、for 循环

循环语句可以让我们反复多次地执行同一段代码。循环语句分为几种不同的类型，但它们的工作原理几乎是一样：只要给定条件任能得到满足，包含在循环语句里的代码就将重复地执行下去，一旦给定条件的求值结果不再是 true，循环也就到此为止。

### while 循环

while 循环与 if 语句非常相似，它们的语法几乎完全一样：

​             `while (condition){`

​                    `statements;`

​              `}`

while 循环与 if 语句唯一的区别是： 只要给定条件的求值结果是 true，包含在花括号里的代码就将反复的执行下去。

#### do...while 循环

类似于 if 语句的情况， while 循环的花括号部分所包含的语句有可能不被执行，因为循环控制条件的求值发生在每次循环开始之前，所以如果循环控制条件的首次求值结果是 false， 那些代码将一次也不会被执行。

在某些场合，我们希望包含在循环语句内部的代码至少执行一次。这时，do 循环是最佳的选择，即使循环控制条件的首次求值结果是 false，包含在花括号里的语句也至少会被执行一次。

​              `var count = 1;`

​              `do {`

​                   alert (count);

​                   count++;

​               `}   while (count < 1);`

上面的 do 循环里，循环控制条件的求值结果永远不会为 true: 变量 count 的初始值是1，所以它在这里永远不会小于1。但是因为 do 循环的控制条件出现在花括号部分之后，所以包含在这个 do 循环内部的代码还是执行了一次。变量 count 的值将是2，尽管循环控制条件的求值结果是 false。

---

### for 循环

for 循环类似与 while 循环，事实上它只是刚才介绍的 while 循环的一种变体。

​               `for (initial condition; test condition; alert condition) {` 

​                    `statements;`

​                `}`

用 for 循环来重复执行一些代码循控制结构将更加清新，与循环有关的所有内容都包含在 for 语句的圆括号部分。

可以把以上的 while 循环的例子改写为 for 循环：

​                `for (var count = 1; count < 11; count++) {`

​                      `alert (count);`

​                `}`

for 循环最常见的用途之一是对某个数组里的全体元素进行遍历处理，这往往还需要用到数组的 `array.length` 属性。

