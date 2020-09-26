# fd-wrapper

I re-used the same script way too many times.  
So why not publish it?

```js
const fdWrapper = require("fd-wrapper");
let fd = new FormData();
fd.set("foo", "bar");
fd.set("123", 456);

let wrapper = fdWrapper(fd);

console.log(wrapper.foo); // bar
console.log(wrapper["123"]); // 456

wrapper.foo = "baz";
console.log(fd.get("foo")); // baz
```
