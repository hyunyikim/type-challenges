### Question

```ts
type Result = Concat<[1], [2]> // expected to be [1, 2]
```

### Solution

```ts
type Concat<T extends unknown[], U extends unknown[]> = [...T, ...U]
```
---
[https://github.com/type-challenges/type-challenges/blob/main/questions/00533-easy-concat/README.md](https://github.com/type-challenges/type-challenges/blob/main/questions/00533-easy-concat/README.md)
