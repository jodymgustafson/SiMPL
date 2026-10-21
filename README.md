# SiMPL
Simple Mathematical Programming Language

Supports
- all math operators
- err(msg?) function to report errors
- common math functions and constants
- custom functions
- variables
- loops
- control logic
- arrays (matrix)
- nil
Examples
- 1+2 * 3 # => 7
- (1+2) * 3 # => 9
- piOver2=pi/2
- matrixA=[ [1, 2, 3], [4, 5, 6] ]
- arrayA=1..3 # => [1, 2, 3]
- add(x,y)= x + y
- avg(array)= r=0, for(i in array, r=r+i), r / length(array)
- sqr(x)= x * x
- c2f(c)= c * 9 / 5 + 32
- abs(x)= x < 0 ? -x : x
- assert(ex,msg)= ex ? 1 : err(msg)
- fact(x)= assert(x > 0, "must be positive"), x == 1 ? 1 : x * fact(x-1)
- fact(x)= x <= 0 ? err("must be positive") : x == 1 ? 1 : x * fact(x-1)
- pow(b,e)= e == 0 ? 1 : b * pow(b, e-1)
- pow(b,e)= e == 0 ? 1 : r=1, for(1..e, r = r * b) # compact syntax
- pow(b,e)= e == 0 ? 1 : r=1, for(i=1, i<e, i=i+1, r = r * b) # full syntax
- pow(b,e)= e == 0 ? 1 : r=1, while(e>1, (e = e - 1, r = r * b))

Define variable syntax
- name=expression
Define function syntax
- name(param,* )=expression
Delete variable/function
- name=nil
If syntax
- conditional_expr ? then_expr {: else_expr}?
Loop syntax
- for({name in}? array, expression)
- for(init_expr, conditional_expr, incr_expr, expression)
- while(conditional_expr, expression)
Array/Matrix
- [ expression,* ]
- start..end

