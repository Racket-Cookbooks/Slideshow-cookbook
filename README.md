# Slideshow Cookbook
Racket Slideshow cookbook


<img src="https://github.com/racket/slideshow/blob/master/slideshow-exe/slideshow/start.png" width="200px;" alt="" align="right"/>

[![Racket](https://img.shields.io/badge/-Racket-darkred?logo=racket)](https://racket-lang.org)
[![Discourse users](https://img.shields.io/discourse/users?label=Discuss%20on%20Racket%20Discourse&logo=racket&server=https%3A%2F%2Fracket.discourse.group)](https://racket.discourse.group/)
[![Racket Discord](https://img.shields.io/discord/571040468092321801?label=Chat%20on%20Racket%20Discord&logo=racket)](https://discord.gg/6Zq8sH5)

Welcome to the Racket Slideshow Cookbook. This is a growing collection of recipes for creating the tastiest presentations with the [Racket Slideshow library](https://docs.racket-lang.org/slideshow/index.html) (documentation).

If you would like to contribute please create an issue or pull request with your contribution. Please include image, code, and short description.

Contributions are accepted on the condition they are licenced under the same terms as Racket: MIT or Apache 2.

## Packages

* [slideshow-repl](https://docs.racket-lang.org/slideshow-repl/index.html): interactive evaluation within a slide presentation
* [`ppict`](https://pkgs.racket-lang.org/package/ppict): progressive picts and slideshows - see [Progressive pict slideshow template](https://github.com/racket-templates/ppict-slideshow-template) at https://github.com/racket-templates/
* [`scribble-slideshow`](https://docs.racket-lang.org/scribble-slideshow/index.html): Write slideshows using Scribble
* [Slideshow LaTeX](https://docs.racket-lang.org/slideshow-latex/index.html): embedding LaTeX in Racket slideshows
* [`slideshow-pretty`](https://pkgs.racket-lang.org/package/slideshow-pretty): Slideshow extensions to add pretty transitions between slides.
* [`slideshow-text-style`](https://docs.racket-lang.org/slideshow-text-style/index.html): Small library that helps with formatting text in a slideshow
* [Staged Slides]([https://docs.racket-lang.org/slideshow-text-style/index.html](https://docs.racket-lang.org/staged-slide/index.html)): `staged-slide`Helpers for building staged slides in Slideshow
* [`lang-slide'](https://docs.racket-lang.org/lang-slide/index.html): A slide that shows all the languages used to build Racket.   `racket -l lang-slide`

##  Some `#lang slideshow` resources / examples

* [mflatt/talks](https://github.com/mflatt/talks/)
* https://github.com/samth/polyconf-2015
* [Robby Findler's ICFP 2014 Keynote](https://github.com/rfindler/icfp-2014-contracts-talk/)
* https://github.com/lexi-lambda/talks/blob/master/2020-06-effects/main.rkt

### [packages tagged slideshow](https://pkgd.racket-lang.org/pkgn/search?tags=slideshow)


### Live code in Slideshow:

https://github.com/mflatt/talks/tree/master/mredtalk3

### Including live video in slides

https://github.com/videolang/website/blob/master/pub/icfp2017/slidesrc/slides.rkt


### [Asumu Takikawa's slideshow tutorial](https://www.asumu.xyz/blog/2018/03/31/making-the-most-of-lang-slideshow/)


### Animated slideshow example

```racket
#lang slideshow

(require slideshow/code
         slideshow/play
         plot)

(play-n (lambda (n1 n2 n3)
          (vl-append (cellophane (t "Hello") (* n1 (- 1.0 n2)))
                     (rectangle (* 10 n1) (* 10 n1))
                     (arrow (* 30 n2) 0)
                     (circle (* 10 n3)))))

(slide (plot-pict (function sqr -1 1 #:label "y = x^2")))
```
