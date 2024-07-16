# Experiment-1

## Exercises

### Exercise-1

```matlab
%% Experiment - 1 | Exercise - 1
clc;
clear;

%% (a)
V1 = [1 3 sqrt(5)]
V2 = [7 5]
V3 = [3 4 5]

V4 = 3 * V1

V5 = 2 * V1 - 3 * V3

% V6 = V1 + V2
% This gives an error.
% Matrix dimensions must agree.


%% (b)
V7 = [2*V3 -V1]


%% (c)
row = 1:7
row(1:2:end)


%% (d)
col = row'
% OR
% col = transpose(row)


%% (e)
m = 0.5
c = -2
x = [0 1.5 3 4 5 7 9 10]
y = m*x + c


%% (f)
t = 1:10


%% (g)
x = t .* sin(t)
y = (t-1)./(t+1)
z = (sin(t.^2) ./ t.^2)
```

### Exercise-2-1

```matlab
%% Experiment - 1 | Exercise - 2
clc;
clear;

c = [1.1 -3.2 3.4 0.6; 0.6 1.2 -0.6 3.1; 1.3 0.6 5.5 0]

%% (a)
c(2, :)


%% (b)
c(:, end)


%% (c)
c(1:2, 2:end)


%% (d)
c(6)


%% (e)
c(4:end)


%% (f)
c(1:2, 2:4)


%% (g)
temp = c(3,1);
c(3, 1) = c(1, 1);
c(1, 1) = temp;
c


%% (h)
c(:, 2) = []


%% (i)
c(2, 2) = 0
```

### Exercise-2-2

```matlab
%% Experiment - 1 | Exercise - 2
clc;
clear;

a = [1 0; 2 1]
b = [-1 2; 0 1]
c = [3 2]
d = 5


%% (a)
size(a)
size(b)
size(c)
size(d)


%% (b)
a+b


%% (c)
a+c


%% (d)
a.*b


%% (e)
a*b


%% (f)
% a*c
% Error.
% Error using  *
% Incorrect dimensions for matrix multiplication. Check that the number of columns in the
% first matrix matches the number of rows in the second matrix. To perform elementwise
% multiplication, use '.*'.


%% (g)
a+d


%% (h)
a.*d


%% (i)
a*d


%% (j)
a./b


%% (k)
a./a


%% (l)
a.^2
```

### Exercise-2-3

```matlab
%% Experiment - 1 | Exercise - 2
clc;
clear;

D = zeros(2, 3)
E = 5 * eye(3)
F = 3 * ones(2)
```

### Exercise-2-4

```matlab
%% Experiment - 1 | Exercise - 2
clc;
clear;

c = [5 -1 3; 9 20 -6; 25 15 5]

%% (a)
C3 = mod(c,3)


%% (b)
L = logical(C3)


%% (c)
c(L == 0)'


%% (d)
c(mod(c, 5) == 0)'
```
