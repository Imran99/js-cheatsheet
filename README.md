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
let 2DInitialised   = new Array(n).fill(0).map( x => new Array(n).fill(1) );
let sequence        = new Array(n).map((_, i) => i));
```

### common operations
```javascript
let includes    = myArray.includes(‘cat’);
let mapped      = myArray.map((element, index) => element++);
let sum         = myArray.reduce((sum, current) => sum + current);
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

let size = map.size;
```

## Set

```javascript
let set = new Set([1, 2, 3]);

let size = mySet.size;
set.add(item);
set.has(item);

let size = set.size;
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
let abs = Math.abs(num);
let int = Math.trunc(num);
let str = num.toFixed(2);
```

## Date
```javascript
let date = new Date();

console.log(date); //Tue Feb 20 2018 09:50:47 GMT+1100 (AEDT)
console.log(date.toUTCString()) //Mon, 19 Feb 2018 22:50:47 GMT
console.log(new Date(date.getTime())); //Tue Feb 20 2018 09:50:47 GMT+1100 (AEDT)
console.log(new Date('12/01/1980')); //Mon Dec 01 1980 00:00:00 GMT+1100 (AEDT)
console.log(Date.parse('12/01/1980')); //Mon Dec 01 1980 00:00:00 GMT+1100 (AEDT)
console.log(date.getDate()); //20
console.log(date.getDay()); //2 (0-6)
console.log(date.getUTCDay()); //1
console.log(date.getFullYear()); //2018
console.log(date.getHours()); //9
console.log(date.getMilliseconds()); //536
console.log(date.getMinutes()); //50
console.log(date.getMonth()); //1
console.log(date.getSeconds()); //47
console.log(date.getTime()); //1519080647536
console.log(date.toDateString()); //Tue Feb 20 2018
console.log(date.toISOString()); //2018-02-19T22:50:47.536Z
```

## Console
```javascript
console.log(`multiline template
literal string
${someVar}`)
```

## Promise
```javascript
let p = new Promise( (resolve, reject) => {
  if(something) {
    resolve(data);
  } else {
    reject(new Error('some error'));
  }
});
```

## Mocha, Chai

```javascript
const should = require('chai').should();

describe(‘Some feature’, () => {
    it(‘should meet expectations’, () => {
      [1,2,3].should.deep.equal([1, 2, 3]);
    });
});
```

## Request

```bash
npm i -S request
npm i -S request-promise
```

```javascript
const request = require('request-promise');

request({
  uri: 'https://swapi.co/api/planets',
  json: true
}).then(r => {
    let planets = r.results
      .map(p => p.name)
      .reduce( (str, p) => str += `, ${p}`);
    console.log(planets);
  })
  .catch(e=>{
    console.log(e);
  });
```

## References
* https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference
* https://github.com/mbeaudru/modern-js-cheatsheet#tdz_sample
* https://www.npmjs.com/package/request-promise
