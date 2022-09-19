### Question

```ts
interface Todo {
  title: string
  description: string
  completed: boolean
}

type TodoPreview = MyPick<Todo, "title" | "completed">

const todo: TodoPreview = {
  title: "Clean room",
  completed: false,
}
```

### Solution

```ts
type MyPick<T, K extends keyof T> = {
  [P in K]: T[P]
}
```

---

[https://github.com/type-challenges/type-challenges/tree/main/questions/00004-easy-pick](https://github.com/type-challenges/type-challenges/tree/main/questions/00004-easy-pick)
