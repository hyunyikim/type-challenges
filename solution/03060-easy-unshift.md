### Question
```ts
type Result = Unshift<[1, 2], 0> // [0, 1, 2,]
```
### Solution
```ts
type Unshift<T extends unknown[], U> = [U, ...T]
```
---
[https://github.com/type-challenges/type-challenges/blob/main/questions/03060-easy-unshift/README.md](https://github.com/type-challenges/type-challenges/blob/main/questions/03060-easy-unshift/README.md)
