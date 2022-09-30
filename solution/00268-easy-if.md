### Question

```ts
type A = If<true, 'a', 'b'>  // expected to be 'a'
type B = If<false, 'a', 'b'> // expected to be 'b'
```

### Solution

```ts
type If<C extends boolean, T, F> = C extends true ? T : F;
```
---
[https://github.com/type-challenges/type-challenges/blob/main/questions/00268-easy-if/README.md](https://github.com/type-challenges/type-challenges/blob/main/questions/00268-easy-if/README.md)
