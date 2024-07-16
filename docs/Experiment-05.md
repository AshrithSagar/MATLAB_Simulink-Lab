# Experiment-5

## Examples

### Example-1

```matlab
%% Experiment - 5
% Example - 1
clc;
clear all;

x = 0:5;
y = [0 10 30 35 37 42];
x_intp = 0 : 0.001 : 5;
y_intp = interp1(x, y, x_intp, 'linear');
plot(x, y, 'd');
hold on;
plot(x_intp, y_intp, '.');
title('y versus x', 'FontSize', 18);
xlabel('x', 'FontSize', 14);
ylabel('y', 'FontSize', 14);
legend('Data points', 'Linear interpolation')
hold off;
```

### Example-2

```matlab
%% Experiment - 5
% Example - 2
clc;
clear all;

x = 0:5;
y = [0 10 30 35 37 42];
x_linfit = 0 : 0.001 : 5;
y_linfit = polyval(polyfit(x, y, 1), x_linfit);
plot(x, y, 's');
hold on;
plot(x_linfit, y_linfit, '.');
axis([0 5 0 60]);
grid;
title('First degree (Linear) fit', 'FontSize', 16);
xlabel('x', 'FontSize', 14);
ylabel('y', 'FontSize', 14);
legend('Data points', 'Linear fit')
hold off;
```

## Exercises

### Exercise-1-1

```matlab
%% Experiment - 5
% Exercise - 1
clc;
clear all;

x = [0 1 2 3 4 5 10];
y = [0 10 25 36 50 60 90];
plot(x, y, 's');
title('Interpolation', 'FontSize', 16);
xlabel('x', 'FontSize', 14);
ylabel('y', 'FontSize', 14);
hold on;
x_intp = 0 : 0.001 : 10;

y_lin = interp1(x, y, x_intp, 'linear');
plot(x_intp, y_lin, '.');
y_cub = interp1(x, y, x_intp, 'cubic');
plot(x_intp, y_cub, 'o');
y_spl = interp1(x, y, x_intp, 'spline');
plot(x_intp, y_spl, '--');

legend('Data points', 'Linear', 'Cubic', 'Spline')
hold off;
```

### Exercise-1-2

```matlab
%% Experiment - 5
% Exercise - 1
clc;
clear all;

x = [0 1 2 3 4 5 10];
y = [0 10 25 36 50 60 90];
x_intp = 0 : 0.001 : 10;

plot(x, y, 's'); hold on;
title('Linear interpolation', 'FontSize', 16);
xlabel('x', 'FontSize', 14);
ylabel('y', 'FontSize', 14);
y_lin = interp1(x, y, x_intp, 'linear');
plot(x_intp, y_lin, '.'); hold off;
legend('Data points', 'Linear');

figure;
plot(x, y, 's'); hold on;
title('Cubic interpolation', 'FontSize', 16);
xlabel('x', 'FontSize', 14);
ylabel('y', 'FontSize', 14);
y_cub = interp1(x, y, x_intp, 'cubic');
plot(x_intp, y_cub, '.'); hold off;
legend('Data points', 'Cubic');

figure;
plot(x, y, 's'); hold on;
title('Spline interpolation', 'FontSize', 16);
xlabel('x', 'FontSize', 14);
ylabel('y', 'FontSize', 14);
y_spl = interp1(x, y, x_intp, 'spline');
plot(x_intp, y_spl, '.'); hold off;
legend('Data points', 'Spline');
```

### Exercise-2

```matlab
%% Experiment - 5
% Exercise - 2
clc;
clear all;

x = [0 1 2 3 4 5 10];
y = [0 10 25 36 50 60 90];
plot(x, y, 's');
xlabel('x', 'FontSize', 14);
ylabel('y', 'FontSize', 14);
title('Polynomial regression', 'FontSize', 16);
hold on;
x_fit = 0 : 0.001 : 10;

y_1 = polyval(polyfit(x, y, 1), x_fit);
plot(x_fit, y_1, '.');
y_2 = polyval(polyfit(x, y, 2), x_fit);
plot(x_fit, y_2, '.');
y_3 = polyval(polyfit(x, y, 3), x_fit);
plot(x_fit, y_3, '.');
y_5 = polyval(polyfit(x, y, 5), x_fit);
plot(x_fit, y_5, '.');
y_7 = polyval(polyfit(x, y, 7), x_fit);
plot(x_fit, y_7, '.');

legend('Data points', 'Order 1', 'Order 2', 'Order 3', 'Order 5', 'Order 7')
hold off;
```
