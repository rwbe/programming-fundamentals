# 🧩 Módulo 05 — Paradigmas de programação

> As diferentes formas de pensar e organizar código.

---

## 🎓 Objetivos de aprendizagem

- Entender o que são paradigmas de programação.
- Conhecer os principais: imperativo, funcional e orientado a objetos.
- Criar classes, objetos, atributos e métodos.
- Usar herança e encapsulamento básicos.

---

## 🗂️ O que é um paradigma?

Um paradigma é um **estilo de escrever e organizar código**. É como uma "filosofia" de programação.

| Paradigma | Ideia central |
|---|---|
| **Imperativo** | Descreve passo a passo *como* fazer |
| **Funcional** | Transforma dados com funções puras |
| **Orientado a Objetos (OOP)** | Modela o mundo em objetos com estado |

Python suporta os três — você pode misturar conforme a necessidade.

---

## 🏭 Orientação a Objetos (OOP)

OOP organiza código em **classes** — modelos que descrevem objetos com:
- **Atributos** — o que o objeto *tem* (dados/estado)
- **Métodos** — o que o objeto *faz* (comportamento)

### Criando uma classe

```python
class Pessoa:
    def __init__(self, nome, idade):
        self.nome = nome
        self.idade = idade

    def apresentar(self):
        return f"Olá, sou {self.nome} e tenho {self.idade} anos."

# Criando objetos
ana = Pessoa("Ana", 30)
carlos = Pessoa("Carlos", 25)

print(ana.apresentar())
# Olá, sou Ana e tenho 30 anos.

print(carlos.nome)  # Carlos
```

### `__init__` — o construtor

`__init__` é chamado automaticamente ao criar um objeto. Define os atributos iniciais.

---

## 🔒 Encapsulamento

Proteger dados internos usando convenções de nomenclatura.

```python
class ContaBancaria:
    def __init__(self, saldo):
        self._saldo = saldo  # convenção: protegido

    def depositar(self, valor):
        if valor > 0:
            self._saldo += valor

    def sacar(self, valor):
        if 0 < valor <= self._saldo:
            self._saldo -= valor
            return valor
        return 0

    def ver_saldo(self):
        return self._saldo

conta = ContaBancaria(1000)
conta.depositar(500)
conta.sacar(200)
print(conta.ver_saldo())  # 1300
```

---

## 🧬 Herança

Uma classe pode **herdar** atributos e métodos de outra.

```python
class Animal:
    def __init__(self, nome):
        self.nome = nome

    def falar(self):
        return "..."

class Cachorro(Animal):
    def falar(self):
        return "Au au!"

class Gato(Animal):
    def falar(self):
        return "Miau!"

dog = Cachorro("Rex")
cat = Gato("Mimi")

print(dog.falar())  # Au au!
print(cat.falar())  # Miau!
```

---

## 🔢 Programação Funcional

Foca em **funções puras** que transformam dados sem efeitos colaterais.

```python
# Funções puras
def dobrar(x): return x * 2
def eh_par(x): return x % 2 == 0

numeros = [1, 2, 3, 4, 5, 6]

# map — aplica função a cada elemento
dobrados = list(map(dobrar, numeros))
print(dobrados)  # [2, 4, 6, 8, 10, 12]

# filter — filtra elementos
pares = list(filter(eh_par, numeros))
print(pares)  # [2, 4, 6]

# List comprehension (mais pythônico)
pares = [n for n in numeros if n % 2 == 0]
```

---

## ✅ Checklist

- [ ] Criar uma classe com `__init__`, atributos e métodos
- [ ] Instanciar objetos e acessar seus atributos
- [ ] Criar uma classe filha que herda de uma classe pai
- [ ] Sobrescrever um método em uma subclasse
- [ ] Usar `map()` ou `filter()` com uma função

---

## 🚀 Próximo módulo

Com OOP em mãos, vamos aprender a **lidar com erros** para escrever código robusto.
