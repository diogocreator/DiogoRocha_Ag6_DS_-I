# DiogoRocha_Ag6_DS_-I
Agenda 06 - Desenvolvimento de Sistemas I » Apresentação » Fichário
# 🛒 Sistema de Desconto Progressivo - Mercado Online

Este projeto consiste em um programa desenvolvido em Python para calcular o desconto progressivo de compras em uma Mercado online, aplicando regras baseadas no valor total informado pelo cliente.

---

## 📌 Regras de Negócio

O sistema aplica as seguintes taxas de desconto com base no valor total da compra:

| Valor da Compra | Desconto Aplicado |
| :--- | :---: |
| Abaixo de R$ 200,00 | **5%** |
| De R$ 200,00 a R$ 299,99 | **10%** |
| A partir de R$ 300,00 | **15%** |

---

## 💻 Código do Programa (`main.py`)

```python
# =========================================================
# Programa: Sistema de Desconto Progressivo
# Descrição: Calcula o valor do desconto e o valor final a
#            ser pago com base no valor total da compra.
# =========================================================

def calcular_desconto():
    # 1. Entrada de dados
    # Solicita ao usuário o valor total da compra e converte para decimal
    valor_compra = float(input("Digite o valor total da compra (R$): ").replace(',', '.'))
    
    # 2. Estrutura de Decisão (Regras de Desconto Progressivo)
    if valor_compra < 200.00:
        percentual_desconto = 0.05
    elif valor_compra < 300.00:
        percentual_desconto = 0.10
    else:
        percentual_desconto = 0.15

    # 3. Processamento / Cálculos
    valor_desconto = valor_compra * percentual_desconto
    valor_final = valor_compra - valor_desconto

    # 4. Saída de dados
    print("\n--- RESUMO DA COMPRA ---")
    print(f"Valor original: R$ {valor_compra:.2f}")
    print(f"Desconto aplicado ({int(percentual_desconto * 100)}%): R$ {valor_desconto:.2f}")
    print(f"Valor total a pagar: R$ {valor_final:.2f}")

# Execução do programa
if __name__ == "__main__":
    calcular_desconto()
   # =========================================================
# Programa: Sistema de Desconto Progressivo
# Descrição: Calcula o valor do desconto e o valor final a
#            ser pago com base no valor total da compra.
# =========================================================


def calcular_desconto():
    # 1. Entrada de dados
    # Solicita ao usuário o valor total da compra e converte para número decimal (float)
    valor_compra = float(
        input("Digite o valor total da compra (R$): ").replace(",", ".")
    )

    # 2. Estrutura de Decisão (Regras de Desconto Progressivo)
    # Se menor que R$ 200,00 -> 5% de desconto
    if valor_compra < 200.00:
        percentual_desconto = 0.05
    # Se entre R$ 200,00 e R$ 299,99 -> 10% de desconto
    elif valor_compra < 300.00:
        percentual_desconto = 0.10
    # Se maior ou igual a R$ 300,00 -> 15% de desconto
    else:
        percentual_desconto = 0.15

    # 3. Processamento / Cálculos
    valor_desconto = valor_compra * percentual_desconto
    valor_final = valor_compra - valor_desconto

    # 4. Saída de dados
    # Exibe os resultados formatados com duas casas decimais
    print("\n--- RESUMO DA COMPRA ---")
    print(f"Valor original: R$ {valor_compra:.2f}")
    print(
        f"Desconto aplicado ({int(percentual_desconto * 100)}%): R$ {valor_desconto:.2f}"
    )
    print(f"Valor total a pagar: R$ {valor_final:.2f}")
