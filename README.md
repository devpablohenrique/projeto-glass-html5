# Curso de Html5 + CSS3
_Curso disponibilizado pelo canal Curso em Video no youtube_ 
Link do curso: https://www.youtube.com/watch?v=epDCjksKMok&list=PLHz_AreHm4dlAnJ_jJtV29RFxnPHDuk9o

# Sobre o projeto

O curso disponibilizado tem como premissa ser de cunho iniciante, apresentando as tecnologias de forma simples e de facil aprendizado.

Sendo dividido em varias areas para o aprendizado, contendo no total 40 Horas, no qual é possivel gerar o certificado caso seja realizado pelo proprio site. 

https://www.cursoemvideo.com/curso/html5/

# Divisão de conteúdo

Ao iniciarmos o nosso projeto, devemos criar a nossa estrutura basica HTML.

    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Document</title>
    </head>
    <body>
        
    </body>
    </html>

Com base nesta estrutura basica podemos criar o nosso projeto.

>Nota: Caso esteja utilizando o VSCode como editor para a criação do projeto, a estrutura basica pode ser criada apertando a tecla "! + Enter".

Com base nesta estrutura, oque iremos alterar logo de cara são as tag's 
- < html lang="en"> => para => < html lang="pt-br">
        Com isto dizemos para o navegador que o conteudo do site esta em portugues - brasileiro.

- <title>Document</title> => para => <title>Tudo sobre Google Glass</title>
    Definimos agora o nome que sera apresentado no Titulo do Site.
 
# Indice

#### Projeto
- MOC - Projeto desenhado do site
#### HTML
- Separação do conteúdo utilizando as Tag's semanticas
  - Header (Cabeçalho)
  - Section (Seção)
  - Aside
  - Footer

---
# Projeto - MOC

Para o desenvolvimento do projeto, foi antes desenhado o Wireframe no site => https://mockflow.com/

Segue a imagem abaixo;

[IMAGEM AQUI]

Com o Wireframe do Projeto conseguimos criar a estrutura de caixa (box-model) em que sera dividida o nosso layout.

# HTML

    Antes de começarmos a separação semantica do site, ele foi envolto em uma DIV geral no qual colocamos o ID de "interface" que logo mais sera configurada o estilo geral do site posteriormente
    
##### HEADER

Resultado visual final;

[IMAGEM AQUI]

Abaixo o codigo desenvolvido para a configuração do cabeçalho do site, 

    <header id="cabecalho"> 
        <hgroup>
            <h1>Google Glass</h1>
            <h2>A revolução do Google está chegando</h2>
        </hgroup>
    
        <img id="icone" src="_imagens/glass-oculos-preto-peq.png" alt="Icone oculos pequeno">
    
        <nav id="menu">
            <h1>Menu Principal</h1>
            <ul type="disk ">
                <li onmouseover="mudaFoto('_imagens/home.png')" onmouseout="mudaFoto('_imagens/glass-oculos-preto-peq.png')"><a href="index.html">Home</a></li>
                <li onmouseover="mudaFoto('_imagens/especificacoes.png')" onmouseout="mudaFoto('_imagens/glass-oculos-preto-peq.png')"><a href="specs.html">Especificações</a></li>
                <li onmouseover="mudaFoto('_imagens/fotos.png')" onmouseout="mudaFoto('_imagens/glass-oculos-preto-peq.png')"><a href="fotos.html">Fotos</a></li>
                <li onmouseover="mudaFoto('_imagens/multimidia.png')" onmouseout="mudaFoto('_imagens/glass-oculos-preto-peq.png')"><a href="multimidia.html">Multimídia</a></li>
                <li onmouseover="mudaFoto('_imagens/contato.png')" onmouseout="mudaFoto('_imagens/glass-oculos-preto-peq.png')"><a href="fale-conosco.html">Fale conosco</a></li>
            </ul>
        </nav>
    </header>

- No inicio do codigo apresentado, temos a declaração da nossa tag < header>, aonde foi definido que seria o nosso cabeçalho, nela temos configurado o #id "cabecalho".
- Logo abaixo, temos um agrupamento de cabeçalhos, definido pela tag < hgroup>.
  - Dentro do grupo de cabeçalhos, temos dois cabeçalhos definidos um < h1>(Titulo) e um < h2>(Subtitulo).
- Foi configurado abaixo do < hgroup> a declaração da tag < img> que é utilizada para realizar a declaração de imagens, configuramos também o id="icone" que sera utilizado no momento da formatação por CSS, ela é responsavel para adicionar a imagem abaixo.
[IMAGEM AQUI]
- Temos agora o nosso menu que utilizamos a estrutura semanantica < nav>, utilizada para a criação da navegação do nosso site.
  - Configuramos um titulo < h1> para o menu.
  - Configuramos também a estrutura de listas do HTML com seu < ul>(Lista) e < li>(Itens da lista).
     - Para os itens da lista foram configuradas algumas funções JavaScript, que são responsaveis pela alteração da foto quando se passa o mouse por cima de qualquer um dos itens, caso não tenha visto, da um pulinho nas paginas e teste rsrs.
     - Cada item da lista também possui um link < a>, que é responsavel pelo direcionamento e navegação para as outras paginas do site.
  > Nota: Verificando posteriormente em outros sites e cursos, a estutrutura de criação de barras de navegação por ul's e li's é amplamente utilizada.
    
    [IMAGEM AQUI]
