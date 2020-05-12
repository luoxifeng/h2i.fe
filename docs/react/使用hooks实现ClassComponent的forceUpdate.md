两种方式useReducer和useState

- useReducer（react官方提供了一种方式）
```javscript
const [, forceUpdate] = useReducer(x => x + 1, 0);
```
- useState
```javscript
const forceUpdate = () => useState(0)[1];
```
