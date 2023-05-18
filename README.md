# Python_Exercise_UNIFEBE

## Os códigos fornecidos estão na linguagem '.m'

---
### Questão 1
```m
% Definindo o intervalo de x
x = -1:0.01:3;

% Calculando as funções u e v
u = log(60*x + 1);
v = 3*sin(6*x);

% Plotando as funções em uma única figura
figure;

% Plotando a função u
subplot(2,1,1);
plot(x, u, 'b', 'LineWidth', 2);
xlabel('x (milhas)');
ylabel('u (milhas por hora)');
title('Gráfico da função u = ln(60x+1)');
grid on;

% Plotando a função v
subplot(2,1,2);
plot(x, v, 'r', 'LineWidth', 2);
xlabel('x (milhas)');
ylabel('v (milhas por hora)');
title('Gráfico da função v = 3sen(6x)');
grid on;

% Ajustando o espaçamento entre os subplots
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