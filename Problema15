
function [Mcomp] = Problema15(k1,k2,d,W,h)

x = sqrt(2*W'*h/k1); % x es la máxima compresión de resorte si x < d

a = k1+2*k2;             % Coeficiente a cuadrática
b = -4*k2*d;             % Coeficiente b cuadrática
c = 2*k2*d^2-2*W'*h;     % Coeficiente c cuadrática

x1 = (-b + sqrt(b^2-4*a*c))/(2*a); % máxima compresión de resorte si x >= d
x2 = (-b - sqrt(b^2-4*a*c))/(2*a); % máxima compresión de resorte si x >= d
  
x3= max([x1 x2]);

if x<d
      Mcomp= x;
      fprintf ('La máxima compresión de resorte es: x = %s \n',num2str(Mcomp));
else
          Mcomp = x3;
          fprintf ('La máxima compresión de resorte es: x = %s \n',num2str(Mcomp));
end


                                           
figure(1)
plot(h,x)
title('Compresión máxima del resorte vs altura');
xlabel ('Altura (h)');
ylabel ('Máxima compresión de resorte (h)');
grid on



figure(2)
[X,Y] = meshgrid(h,x);
Z = peaks(X,Y);
meshc(Z)
title('Compresión máxima del resorte vs altura');
xlabel ('Eje x');
ylabel ('Eje y');
zlabel ('Eje z');
colormap winter;
grid on

%Problema15(10^4,1.5*10^4,0.1,100,0:1/7:2)

