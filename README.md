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
- Configuração de estilo - CSS utilizado na pagina principal

---
# Projeto - MOC

Para o desenvolvimento do projeto, foi antes desenhado o Wireframe no site => https://mockflow.com/

Segue a imagem abaixo;

[IMAGEM AQUI]

Com o Wireframe do Projeto conseguimos criar a estrutura de caixa (box-model) em que sera dividida o nosso layout.

# HTML

    Antes de começarmos a separação semantica do site, ele foi envolto em uma DIV geral no qual colocamos o ID de "interface" que logo mais sera configurada o estilo geral do site posteriormente
    
### HEADER

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

## SECTION

 Foi utilizado para o exercicio a criação de uma seção, segue a imagem dela no site final.
 
 [IMAGEM AQUI]
 
Segue o codigo HTML.

    <section id="corpo">
                <article id="noticia-principal">
                    <header id="cabecalho-artigo">
                        <hgroup>
                            <h3>Tecnologia > Inovações</h3>
                            <h1>Saiba tudo sobre o Google Glass</h1>
                            <h2>por Gustavo Guanabara</h2>
                            <h3 class="direita">Atualizado em 23/Abril/2013</h3>
                        </hgroup>
                    </header>
    
                    <h2>O que é </h2>
                    <p> O <span style="font-weight: 900;">Google Glass</span> é um acessório em forma de óculos que possibilita a interação dos usuários com diversos conteúdos em realidade aumentada. Também chamado de <a href="http://google.com" target="_blank">Project Glass</a>,
                        o eletrônico é capaz de tirar fotos a partir de comandos de voz, enviar mensagens instantâneas e realizar vídeoconferências. Seu lançamento está previsto para 2014, e seu preço deve ser de US$ 1,5 mil. Atualmente o <em>Google Glass</em>                    encontra-se em fase de testes e já possui um vídeo totalmente gravado com o dispositivo. Além disso, a companhia de buscas registrou novas patentes anti-furto e de desbloqueio de tela para o acessório.</p>
    
                    <figure class="foto-legenda">
                        <img src="_imagens/glass-quadro-homem-mulher.jpg" alt="">
                        <figcaption>
                            <h3>Google Glass</h3>
                            <p>Uma nova maneira de ver o mundo.</p>
                        </figcaption>
                    </figure>
    
                    <h2>Data de lançamento</h2>
                    <p> Não há uma data específica e oficial para o dispositivo ser lançado, ainda. Pode ser que ele esteja disponível em demonstrações a partir de 2013, mas seu lançamento para as lojas fica para, pelo menos, 2014.</p>
    
                    <h2>Especificações Técnicas</h2>
                    <table id="tabelaspec">
                        <caption>Tabela Técnica do Google Glass <span>Mar/2013</span></caption>
                        <tr>
                            <td class="ce">Tela</td>
                            <td class="cd">Resolução equivalente a tela de 25"</td>
                        </tr>
                        <tr>
                            <td rowspan="2" class="ce">Camera</td>
                            <td class="cd">5MP para fotos</td>
                        </tr>
                        <tr>
                            <td class="cd">720p para vídeos</td>
                        </tr>
                        <tr>
                            <td rowspan="2" class="ce">Conectividade</td>
                            <td class="cd">Wi-Fi</td>
                        </tr>
                        <tr>
                            <td class="cd">Bluetooth</td>
                        </tr>
                        <tr>
                            <td class="ce">Memória Interna</td>
                            <td class="cd">12GB</td>
                        </tr>
    
                    </table>
    
                    <h2>Como funciona</h2>
                    <p> De acordo com fontes próximas do Google, os óculos vão contar com uma pequena tela de LCD ou AMOLED na parte superior e em frente aos olhos do usuário. Com o uso de uma câmera e GPS, você pode se situar, assim como selecionar opções com
                        o movimento da cabeça</p>
    
                    <h2>O que você pode fazer com o Google Glasses</h2>
                    <p> O vídeo de divulgação do Google mostra que você pode se transformar em uma espécie de “super-humano”, já que o aparelho pode indicar a quantos metros você está de seu destino, se o metrô está aberto ou fechado, mostrar o clima, agenda
                        e até mesmo permitir que você marque encontros apenas com comandos de voz.</p>
    
                    <div id="indexVideo1">
                        <video id="video1" controls="controls" poster="_imagens/video-mini01.jpg">
                            <source src="_media/how-it-feels.mp4" type="video/mp4">
                            Desculpe, mas não foi possivel carregar o Video
                        </video>
                    </div>
                </article>
            </section>
            
