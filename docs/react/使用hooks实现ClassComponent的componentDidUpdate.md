```javascript
const useDidUpdate = (callback = () => {}) => {
  const mounting = useRef(true);
  useEffect(() => {
    if (mounting.current) {
      mounting.current = false;
    } else {
      callback();
    }
  });
}
```