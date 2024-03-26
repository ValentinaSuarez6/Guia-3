# Guia-3
GUIA #3 SIMULACIÓN COMPUTACIONAL

CÓDIGO 1: 

A = randi([0, 10], 4, 4);
B = randi([0, 10], 4, 4);

suma = A + B;
resta = A - B;
mulmatrices = A * B;
multermino = A .* B;
inversaA = A \ B;
inversaB = A / B;
cuadradoA = A ^ 2;
divisionA_B = A./ B;
divisionB_A = B./ A;
elevadoB = A .^ B;


x = linspace(0, 10, 1000);
y1 = exp(x)./(100 + 100*sin(x));
y2 = x.^3 - 10*x.^2 + 5*x + 20;

figure
plot(x, y1, 'r', 'LineWidth', 2)
hold on
plot(x, y2, 'b', 'LineWidth', 2)
title('Gráficas de f(x) y g(x)')
xlabel('x')
ylabel('y')
legend('f(x)', 'g(x)')
grid on
line([0, 10], [0, 0], 'Color', 'k', 'LineStyle', '--')
hold off


CÓDIGO 2

x = linspace(-10, 10, 40);

funcion1 = @(x) abs(x);
funcion2 = @(x) sqrt(x);
funcion3 = @(x) cos(x);
funcion4 = @(x) exp(x);
funcion5 = @(x) log10(x);






figure;

subplot(5,1,1);
plot(x, funcion1(x), 'b-', 'LineWidth', 2);
title('Función |x|');
xlabel('x');
ylabel('y');
grid on;

subplot(5,1,2);
plot(x, funcion2(x), 'r-', 'LineWidth', 2);
title('Función √x');
xlabel('x');
ylabel('y');
grid on;

% Gráfica de la función cos(x)
subplot(5,1,3);
plot(x, funcion3(x), 'g-', 'LineWidth', 2);
title('Función cos(x)');
xlabel('x');
ylabel('y');
grid on;

subplot(5,1,4);
plot(x, funcion4(x), 'm-', 'LineWidth', 2);
title('Función ex');
xlabel('x');
ylabel('y');
grid on;

subplot(5,1,5);
plot(x, funcion5(x), 'c-', 'LineWidth', 2);
title('Función log10(x)');
xlabel('x');
ylabel('y');
grid on;











CÓDIGO 3 

function [A, maximos_fila, promedios_columna, num_elementos, A_ordenada, elemento_xy] = generar_matriz(n, x, y)
      A = magic(n);
        disp('Matriz A:');
    disp(A);
    
      maximos_fila = max(A, [], 2);
    
        promedios_columna = mean(A);
    
        num_elementos = numel(A);
    
      A_ordenada = sort(A);
    
        elemento_xy = A(x, y);
end

