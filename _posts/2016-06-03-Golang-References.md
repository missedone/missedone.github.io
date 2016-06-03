---
layout: post
title: Golang References
categories: [language]
tags: [go, golang, references]
description: the collection of Golang relate articles.
---

## Language

### [Concurrency](http://www.golangbootcamp.com/book/concurrency)

* [Concurrency is not parallelism](https://blog.golang.org/concurrency-is-not-parallelism)

### [Goroutines](http://www.golangbootcamp.com/book/concurrency#sec-goroutines)

* [How to Wait for All Goroutines to Finish Executing Before Continuing](http://nathanleclaire.com/blog/2014/02/15/how-to-wait-for-all-goroutines-to-finish-executing-before-continuing/)

### [Channels](http://www.golangbootcamp.com/book/concurrency#sec-channels)

#### [Go Concurrency Patterns](https://talks.golang.org/2012/concurrency.slide#1)

* [Go Concurrency Patterns: Pipelines and cancellation](http://blog.golang.org/pipelines)
* [Go Concurrency Patterns: Context](http://blog.golang.org/context)
* [Go Concurrency Patterns: Timing out, moving on](http://blog.golang.org/go-concurrency-patterns-timing-out-and)
* [Advanced Go Concurrency Patterns](http://talks.golang.org/2013/advconc.slide#1)
* [Concurrent error handling](http://blog.schaeffer.io/2015/01/10/errors-and-concurrency/)

### Error Handling

## Practices

* 2016
  * [Go best practices, six years in](https://peter.bourgon.org/go-best-practices-2016/)
  * [Programming Patterns in Go](https://www.infoq.com/news/2016/03/go-patterns)

## Tools

### Dependency Management

I prefer standard [vendoring](https://docs.google.com/document/d/1Bz5-UB7g2uPBdOx-rw5t9MxJwkfpx90cqG9AFL0JAYo/edit) for 
dependencies management, which is offically released since Go 1.6.

The main reason is the IDEs like Intellij Go Plugin and Microsoft Visual Studio Code Go Plugin have better nature support 
for the standard vendoring structure.

Previously I use [gb](https://getgb.io) a lot which is a **project based** build tool for golang, the only drawback of gb 
is it does [not support go-gettable](https://github.com/constabulary/gb/issues/284).

### Build

* Cross Platform Compiling
  * [Dave.C: Cross compilation just got a whole lot better in Go 1.5](http://dave.cheney.net/2015/03/03/cross-compilation-just-got-a-whole-lot-better-in-go-1-5)
* [Golang Auto Build Versioning](http://www.atatus.com/blog/golang-auto-build-versioning/)

## Reference sites

* Libs
  * [Awesome Go](http://awesome-go.com)
  * [List of Go Projects](https://github.com/golang/go/wiki/Projects)
* Api Docs
  * [Go Walker](https://gowalker.org)
    Go Walker is a server that generates Go projects API documentation on the fly for the projects on GitHub.
* [Go Language Patterns](http://www.golangpatterns.info/)

## Books

* https://github.com/dariubs/GoBooks
