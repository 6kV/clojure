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
(defn inc-maker<br/>  
"Create a custom incrementor"  
[inc-by]  
#(+ % inc-by))  
(def inc3 (inc-maker 3))  
(inc3 7)  
; => 10  
`
