# SQL中的SUM()、AVG()、COUNT()等聚集函数对NULL值的处理方法
NULL是SQL中比较特殊的一个值，所以考试就喜欢涉及NULL值， 特别是配合聚集函数来出题，这里做一下总结。不过NULL值不仅仅只出现在聚集函数中，还有其他的几种场合，后续进行补充

## SUM()

该聚集函数可以用来对单个列求和，也可以对多个列运算后进行求和

当列中含有NULL值的时候，SUM()会忽略该NULL值，而且如果涉及多列的运算，某一列的值为NULL，也会忽略该列

## AVG()

其实AVG()和SUM()相同，也是会忽略NULL值，注意不要思维惯性地认为将NULL值当作0代入计算

## COUNT()

这个聚集函数处理NULL值的时候就比较特殊了，它有以下两种情况

1.  COUNT(*)

   如此的话，它会对表中的行数进行统计，而不管某一行是否有NULL值

2. COUNT(字段名） 

   此时会对特定的列进行统计，但会忽略NULL值

