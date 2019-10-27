# clojure

### Leiningen
 + **lein new app clojure-noob**
 + **lein run**
 + **lein uberjar** :will create the jar
 + **lein repl** : REPL : read, evaluate, prints and loops 
 
#### Control Flow 

 + `(if boolean-form
     then-form
     optional-else-form)`
     
#### Naming with def

you can use def to bind a name to a value in clojure

`(def failed-protagonist-names
["Larry Potter" "Doreen the Explorer" "The Incredible Bulk"])`

#### data structures

All clojure's data structures are immutable 

#### Map 

` {:a 1 :b 2} `

#### Vector 

` [1 2 3]`

#### Lists

`'(1 2 3)`

#### Set

`#{1 2 3}`

#### Anonymous function

`(fn [x] (str "hello" " world")`

#### Returned Function 
functions can return other functions. The returned functions are closures, which means that they can access all the variables that were in scope when the function was created

`
(defn inc-maker
"Create a custom incrementor"  
[inc-by]  
#(+ % inc-by))
(def inc3 (inc-maker 3))
(inc3 7)  
; => 10  
`

#### let 
let binds names to values

`(let [x 3]
x)`

let forms have two main uses. First, they provide clarity by allowing you to name things. Second, they allow you to evaluate an expression only once and reuse the result. This is especially important when you need to reuse the result of an expensive function call, like a network API call. It’s also important when the expression has side effects.

#### loop

`
(loop [iteration 0]
(println (str "Iteration " iteration))
(if (> iteration 3)
(println "Goodbye!")
(recur (inc iteration))))`

#### Regular Expression

regular expression are tools for performing pattern matching on Text.
`(re-find #"^left-" "left-eye")`

#### Reduce

The pattern of process each element in a sequence and build a result is so com-
mon that there’s a built-in function for it called reduce . Here’s a simple
example:
`
;; sum with reduce
(reduce + [1 2 3 4])
; => 10
`

This is like telling Clojure to do this:

`(+ (+ (+ 1 2) 3) 4)`

