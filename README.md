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
✔ validator.js              1.015.285 rps
✔ validate.js                 516.617 rps
✔ validatorjs                 259.151 rps
✔ joi                         214.613 rps
✔ ajv                       9.679.298 rps
✔ mschema                     942.546 rps
✔ parambulator                 32.944 rps
✔ fastest-validator        11.547.593 rps
✔ ow                           94.294 rps
✔ yup                          69.062 rps
✔ zod                         399.667 rps
✔ typanion                    876.791 rps

   validator.js            -91,21%      (1.015.285 rps)   (avg: 984ns)
   validate.js             -95,53%        (516.617 rps)   (avg: 1μs)
   validatorjs             -97,76%        (259.151 rps)   (avg: 3μs)
   joi                     -98,14%        (214.613 rps)   (avg: 4μs)
   ajv                     -16,18%      (9.679.298 rps)   (avg: 103ns)
   mschema                 -91,84%        (942.546 rps)   (avg: 1μs)
   parambulator            -99,71%         (32.944 rps)   (avg: 30μs)
   fastest-validator            0%     (11.547.593 rps)   (avg: 86ns)
   ow                      -99,18%         (94.294 rps)   (avg: 10μs)
   yup                      -99,4%         (69.062 rps)   (avg: 14μs)
   zod                     -96,54%        (399.667 rps)   (avg: 2μs)
   typanion                -92,41%        (876.791 rps)   (avg: 1μs)
-----------------------------------------------------------------------
```

[![Result](https://user-images.githubusercontent.com/306521/68978853-404a8500-07fc-11ea-94e4-0c25546dad04.png)](https://cloud.highcharts.com/show/yqowupa)
