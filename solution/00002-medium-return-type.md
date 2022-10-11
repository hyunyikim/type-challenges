### Question
```ts
const fn = (v: boolean) => {
  if (v)
    return 1
  else
    return 2
}

type a = MyReturnType<typeof fn> // should be "1 | 2"
```
### Solution
```ts
type MyReturnType<T> = T extends (...args: any) => infer R ? R : T
```
---
[https://github.com/type-challenges/type-challenges/tree/main/questions/00002-medium-return-type](https://github.com/type-challenges/type-challenges/tree/main/questions/00002-medium-return-type)
