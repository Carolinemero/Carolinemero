import math

class Triangulo:
    def _init_(self, base: float = 0.0, altura: float = 0.0):
        self.base = base
        self.altura = altura

    def _str_(self):
        return f'Triangulo [base={self.base}, altura={self.altura}]'

    def calcular_area(self):
        return (self.base * self.altura) / 2

    def calcular_perimetro(self):
        hipotenusa = math.sqrt(self.base * 2 + self.altura * 2)
        return self.base + self.altura + hipotenusa

if _name_ == '_main_':
    t = Triangulo(base=4, altura=3)
    print(t)
    print(f'El área del Triangulo es: {t.calcular_area()}')
    print(f'El perímetro del Triangulo es: {t.calcular_perimetro()}')
