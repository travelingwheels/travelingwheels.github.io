---
layout: post
title:      "Iteration vs looping"
date:       2019-09-18 00:01:20 -0400
permalink:  iteration_vs_looping
---

So here are a coulpe of questions I had about looping and iteration: what is the diiference, and why use one over the other. 

On the surface both loops and iterators are used to repeat a chunk of code. The subtle difference here is that iteration lets you abstract away certain details of code. For example:
```
# loop               vs.           iterator

i = 0                              5.times do
while i < 5                         
  puts "hello"                       puts "hello"
  i += 1
end                                end
```
Both lines of code do the same thing, but as you can see in this example iteration is cleaner. It is easier to write, read and understand.

Also there is the possibility of an infinite loop  if you fail to ensure that the termination condition (the one that must be true so the loop stops) really occurs. For example, trying to count from a number (that the user entered) to 100 in steps of 10
```
number = gets.chomp.to_i    
while number != 100
  puts number += 10
end
```
The problem here is if the user types in say 5 the program breaks. The fix is simple just change the loop condition to be number < 100 instead, but why risk it. An infinite loop would be impossible if we use an iterator instead:
```
(number..100).step(10).each {|n| puts n}
```
In my opinion (which I am an expert on) looping is a risk when writing code.  Thats not to say I don't use it, but whenever possible I try to iterate when refactoring my code.
