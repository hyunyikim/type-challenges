### Question
```ts
type isPillarMen = Includes<['Kars', 'Esidisi', 'Wamuu', 'Santana'], 'Dio'> // expected to be `false`
```
### Solution
```ts
type Includes<T extends unknown[], U> = U extends T[number] ? true : false
```
---
[https://github.com/type-challenges/type-challenges/tree/main/questions/00898-easy-includes](https://github.com/type-challenges/type-challenges/tree/main/questions/00898-easy-includes)
