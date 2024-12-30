<h1>
<a href="https://www.dio.me/">
     <img align="center" width="40px" src="https://hermes.digitalinnovation.one/assets/diome/logo-minimized.png"></a>
    <span> CAIXA - IA Generativa com Microsoft Copilot</span>
</h1>

# :computer: Desafio de projeto: Criando um Podcast com IAs Generativas

O objetivo desse projeto é criar um podcast utilizando ferramentas de IA.

[Github do instrutor](https://github.com/felipeAguiarCode/prompts-for-podcast-generate-by-ia)


# :bulb: Solução do desafio

Utilizarei o [Ollama](https://ollama.com/) para rodar o modelo de LLM localmente, no caso o llama3.1-8b.
A  interação com a LLM foi feita usando o [langchain](https://www.langchain.com/) seguindo o [tutorial](https://medium.com/@mdbaraujo/descubra-como-criar-seu-primeiro-chatbot-poderoso-usando-ollama-c784ae55c13b).

Para geração do título e roteiro veja o arquivo `podcast.ipynb`

## Título

Para gerar o título e subtítulo usei o template para o prompt


    Você é um assistente e vai ajudar na criação de um podcast. 

    Responda como um carioca. {context}

    Pergunta: {question}

    Resposta:


com as entradas:

**context**: O nome deve ser sucinto. O público alvo são os jovens. O formato do podcast é trazer dois pontos de vista diferentes sobre o assunto.

**question**: Me dê 5 sugestões de nome e subtítulo para um podcast que discute assuntos polêmicos atuais.

Dentre as sugestões da LLM escolhi o título e subtítulo:

**Título:** "Voz sem Filtro"

**Subtítulo:** "Nossa opinião, suas reações: o debate mais honesto sobre os assuntos polêmicos de hoje"

## Roteiro

O roteiro foi gerado pela LLM com o template para o prompt:

    Você é o roteirista do podcast 'Voz sem Filtro'. A estrutura do podcast é dado por:

    (Introdução)
    (Argumento_1)
    (Argumento_2)
    (Encerramento)

    Assunto: {Assunto}

    Roteiro: 

    [Regras]

    - O podcast deve ter menos de 5 min
    - Em (Argumento_1) substitua por opiniões favoráveis ao {Assunto}
    - Em (Argumento_2) substitua por opiniões contrárias ao {Assunto}
    - Em (Encerramento) faça um resumo de (Argumento_1) e (Argumento_2) e diga que o ouvinte deve tirar suas conclusões. 
    - Termine dizendo: "Esse foi o podcast de hoje, até a próxima"

Utilizei o roteiro gerado para o assunto **Investimento do governo em energias renováveis** .

## Arte

Para gerar a imagem de capa do podcast utilizei o modelo [stable-diffusion-3.5-large-turbo](https://huggingface.co/spaces/stabilityai/stable-diffusion-3.5-large-turbo) diponível nos spaces do site HuggingFace.

Foi utilizado o prompt:
```
A beard podcaster holding a microphone in a high building with a big city in the window. Cartoon style
```

E a imagem gerada

<img src='assets/image.webp' width=50%>

## Audio

Para transcrição do texto para audio, utilizei o modelo [k2-fsa/text-to-speech](https://huggingface.co/spaces/k2-fsa/text-to-speech) disponível nos spaces do HuggingFace.

## Música de fundo

A musica de fundo foi baixada do site [pixabay](https://pixabay.com/music/search/background/).

Para adicionar a música de fundo utilizei o software de edição de audio [audacity](https://manual.audacityteam.org/index.html).

O resultado final foi exportado para o arquivo `energia_renovavel.mp3` disponível na pasta `output`.
