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
✔ validator.js              1.028.961 rps
✔ validate.js                 539.468 rps
✔ validatorjs                 360.864 rps
✔ joi                         317.370 rps
✔ ajv                      12.852.562 rps
✔ mschema                   1.317.827 rps
✔ parambulator                 48.926 rps
✔ fastest-validator        13.994.413 rps
✔ yup                          79.091 rps
✔ zod                         473.776 rps

   validator.js            -92,65%      (1.028.961 rps)   (avg: 971ns)
   validate.js             -96,15%        (539.468 rps)   (avg: 1μs)
   validatorjs             -97,42%        (360.864 rps)   (avg: 2μs)
   joi                     -97,73%        (317.370 rps)   (avg: 3μs)
   ajv                      -8,16%     (12.852.562 rps)   (avg: 77ns)
   mschema                 -90,58%      (1.317.827 rps)   (avg: 758ns)
   parambulator            -99,65%         (48.926 rps)   (avg: 20μs)
   fastest-validator            0%     (13.994.413 rps)   (avg: 71ns)
   yup                     -99,43%         (79.091 rps)   (avg: 12μs)
   zod                     -96,61%        (473.776 rps)   (avg: 2μs)
-----------------------------------------------------------------------
```

[![Result](https://user-images.githubusercontent.com/306521/68978853-404a8500-07fc-11ea-94e4-0c25546dad04.png)](https://cloud.highcharts.com/show/yqowupa)
