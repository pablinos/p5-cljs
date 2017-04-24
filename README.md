# p5-cljs

A wrapper library building on `cljsjs.p5` (externs for [P5](http://p5js.org)), inspired by [Quil](http://quil.info/). It's far from complete and there's probably something intelligent I could do with macros to avoid all the repetition, but what's there is usable.

## Usage

Add `p5-cljs` as a dependency and then create a sketch by passing in your `setup` and `draw` functions.

```clojure
(ns application.core
  (:require 
    [p5-cljs.core :as p]))

  (p/create-sketch 
   {
    :element-id "sketch"
    :setup setup-fn
    :draw draw-fn
    })
```

The wrappers allow you to call `(p/rect x y w h)` and have it operate on the 'current' sketch. 

