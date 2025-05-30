def raiz_newton(c, n, p, max_iter=10000):
    iter_count = 0

    while iter_count < max_iter:
        nc = 0.5 * (c + n / c)
        erro = abs(nc - c)

        if n < 0:
            return print('Essa raiz não existe.')

        if n == 0:
            return print('Essa raiz não existe.')

        if erro < p:
            return nc

        c = nc
        iter_count += 1

    return c


n = float(input('Digite um número o qual você gostaria de saber a raiz: '))
c = 1
p = 0.00000001

r = raiz_newton(c, n, p, max_iter=1000)

print("O resultado dessa raiz é {}".format(r))
