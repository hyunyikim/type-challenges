### Question
```ts
  type tesla = ['tesla', 'model 3', 'model X', 'model Y']
  type spaceX = ['FALCON 9', 'FALCON HEAVY', 'DRAGON', 'STARSHIP', 'HUMAN SPACEFLIGHT']
  
  type teslaLength = Length<tesla>  // expected 4
  type spaceXLength = Length<spaceX> // expected 5
```

### Solution
```ts
  type Length<T extends any[]> = T['length']
  type Legnth<T extends {length: number}> = T['length']
```
---
[https://github.com/type-challenges/type-challenges/tree/main/questions/00018-easy-tuple-length](https://github.com/type-challenges/type-challenges/tree/main/questions/00018-easy-tuple-length)
