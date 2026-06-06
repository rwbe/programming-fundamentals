# ⚙️ Módulo 04 — Funções e escopo

> Organizar código em blocos reutilizáveis e entender onde cada variável "vive".

---

## 🎓 Objetivos de aprendizagem

- Criar e chamar funções com `def`.
- Usar parâmetros, argumentos e valores padrão.
- Retornar valores com `return`.
- Entender o escopo de variáveis (local vs. global).
- Usar funções lambda para expressões simples.

---

## 📦 O que é uma função?

Uma função é um **bloco de código nomeado** que executa uma tarefa específica.

```python
def saudar():
    print("Olá, mundo!")

saudar()  # chama a função
# Olá, mundo!
```

### Por que usar funções?

- **Evita repetição** — escreva uma vez, use várias.
- **Facilita manutenção** — mudança em um lugar atualiza tudo.
- **Melhora a leitura** — nomes descritivos tornam o código legível.

---

## 🔧 Parâmetros e argumentos

```python
def saudar(nome):
    print(f"Olá, {nome}!")

saudar("Ana")     # Olá, Ana!
saudar("Carlos")  # Olá, Carlos!
```

### Valores padrão

```python
def saudar(nome, saudacao="Olá"):
    print(f"{saudacao}, {nome}!")

saudar("Ana")              # Olá, Ana!
saudar("Carlos", "Oi")     # Oi, Carlos!
```

### Múltiplos parâmetros

```python
def calcular_imc(peso, altura):
    imc = peso / (altura ** 2)
    return round(imc, 2)

resultado = calcular_imc(70, 1.75)
print(f"IMC: {resultado}")  # IMC: 22.86
```

---

## ↩️ `return` — retornar valores

```python
def somar(a, b):
    return a + b

total = somar(3, 4)
print(total)  # 7
```

### Múltiplos retornos

```python
def dividir(a, b):
    if b == 0:
        return None, "Divisão por zero"
    return a / b, None

resultado, erro = dividir(10, 2)
print(resultado)  # 5.0
```

---

## 🌍 Escopo de variáveis

**Escopo local** — variável criada dentro de uma função. Só existe ali.

```python
def minha_funcao():
    x = 10       # variável local
    print(x)

minha_funcao()
# print(x)  → NameError: name 'x' is not defined
```

**Escopo global** — variável criada fora de qualquer função.

```python
mensagem = "Olá!"  # variável global

def mostrar():
    print(mensagem)  # acessa a global

mostrar()  # Olá!
```

---

## ⚡ Lambda — função anônima de uma linha

```python
dobrar = lambda x: x * 2
print(dobrar(5))   # 10

# Útil com sorted(), map(), filter()
numeros = [3, 1, 4, 1, 5, 9]
ordenados = sorted(numeros)
print(ordenados)    # [1, 1, 3, 4, 5, 9]

palavras = ["banana", "maçã", "kiwi"]
por_tamanho = sorted(palavras, key=lambda p: len(p))
print(por_tamanho)  # ['kiwi', 'maçã', 'banana']
```

---

## 🔑 Keyword arguments

```python
def criar_perfil(nome, idade, cidade):
    return f"{nome}, {idade} anos, {cidade}"

# Posicional
print(criar_perfil("Ana", 30, "São Paulo"))

# Por nome (ordem não importa)
print(criar_perfil(cidade="Recife", nome="Carlos", idade=25))
```

---

## \*args e \*\*kwargs

```python
def somar_tudo(*numeros):
    return sum(numeros)

print(somar_tudo(1, 2, 3, 4, 5))  # 15

def mostrar_info(**dados):
    for chave, valor in dados.items():
        print(f"{chave}: {valor}")

mostrar_info(nome="Ana", idade=30, cidade="SP")
```

---

## ✅ Checklist

- [ ] Criar funções com `def` e chamá-las
- [ ] Usar parâmetros com e sem valores padrão
- [ ] Retornar valores com `return`
- [ ] Entender a diferença entre escopo local e global
- [ ] Criar uma função lambda simples
- [ ] Usar `*args` ou `**kwargs` em pelo menos um exemplo

---

## 🚀 Próximo módulo

Com funções dominadas, vamos explorar os **paradigmas de programação** — incluindo Orientação a Objetos.
