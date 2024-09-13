# ChatBoot
ChatBoot em Python 


# Meu Projeto

Descrição do meu projeto.

## Como Usar

Aqui está um exemplo de código para começar:

```python
import requests

def obter_dados(url):
    resposta = requests.get(url)
    dados = resposta.json()
    return dados

url = "https://api.example.com/dados"
dados = obter_dados(url)
print(dados)
