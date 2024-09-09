# TypeScript

## 是否有使用过 TypeScript？在项目中是如何使用的？

## 什么是泛型，在项目中的最佳实践？

泛型是指在定义函数、接口或类时，不预先指定具体的类型，而是在使用时再指定类型的一种特性。

在项目中，泛型可以帮助我们提高代码的复用性和灵活性。例如，在定义一个函数时，我们可以使用泛型来指定函数的参数类型和返回值类型，这样就可以在不同的场景下使用同一个函数。

最佳实践：

- 在定义函数时，尽量使用泛型
- 在定义接口时，尽量使用泛型
- 在定义类时，尽量使用泛型

举个例子

```typescript
function createArray<T>(length: number, value: T): T[] {
  return Array(length).fill(value);
}

const result = createArray(3, "a");
console.log(result); // ['a', 'a', 'a']
```
