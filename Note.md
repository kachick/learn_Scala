Scala
=====

emacs
-----

~/.emacs.d/scala-mode

    https://github.com/scala/scala-dist/tree/master/tool-support/src/emacs

~/.emacs.d/init.el

    (add-to-list 'load-path "~/.emacs.d/scala-mode")
    (require 'scala-mode-auto)
    (add-to-list 'auto-mode-alist '("\\.scala$" . scala-mode))
    

func
----

    def func(x: Type, y: Type): [Type] = {
          if (x) else y
        }


void
----

    Unit

REPL
----

scala であがり、 :quit で抜けられる。
irbよりghciっぽい感じ
一行（評価?）毎に resN みたいな名前が付けられて表示され、その後利用出来る。

OneLiner
-------

    scala -e 'code'

Compile
--------

    scalac foo.scala
    scalac -encoding ENCODING foo.scala

Run
---

    scala SCRIPT
    scala COMPILED

---------------------------------------------------

Scala vs Ruby
-------------

## ARGV

    ARGV[0]

    args(0)

## Comment

### One Line

    # ~$
  
    // ~$

### Multi Line

    ==begin
    ==end

    /*
    */

## NameSpace

RubyでいうとこのKernelにあたるのがPredef
print系は実態がConsoleだけど、ここで定義されてるのでどこでもたたける
RubyだとObjectにある定数のStringやらは、java.lang.Stringへの別名としてPredefへ入っている