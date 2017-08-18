# 理解 js 闭包特别好的例子

```js
var variable = "top-level";
function printVariable() {
  console.log("inside printVariable, the variable holds '" +variable + "'.");
}
function test() {
  var variable = "local";
  console.log("inside test, the variable holds '" + variable + "'.");
  printVariable();
}
test();

var variable = "top-level";
function parentFunction() {
  var variable = "local";
  function childFunction() {
    console.log(variable);
  }
  childFunction();
}

var variable = "top-level";
function parentFunction() {
  var variable = "local";
  function childFunction() {
    console.log(variable);
  }
  return childFunction;
}
var child = parentFunction();
child();
//最后一个输出local

//闭包实现递归
function power(base, exponent) {
  if (exponent == 0)
    return 1;
  else
    return base * power(base, exponent - 1);
}
```
