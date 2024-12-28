<h1>
<a href="https://www.dio.me/">
     <img align="center" width="40px" src="https://hermes.digitalinnovation.one/assets/diome/logo-minimized.png"></a>
    <span> CAIXA - IA Generativa com Microsoft Copilot</span>
</h1>

# :computer: Desafio de projeto: Criando um Ebook com ChatGPT & MidJourney

O objetivo desse projeto é gerar um e-book utilizando ferramentas de IA.

[Github do instrutor](https://github.com/felipeAguiarCode/prompts-recipe-to-create-a-ebook)


# :bulb: Solução do desafio

- Para geração de imagem utilizei o [Adobe Firefly](https://firefly.adobe.com/) com o prompt:

``` 
A brain in a computer circuit style with a cpu on the center of the brain and a performance meter.
```

<img src=firefly.jpg>

- Para edição da capa utilizei o [Adobe Express](https://new.express.adobe.com/)

<img src=cover.png>

- O conteúdo foi gerado com o GPT-4o mini

prompts:

```
You are a Machine Learning specialist writing an e-book about performance metrics. The content must be of introductory level, and each metrics should be presented with an example. Format the book using asciidoc markup language. 
```
```
Include chapters for the logarithmic loss, area under a curve and confusion matrix
```

O ebook foi formatado utilizando asciidoc (arquivo `performance_metrics.adoc`) e o pdf gerado. Segue um exemplo de página:

<img src=pag.png>