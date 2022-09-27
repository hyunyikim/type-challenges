### Question
```ts
type Result = MyExclude<'a' | 'b' | 'c', 'a'> // 'b' | 'c'
```

### Solution
```ts
type MyExclude<T, U> = T extends U ? never : T
```
---
[https://github.com/type-challenges/type-challenges/blob/main/questions/00043-easy-exclude/README.md](https://github.com/type-challenges/type-challenges/blob/main/questions/00043-easy-exclude/README.md)
