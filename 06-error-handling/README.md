# 🛡️ Módulo 06 — Tratamento de Erros

> Como lidar com falhas de forma elegante e escrever código robusto.

---

## 🎓 Objetivos de aprendizagem

- Entender a diferença entre erros de sintaxe e exceções.
- Usar `try`, `except`, `else` e `finally`.
- Capturar tipos específicos de exceção.
- Lançar exceções com `raise`.
- Criar exceções personalizadas.

---

## 🚨 Tipos de erro

### Erro de sintaxe

Impede o código de rodar. Detectado antes da execução.

```python
# ❌ Faltou o dois-pontos
if True
    print("ops")
# SyntaxError: expected ':'
```

### Exceção (runtime error)

Ocorre durante a execução.

```python
print(10 / 0)
# ZeroDivisionError: division by zero

int("abc")
# ValueError: invalid literal for int() with base 10: 'abc'

lista = [1, 2, 3]
print(lista[10])
# IndexError: list index out of range
```

---

## 🛡️ `try / except`

```python
try:
    resultado = 10 / 0
except ZeroDivisionError:
    print("Não é possível dividir por zero.")
```

### Capturar múltiplos tipos

```python
def converter(texto):
    try:
        return int(texto)
    except ValueError:
        print(f"'{texto}' não é um número válido.")
        return None
    except TypeError:
        print("Tipo de dado inválido.")
        return None

print(converter("42"))    # 42
print(converter("abc"))   # 'abc' não é um número válido.
```

---

## 📋 `else` e `finally`

```python
def ler_arquivo(caminho):
    try:
        arquivo = open(caminho, 'r')
    except FileNotFoundError:
        print(f"Arquivo '{caminho}' não encontrado.")
    else:
        # Só executa se não houve exceção
        conteudo = arquivo.read()
        arquivo.close()
        print(conteudo)
    finally:
        # SEMPRE executa, com ou sem erro
        print("Operação concluída.")
```

---

## 🚀 Lançando exceções com `raise`

```python
def sacar(saldo, valor):
    if valor <= 0:
        raise ValueError("O valor de saque deve ser positivo.")
    if valor > saldo:
        raise ValueError(f"Saldo insuficiente. Saldo atual: R$ {saldo:.2f}")
    return saldo - valor

try:
    novo_saldo = sacar(100, 200)
except ValueError as e:
    print(f"Erro: {e}")
# Erro: Saldo insuficiente. Saldo atual: R$ 100.00
```

---

## 🏗️ Exceções personalizadas

```python
class SaldoInsuficienteError(Exception):
    def __init__(self, saldo, valor):
        self.saldo = saldo
        self.valor = valor
        super().__init__(f"Saldo R${saldo:.2f} insuficiente para sacar R${valor:.2f}")

def sacar(saldo, valor):
    if valor > saldo:
        raise SaldoInsuficienteError(saldo, valor)
    return saldo - valor

try:
    sacar(50.0, 100.0)
except SaldoInsuficienteError as e:
    print(e)
```

---

## 📌 Exceções comuns em Python

| Exceção | Quando ocorre |
|---|---|
| `ValueError` | Valor inválido para uma operação |
| `TypeError` | Tipo de dado errado |
| `KeyError` | Chave não existe em dicionário |
| `IndexError` | Índice fora do range da lista |
| `FileNotFoundError` | Arquivo não encontrado |
| `ZeroDivisionError` | Divisão por zero |
| `AttributeError` | Atributo/método não existe |
| `ImportError` | Módulo não encontrado |

---

## ✅ Checklist

- [ ] Usar `try/except` para capturar uma exceção
- [ ] Capturar tipos específicos de exceção
- [ ] Usar `finally` para garantir limpeza de recursos
- [ ] Lançar uma exceção com `raise` e uma mensagem clara
- [ ] Criar uma exceção personalizada

---

## 🚀 Próximo módulo

Com código robusto, vamos aprender a **organizar projetos com módulos e pacotes**.
