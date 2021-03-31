# TechNumber
Introduce tech number definitions and properties


## Definition
A tech number is defined after the process below:

1. write down any number of even digits, say 2025
1. equally divide it into two halves; in this case 20 and 25
1. add them into a number (20 + 25 = 45)
1. square the result (45<sup>2</sup> = 2025)
1. if the result is just the original number, this is a tech number 

_2025 is a tech number_. There are many others like: 81, 2035, 9801, etc

## Properties
Tech number judgement is a good programming practice. Furthermore, there are something noticible. 

Do this in base 2 system:

1. write down any number of even digits, say 1001<sub>2</sub>(=9<sub>10</sub>)
1. equally divide it into two halves; in this case 10<sub>2</sub> and 1<sub>2</sub>
1. add them into a number: 10<sub>2</sub> + 1<sub>2</sub> = 11<sub>2</sub>
1. square the result: (11<sub>2</sub> )<sup>2</sup> = 1001<sub>2</sub>

thus _9 is a tech number of base 2_.

In general, whether a (natrual) number a tech number depends on base system. Let d be a base number, and consider a number as

> x = (d<sup>n</sup> - 2)d<sup>n</sup> + 1

this number is of (2n-2) digit and can be devided into two (n-1)-digit numbers. One can readily recognized this as
 > x = [(d<sup>n</sup> - 2) + 1]<sup>2</sup>
 
Choose (d<sup>n</sup> - 2), shift by n digits (time by d<sup>n</sup>), and plus 1. This is a formula for some tech numbers of base d. QED.

Try verifying these tech numbers:

110001<sub>2</sub> = 49

776001<sub>8</sub> = 261,121

998,001

ffe001<sub>16</sub> = 16,769,025

## Generalization

Let number (a+b) less than d<sup>n</sup> and let y less than d<sup>2n</sup>

>y = (a+b)<sup>2</sup> = (αd<sup>n</sup> + β)<sup>2</sup>

,where α, β < d<sup>n</sup>. To assert 

>y = (a+b-β<sup>2</sup>)d<sup>n</sup> + β<sup>2</sup>

is quilvalent to solve
> _a+b = α<sup>2</sup>d<sup>n</sup>+(2αβ+β<sup>2</sup>)_

The simplist chose is a+b = d<sup>n</sup>-1, and (α, β) = (1, -1)

,which gives the base-trivial tech number formula above. 

In general, the solutions depends on what base, d, is used. Tech number is overall defined unber base system.

## [Demostration](http://tpcg.io/tEjMtLoT)

An online tech number verifier, coded with Java.

input in STDIN block takes format 
> base number anything else

Choose base system and then type number string.
