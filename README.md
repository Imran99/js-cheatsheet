# JS Cheatsheet

## Data Types
```javascript
let bool    = true;
let n       = null;
let undef   = undefined;
let integet = new Number(1);
let float   = new Number(1.2);
let obj     = new SomeObject();
```

## Array
```javascript
let zeroInitialised = new Array(5).fill(0);
```

### common operations
```javascript
let sum         = myArray.reduce((a, b) => a + b);
let includes    = myArray.includes(‘cat’)
let mapped      = myArray.map((element, index) => element++)
let sum         = myArray.reduce((accumulator, current) => accumulator + current, initialVal)
let ascending   = ints.sort((a, b) => a - b);
let filtered    = arrayWithNulls.filter(e => e !== null);
```

### stack
```javascript
let peek  = stack[stack.length-1];
let pop   = stack.pop();
let push  = stack.push(x);
```

## String

```javascript
let charArray = myString.split(‘’)
let char      = myString[1];
let repeating = ‘abc’.repeat(10);
let anInt     = parseInt(someString);
let aFloat    = parseFloat(someString);
let reversed  = s.split('').reverse().join('');
let lines     = input.split('\n');
```

## Map

```javascript
let map = new Map([
  ['[', ']'],
  ['(', ')'],
  ['{', '}'],
]);

map.has(key)
let val = map.get(key)
map.set(key, val)
```

## Set

```javascript
let set = new Set([1, 2, 3]);

let size = mySet.size;
set.add(item);
set.has(item);
```

## for ... of

```javascript
for (let o of someIterable) {
  console.log(o);
}
```

## Switch Case

```javascript
switch (‘Papayas’) {
  case 'Oranges':
    console.log('Oranges are $0.59 a pound.');
    break;
  case 'Mangoes':
  case 'Papayas':
    console.log('Mangoes and papayas are $2.79 a pound.');
    break;
  default:
    console.log('Sorry, we are out of ' + expr + '.');
}
```

## try ... catch ... throw

```javascript
try {
  if(something) {
    throw new Error(‘some error message’);
  }
} catch (e) {
  console.log(e.message);
}
```

## Classes

```javascript
class Rectangle {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }

  // Getter
  get area() {
    return this.calcArea();
  }

  // Method
  calcArea() {
    return this.height * this.width;
  }

  static distance(a, b) {
    const dx = a.x - b.x;
    const dy = a.y - b.y;

    return Math.hypot(dx, dy);
  }
}
```

## Math
```javascript
lat abs     = Math.abs(num);
let int     = Math.trunc(num);
let rounded = num.toFixed(2);
```

## Mocha, Chai

```javascript
describe(‘Some feature’, () => {
    it(‘should meet expectations’, () => {
      [1,2,3].should.deep.equal([1, 2, 3]);
    });
});
```

## References
* https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference
* https://github.com/mbeaudru/modern-js-cheatsheet#tdz_sample
