# 🎯 Módulo 01 — Introdução à Programação

> Do zero absoluto ao seu primeiro código funcionando.

---

## 🎓 O que você vai aprender aqui

- O que é programar (de verdade, sem enrolação)
- Como o computador entende o que você escreve
- O que são linguagens de programação e por que existem tantas
- Como escolher por onde começar
- Como rodar seu primeiro código

---

## 💬 Então, o que é programar?

Programar é escrever instruções para o computador seguir.

Parece simples. E no fundo, é mesmo.

O computador não é inteligente — ele é incrivelmente obediente. Ele faz **exatamente** o que você mandar. Nem mais, nem menos. Seu trabalho como programador é aprender a dar ordens claras.

Pensa assim: quando você pede uma pizza, você faz um pedido específico. Se você fala só "pizza", a pessoa do outro lado não sabe o que fazer. Você precisa dizer o sabor, o tamanho, o endereço. Programar é a mesma coisa — você precisa ser específico.

---

## 🧩 O que é um programa?

Um programa é um conjunto de instruções que o computador executa, uma por uma, para fazer alguma coisa útil.

Quando você abre o WhatsApp, está rodando um programa. Quando você faz uma busca no Google, um programa processa seu texto e devolve resultados. Quando o GPS te dá uma rota, há um programa calculando o caminho.

Tudo que acontece no computador ou celular foi escrito por alguém.

---

## 🗣️ O que é uma linguagem de programação?

Computadores não entendem português, inglês ou japonês. Eles entendem apenas **bits** — zeros e uns. Mas escrever em zeros e uns seria impossível para humanos.

Aí entram as linguagens de programação: são uma forma de escrever instruções que tanto humanos conseguem ler quanto computadores conseguem executar.

Exemplos:

- **Python** — simples, versátil, ótimo pra começar
- **JavaScript** — a linguagem da web
- **Java** — muito usada em empresas
- **C++** — poderosa e rápida, usada em games e sistemas
- **Go, Rust, Ruby, Swift...** — cada uma com seu propósito

A boa notícia: os conceitos fundamentais são os mesmos em todas. Quem aprende bem uma, aprende a segunda muito mais rápido.

---

## 🔄 Como o computador executa o código?

Existem dois jeitos principais:

### Interpretado
O código é lido e executado linha por linha, na hora.

Python funciona assim. Você escreve, roda, vê o resultado. É ótimo para aprender porque o ciclo de feedback é instantâneo.

```python
print("Olá!")  # Python executa essa linha imediatamente
```

### Compilado
O código é transformado em um arquivo executável antes de rodar.

C e Go funcionam assim. Você escreve → compila (traduz para código de máquina) → executa. É mais rápido em produção, mas tem um passo a mais.

Para quem está começando, não precisa se preocupar muito com isso agora. Python é interpretado, então você vai escrever e já ver funcionando.

---

## 🐍 Por que Python para começar?

Python é a linguagem mais recomendada para iniciantes por algumas razões práticas:

**A sintaxe é limpa.** Ela parece quase inglês.

```python
nome = "Ana"
print("Olá, " + nome + "!")
```

**Você vê resultado rápido.** Sem configuração complicada, sem muitos arquivos. Escreveu, rodou.

**É usada pra tudo.** Web, automação, ciência de dados, inteligência artificial, scripts de produtividade. Aprender Python abre muitas portas.

**A comunidade é gigante.** Qualquer dúvida que você tiver, alguém já perguntou e respondeu no Stack Overflow.

---

## 🧪 Seu primeiro programa

Todo programador começa com o mesmo programa. É uma tradição.

```python
print("Olá, mundo!")
```

**O que acontece aqui:**
- `print` é uma função — ela manda o computador imprimir alguma coisa na tela
- O texto entre aspas é o que vai aparecer
- Os parênteses delimitam o que você está passando pra função

**Saída:**
```
Olá, mundo!
```

É simples, mas importante: você acabou de dar uma instrução ao computador e ele obedeceu. Esse é o começo de tudo.

---

## 🖥️ O que é um REPL?

REPL significa **Read → Eval → Print → Loop**.

É um ambiente onde você digita código e vê o resultado imediatamente, linha por linha. Como uma conversa com o computador.

No Python, você abre o REPL digitando `python` no terminal:

```
>>> 2 + 2
4
>>> print("oi")
oi
>>> nome = "Carlos"
>>> nome
'Carlos'
```

O REPL é perfeito para testar ideias, entender como algo funciona e experimentar sem medo de quebrar nada.

---

## 💡 Como escolher sua primeira linguagem

Se você ainda está em dúvida, aqui vai uma orientação direta:

| Se você quer... | Comece com |
|---|---|
| Aprender os fundamentos | Python |
| Criar sites | JavaScript |
| Desenvolver apps iOS | Swift |
| Desenvolver apps Android | Kotlin |
| Trabalhar com dados e IA | Python |
| Fazer games | C# (Unity) ou Python |
| Automação e scripts | Python |

**Para a maioria das pessoas que estão começando: Python.** Mas o mais importante não é a linguagem — é entender os conceitos. Depois que você domina variáveis, funções, loops e lógica, trocar de linguagem é muito mais fácil.

---

## ⚠️ Pegadinhas que todo iniciante cai

### Ficar trocando de linguagem
"Python é muito lento. Vou tentar JavaScript. Ah, mas ouvi que Go é melhor..."

Isso é armadilha. A linguagem é ferramenta. O que importa é aprender a pensar como programador, e isso você aprende com qualquer linguagem.

### Configurar mais do que programar
Gastar horas instalando plugins, temas, extensões antes de escrever uma linha. Comece simples. Você pode configurar depois.

### Copiar código sem entender
Copiar de tutorial é normal — todo mundo faz. Mas sempre leia o que copiou e tente explicar para si mesmo o que cada parte faz. Se não conseguir explicar, você não aprendeu ainda.

### Esperar entender tudo antes de praticar
Você não aprende a andar de bicicleta lendo sobre equilíbrio. Você cai algumas vezes e aprende fazendo. Com programação é igual.

---

## ✅ Checklist — antes de seguir

Confirme que você consegue:

- [ ] Explicar o que é um programa com suas próprias palavras
- [ ] Diferenciar linguagem interpretada de compilada
- [ ] Dizer por que Python é boa escolha para iniciantes
- [ ] Rodar um `print("Olá, mundo!")` no seu computador
- [ ] Abrir e usar um REPL do Python

---

## 📚 Para ir além

Se quiser aprofundar antes de continuar:

- [Automate the Boring Stuff with Python](https://automatetheboringstuff.com/) — gratuito online, em inglês
- [Pense em Python](https://pense-em-python.caravela.club/) — tradução gratuita em português
- [CS50 de Harvard](https://cs50.harvard.edu/x/) — o melhor curso introdutório de ciência da computação do mundo, gratuito

---

## 🚀 Próximo passo

Agora você entende o que é programação. No próximo módulo, vamos aprender como o computador **armazena informações** — variáveis e tipos de dados.
