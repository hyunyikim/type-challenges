### Question
```ts
interface Todo {
  title: string
  description: string
  completed: boolean
}

const todo: MyReadonly2<Todo, 'title' | 'description'> = {
  title: "Hey",
  description: "foobar",
  completed: false,
}

todo.title = "Hello" // Error: cannot reassign a readonly property
todo.description = "barFoo" // Error: cannot reassign a readonly property
todo.completed = true // OK
```
### Solution
```ts
type MyReadonly2<T, K extends keyof T = keyof T> = T & {
  readonly [P in K]: T[P]
}
```
---
[https://github.com/type-challenges/type-challenges/blob/main/questions/00008-medium-readonly-2/README.md](https://github.com/type-challenges/type-challenges/blob/main/questions/00008-medium-readonly-2/README.md)
