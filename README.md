# validator benchmark

## Packages in benchmark

| Package | Stars | Quality |
| ------- | ----- | ------- |
| [validator.js](https://github.com/guillaumepotier/validator.js) | 251 | 70
| [validate.js](https://github.com/ansman/validate.js) | 2,132 | 73
| [validatorjs](https://github.com/skaterdav85/validatorjs) | 1,119 | 71
| [joi](https://github.com/hapijs/joi) | 13,645 | 89
| [ajv](https://github.com/epoberezkin/ajv) | 6,468 | 87
| [mschema](https://github.com/mschema/mschema) (*) | 107 | 31
| [parambulator](https://github.com/rjrodger/parambulator) (*) | 41 | 68
| [fastest-validator](https://github.com/icebob/fastest-validator) | 691 | 68
| [yup](https://github.com/jquense/yup) | 7,314 | 71

 (*) not supported advanced types (email, url, ...etc)

## Benchmark #1 (simple object)

### Test object
```js
let object = {
    name: "john doe",
    email: "john.doe@company.space",
    firstName: "John",
    phone: "123-4567",
    age: 33
}
```

### Code
[/suites/simple.js](https://github.com/icebob/validator-benchmark/blob/master/suites/simple.js)

### Result

```
Platform info:
==============
   Windows_NT 10.0.22000 x64
   Node.JS: 16.14.0
   V8: 9.4.146.24-node.20
   CPU: 12th Gen Intel(R) Core(TM) i5-12600K × 16
   Memory: 32 GB

Suite: Simple object
✔ validator.js              1.033.357 rps
✔ validate.js                 537.337 rps
✔ validatorjs                 365.611 rps
✔ joi                         318.212 rps
✔ ajv                      13.199.169 rps
✔ mschema                   1.292.487 rps
✔ parambulator                 49.237 rps
✔ fastest-validator        14.002.822 rps
✔ yup                          79.317 rps

   validator.js            -92,62%      (1.033.357 rps)   (avg: 967ns)
   validate.js             -96,16%        (537.337 rps)   (avg: 1μs)
   validatorjs             -97,39%        (365.611 rps)   (avg: 2μs)
   joi                     -97,73%        (318.212 rps)   (avg: 3μs)
   ajv                      -5,74%     (13.199.169 rps)   (avg: 75ns)
   mschema                 -90,77%      (1.292.487 rps)   (avg: 773ns)
   parambulator            -99,65%         (49.237 rps)   (avg: 20μs)
   fastest-validator            0%     (14.002.822 rps)   (avg: 71ns)
   yup                     -99,43%         (79.317 rps)   (avg: 12μs)
-----------------------------------------------------------------------
```

[![Result](https://user-images.githubusercontent.com/306521/68978853-404a8500-07fc-11ea-94e4-0c25546dad04.png)](https://cloud.highcharts.com/show/yqowupa)
