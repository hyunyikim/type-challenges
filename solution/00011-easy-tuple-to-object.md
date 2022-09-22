### Question
```ts
const tuple = ['tesla', 'model 3', 'model X', 'model Y'] as const
type result = TupleToObject<typeof tuple> // expected { tesla: 'tesla', 'model 3': 'model 3', 'model X': 'model X', 'model Y': 'model Y'}
```
### Solution
```ts
typeof TupleToObject<T extends readonly (string | number)[]> = {
  [K in T[number]]: K
}
```

---
https://github.com/type-challenges/type-challenges/blob/main/questions/00011-easy-tuple-to-object/README.md
