# 🍔 Desafio 2 — Sistema de Pedidos da Lanchonete AI Burgers

> Projeto educacional do **Programa AI** · João Pessoa, PB

[![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=flat&logo=python&logoColor=white)](https://www.python.org/)
[![Programa AI](https://img.shields.io/badge/Programa-AI-ff9f1c?style=flat)](https://github.com/kelsonvictr)

---

## 📖 Sobre o Projeto

Este é o **Desafio 2** da trilha **Programa AI**, onde os alunos constroem um sistema interativo de pedidos para a fictícia *Lanchonete AI Burgers*. O objetivo é consolidar conceitos fundamentais de Python como **loops**, **condicionais**, **listas** e **funções com `return`**.

A página `index.html` serve como um guia interativo passo a passo — com código comentado, analogias e uma simulação animada do programa rodando no terminal.

---

## 🎯 Objetivo

Criar um programa em Python onde o cliente:

1. Visualiza o cardápio com preços
2. Escolhe itens repetidamente (usando `while`)
3. Finaliza o pedido digitando `0`
4. Recebe a conta com o total calculado (usando `for`)

---

## 🍔 Cardápio

| # | Item | Preço |
|---|------|-------|
| 1 | X-Burger | R$ 15 |
| 2 | X-Salada | R$ 18 |
| 3 | Batata Frita | R$ 10 |
| 4 | Refrigerante | R$ 7 |
| 0 | Finalizar Pedido | — |

---

## 🐍 Código Completo

```python
# 🍔 Sistema de Pedidos — Lanchonete AI Burgers
# Desafio 2 — Programa AI

def mostrar_menu():
    print("🍔 Bem-vindo à Lanchonete AI Burgers!")
    print("1 - X-Burger ........ R$15")
    print("2 - X-Salada ........ R$18")
    print("3 - Batata Frita .... R$10")
    print("4 - Refrigerante .... R$7")
    print("0 - Finalizar Pedido")

def preco_item(opcao):
    if opcao == 1:
        return 15
    elif opcao == 2:
        return 18
    elif opcao == 3:
        return 10
    elif opcao == 4:
        return 7
    else:
        return 0

pedidos = []

while True:
    mostrar_menu()
    opcao = int(input("Digite o número do item: "))

    if opcao == 0:
        break
    elif opcao == 1 or opcao == 2 or opcao == 3 or opcao == 4:
        pedidos.append(opcao)
        print("✅ Item adicionado!")
    else:
        print("⚠️ Opção inválida!")

total = 0
for p in pedidos:
    total += preco_item(p)

print(f"🧾 Total de {len(pedidos)} item(s) - Valor total: R${total}")
```

---

## 🧠 Conceitos Abordados

| Conceito | Como é usado |
|---|---|
| `def` / função | `mostrar_menu()` — imprime o cardápio |
| `return` | `preco_item(opcao)` — devolve o preço do item |
| Lista + `.append()` | `pedidos = []` — armazena os pedidos |
| `while True` / `break` | Loop principal que repete até o cliente finalizar |
| Loop `for` | Percorre `pedidos` somando os preços (padrão acumulador) |
| `if / elif / else` | Valida opção e decide o preço de cada item |

### 🆕 Novidades em relação ao Desafio 1

- Funções com **`return`** (que devolvem um valor, não apenas imprimem)
- Loop **`for`** para percorrer uma lista e acumular um total
- Menu com **4 opções** e **preços** associados

---

## 🚀 Como Executar

1. Salve o código acima como `lanchonete_ai.py`
2. Execute no terminal:

```bash
python lanchonete_ai.py
```

3. Siga as instruções na tela — escolha seus itens e digite `0` para ver a conta!

---

## 🌐 Guia Interativo

Abra o arquivo `index.html` no navegador para acessar o tutorial completo com:

- Explicações passo a passo de cada parte do código
- Animações e simulação do programa no terminal
- Analogias para facilitar o entendimento de `return` e `for`

---

## 🚀 Desafios Extras

Depois de concluir o desafio principal, tente:

- ✦ Mostrar o **nome de cada item** no resumo final (não só o número)
- ✦ Aplicar **10% de desconto** se o total passar de R$ 50
- ✦ Pedir o **nome do cliente** e incluir no recibo
- ✦ Limitar o pedido a no máximo **10 itens**

---

## 👩‍💻 Sobre o Programa AI

O **Programa AI** é uma iniciativa de ensino de programação com foco em Python e Inteligência Artificial, baseada em João Pessoa, PB.

---

*Feito com 🍔 para os alunos da Programa AI*
