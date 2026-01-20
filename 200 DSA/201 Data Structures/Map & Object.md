
|Feature|`Map`|`Object`|
|---|---|---|
|**Key Types**|Can be **any data type** (strings, numbers, booleans, objects, functions, etc.).|Must be a `String` or `Symbol` (other types are converted to strings).|
|**Order**|**Maintains insertion order**.|**Does not guarantee order** (though in modern JS, string-keyed properties have an order, it's less consistent).|
|**Size**|Has a built-in `.size` property for easy and fast retrieval of the count.|Size must be determined manually, e.g., using `Object.keys().length`, which is less performant.|
|**Iteration**|Directly iterable using `for...of` loops, which return key-value pairs in insertion order.|Not directly iterable with `for...of`; requires methods like `Object.keys()`, `Object.values()`, or `Object.entries()`.|
|**Prototype**|Does not have a prototype by default, so no default keys can cause collisions with user data.|Has a prototype, which means default properties (like `toString`, `hasOwnProperty`) exist and could potentially be overwritten.|
|**Performance**|Generally better performance for frequent additions/deletions and large datasets.|Generally better performance for read-heavy operations with a fixed, small set of string-based keys.|
|**JSON Support**|No direct built-in support for JSON serialization; requires manual conversion.|Has direct, native support for `JSON.stringify()` and `JSON.parse()`.|

Map example:
```javascript
const myMap = new Map([
  ["id", 1],
  ["name", "Alice"],
  ["role", "Admin"]
]);
```

### Methods
- has()
- set()
- get()

### Properties
- size

### Things to Remember:
- Can't use brackets to access a Map's value
- 