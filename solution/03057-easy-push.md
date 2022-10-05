### Question
```ts
type Result = Push<[1, 2], '3'> // [1, 2, '3']
```
### Solution
```ts
type Push<T extends unknown[], U> = [...T, U]
```
[https://github.com/type-challenges/type-challenges/blob/main/questions/03057-easy-push/README.md](https://github.com/type-challenges/type-challenges/blob/main/questions/03057-easy-push/README.md)
