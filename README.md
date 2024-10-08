# ChatBotAI


# Chatbot AI em Python: Criação de um Assistente Inteligente com Código Mínimo

Este projeto fornece uma solução avançada para a criação de chatbots em Python, minimizando a necessidade de codificação extensa. Nossa IA de chatbot é projetada para oferecer uma gama abrangente de funcionalidades que incluem:

Inteligência Artificial Avançada: Aproveite algoritmos sofisticados para entender e responder a uma ampla variedade de consultas dos usuários.

Manipulador de Conversas: Gerencie diálogos complexos com facilidade, mantendo a fluidez e a relevância das interações.

Integração Simples com APIs REST: Conecte seu chatbot a serviços externos e APIs com uma integração direta e intuitiva, ampliando suas capacidades sem esforço.

Chamadas de Funções Python: Execute funções Python diretamente a partir do chatbot, permitindo a realização de operações personalizadas e interativas.

Funcionalidades Avançadas:

Aprendizado: Adapte-se e evolua com base nas interações passadas para oferecer respostas cada vez mais precisas.
Memória: Armazene informações relevantes de conversas anteriores para melhorar a contextualização e a personalização.
Comutação Condicional: Alterne entre diferentes modos de operação e respostas com base em condições específicas ou contextos de conversa.
Tratamento Baseado em Tópicos: Direcione conversas para tópicos específicos e mantenha o diálogo relevante e focado.

# Exemplo de Imagens

<img src="https://github.com/Lucasbarbosa332/ChatBoot/blob/main/chat%20bot%20phyton/components/images/clothing.gif?raw=true" width="30%" alt="Clothing GIF">

<img src="https://github.com/Lucasbarbosa332/ChatBoot/blob/main/chat%20bot%20phyton/components/images/demo_gui.gif?raw=true" width="30%" alt="Demo GUI GIF">

<img src="https://raw.githubusercontent.com/Lucasbarbosa332/ChatBoot/8c0a9492254d54a9ab88ffe77edf02b16355e3cc/chat%20bot%20phyton/components/images/ChatBot%20AI.svg" width="30%" alt="ChatBot AI SVG">



## Instalação

Instale a partir do PyPI: pip install chatbotAI

pip install wikipedia-api chatbot

![--------------------------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)


## Aqui está um exemplo de como integrar a API de pesquisa da Wikipedia em um chatbot:

```python
from chatbot import Chat, register_call
import wikipedia

@register_call("whoIs")
def who_is(session, query):
    try:
        return wikipedia.summary(query)
    except Exception:
        for new_query in wikipedia.search(query):
            try:
                return wikipedia.summary(new_query)
            except Exception:
                pass
    return "I don't know about " + query

first_question = "Hi, how are you?"
Chat("examples/Example.template").converse(first_question)




