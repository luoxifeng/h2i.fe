---
title: 使用hooks实现useReducer
layout: page
---

模拟实现

```javascript
const useReducer = (reducer, initState) => {
  const [state, setState] = useState(initState);
  const dispatch = (action) => {
    const nextState = reducer(action);
    setState(nextState);
  };
  return [state, dispatch];
}
```

demo
```javascript
function Todos() {
  const [todos, dispatch] = useReducer(todosReducer, []);

  function handlerAction(payload) {
    dispatch({ 
      type: 'add', 
      payload 
    });
  }
}
```

