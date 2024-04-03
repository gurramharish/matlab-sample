# matlab-sample

# 1st question
% Define the objective function
fun = @(x) x(1)^2 + x(2)^2;

% Define the constraints
A = [1, 1];
b = 1;

% Define the initial guess
x0 = [0, 0];

% Solve the optimization problem
options = optimoptions('fmincon', 'Display', 'iter');
[x, fval] = fmincon(fun, x0, A, b, [], [], [], [], [], options);

% Display the results
disp('Optimization Results:');
disp(['x = ', num2str(x)]);
disp(['fval = ', num2str(fval)]);


## 3rd question answer
% Define the coefficients
a = $a_value$;
b = $b_value$;
c = $c_value$;

% Calculate the discriminant
discriminant = b^2 - 4*a*c;

% Check the nature of roots
if discriminant > 0
    disp('The equation has two distinct real roots.');
elseif discriminant == 0
    disp('The equation has one real root (double root).');
else
    disp('The equation has two complex conjugate roots.');
end

% Calculate the roots
if discriminant >= 0
    root1 = (-b + sqrt(discriminant)) / (2*a);
    root2 = (-b - sqrt(discriminant)) / (2*a);
    disp(['Root 1 = ', num2str(root1)]);
    disp(['Root 2 = ', num2str(root2)]);
end