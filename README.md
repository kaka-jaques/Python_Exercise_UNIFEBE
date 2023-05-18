# Python_Exercise_UNIFEBE

## Os códigos fornecidos estão na linguagem '.m'

---
### Questão 1
```m
x = -1:0.01:3;

u = log(60*x + 1);
v = 3*sin(6*x);

figure;

subplot(2,1,1);
plot(x, u, 'b', 'LineWidth', 2);
xlabel('x (milhas)');
ylabel('u (milhas por hora)');
title('Gráfico da função u = ln(60x+1)');
grid on;

subplot(2,1,2);
plot(x, v, 'r', 'LineWidth', 2);
xlabel('x (milhas)');
ylabel('v (milhas por hora)');
title('Gráfico da função v = 3sen(6x)');
grid on;

spacing = 0.05;
set(gcf, 'Position', get(0, 'Screensize'));
set(gcf, 'Units', 'Normalized');
set(gcf, 'OuterPosition', [0 0 1 1]);
pos1 = get(gca, 'Position');
pos2 = [pos1(1), pos1(2) + pos1(4) + spacing, pos1(3), pos1(4)];
set(gca, 'Position', pos1);
set(gca, 'Units', 'Normalized');
set(gca, 'OuterPosition', pos2);
```

---

### Questão 2

```m
x = 0:0.01:2*pi/4;

y = exp(-2*x) .* sin(3*x);

plot(x, y, 'b', 'LineWidth', 2);
xlabel('x');
ylabel('y');
title('Gráfico da função y = e^{-2x} \cdot sin(3x)');
grid on;
```

---

### Questão 3

```m
x1 = linspace(-5, 15, 250);
y1 = 3*x1.^3 + 3*x1.^2 - 4*x1 + 10;

figure;
plot(x1, y1, 'b', 'LineWidth', 2);
xlabel('x');
ylabel('y');
title('Gráfico da função y = 3x^3 + 3x^2 - 4x + 10');
grid on;

x2 = linspace(-7, exp(-2), 250);
y2 = 2*exp(x2/4);

figure;
plot(x2, y2, 'r', 'LineWidth', 2);
xlabel('x');
ylabel('y');
title('Gráfico da função y = 2e^{(x/4)}');
grid on;
```

---

### Questão 4

```m
x = input('Digite um valor para x: ');

if x < -2
    result = 2 * x^3 - 4 * x;
elseif -2 <= x && x <= 4
    result = x^2 + 3 * x;
else
    result = cos(x^(2/3));
end

fprintf('O valor de f(x) é: %.2f\n', result);
```
