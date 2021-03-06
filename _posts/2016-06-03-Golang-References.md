---
layout: post
title: Golang References
categories: [language]
tags: [go, golang, references]
description: the collection of Golang relate articles.
---

## 1. Language

### Pointer

* [Pointing to Go — The Go Pointer Type](https://medium.com/learning-the-go-porgramming-language/pointing-to-go-the-go-pointer-type-a3c3f587592f#.nf9uff9ol)

### Concurrency

* ['Concurrency' Chapter in Book 'Go Bootcamp'](http://www.golangbootcamp.com/book/concurrency)
* [Concurrency is not parallelism](https://blog.golang.org/concurrency-is-not-parallelism)

#### Goroutines

* ['Goroutines' in Book 'Go Bootcamp'](http://www.golangbootcamp.com/book/concurrency#sec-goroutines)
* [How to Wait for All Goroutines to Finish Executing Before Continuing](http://nathanleclaire.com/blog/2014/02/15/how-to-wait-for-all-goroutines-to-finish-executing-before-continuing/)

#### Channels

* ['Channels' in Book 'Go Bootcamp'](http://www.golangbootcamp.com/book/concurrency#sec-channels)
* [Channels Are Not Enough](https://gist.github.com/kachayev/21e7fe149bc5ae0bd878)
* [Davc.C: Curious Channels](http://dave.cheney.net/2013/04/30/curious-channels)

#### Go Concurrency Patterns

* [Rob.P: Go Concurrency Patterns - Slides](https://talks.golang.org/2012/concurrency.slide#1)
* [Go Concurrency Patterns: Pipelines and cancellation](http://blog.golang.org/pipelines)
* [Go Concurrency Patterns: Context](http://blog.golang.org/context)
* [Go Concurrency Patterns: Timing out, moving on](http://blog.golang.org/go-concurrency-patterns-timing-out-and)
* [Advanced Go Concurrency Patterns](http://talks.golang.org/2013/advconc.slide#1)
* [Concurrent error handling](http://blog.schaeffer.io/2015/01/10/errors-and-concurrency/)

### Error Handling

* [Dave.C: Don’t just check errors, handle them gracefully](http://dave.cheney.net/2016/04/27/dont-just-check-errors-handle-them-gracefully)

## 2. Practices

### General

* 2016
  * [Go best practices, six years in](https://peter.bourgon.org/go-best-practices-2016/)
  * [Programming Patterns in Go](https://www.infoq.com/news/2016/03/go-patterns)

### Tips & Gotchas

* [SliceTricks](https://github.com/golang/go/wiki/SliceTricks)
* 2015
  * [50 Shades of Go: Traps, Gotchas, and Common Mistakes for New Golang Devs](http://devs.cloudimmunity.com/gotchas-and-common-mistakes-in-go-golang/)
  * [Reduce allocation in Go code](https://methane.github.io/2015/02/reduce-allocation-in-go-code/)
  * [3 Go Gotchas - range, append, variable shadowing](http://bryce.is/writing/code/jekyll/update/2015/11/01/3-go-gotchas.html?utm_source=golangweekly&utm_medium=email)

### Design Pattern

* [Singleton Pattern in Go](http://marcio.io/2015/07/singleton-pattern-in-go/)
* MapReduce
  * [Cheap MapReduce in Go](http://marcio.io/2015/07/cheap-mapreduce-in-go/)
* [Nil Channels Always Block](http://www.godesignpatterns.com/2014/05/nil-channels-always-block.html)
* [Effective Go](https://golang.org/doc/effective_go.html)

### Misc

* [Calculating Multiple File Hashes in a Single Pass](http://marcio.io/2015/07/calculating-multiple-file-hashes-in-a-single-pass/)

## 3. Tools

### Dependency Management

I prefer standard [vendoring](https://docs.google.com/document/d/1Bz5-UB7g2uPBdOx-rw5t9MxJwkfpx90cqG9AFL0JAYo/edit) for 
dependencies management, which was offically released since Go 1.6.

The main reason is the IDEs like Intellij Go Plugin and Microsoft vscode-go Plugin have better nature support 
for the standard vendoring structure.

Previously, I used to use [gb](https://getgb.io) a lot which is a **project based** build tool for golang, one drawback of gb 
is it does [not support go-gettable](https://github.com/constabulary/gb/issues/284), the other is MS vscode-go does not support it well.

### Build

* Cross Platform Compiling
  * [Dave.C: Cross compilation just got a whole lot better in Go 1.5](http://dave.cheney.net/2015/03/03/cross-compilation-just-got-a-whole-lot-better-in-go-1-5)
* [Golang Auto Build Versioning](http://www.atatus.com/blog/golang-auto-build-versioning/)

## 4. Reference sites

* Libs
  * [Awesome Go](http://awesome-go.com)
  * [List of Go Projects](https://github.com/golang/go/wiki/Projects)
* Api Docs
  * [Go Walker](https://gowalker.org)
    Go Walker is a server that generates Go projects API documentation on the fly for the projects on GitHub.
* News
  * [Go Newsletter](http://golangweekly.com)

## 5. Books

* https://github.com/dariubs/GoBooks
