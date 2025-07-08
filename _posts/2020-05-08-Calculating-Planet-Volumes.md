---
layout: post
title: Calculating Planet Volumes
image: "/posts/planetary-system.jpg"
tags: [Numpy, PlannetVolumes]
---

In this post I'm going to calculate the volumes of all the planets in our solar systems based on their radius measurements in NumPy. We are going to find out not only for 8 planets but to do it for 1 Million planets to see how numpy apply mathematical operations to our array object.

If you're not sure what a the radius measurements for each of the eight planets in our solar system. Here it is a detailed breakdown: Mercury (2,439.7 km), Venus (6,051.8 km), Earth (6,371 km), Mars (3,389.5 km), Jupiter (69,911 km), Saturn (58,232 km), Uranus (25,362 km), and Neptune (24,622 km).

Let's get into it!

---

First let's start by creating an array that we need and let us call it radii. It is going to be one dimentional array that contains the radius measurements for each of the eight planets in our solar system.

```ruby
radii = np.array([2439.7, 6051.8, 6371, 3389.7, 69911, 58232, 25362, 24622])
```

In general, to find a area of the sphere is 4/3 * np.pi * r**3

Let's say r = 10 and create an object called volume

```ruby
r = 10
volume = 4/3 * np.pi * r**3
print(volume)
>>>4188.790204786391
```

Pretty Cool!

Now we're going to calculate the volumes of all planets.

We're going to again create an object called volumes and change radii object instead of r.

```ruby
volumes = 4/3 * np.pi * radii**3
print(volumes)
>>>[6.08272087e+10 9.28415346e+11 1.08320692e+12 1.63144486e+11
 1.43128181e+15 8.27129915e+14 6.83343557e+13 6.25257040e+13]
```
Amazing!

The next thing to do would be to put it into a array of random numbers, which you can see below:

```ruby
radii = np.random.randint(1, 1000, 1000000)
volumes = 4/3 * np.pi * radii**3
print(volumes)
>>>[6.08272087e+10 9.28415346e+11 1.08320692e+12 1.63144486e+11
 1.43128181e+15 8.27129915e+14 6.83343557e+13 6.25257040e+13]
[6.74349917e+08 2.72989474e+09 6.02674020e+08 ... 2.80328149e+08
 5.42460479e+06 4.10384912e+08]
```

Its so fast when we ran this piece of code

That is pretty cool!

I hoped you enjoyed learning about to calculate volumes of all planets, and one way to search for them using Numpy.

---

###### The reason why its so fast method because a single NumPy array can only contain a single data type whereas say a list or a tuple could contain many different datatypes, and this restriction to only contain a single datatype has a huge benefit NumPy has enormous computation speed than a python for loop do.


...where we firstly force the identification of the lowest number in the number_range into our prime variable, and following that we remove it.

However, because we have to sort the list for each iteration of the loop in order to get the minimum value, it's slightly slower than what we saw with pop()!