-   Para a seção criamos apenas um artigo, no qual contém o nosso conteúdo principal.
-   Dentro do nosso article, temos uma Tag já utilizada que é a Tag Header, utilizamos ela para criar um segundo cabeçalho dentro da nossa pagina.
-   Novas Tag's - p - span - em
    -   A tag ( p) é utilizada para a criação de paragrafos.
    -  (span) Utilizado para a seleção de uma parte especifica na qual deseja realizar a formatação, seja ela inline aplicada diretamente na tag, ou posteriormente via CSS utilizando classes, Ids, Tagname... etc.  
    -  (em) Serve para darmos enfase, visualmente possui efeito de italico. 
    > O elemento <em> é frequentemente usado para indicar um contraste implícito ou explícito.
-   Novas Tag's - Figure - figcaption
    - A Tag (figure) é utilizada para que possamor criar a legenda de uma imagem de forma semantica, para que os navegadores consigam identificar que aquela legenda é referenciada para aquela imagem.
    - Figcaption contém o oque vai ser a legenda da imagem.
- Novas Tag - video - source
  - A tag video ela serve para anexarmos um video em nossa pagina.
  - (source) Com ela conseguimos direcionar o video (neste caso, pois pode ser utilizada em imagens também) de forma a conseguirmos configurar mais de uma fonte de video, utilizado para quando se trabalha com varios navegadores e algum deles não lide muito bem com um tipo de dado.
> Nota importante
> Com base no redimencionamento do nosso video, uma dica importante foi para utilziarmos ela dentro de uma DIV especifica para o video, para que possamos trabalhar a estilização da DIV para conseguirmos deixar o video responsivo.

## Aside

Criação do nosso conteúdo lateral.

[IMAGEM AQUI]

Aqui o codigo utilizado;

    <aside id="lateral">
        <h1>Outras Notícias</h1>
        <h2>Vídeo mais recente</h2>
        <div id="indexVideo2">
            <video id="video2" controls="controls" poster="_imagens/video-mini02.jpg">
                <source src="_media/one-day.mp4" type="video/mp4">
                Desculpe, mas não foi possivel carregar o Video
            </video>
        </div>

        <h2>Novidades no Glass</h2>
        <p> O Google enfim revelou as especificações completas do Google Glass, e com ele uma surpresa ainda inédita no mercado: a gigante das buscas usará um sistema de áudio baseado na transdução por condução. Através das hastes dos óculos, o som será
            transmitido para o ouvido do usuário por meio de microvibrações em determinados ossos de sua cabeça, sem usar nenhum tipo de alto-falante.</p>
        <p>Além da surpresa do áudio, a tela montada a frente do olho do usuário também chamou atenção. Serão 640 x 360 pixels de resolução que, em proporção, equivaleria a um monitor de 25 polegadas de alta definição colocado a 2,5 metros de distância
            do espectador.
        </p>
    </aside>

## FOOTER

Criação do nosso rodapé.

[IMAGEM AQUI]

Aqui o codigo utilizado;

    <footer id="rodape">
        <p>Copyright &copy; 2013 - by Gustavo Guanabara <br>
            <a href="http://facebook.com/cursosemvideo" target="_blank">Facebook</a> | <a href="http://twitter.com/cursosemvideo" target="_blank">Twitter</a></p>
    </footer>
    
# Configuração de Estilo
    
