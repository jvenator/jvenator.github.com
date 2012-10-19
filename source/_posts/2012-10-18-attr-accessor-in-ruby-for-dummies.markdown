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

Without further ado I introduce to you **attr_accessor**, a *setter* and *getter* method for classes in Ruby. First let's look at how you might generally see attr_accesor in the wild. Here I'm creating both a model and a controller for a *Dog* class, which will have several attributes such as *name*, *age* and *breed*. For simplicity I'm only including a *show* method in the controller and setting the @dog instance variable by searching for a specific dog record using it's id value.

{% codeblock Dog model - dog.rb %}
class Dogs
	attr_accessor :name, :age, :breed

end
{% endcodeblock %}

{% codeblock Dog controlloer - dogs_controller.rb %}
class DogsController < ApplicationController
	
	def show
		@dog = Dogs.find(params[:id])
	end

end
{% endcodeblock %}

As you'd expect, if I wanted to now make a call for this particular age or breed in a 'show' page, I might do something like this.

{% codeblock Dog show view - show.html.erb %}

<h1><%= @dog.name %></h1>
<p>Age: <%= @dog.age %></p>
<p>Breed: <%= @dog.breed %></p>

{% endcodeblock %}