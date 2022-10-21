### Question
```ts
type Arr = ['1', '2', '3']
type Test = TupleToUnion<Arr> // expected to be '1' | '2' | '3'
```
### Solution
```ts
type TupleToUnion<T extends any[]> = T[number] 
```
---
[https://github.com/type-challenges/type-challenges/blob/main/questions/00010-medium-tuple-to-union/README.md](https://github.com/type-challenges/type-challenges/blob/main/questions/00010-medium-tuple-to-union/README.md)
