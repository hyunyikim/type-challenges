### Question
```ts
type X = { 
  x: { 
    a: 1
    b: 'hi'
  }
  y: 'hey'
}

type Expected = { 
  readonly x: { 
    readonly a: 1
    readonly b: 'hi'
  }
  readonly y: 'hey' 
}

type Todo = DeepReadonly<X> // should be same as `Expected`
```
### Solution
```ts
type DeepReadonly<X> = {
  readonly [P in keyof X]: X[P] extends Record<string, unknown> ? DeepReadonly<X[P]> : X[P]
}
```
---
[https://github.com/type-challenges/type-challenges/blob/main/questions/00009-medium-deep-readonly/README.md](https://github.com/type-challenges/type-challenges/blob/main/questions/00009-medium-deep-readonly/README.md)
