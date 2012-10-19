---
layout: post
title: "Knowing Rails Doesn't Mean You Know Ruby: Part 1 | attr_accessor"
date: 2012-10-18 20:48
comments: true
categories: 
published: false
---

The [Ruby](http://en.wikipedia.org/wiki/Ruby_(programming_language)) community was a small one for nearly a decade after its creation in 1995 by [Yukihiro "Matz" Matsumoto](http://en.wikipedia.org/wiki/Yukihiro_Matsumoto), until the the [Ruby on Rails](http://en.wikipedia.org/wiki/Ruby_on_Rails) framework was created in 2004 by [David Heinemeier Hansson](http://en.wikipedia.org/wiki/David_Heinemeier_Hansson). Rails' increasing reputation as the go-to option for rapid prototyping and deployment among fast moving and agile startups, dev shops and internal teams are larger companies has led to exponential growth in both the Ruby and Rails communities.

For better or worse, many people have come to Ruby by way of Rails. It is not uncommon for people new to Rails, especially those that are new to programming in general, to have little or no experience with Ruby as a standalone programming language. While initially these individuals will make encouraging and tangible progress, it quickly plateau's, not only in terms of their ability to build within the Rails framework, but also in terms of their ability to interact with and learn from more experienced programmers. These are things I've experienced in my own efforts to become a competent and productive programmer, and have witnessed in the journeys of many others on similar paths. This series of posts will attempt to share some of the lessons I've learned that may be helpful to others in a similar position.

Without further ado I introduce to you **attr_accessor**, a *setter* and *getter* method for classes in Ruby.