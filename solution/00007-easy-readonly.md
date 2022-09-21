### Qustion
```ts
  interface Todo {
    title: string
    description: string
  }
  
  const todo: MyReadonly<Todo> = {
    title: "Hey",
    description: "foobar"
  }
  
  todo.title = "Hello" // Error: cannot reassign a readonly property
  todo.description = "barFoo" // Error: cannot reassign a readonly property
```

### Solution
```ts
type MyReadonly<T> = {
  readonly [K in keyof T]: T[K]
}
```
---
[https://github.com/type-challenges/type-challenges/tree/main/questions/00007-easy-readonly](https://github.com/type-challenges/type-challenges/tree/main/questions/00007-easy-readonly)
