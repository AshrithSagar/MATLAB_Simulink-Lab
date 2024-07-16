# Experiment-3

## Examples

### Example-1

```matlab
%% Experiment - 3
% Example - 1
clc;
clear all;

v = [6, -41, 97, -97, 41, -6];
s = roots(v);
fprintf('The first root is: %f\n', s(1));
fprintf('The second root is: %f\n', s(2));
fprintf('The third root is: %f\n', s(3));
fprintf('The fourth root is: %f\n', s(4));
fprintf('The fifth root is: %f\n', s(5));

syms x;
X = transpose( solve(6*x^5 - 41*x^4 + 97*x^3 - 97*x^2 + 41*x - 6 == 0) )
```

### Example-2

```matlab
%% Experiment - 3
% Example - 2
clc;
clear all;

A = [1 1 1; 1 2 3; 1 4 9];
b = [3; 4; 6];
X = transpose( A \ b )
```

### Example-3

```matlab
%% Experiment - 3
% Example - 3
clc;
clear all;

p = [8 -7 12 -5 8 13 -12 9];
f_2 = polyval(p, 2)
roots_f = roots(p)
x = linspace(0, 20);
y = polyval(p, x);
plot(x, y)
```

### Example-4

```matlab
%% Experiment - 3
% Example - 4
clc;
clear all;

syms x;
f = (x^2 + 4) / (x - 4);
L = limit(f, x, 2)
```

### Example-5

```matlab
%% Experiment - 3
% Example - 5
clc;
clear all;

syms x;
f = (x + 2) * (x^2 + 3);
diff_f = diff(f)
```

### Example-6

```matlab
%% Experiment - 3
% Example - 6
clc;
clear all;

syms x;
f = x^3 - 2*x + 5;
Area = int(f, 1, 2);
fprintf('Area under the curve (%s) is %f\n', f, Area)
```

## Exercises

### Exercise-1

```matlab
%% Experiment - 3
% Exercise - 1
clc;
clear all;

syms x;
X = linspace(0, 20);

p1 = [3 -10 7 9];
roots_roots_p1 = roots(p1)
f1 = 3*x^3 - 10*x^2 + 7*x + 9;
roots_solve_p1 = double( solve(f1) )
subplot(3, 1, 1)
Y = polyval(p1, X);
plot(X, Y)
title(string(f1))

p2 = [4 5 5 -2 3 -7];
roots_roots_p2 = roots(p2)
f2 = 4*x^5 + 5*x^4 + 5*x^3 - 2*x^2 + 3*x - 7;
roots_solve_p2 = double( solve(f2) )
subplot(3, 1, 2)
Y = polyval(p2, X);
plot(X, Y)
title(string(f2))

p3 = [7 0 0 0 4 0 0 0 -4];
roots_roots_p3 = roots(p3)
f3 = 7*x^8 + 4*x^4 - 4;
roots_solve_p3 = double( solve(f3) )
subplot(3, 1, 3)
Y = polyval(p3, X);
plot(X, Y)
title(string(f3))
```

### Exercise-2

```matlab
%% Experiment - 3
% Exercise - 2
clc;
clear all;

syms x1 x2 x3 x4

A1 = [3 -5 -7; 4 4 -8; 5 3 0];
b1 = [10; -3; 2];
MX1 = transpose( A1 \ b1 )
Eqns1 = [3*x1 - 5*x2 - 7*x3 == 10, 4*x1 + 4*x2 - 8*x3 == -3, 5*x1 + 3*x2 == 2];
S1 = solve(Eqns1);
SX1 = [ double(S1.x1), double(S1.x2), double(S1.x3) ]

A2 = [-6 -5; 5 0];
b2 = [4; 8];
MX2 = transpose( A2 \ b2 )
Eqns2 = [-6*x1 - 5*x2 == 4, 5*x1 == 8];
S2 = solve(Eqns2);
SX2 = [ double(S2.x1), double(S2.x2) ]

A3 = [-9 -5 9 8; -5 -2 0 -3; -8 -9 0 -8; -7 8 -3 6];
b3 = [-2; -5; -2; -8];
MX3 = transpose( A3 \ b3 )
Eqns3 = [-9*x1 - 5*x2 + 9*x3 + 8*x4 == -2; -5*x1 - 2*x2 - 3*x4 == -5; -8*x1 - 9*x2 - 8*x4 == -2; -7*x1 + 8*x2 - 3*x3 + 6*x4 == -8];
S3 = solve(Eqns3);
SX3 = [ double(S3.x1), double(S3.x2), double(S3.x3), double(S3.x4) ]
```

### Exercise-3

```matlab
%% Experiment - 3
% Exercise - 3
clc;
clear all;

syms x;
f = (3*x + 5) / (x - 3);
g = (x^2 + 1);

L_x_4 = limit(f, x, 4)
L_g_4 = limit(g, x, 4)
L_f_plus_g_4 = limit(f+g, x, 4)
L_f_minus_g_4 = limit(f-g, x, 4)
L_f_times_g_4 = limit(f*g, x, 4)
L_f_upon_g_4 = limit(f/g, x, 4)
```

### Exercise-4

```matlab
%% Experiment - 3
% Exercise - 4
clc;
clear all;

syms x h;

f1 = sin(x)
diff_f1 = diff(f1)
E1 = (subs(f1, x, x + h) - f1)/ h;
CLT_f1 = limit(E1, h, 0)

f2 = x^2 + 1
diff_f2 = diff(f2)
E2 = (subs(f2, x, x + h) - f2)/ h;
CLT_f2 = limit(E2, h, 0)

f3 = log(2*x - 1) - log(2*x + 1) + 2*atan(2*x)
diff_f3 = diff(f3)
E3 = (subs(f3, x, x + h) - f3)/ h;
CLT_f3 = limit(E3, h, 0)
```

### Exercise-5

```matlab
%% Experiment - 3
% Exercise - 5
clc;
clear all;

syms x;

p = [3 -10 7 9];
f1 = 3*x^3 - 10*x^2 + 7*x + 9
Area_f1 = double( int(f1, 1, 2))
subplot(3, 1, 1);
fplot(f1, [1 2])
title(string(f1));

p = [4 5 5 -2 3 -7];
f2 = 4*x^5 + 5*x^4 + 5*x^3 - 2*x^2 + 3*x - 7
Area_f2 = double( int(f2, 1, 2))
subplot(3, 1, 2);
fplot(f2, [1 2])
title(string(f2));

p = [3 -10 7 9];
f3 = 7*x^8 + 4*x^4 - 4
Area_f3 = double( int(f3, 1, 2) )
subplot(3, 1, 3);
fplot(f3, [1 2])
title(string(f3));
```
