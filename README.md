# JS Kata Template

A template for writing basic JavaScript katas with mutation testing from [Stryker](https://stryker-mutator.io/) to check your coverage.

## Running

```
git clone git@github.com:jbrunton/js-kata-template.git
npm install
```

To run tests:

```
npm test
```

To watch for changes:

```
npm test:watch
```

To run mutation tests:

```
npm 
```

## Transformation Priority Premise

| Transformation | Notes |
| -------------- | ----- |
| `({} → nil)` | no code at all->code that employs nil |
| `(nil → constant)` | |
| `(constant → constant+)` | a simple constant to a more complex constant |
| `(constant → scalar)` | replacing a constant with a variable or an argument |
| `(statement → statements)` | adding more unconditional statements |
| `(unconditional → if)` | splitting the execution path |
| `(scalar → array)` | |
| `(array → container)` | |
| `(statement → recursion)` | |
| `(if → while)` | |
| `(expression → function)` | replacing an expression with a function or algorithm |
| `(variable → assignment)` | replacing the value of a variable |

Source: [Transformation Priority Premise](http://blog.cleancoder.com/uncle-bob/2013/05/27/TheTransformationPriorityPremise.html) by Robert C. Martin.