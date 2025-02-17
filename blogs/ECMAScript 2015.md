# ES6
## 1.块级作用域变量声明
在ES6中引入了`let`和`const`块级作用域的概念，解决了`var`在声明变量时的作用域问题。
>块级作用域，即它只在声明它的代码块（如if、for、while、函数等等）中有效。  
>全局作用域，即全局有效。  
>函数作用域，只在函数中生效。

在ES5中我们可以在代码中任意位置声明变量，甚至可以重写已声明的变量
```js
var name = 'anna';
var name = 'tom';
console.log(name);
>> tom
```
其实这一块在日常开发的过程中是异常危险的，可能会出现设置的值在其他地方被改变。

- `let`
	- let声明的变量作用域是块或者函数。
	- let声明的变量只能在执行到声明所在的位置之后才能访问（暂时性死区）。
	```js 
	// ❌ 错误
	tom = 'man';
	let tom;
	// 会出现 Cannot access 'tom' before initialization

	// ✔️ 正确
	let tom;
	tom = 'man';
	```
- `const` 
	- const声明的变量也具有块级作用域，但是它常用于声明常量（不可修改的变量）。
	```js
	// ❌ 错误 使用const后在使用 = 赋值就会报错 Assignment to constant variable.
	const a = [];
	a = [1]

	// ✔️ 正确
	const b = [];
	b.push(1)
	```
	- const声明的变量必须在声明时进行赋值
	```js
	// ❌ 错误
	const data;
	// 会出现 " 必须初始化“const”声明 "

	// ✔️ 正确
	const data = []
	```
- `var`和`const`与`let`的区别
	- `var`声明的变量是函数或者全局作用域，而不是块级作用域。
	- `var`声明会被提升到函数/全局作用域的顶部，即声明语句在使用变量之前。
## 2.模板字面量
模板字符串是新引入的一种特性，为了更加简洁和强大的字符串处理方式，支持如嵌入表达式、支持多行字符串等等。
- 基本语法
- 插入表达式
- 多行字符串
## 3.箭头函数
## 4.Class类
## 5.解构赋值
## 6.默认参数
## 7.扩展运算符
## 8.符号（Symbol）
## 9.Promise
## 10.模块化（Modules）
## 11.Set与Map数据结构
## 12.Array方法增强
## 13.生成器函数（Generator Function）
## 14.异步函数（Async/Await）
## 15.尾调用优化