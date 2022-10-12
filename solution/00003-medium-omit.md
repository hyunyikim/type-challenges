### Question
```ts
interface Todo {
  title: string
  description: string
  completed: boolean
}

type TodoPreview = MyOmit<Todo, 'description' | 'title'>

const todo: TodoPreview = {
  completed: false,
}
```
### Solution
```ts
type MyOmit<T, K extends keyof T> = {
  [P in keyof T as P extends K ? never : P]: T[P]
}
```
---
[https://github.com/type-challenges/type-challenges/blob/main/questions/00003-medium-omit/README.md](https://github.com/type-challenges/type-challenges/blob/main/questions/00003-medium-omit/README.md)
