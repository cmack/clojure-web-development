# Learning Clojure

## Intro to Clojure

I highly recommend you visit [clojure-doc](http://clojure-doc.org/) and click
"Getting Started" or watch [Chas Emerick's Starting Clojure](http://cemerick.com/2012/05/02/starting-clojure/).

## Books

[Clojure for the Brave and True](http://www.braveclojure.com/)
is about the best book out there for getting started.

## Docs

[clojuredocs](https://clojuredocs.org/) (not to be confused with clojure-doc)
is full of *fantastic* documentation. Additionally, Clojure has docstrings!
The Clojure repl has a convenience function for fetching them for reference.

Just run `lein repl` and then:

```clojure
(doc map)
-------------------------
clojure.core/+ ;; 1
([] [x] [x y] [x y & more]) ;; 2
  Returns the sum of nums. (+) returns 0. Does not auto-promote ;; 3
  longs, will throw on overflow. See also: +'
  nil ;; 4
```

The docs will show:
1. the fully namespaced name of the function
2. The arguments of the function
3. The string describing how the function can be used

4 is just the return value that the REPL spits up.

## Exercises

If you're *just* getting started I recommend checking out the
[Clojure Koans](http://clojurescriptkoans.com/) or
[4Clojure](http://www.4clojure.com/) for the basics.

If you have the basics down and just want to level up a little maybe
try some [Exercism](http://exercism.io/), [99 Lisp problems](https://github.com/nashville-lispers/99-problems),
or [the Evercraft kata](https://github.com/nashville-lispers/evercraft-kata).

## MOAR!

If you want a more complete list of references check out the Nashville Lisper's
[resources repo](https://github.com/nashville-lispers/resources)