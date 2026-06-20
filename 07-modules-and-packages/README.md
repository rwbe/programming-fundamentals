# 📚 Módulo 07 — Módulos e Pacotes

> Como organizar código em arquivos e usar bibliotecas externas.

---

## 🎓 Objetivos de aprendizagem

- Importar módulos da biblioteca padrão do Python.
- Criar seus próprios módulos.
- Instalar e usar pacotes externos com `pip`.
- Entender a estrutura de um pacote Python.
- Usar ambientes virtuais.

---

## 📦 O que é um módulo?

Um módulo é simplesmente um **arquivo `.py`** que você pode importar em outros arquivos.

```python
# math_utils.py
def somar(a, b):
    return a + b

def multiplicar(a, b):
    return a * b

PI = 3.14159
```

```python
# main.py
import math_utils

resultado = math_utils.somar(3, 4)
print(resultado)   # 7
print(math_utils.PI)  # 3.14159
```

---

## 📥 Formas de importar

```python
# Importar o módulo inteiro
import math
print(math.sqrt(16))  # 4.0

# Importar funções específicas
from math import sqrt, pi
print(sqrt(25))  # 5.0
print(pi)        # 3.14159...

# Alias (apelido)
import numpy as np    # convenção da comunidade
import pandas as pd   # convenção da comunidade

# ⚠️ Evite importar tudo
from math import *    # poluição do namespace
```

---

## 📚 Biblioteca padrão (sem instalar nada)

Python já vem com muitas ferramentas prontas:

```python
# os — sistema operacional
import os
print(os.getcwd())          # diretório atual
os.makedirs("nova_pasta", exist_ok=True)

# datetime — datas e horas
from datetime import datetime, date
hoje = date.today()
agora = datetime.now()
print(f"Hoje: {hoje}")
print(f"Agora: {agora:%H:%M:%S}")

# random — números aleatórios
import random
n = random.randint(1, 10)
escolha = random.choice(["a", "b", "c"])

# json — trabalhar com JSON
import json
dados = {"nome": "Ana", "idade": 30}
texto = json.dumps(dados, ensure_ascii=False)
volta = json.loads(texto)
```

---

## 🌐 Instalar pacotes externos com `pip`

```bash
# Instalar um pacote
pip install requests

# Instalar versão específica
pip install requests==2.31.0

# Ver pacotes instalados
pip list

# Salvar dependências
pip freeze > requirements.txt

# Instalar a partir do arquivo
pip install -r requirements.txt
```

### Pacotes populares

| Pacote | Para quê serve |
|---|---|
| `requests` | Fazer requisições HTTP |
| `pandas` | Análise de dados |
| `numpy` | Computação numérica |
| `flask` / `fastapi` | Criar APIs web |
| `sqlalchemy` | Banco de dados |
| `pytest` | Testes automatizados |
| `pillow` | Manipulação de imagens |

---

## 🏗️ Estrutura de um projeto Python

```
meu_projeto/
├── main.py              # ponto de entrada
├── requirements.txt     # dependências
├── README.md            # documentação
└── src/
    ├── __init__.py      # marca como pacote
    ├── utils.py         # funções utilitárias
    └── models.py        # modelos de dados
```

---

## 🧪 Ambiente virtual (venv)

Isola as dependências de cada projeto.

```bash
# Criar ambiente virtual
python -m venv .venv

# Ativar (Linux/Mac)
source .venv/bin/activate

# Ativar (Windows)
.venv\Scripts\activate

# Desativar
deactivate
```

---

## ✅ Checklist

- [ ] Criar um arquivo `.py` e importá-lo em outro
- [ ] Usar pelo menos 3 módulos da biblioteca padrão
- [ ] Instalar um pacote com `pip`
- [ ] Criar um `requirements.txt`
- [ ] Criar e ativar um ambiente virtual

---

## 🚀 Próximo módulo

Com projetos organizados, vamos aprender a **escrever testes** para garantir que o código funciona.
