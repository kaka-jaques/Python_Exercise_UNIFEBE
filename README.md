# Python_Exercise_UNIFEBE

## Os códigos fornecidos estão na linguagem '.m'

---
### Questão 1 - 
Utilize o Matlab para plotar, separadamente e em uma única figura, as funções  u= ln(60x+1) e v=3 sen⁡(6x) ao longo do intervalo -1≤ x□(≤) 3.
Rotule adequadamente a plotagem e cada uma das curvas. As variáveis u e v representam velocidades em milhas por hora; a variável x representa distância em milhas.

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

### Questão 2 - 
Seja a função y = e-2x.sen(3x). Como seria seu gráfico no intervalo 0<=x<=2e(π/4)?.
Rotule os eixos x e y, titule o gráfico e insira linhas de grade.  


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

### Questão 3 - 
Plote o gráfico das seguintes funções, utilizando a comando _linspace_ para criar o intervalo especificado com, no mínimo 250 pontos.
 - a) y = 3x3 + 3x2 - 4x +10, x ϵ [-5;15]
 - b) y = 2e^(x/4),  x ϵ [-7;e(-2)]

Rotule os eixos x e y, titule o gráfico e insira linhas de grade.  


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

### Questão 4 - 
Elabore um algoritmo que solicite a entrada de um escalar, permita calcular os valores para a função, e imprima uma mensagem com o resultado dessa função
f(x) = {(2x^3  - 4x,se x<-2@x^2  + 3x,    se -2≤x≤4@cos(x^(2/(3 ))),se x>4)



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

---

# PARTE 2

### QUESTÃO 1 - 
Seja a função y = e-x.sen(x). Como seria seu gráfico no intervalo 0<=x<=e(π). Rotule os eixos x e y e titule o gráfico.  

```m
x = linspace(0, exp(pi), 1000);

y = exp(-x) .* sin(x);

plot(x, y, 'b', 'LineWidth', 2);
xlabel('x');
ylabel('y');
title('Gráfico da função y = e^{-x} \cdot sin(x)');
grid on;
```

---

### QUESTÃO 2 - 
Plote o gráfico das seguintes funções, no intervalo especificado:
- a)	y = x3 – 5x2 + 2x + 5, x ϵ [-20;20]
- b)	y = sen(x).cos(2x),  x ϵ [-2π;π]

Rotule os eixos x e y e titule o gráfico.  



```m
x_a = linspace(-20, 20, 1000);
y_a = x_a.^3 - 5*x_a.^2 + 2*x_a + 5;

figure;
plot(x_a, y_a, 'b', 'LineWidth', 2);
xlabel('x');
ylabel('y');
title('Gráfico da função y = x^3 - 5x^2 + 2x + 5');
grid on;

x_b = linspace(-2*pi, pi, 1000);
y_b = sin(x_b) .* cos(2*x_b);

figure;
plot(x_b, y_b, 'r', 'LineWidth', 2);
xlabel('x');
ylabel('y');
title('Gráfico da função y = sin(x) * cos(2x)');
grid on;

```

---

### QUESTÃO 3 - 
Utilize o Matlab para plotar, separadamente e em uma única figura, as funções  u= ln(60x+1) e v=3 sen⁡(6x) ao longo do intervalo -1≤ x□(≤) 3.
Rotule adequadamente a plotagem e cada uma das curvas. As variáveis u e v representam velocidades em milhas por hora; a variável x representa distância em milhas.


```m
x = linspace(-1, 3, 1000);

u = log(60*x + 1);
v = 3*sin(6*x);

figure;

subplot(2,1,1);
plot(x, u, 'b', 'LineWidth', 2);
xlabel('x (milhas)');
ylabel('u (milhas por hora)');
title('Velocidade u = ln(60x+1)');
grid on;

subplot(2,1,2);
plot(x, v, 'r', 'LineWidth', 2);
xlabel('x (milhas)');
ylabel('v (milhas por hora)');
title('Velocidade v = 3sen(6x)');
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

### QUESTÃO 4 - 
Elabore um algoritmo que solicite a entrada de um escalar, permita calcular os valores para a função, e imprima uma mensagem com o resultado dessa função
f(x) = {(2x -1,se x<-1@x^2  + 3x,    se -1≤x≤1@exp(x^(2/(3 ))),se x>1)



```m
x = input('Digite um valor para x: ');

if x < -1
    result = 2 * x - 1;
elseif -1 <= x && x <= 1
    result = x^2 + 3 * x;
else
    result = exp(x^(2/3));
end

fprintf('O valor de f(x) é: %.2f\n', result);
```