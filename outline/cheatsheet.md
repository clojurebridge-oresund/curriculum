## Data Structures - Vector

### Creating a vector

```clj
(vector 5 10 15)
[1 2 3 4 5]
[56.9 60.2 61.8 63.1 54.3 66.4 66.5 68.1 70.2 69.2 63.1 57.1]
[]
```

#### Functions for vectors

```clj
(vector? [5 10 15])
;=> true

(vector 5 10 15)
;=> [5 10 15]

(conj [5 10] 15)
;=> [5 10 15]

(count [5 10 15])
;=> 3

(nth [5 10 15] 1)
;=> 10

(first [5 10 15])
;=> 5
```

## Data Structures2 - Keyword, Maps

#### Creating a map

```clj
{:firstname "Sally" :lastname "Brown"}
{:a 1 :b "two"}
{}
```


#### Functions for Maps

```clj
; determine if value is a map
(map? {:firstname "Sally" :lastname "Brown"})
;=> true

; using keyword :firstname get the value
(get {:firstname "Sally" :lastname "Brown"} :firstname)
;=> "Sally"

; using keyword :firstname get the value and return :MISS if key doesn't exist in map
(get {:firstname "Sally"} :lastname :MISS)
;=> :MISS

; add a key/value to the map
(assoc {:firstname "Sally"} :lastname "Brown")
;=> {:firstname "Sally", :lastname "Brown"}

; remove (disassociate) the key/value of :lastname
(dissoc {:firstname "Sally" :lastname "Brown"} :lastname)
;=> {:firstname "Sally"}

; merge two maps
(merge {:firstname "Sally"} {:lastname "Brown"})
;=> {:firstname "Sally", :lastname "Brown"}

; get number of key/value pairs in this map
(count {:firstname "Sally" :lastname "Brown"})
;=> 2

; get all the keys in this map
(keys {:firstname "Sally" :lastname "Brown"})
;=> (:firstname :lastname)

; get all the values in this map
(vals {:firstname "Sally" :lastname "Brown"})
;=> ("Sally" "Brown")
```

## Defining Functions

```clj
(defn function-name
  "description of function, optional"
  [param1 param2]
  ((function-body)))
```

* Functions that return true or false--called predicates--usually end in ?
* map and reduce - Functions that take other functions

## Flow Control

```clj
(if conditional-expression
  expression-to-evaluate-when-true
  expression-to-evaluate-when-false)
```

## Boolean logic with and, or and not

| x     | y     | (and x y) | (or x y) | (not x) | (not y) |
| ----- | ----- | --------- | -------- | ------- | ------- |
| false | false | false | false | true  | true  |
| true  | false | false | true  | false | true  |
| true  | true  | true  | true  | false | false |
| false | true  | false | true  | true  | false |

## let 
Assigning names to values inside of functions

```clj
(let [firstname (:firstname user)              ; assign to `firstname`
      message (str "Hello, " firstname "!")]   ; assign to `message`
  (println message))                           ; do something with `message`
```


