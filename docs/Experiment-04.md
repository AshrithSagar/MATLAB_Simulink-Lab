# Experiment-4

## Examples

### Example-1

```matlab
%% Experiment - 4
% Example - 1
clc;
clear all;

A = [1 2 3; 5 6 7; 9 10 11; 13 14 15]
rank_A = rank(A)
```

### Example-2

```matlab
%% Experiment - 4
% Example - 2
clc;
clear all;

A = [1 2 3; 5 6 7; 9 10 11; 13 14 15]
rref_A = rref(A)
```

### Example-3

```matlab
%% Experiment - 4
% Example - 3
clc;
clear all;

A = [2 -3 -1; 1/2 1 -1; 0 1 -1]
[L U P] = lu(A)
```

### Example-4

```matlab
%% Experiment - 4
% Example - 4
clc;
clear all;

A = [1 2 3; 4 5 6; 7 8 0]
p = poly(A)
```

### Example-5

```matlab
%% Experiment - 4
% Example - 5
clc;
clear all;

A = [1 8 -10; -4 2 4; -5 2 8]
[V D] = eig(A);
disp('The eigen values are: ')
disp(diag(D))
disp('The corresponding eigen vectors are: ')
disp(V)
```

## Exercises

### Exercise-1

```matlab
%% Experiment - 4
% Exercise - 1
clc;
clear all;

A = [3 1 1; 1 0 2; 1 2 0]
rank_A = rank(A)
rref_A = rref(A)
[L_A U_A] = lu(A)

B = [-3 -9 0; 3 9 -1; 6 6 -1]
rank_B = rank(B)
rref_B = rref(B)
[L_B U_B] = lu(B)

C = [-3 1 -6; 9 3 -4; 8 2 -1]
rank_C = rank(C)
rref_C = rref(C)
[L_C U_C] = lu(C)
```

### Exercise-2

```matlab
%% Experiment - 4
% Exercise - 2
clc;
clear all;

A = [3 1 1; 1 0 2; 1 2 0]
[V_A D_A] = eig(A);
disp('The eigen values of A are: ')
disp(diag(D_A))
disp('The corresponding eigen vectors of A are: ')
disp(V_A)

B = [-3 -9 0; 3 9 -1; 6 6 -1]
[V_B D_B] = eig(B);
disp('The eigen values of B are: ')
disp(diag(D_B))
disp('The corresponding eigen vectors of B are: ')
disp(V_B)

C = [-3 1 -6; 9 3 -4; 8 2 -1]
[V_C D_C] = eig(C);
disp('The eigen values of C are: ')
disp(diag(D_C))
disp('The corresponding eigen vectors of C are: ')
disp(V_C)
```

### Exercise-3

```matlab
%% Experiment - 4
% Exercise - 3
clc;
clear all;

A = [-1 0 3 -3; 10 -6 4 10; 1 0 -2 -10]
[U_A, S_A, V_A] = svd(A)

B = [8 -5 5 ; 9 -3 -8; 6 4 3; -8 -8 0]
[U_B, S_B, V_B] = svd(B)
```
