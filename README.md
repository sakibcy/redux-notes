# Redux

- [Pros]()
- [Cons]()

## Pros

- Predictable state changes
- Centralized state
- Easy debugging
- Preserve page state
- Undo/redo
- Ecosystem of add-ons

## Cons

- Complexity
- Verbosity

## When not to use REDUX

- Tight budget
- Small to medium-size apps
- Simple UI/data flow
- Static data
- [You Might Not Need Redux by Dan Abramov]()

## Functional programming

## curring

```javascript
// javascript

function add(a) {
  return function (b) {
    return a + b;
  };
}

const add2 = (a) => (b) => a + b;

add(1)(3);
add2(1)(4);
```

## Pure function

A ‘Pure function’ is a function whose inputs are declared as inputs and none of them should be hidden. The outputs are also declared as outputs.

Pure functions act on their parameters. It is not efficient if not returning anything. Moreover, it offers the same output for the given parameters

- No random values
- No current date/time
- No global state (DOM, files, db, etc)
- No mutation of parameters

```javascript
function func(a, b) {
  return a + b;
}
```

#### Benefits

- Self-documenting
- Easily testable
- Concurrency
- Cacheable

## Immutable Data

Immutable Data means that you should easily able to create data structures instead of modifying ones which is already exist.

```javascript
const person = {
    name: "Sakib",
    address: {
        country: "Bangladesh",
        city: "Dhaka"
    }
};

const updated = {
    ...person,
    address: {
        ...person.address,
        city: "Khulna"
    },
    name = "Hasan"
};

console.log(person);
```

#### Note: we have libraries for doing immutability

- immer
- immutable
- mori

here when we are modifying object, we are not directly changing it. We first copy and create new object then modify the new object

### Pros

- Predictability
- Faster Change Detection
- Concurrency

### Cons

- Performance
- Memory overhead
