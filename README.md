# 一. 数据类型 (type)
	long语言数据类型分为两类，基本数据类型(primitive)和引用类型(reference)
  
## 1. 基本数据类型 (primitive)
* 无符号整数(unsigned integer) 

```
uint8 uint16 uint32 uint64 uint
```
	
  
* 有符号整数(signed integer)

```
int8 int16 int32 int64 int
```

* 浮点数

```
float double
```
  
* 字符(char)

```
char unsigned char signed char
```
  
* 布尔(boolean)

```
bool
```
  
* 字符串(string)

```
string
```
  
* nil

## 2. 引用类型(reference)
	object, array, tuple 和 function
	
# 二. 表达式(expression)

## 1. 初始化表达式 
```
	var i = 1   // int 类型自动推导
	var i : uint8 = 0 // uint8 指定数据类型
	
	const j = 2
	j = 1 // error
	
	var isOpen = true // boolean
	
	var lang = "long" // string
	
	var arr = [0, 1, 2, 3] // array
	
	var tuple = [0, "string"] // tuple
	
	var sum = function (a, b) {  // function
		return a + b
	}
	
	var a = 10, b = 10
	var c = sum(a, b)    // function call 
	
	var obj = {
		name : "Lily"
		age : 19
	}
	
```

## 2. 算数表达式
	+ - * \ % 

## 3. 逻辑表达式
	|| && ! == != <= >= 
	
## 4. 位运算表达式
	| & ^ << >>
	
## 5. 赋值表达式
	= += -= *= /=
	
```
var i, j = 0, 1  // tuple assign
i, j = j, i
```
	
## 6. 三元表达式
	a?b:c
	
## 7. 字符串连接
```
	var str1 = "hello "
	var str2 = "world"
	var str = str1 + str2
	
	var str3 = "hello " + 3 // error
	
	var str4 = "hello " .. 3 // "hello 3"
```
	
# 三. 语句(statement)
	long语言语句以line break结尾
```
	var i = 0
	var j = 2
```

## 1. 循环语句
```
	for true {
		// 无限循环
	}
	
	for var i=0; i<10; i++ {
		print(i) //
	}
	
	var objs = ["a", "b", "c"]
	for var o in objs {
		print o //
	}
	
	for var i in [0-10] {
		print i 
	}
	
	{
	
	} for true // 
```

## 2. 分支语句
```
	var i = true
	if i {
		print true
	} else {
		print false
	}
	
	var input = "hello"
	switch input {
		case "hello":
		break;
		default: 
		break;
	}
```

## 3. continue, break, goto


## 4. return

```
function abc() {
	retrun [1, "string"]
}

var i, str = abc()
```

# 四. 协程(coroutine)
```
var range = function() {
	for var i=0; i<10; i++ {
		yield i
	}
}
for var i in range() {
	print i // 0, 1, 2, 3, 4, 5, 6, 7, 8, 9
}
```

# 五. 原型(prototype)
```
	var a = { a : 1 }
	var b = { b : 2 }
	b.prototype = a
	print b.a // 1
```

# 六. 模块(module)
```
file: math.long
var _m = {
	sum : function(a, b) {
		return a + b
	}
}
return _m

file: main.long
var math = require 'math'
var sum = math.sum(1, 2)
print sum
```

# 七. 标准库
1. Object

```
	var a = { a : 1 }
	var b = Object.create(a)
	print b.a // 1
```

2. String

```
	var str = "hello world"
	var arr = String.split(str, " ") // ["hello", "world"]
```

3. Array

```
	var arr = [1, 2, 3]
	Array.join(arr, "~") // "1~2~3"
```

4. Gereric

```
	var _ = require 'gereric'
	var arr = [1, 2, 3]
	_.map(arr, function(e) {
		print e + 1 // 2, 3, 4
	})
```
