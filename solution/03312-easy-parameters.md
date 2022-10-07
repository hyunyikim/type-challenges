### Question
```ts
const foo = (arg1: string, arg2: number): void => {}
type FunctionParamsType = MyParameters<typeof foo> // [arg1: string, arg2: number]
```
### Solution
```ts
type MyParameters<T extends (...args: any[]) => any> = T extends (...args: infer P) => any ? P : [];
```
---
[https://github.com/type-challenges/type-challenges/blob/main/questions/03312-easy-parameters/README.md](https://github.com/type-challenges/type-challenges/blob/main/questions/03312-easy-parameters/README.md)
