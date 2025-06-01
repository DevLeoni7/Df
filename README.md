def raiz_newton(c, n, p, max_iter=10000):
    # Verificar se o número é negativo ou zero
    if n < 0:
        return "Essa raiz não existe. Número negativo."
    if n == 0:
        return 0  # A raiz quadrada de zero é zero

    iter_count = 0

    # Loop do método de Newton-Raphson
    while iter_count < max_iter:
        nc = 0.5 * (c + n / c)  # Fórmula de Newton
        erro = abs(nc - c)  # Cálculo do erro

        # Se o erro for menor que a precisão desejada, retorna o resultado
        if erro < p:
            return nc

        c = nc
        iter_count += 1

    return c  # Retorna o resultado após o número máximo de iterações

# Entrar com o valor para calcular a raiz
n = float(input('Digite um número o qual você gostaria de saber a raiz: '))
c = 1  # Valor inicial da aproximação
p = 0.00000001  # Precisão desejada

r = raiz_newton(c, n, p, max_iter=1000)

# Exibir o resultado
print("O resultado dessa raiz é: {}".format(r))
