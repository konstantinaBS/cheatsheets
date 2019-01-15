## Accessing "private" functions

`#'` is a subsitute for `var`

e.g. `#'a.b/d` is equivalent to `(var a.b/d)`

When Clojure sees the var, it automatically substitutes the function before evaluation

source: https://stackoverflow.com/questions/37471253/how-can-i-write-unit-tests-for-private-clojure-functions
