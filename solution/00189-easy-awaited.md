### Question 
```ts
type ExampleType = Promise<string>
type Result = MyAwaited<ExampleType> // string
```

### Solution
```ts
type MyAwaited<T> = T extends Promise<infer R> ? MyAwaited<R> : T;
```
---
[https://github.com/type-challenges/type-challenges/blob/main/questions/00189-easy-awaited/README.md](https://github.com/type-challenges/type-challenges/blob/main/questions/00189-easy-awaited/README.md)
