# 📦 Módulo 02 — Variáveis e tipos de dados

> Como o computador armazena e classifica informações.

---

## 🎓 Objetivos de aprendizagem

Ao final deste módulo você será capaz de:

- Declarar variáveis e atribuir valores a elas.
- Identificar os tipos de dados mais comuns.
- Entender como Python infere tipos automaticamente.
- Converter dados entre tipos diferentes.
- Evitar erros comuns ao trabalhar com tipos.

---

## 🧩 O que é uma variável?

Uma variável é um **nome que aponta para um valor** armazenado na memória.

```python
nome = "Ana"
idade = 25
altura = 1.68
ativo = True
```

Pense em uma variável como uma caixa com um rótulo. O rótulo é o nome (`nome`, `idade`), e o conteúdo é o valor (`"Ana"`, `25`).

---

## 📋 Tipos de dados fundamentais

### `str` — Texto (string)

```python
nome = "Fundamentos de Programação"
linguagem = 'Python'
mensagem = """Pode usar
múltiplas linhas."""
```

### `int` — Número inteiro

```python
ano = 2024
quantidade = 10
temperatura = -5
```

### `float` — Número decimal

```python
preco = 49.90
pi = 3.14159
taxa = 0.07
```

### `bool` — Verdadeiro ou falso

```python
logado = True
admin = False
```

### `None` — Ausência de valor

```python
resultado = None  # ainda não definido
```

---

## 🔍 Como verificar o tipo

```python
x = 42
print(type(x))   # <class 'int'>

y = "olá"
print(type(y))   # <class 'str'>
```

---

## 🔄 Conversão de tipos

```python
# str → int
numero = int("10")     # 10

# int → str
texto = str(42)        # "42"

# str → float
preco = float("9.99")  # 9.99

# int → bool
ativo = bool(1)        # True
vazio = bool(0)        # False
```

---

## 🧮 Operações básicas

```python
a = 10
b = 3

print(a + b)   # 13  (adição)
print(a - b)   # 7   (subtração)
print(a * b)   # 30  (multiplicação)
print(a / b)   # 3.33 (divisão)
print(a // b)  # 3   (divisão inteira)
print(a % b)   # 1   (resto)
print(a ** b)  # 1000 (potência)
```

### Strings

```python
nome = "Ana"
sobrenome = "Silva"

completo = nome + " " + sobrenome  # "Ana Silva"
repetido = "ha" * 3                # "hahaha"
tamanho = len(completo)            # 9
maiusculo = completo.upper()       # "ANA SILVA"
```

---

## ⚠️ Erros comuns

```python
# ❌ Não misture tipos sem converter
resultado = "Tenho " + 25 + " anos"
# TypeError: can only concatenate str (not "int") to str

# ✅ Correto
resultado = "Tenho " + str(25) + " anos"

# ✅ Ou use f-string (mais moderno)
idade = 25
resultado = f"Tenho {idade} anos"
```

---

## 💡 F-strings (forma moderna)

```python
nome = "Carlos"
nota = 9.5

print(f"Olá, {nome}! Sua nota foi {nota}.")
# Olá, Carlos! Sua nota foi 9.5.

print(f"Nota formatada: {nota:.1f}")
# Nota formatada: 9.5
```

---

## ✅ Checklist

Antes de avançar, confirme que você consegue:

- [ ] Criar variáveis de diferentes tipos
- [ ] Usar `type()` para verificar o tipo de um valor
- [ ] Converter entre `int`, `float`, `str` e `bool`
- [ ] Criar f-strings com variáveis embutidas
- [ ] Realizar operações matemáticas básicas

---

## 🚀 Próximo módulo

Com variáveis em mãos, vamos aprender a **tomar decisões e repetir ações** com controle de fluxo.
