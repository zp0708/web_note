### 数组

定义

``` javascript
var arr = new Array(1, true, "hello");
// 数组长度为10
var arr = new Array(10);
var arr = Array();
```

属性

``` js
var arr = Array(1, 2, 3);
// length 数组长度
arr.length();  // 3
// 访问数组, 数组下标可以是表达式
let a = arr[0]; // a = 1
```

遍历

``` js
var arr = [1, 2, 3];
for (var i = 0; i < arr.length(); i++) {
    console.log(arr[i]);
}

// for in
for (var i in arr) {
    console.log(arr[i]);
}
```

堆栈方法

```js
// push 推入元素
var arr = [1, 2, 3];
arr.push(4);
for (var i = 0; i < arr.length; i++) {
    console.log(arr[i]); 
}
// 1, 2, 3, 4

// pop 移除数组尾部元素
var arr = [1, 2, 3];
arr.pop();
for (var i = 0; i < arr.length; i++) {
    console.log(arr[i]); 
}
// 1, 2

// shift 从数组的头部移除袁术
var arr = [1, 2, 3];
arr.shift();
for (var i = 0; i < arr.length; i++) {
    console.log(arr[i]); 
}
// 2, 3

// unshift 从数组头部插入元素
var arr = [1, 2, 3];
arr.unshift(4, 5);
for (var i = 0; i < arr.length; i++) {
    console.log(arr[i]); 
}
// 4, 5, 1, 2, 3
```

方法

``` js
// concat 将数组和数组合并，原数组不会被修改，返回值为合并后的数组
var arr1 = [1, 2, 3];
var arr2 = [4, 5]
arr = arr1.concat(arr2);
for (var i = 0; i < arr.length; i++) {
    console.log(arr[i]); 
}

// slice 获取数组中指定区域元素，并作为数组返回

var arr1 = [1, 2, 3];
arr = arr1.slice(0, 2);
for (var i = 0; i < arr.length; i++) {
    console.log(arr[i]); 
}
// 1, 2

// splice 可以完成删除，插入，替换操作
// 参数1：截取的开始下标
// 参数2：截取的长度
// 参数3：在截取的开始下标位置，我们要插入的元素，插入的元素个数不限
var arr1 = [1, 2, 3];
arr = arr1.splice(0, 2, 4, 5);
for (var i = 0; i < arr.length; i++) {
    console.log(arr[i]); 
}
// 1, 2
for (var i = 0; i < arr1.length; i++) {
    console.log(arr1[i]); 
}
// 4, 5, 3

// join 使用拼接符将数组中的元素拼接成字符串
var arr1 = [1, 2, 3];
console.log(arr1.join(','))
// '1,2,3'
```