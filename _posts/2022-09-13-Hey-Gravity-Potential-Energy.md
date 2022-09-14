---
layout: post
title: "Hey Gravity Potential Energy"
date : 2022-09-13
tags:
  - Physics
toc: true
comments: true
category : Physics
author : Chanhaeng Lee
---



### Gravitational Energy[^1]

I'd like to understand gravitational force[^2] and its potential energy[^3].  In physics, **potential energy** is "the energy held by an object because of its position relative to other objects, stresses within itself, its electric charge, or other factors".  **work**[^4] is "the energy transferred to or from an object via the application of force along a displacement". Normally the work is the product of force and displacement.

To understand more, we often refer to an example of the gravitational energy. If we say that a ball has a $$mgh$$ potential energy by the gravity force, and if we lift the ball, then the ball has more potential energy because it has more height from the Earth. However, we need to study more about this. What if the ball is in the infinity distance from the Earth? then the potential energy is infinity?

In Newtonian mechanics, two or more masses always pull each other with a gravitational force. This gravitational energy is said to be always negative due to the conservation of energy, to make it zero when the objects are in the infinity distance. With the above example, we can think the $$mgh$$ potential energy will not be 0 if the ball keep getting far from the earth. The reason why it's like that is the $$mgh$$ equation is derived when the gravitational energy is assumed as 0 when an object is in the surface of the Earth. so, that's why there starts to be a point that makes me confused. 

Therefore, we can think of the $$mgh$$ equation as the simple one that makes us understand the idea of potential energy. We can do some math to understand the gravitational energy. By Newton's law of gravitation,


$$
F = \frac{GMm}{r^2}
$$




where $$G$$ is the gravitational constant, $$M$$ and $$m$$ are the mass of two objects, respectively, and $$r$$ is the distance between two objects. The work done by this force from infinity to the destination $$R$$ is


$$
W = \int^R_{\infty} \frac{GMm}{r^2} \; dr = - \frac{GMm}{r} \Bigg|^R_{\infty} = -\frac{GMm}{r}
$$


Since $$W = - \Delta U$$ and $$\Delta U = - W = \frac{GMm}{r}$$, where $$U$$ is potential energy and $$W$$ is work. so we can think that, if the gravitational force works on an object from $$x$$ to $$y$$, then its amount of change of potential energy is $$\Delta U =   - \int^y_x \frac{GMm}{r^2} = \frac{GMm}{y}  - \frac{GMm}{x}$$.

So let's clear our confusing points in this gravitational energy. I really love this answer[^5]. The gravitational potential energy equations are made relative to a frame of reference. This equation $$U = mgh$$ depends on the reference that if $$r$$ approaches to 0 (which means that an object is in the surface of the earth), its potential energy should be zero. The equation $$U = - \frac{GMm}{r}$$ depends on the reference that if $$r$$ approaches to 0 (which means that two objects are infinitely far apart ), its potential energy should be zero. Therefore, The first equation says that if the two (an object and the Earth) are far part, the potential energy should increase. The second equation says that if the two (an object and the other) are getting close, the potential energy should increase. You might be confused with the second equation, however you should be careful with the negative sign. If two objects are getting closer, the $$r$$ will be smaller, and finally the potential energy gets bigger because it's minus.

So, I think if there is no statement that you should calculate the gravitational potential energy relative to the Earth, then you can just use the $$U = - \frac{GMm}{r}$$ which depends on the assumption I told you above.



---

[^1]: Gravitational energy. (2022, September, 14). In Wikipedia. https://en.wikipedia.org/wiki/Gravitational_energy
[^2]: Newton's law of universal gravitation. (2022, September, 14). In Wikipedia. https://en.wikipedia.org/wiki/Newton%27s_law_of_universal_gravitation
[^3]: Potential energy. (2022. September, 14). In Wikipedia. https://en.wikipedia.org/wiki/Potential_energy
[^4]: Work (physics). (2022, September, 14). In Wikipedia. https://en.wikipedia.org/wiki/Work_(physics)
[^5]: Why is gravitational potential energy negative, and what does that mean? https://physics.stackexchange.com/questions/17082/why-is-gravitational-potential-energy-negative-and-what-does-that-mean