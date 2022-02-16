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
✔ validator.js                999.925 rps
✔ validate.js                 517.071 rps
✔ validatorjs                 317.847 rps
✔ joi                         267.952 rps
✔ ajv                       9.803.050 rps
✔ mschema                     927.354 rps
✔ parambulator                 34.191 rps
✔ fastest-validator        10.614.409 rps
✔ ow                           74.893 rps
✔ yup                          71.066 rps
✔ zod                         349.634 rps

   validator.js            -90,58%        (999.925 rps)   (avg: 1μs)
   validate.js             -95,13%        (517.071 rps)   (avg: 1μs)
   validatorjs             -97,01%        (317.847 rps)   (avg: 3μs)
   joi                     -97,48%        (267.952 rps)   (avg: 3μs)
   ajv                      -7,64%      (9.803.050 rps)   (avg: 102ns)
   mschema                 -91,26%        (927.354 rps)   (avg: 1μs)
   parambulator            -99,68%         (34.191 rps)   (avg: 29μs)
   fastest-validator            0%     (10.614.409 rps)   (avg: 94ns)
   ow                      -99,29%         (74.893 rps)   (avg: 13μs)
   yup                     -99,33%         (71.066 rps)   (avg: 14μs)
   zod                     -96,71%        (349.634 rps)   (avg: 2μs)
-----------------------------------------------------------------------
```

[![Result](https://user-images.githubusercontent.com/306521/68978853-404a8500-07fc-11ea-94e4-0c25546dad04.png)](https://cloud.highcharts.com/show/yqowupa)
