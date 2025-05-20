# calculadoraEBAC
Este projeto apresenta uma calculadora simples desenvolvida em Python, projetada para rodar em sistemas Linux. Ela realiza operações básicas como adição, subtração, multiplicação e divisão. O código é leve, funcional e pode ser executado diretamente pelo terminal com o comando python3.

O objetivo é demonstrar a integração entre Python e o ambiente Linux, além de facilitar o uso de scripts para operações rápidas. A calculadora recebe dois números e a operação desejada, retornando o resultado no terminal.

Exemplo de uso no terminal:

$ python3 calculadora.py
Digite o primeiro número: 10
Digite a operação (+, -, *, /): *
Digite o segundo número: 5
Resultado: 50

Também pode ser integrada a um script .sh, facilitando sua execução com um simples clique ou comando:

#!/bin/bash
python3 calculadora.py
----------------------------------------------------------------------------------

1. calculadora.py (Código Python)

def calculadora():
    try:
        num1 = float(input("Digite o primeiro número: "))
        operacao = input("Digite a operação (+, -, *, /): ")
        num2 = float(input("Digite o segundo número: "))

        if operacao == '+':
            resultado = num1 + num2
        elif operacao == '-':
            resultado = num1 - num2
        elif operacao == '*':
            resultado = num1 * num2
        elif operacao == '/':
            if num2 != 0:
                resultado = num1 / num2
            else:
                print("Erro: divisão por zero.")
                return
        else:
            print("Operação inválida.")
            return

        print(f"Resultado: {resultado}")
    except ValueError:
        print("Erro: entrada inválida.")

if _name_ == "_main_":
    calculadora()


---

2. executar_calculadora.sh (Shell Script)

#!/bin/bash

# Executa a calculadora Python
python3 calculadora.py


---

Instruções para usar no Linux:

1. Salve os dois arquivos na mesma pasta.


2. Dê permissão de execução ao script .sh:



chmod +x executar_calculadora.sh

3. Execute a calculadora:



./executar_calculadora.sh
