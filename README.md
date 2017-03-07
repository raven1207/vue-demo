# study
function f1(){}
var f2=new Function(){}
var f3=function(){}
var o4=new Object();
var o5={};
var o6=new f1();
f1,f2,f3皆为函数对象。o4,o5,o6皆为普通对象
1.Object.__proto__ === Function.prototype // true
  Object是函数对象，是通过new Function()创建，所以Object.__proto__指向Function.prototype。

2.Function.__proto__ === Function.prototype // true
  Function 也是对象函数，也是通过new Function()创建，所以Function.__proto__指向Function.prototype。
  
Object是函数对象，是通过new Function()创建，所以Object._proto_指向Function.prototype.
Function.prototype.__proto__ === Object.prototype //true
JS一直强调万物皆对象，函数对象也是对象，给他认个祖宗，指向Object.prototype。Object.prototype.__proto__ === null，保证原型链能够正常结束。
