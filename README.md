expressão = input('Digite uma função f(x):')
x = float(input('Digite um valor para x :'))
h = float(input('Digite um valor para h :'))

def f(x):
    return eval(expressão)
 
def derivada_central(f,x,h):
    return (f(x + h) - f(x - h)) / (2*h)
     
r = derivada_central(f,x,h)
 
print('O resultado da aproximacao da derivada é {:.3f}'.format(r))
