# 🔀 Módulo 03 — Controle de fluxo

> Como fazer o código tomar decisões e repetir ações.

---

## 🎓 Objetivos de aprendizagem

- Usar `if`, `elif` e `else` para tomar decisões.
- Repetir blocos de código com `for` e `while`.
- Controlar loops com `break`, `continue` e `pass`.
- Escrever condições compostas com `and`, `or` e `not`.

---

## 🤔 Condicionais — `if / elif / else`

O código executa diferentes caminhos dependendo de uma condição.

```python
temperatura = 32

if temperatura > 30:
    print("Está quente! 🌞")
elif temperatura > 20:
    print("Temperatura agradável. 😊")
else:
    print("Está frio! 🧥")
```

**Saída:** `Está quente! 🌞`

### Condições compostas

```python
dia = "sábado"
chovendo = False

if dia in ("sábado", "domingo") and not chovendo:
    print("Dia perfeito para sair!")
else:
    print("Fica em casa.")
```

---

## 🔁 Loop `for` — repetição com sequência

Use quando você sabe **quantas vezes** quer repetir, ou quando quer percorrer uma coleção.

```python
frutas = ["maçã", "banana", "laranja"]

for fruta in frutas:
    print(f"Eu gosto de {fruta}")
```

### `range()` — gerar sequências numéricas

```python
for i in range(5):
    print(i)          # 0, 1, 2, 3, 4

for i in range(1, 6):
    print(i)          # 1, 2, 3, 4, 5

for i in range(0, 10, 2):
    print(i)          # 0, 2, 4, 6, 8
```

### `enumerate()` — índice + valor

```python
linguagens = ["Python", "JavaScript", "Go"]

for idx, lang in enumerate(linguagens, start=1):
    print(f"{idx}. {lang}")
# 1. Python
# 2. JavaScript
# 3. Go
```

---

## 🔄 Loop `while` — repetição com condição

Use quando você não sabe exatamente quantas vezes vai repetir.

```python
contador = 0

while contador < 5:
    print(f"Contador: {contador}")
    contador += 1
```

---

## 🛑 `break`, `continue` e `pass`

```python
# break — encerra o loop
for n in range(10):
    if n == 5:
        break
    print(n)   # 0 1 2 3 4

# continue — pula para a próxima iteração
for n in range(5):
    if n == 2:
        continue
    print(n)   # 0 1 3 4

# pass — não faz nada (placeholder)
for n in range(3):
    pass       # bloco vazio sem erro
```

---

## 🐍 List Comprehension (Pythônico)

Uma forma elegante de criar listas a partir de loops.

```python
# Forma tradicional
quadrados = []
for n in range(1, 6):
    quadrados.append(n ** 2)

# List comprehension
quadrados = [n ** 2 for n in range(1, 6)]
print(quadrados)  # [1, 4, 9, 16, 25]

# Com filtro
pares = [n for n in range(10) if n % 2 == 0]
print(pares)  # [0, 2, 4, 6, 8]
```

---

## ⚠️ Cuidado: loop infinito

```python
# ❌ Isso nunca termina!
while True:
    print("Socorro")

# ✅ Sempre garanta uma condição de saída
tentativas = 0
while tentativas < 3:
    tentativas += 1
    print(f"Tentativa {tentativas}")
```

---

## ✅ Checklist

- [ ] Escrever condicionais com `if`, `elif` e `else`
- [ ] Usar `and`, `or`, `not` em condições
- [ ] Percorrer listas com `for`
- [ ] Usar `range()` e `enumerate()`
- [ ] Criar loops `while` com condição de parada
- [ ] Usar `break` e `continue`
- [ ] Escrever uma list comprehension simples

---

## 🚀 Próximo módulo

Agora que o código sabe tomar decisões, vamos aprender a **organizar ações em funções**.