CSS3 utilizado na configuração da pagina principal -HOME-.
    
    @charset "UTF-8";                                       -- Configuração para que o navegador saiba os caracteres que vão ser                          utilizados
    
    @import url('https://fonts.googleapis.com/css2?family=Titillium+Web&display=swap');    
    @font-face {
        font-family: 'FonteLogo';
        src: url("../_fonts/bubblegum-sans-regular.otf");
    }                                                       -- Importações de fontes
    
    p {
        font-family: Arial, Helvetica, sans-serif;          --Definição da familia da fonte
        text-align: justify;                                -- Configura o texto justificado
        text-indent: 50px;                                  -- Cria um espaço de 50px no inicio do Paragrafo
    }
    
    a {
        color: #606060;                                     -- Define a cor da fonte para todos os links
        text-decoration: none;                              -- Remove o sublinhado de todos os links
    }
    
    a:hover {
        text-decoration: underline;                         -- Ao passar o mouse em cima do link, sera adicionado o sublinhado.
    }
    
    body {
        background-color: #dddddd;                          -- Cor de fundo para o body
        color: rgb(0, 0, 0);                                -- As letras por padrão terão a cor preta
    }
    
    div#interface {
        width: 90%;                                         -- Largura de 90% do tamanho do objeto pai, no caso o body.
        background-color: #ffffff;                          -- Cor de background
        margin: -20px auto 0px auto;                        -- Definição da margin sendo, topo -20px direita automatica, baixo 0px e esquerda automatica.
        box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.5);        --Sombra para a caixa
        padding: 10px;                                      -- Preenchimento de 10px
    }
    
    header#cabecalho img#icone {
        position: absolute;                                 -- Posição absoluta dentro do site, podendo ser configurada dentro do ste livremente, ou dentro do container anterior caso o item pai seja declarado como relative.
        left: 84%;                                          -- 84% de distacia da borda esquerda
        top: 70px;                                          -- 70px de distancia da borda superior
    }
    
    header#cabecalho {
        border-bottom: 1px solid #606060;                   -- Define a borda inferior com 1px de espessura, solida e com a cor.
        height: 150px;                                      -- Altura de 150px
        background: url("../_imagens/glass-logo-peq.jpg") no-repeat 0px 80px; -- Define o backgroud com uma imagem, sem repetição e com largura de 80px
    }
    
    header#cabecalho h1 {
        font-family: 'FonteLogo', Helvetica, sans-serif;    -- Define a familia da fonte que sera utilizada
        font-size: 30pt;                                    -- Tamanho da Fonte
        color: #606060;                                     -- Cor da fonte
        text-shadow: 1px 1px 1px rgba(0, 0, 0, 0.6);        -- Sombra para o texto, sendo os parametros, deslocamento horizontal de 1x, deslocamento vertical de 1px, espalhamento de 1px e cor preta com 0.6 de transparencia. 
        padding: 0px;                                       -- Preenchimento de 0px.
        margin-bottom: 0px;                                 -- Margem inferior de 0px
    }
    
    header#cabecalho h2 {
        font-family: 'Titillium Web', sans-serif;           -- Define a familia da fonte a ser utiliziada
        color: #888888;                                     -- Define a cor da fotne
        font-size: 15pt;                                    -- Tamanho da fonte
        padding: 0px;                                       -- Preenchimento de 0px
        margin-top: 0px;                                    -- Margem de 0px
    }
    
    
    /* Formatação de imagens com legendas   */
    
    figure.foto-legenda {
        position: relative;                                 -- O componente possui posição realtiva, ele ira se comportar de forma a ficar posicionado aonde ele realmente esta no HTML
        border: 8px solid white;                            -- Borda de 8px de espessura, solida e branca
        box-shadow: 1px 1px 4px black;                      -- Sombra da caixa.
    }
    
    figure.foto-legenda img {
        width: 100%;                                        -- Largura da imagem com 100%
        height: 100%;                                       -- Altura da imagem com 100%
    }
    
    figure.foto-legenda figcaption {
        opacity: 0;                                         -- Configura a legenda como invisivel
        position: absolute;                                 -- Posição absoluta
        top: 0px;                                           -- 0px de distancia para o topo
        background-color: rgba(0, 0, 0, 0.4);               -- Transparencia de fundo
        color: white;                                       -- Cor da fonte
        width: 100%;                                        -- Largura de 100%
        height: 100%;                                       -- Altura de 100%
        padding: 10px;                                      -- Preenchimento de 10px
        box-sizing: border-box;                             -- Configuração para que o conteudo não sobreponha a borda da caixa
        transition: opacity 1s;                             -- Configuração da transição
    }
    
    figure.foto-legenda:hover figcaption {
        opacity: 1;                                         -- Ao passar o mouse em cima, sera ativada a opacidade 1, trasendo assim a visualização da legenda.
    }
    
    
    /* Formatação do Menu */
    
    nav#menu {
        display: block;                                     -- Transformação do menu em um item de bloco
    }
    
    nav#menu ul {
        list-style: none;                                   -- Remove o estilo da lista
        text-transform: uppercase;                          -- Configura todos as letras em MAIUSCULAS
        position: absolute;                                 -- Posição absoluta
        top: -20px;                                         -- -20px de distancia do topo
        right: 100px;                                       -- 100px de distancia da margem direita
    }
    
    nav#menu li {
        display: inline-block;                              -- Define cada item da lista como um elemento inline-block - elemento inline que contém algumas das propriedades de bloco
        background-color: #dddddd;                          -- Cor de fundo
        padding: 10px;                                      -- Prenchimento de 10px
        margin: 2px;                                        -- 2px de margem
        transition: background-color 1s;                    -- Configuração da transição
    }
    
    nav#menu li:hover {
        background-color: #606060;                          -- Ao passar o mouse em cima de cada item da lista/menu, a cor de fundo sera alterada
    }
    
    nav#menu h1 {
        display: none;                                      -- Remove o item da visualização
    }
    
    nav#menu a {
        color: black;                                       -- Cor do Texto como preto
        text-decoration: none;                              -- Remove o sublinhado do item.
    }
    
    nav#menu a:hover {
        color: white;                                       -- Ao passar o mouse em cima, a cor da letra sera alterada para branco
        text-decoration: underline;                         -- Ao passar o mouse sera adicionado o sublinhado ao conteúdo.
    }
    
    section#corpo {
        display: block;                                     -- Configura o item como display block
        width: 66%;                                         -- Largura de 66%
        float: left;                                        -- Flutuar a esquerda
        border-right: 1px solid #606060;                    -- Configura borda lateral direita
        padding-right: 15px;                                -- Preenchimento a esquerda de 15px
    }
    
    article#noticia-principal h2 {
        font-size: 13pt;                                    -- Tamanho da fonte para o h2 do artigo
        color: #606060;                                     -- Configuração da cor da fonte
        background-color: #dddddd;                          -- Cor de fundo
        padding: 5px 0px 5px 10px;                          -- Configuração do preenchimento
        margin: 10px 0px 10px 0px;                          -- Configuração da margem
    }
    
    header#cabecalho-artigo h1 {
        font-family: 'FonteLogo';                           -- Fonte utilizada 
        font-size: 20pt;                                    -- Tamanho da fonte para o h1 do artigo
        color: #606060;                                     -- Configuração da cor da fonte
        margin-bottom: 0px;                                 -- Configuração da margem
        margin-top: 0px;                                    -- Configuração da margem
    }
    
    .direita {
        text-align: right;                                  -- Configuração do alinhamento do texto
    }
    
    header#cabecalho-artigo h2 {
        font-size: 13pt;                                    -- Tamanho da fonte
        color: #cecece;                                     -- Configuração da cor da fonte
        background-color: #ffffff;                          -- Cor de fundo
        margin: 0px;                                        -- Configuração da margem
    }
    
    header#cabecalho-artigo h3 {
        font-size: 13px;                                    -- Tamanho da fonte
        color: #606060;                                     -- Configuração da cor da fonte
    }
    
    table#tabelaspec {
        border: 1px solid #606060;                          -- Define a configuração para a borda
        border-spacing: 0px;                                -- Define o distanciamento entre cada celula
        margin-left: auto;                                  -- Centraliza os itens ao centro
        margin-right: auto;                                 -- Centraliza os itens ao centro
    }
    
    table#tabelaspec td {
        border: 1px solid #606060;                          -- Define a configuração para a borda
        padding: 10px;                                      -- Preenchimento de 10px 
        text-align: center;                                 -- Alinhamento do Texto ao centro
        vertical-align: middle;                             -- Alinhamento vertical do item da tabela ao centro
    }
    
    table#tabelaspec td.ce {
        color: #ffffff;                                     -- Cor da fonte
        background-color: #606060;                          -- Cor de fundo
        vertical-align: top;                                -- Alinhamento vertical ao top
        font-weight: bold;                                  -- Configura o negrito
    }
    
    table#tabelaspec td.cd {
        background-color: #cecece;                          -- Cor de fundo
    }
    
    table#tabelaspec caption {
        color: #888888;                                     -- Cor da fonte
        font-size: 13pt;                                    -- Tamanho da fonte
        font-weight: bolder;                                -- Configura o negrito
    }
    
    table#tabelaspec caption span {
        display: block;                                     -- Configura o display em bloco
        float: right;                                       -- Flutuar a direita
        color: black;                                       -- Cor da fonte
        font-size: 8pt;                                     -- Tamanho da fotne
        margin-top: 8px;                                    -- Margem superior de 8px
    }
    
    aside#lateral {
        display: block;                                     -- Display em bloco
        width: 30%;                                         -- Largura de 30px
        float: right;                                       -- Flutuar a direita
        background-color: #dddddd;                          -- Cor de fundo
        padding: 10px;                                      -- Preenchimento de 10px
        margin-top: 10px;                                   -- Margem top de 10px
        box-shadow: 2px 2px 2px rgba(0, 0, 0, 0.5);         -- Sombra da caixa
    }
    
    aside#lateral h1 {
        font-family: 'FonteLogo', sans-serif;               -- Familia da fonte
        font-size: 20pt;                                    -- Tamanho da fonte
        color: #606060;                                     -- Cor da fonte
        margin-top: 0px;                                    -- Margem superior de 0px
    }
    
    aside#lateral h2 {
        background-color: #606060;                          -- Cor de fundo
        font-size: 13pt;                                    -- Tamanho da fonte
        color: white;                                       -- Cor da Fonte
        padding: 5px;                                       -- Preenchimento de 5px
    }
    
    footer#rodape {
        clear: both;                                        -- Remove as orientações de flutuação para o item em questão
        border-top: 1px solid #606060;                      -- Borda superior
    }
    
    footer#rodape p {
        text-align: center;                                 -- Alinha o texto do paragrafo ao centro
    }
