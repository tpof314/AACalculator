# AA计算器

和朋友一起出去旅游，最后回来要算账，通常会觉得非常麻烦。这是一段专门用来AA的js代码。只要把每个人的花费输入进去，就可以算出一套最后的AA方案。

## 界面版演示

这几天还给这个计算器做了一个界面。点击下面的链接就可以进入：

[https://aa.dgcontinent.com/](https://aa.dgcontinent.com/)

## 使用方法

1. 创建一个“AA计算器”对象.
```javascript
let aa = new AACalculator();
```

2. 通过`assignPersonCost()`函数，把每个人的花费填进去。
```javascript
aa.assignPersonCost("小强", 20.8);
aa.assignPersonCost("张三", 10.5);
aa.assignPersonCost("赵四", 60.2);
aa.assignPersonCost("汤姆", 66);
aa.assignPersonCost("杰瑞", 6);
aa.assignPersonCost("米老鼠", 0);
```

3. 用`computeAAResult()`函数，计算出一套最终的AA方案。
```javascript
var results = aa.computeAAResult();
console.log(results);
```

输入结果如下：
```
[ { from: '米老鼠', to: '汤姆', amount: 27.25 },
  { from: '杰瑞', to: '汤姆', amount: 11.5 },
  { from: '杰瑞', to: '赵四', amount: 9.75 },
  { from: '张三', to: '赵四', amount: 16.75 },
  { from: '小强', to: '赵四', amount: 6.45 } ]
```
