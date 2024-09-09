# JavaScript

## Array

### 数组的增删改查

增：

```javascript
let arr = [1, 2, 3];
arr.push(4); // 在数组末尾添加元素
arr.unshift(0); // 在数组开头添加元素
arr.splice(1, 0, "a", "b"); // 在指定位置添加元素
```

删除：

```javascript
let arr = [1, 2, 3, 4];
arr.pop(); // 删除数组末尾的元素
arr.shift(); // 删除数组开头的元素
arr.splice(1, 2); // 删除指定位置的元素
```

改：

```javascript
let arr = [1, 2, 3];
arr[1] = "a"; // 修改指定位置的元素
arr.splice(1, 1, "a", "b"); // 修改指定位置的元素
// splice(start, deleteCount, item1, item2, ...)
console.log(arr); // 输出: [1, 'a', 'b', 3]
```

查：

```javascript
let arr = [1, 2, 3];
console.log(arr[1]); // 输出: 2
console.log(arr.indexOf(3)); // 输出: 2
console.log(arr.includes(2)); // 输出: true
```

### 数组的遍历

for 循环：

```javascript
let arr = [1, 2, 3];
for (let i = 0; i < arr.length; i++) {
  console.log(arr[i]);
}
```

forEach 方法：

```javascript
let arr = [1, 2, 3];
arr.forEach((item, index, array) => {
  console.log(item, index, array);
});
// 输出: 1 0 [1, 2, 3]
// 输出: 2 1 [1, 2, 3]
// 输出: 3 2 [1, 2, 3]
```

map 方法：

```javascript
let arr = [1, 2, 3];
let newArr = arr.map((item, index, array) => {
  return item * 2;
});
console.log(newArr); // 输出: [2, 4, 6]
```

filter 方法：

```javascript
let arr = [1, 2, 3, 4, 5];
let newArr = arr.filter((item, index, array) => {
  return item > 2;
});
console.log(newArr); // 输出: [3, 4, 5]
```

## Object

### 对象的增删改查

删除：

```javascript
let obj = {
  name: "张三",
  age: 20,
  gender: "男",
};
delete obj.age;
```

### 对象的遍历

for...in 循环：

```javascript
let obj = {
  name: "张三",
  age: 20,
  gender: "男",
};
for (let key in obj) {
  console.log(key, obj[key]);
}
```

Object.keys() 方法：

```javascript
let obj = {
  name: "张三",
  age: 20,
  gender: "男",
};
let keys = Object.keys(obj);
console.log(keys); // 输出: ['name', 'age', 'gender']
```

### Array.map 与 Array.forEach 的区别：

相同点：

- 都是数组的方法
- 都是遍历数组中的每一个元素

不同点：

- map 方法会返回一个新的数组，而 forEach 方法不会返回任何值
- map 方法可以对数组中的每一个元素进行操作，而 forEach 方法只能遍历数组中的每一个元素
- map 方法可以链式调用，而 forEach 方法不能
