---
layout: post
title: Floating Point Number
date: 2022-12-20
description : summary for floating point number
tags : CS
category: CS
---



# Floating Point Number

Floating Point Number is represented in a computer according to [IEEE 754](https://en.wikipedia.org/wiki/IEEE_754).

According to the wikipedia, the format is specified by:

* base (or *radix*) $$b$$, which is either 2 (binary) or 10 (decimal) in IEEE 754;
* a precision $$p$$;
* an exponent range from $$emin$$ to $$emax$$, with $$emin = 1 - emax$$ for all IEEE 754 formats.

The format can describe the next values

* Finite numbers
  * finite numbers are described by three integers
  * $$s$$ : a sign (zero or one)
  * $$c$$ : a significant (or coefficient) having no more than $$p$$ digits when written in base $$b$$. (i.e., an integer in the range through 0 to $$b^p - 1$$)
  * $$q$$ : an exponent such that $$emin \le q + p - 1 \le emax$$.
  * The numerical value of such a finite number is $$(-1)^s \times c \times b^q$$
  * There are two zero values, called *signed zeros*: the sign bit specifies whether a zero is +0 (positive zero) or -0 (negative zero).
* Two infinities: $$+\infty$$ and $$-\infty$$.
* Two kinds of NaN (not-a-number): a quiet NaN (qNaN) and a signaling NaN (sNaN).



The next illustration shows the layout for 32-bit floating point:

![32-bit-floating-point-layout](https://upload.wikimedia.org/wikipedia/commons/thumb/d/d2/Float_example.svg/885px-Float_example.svg.png)