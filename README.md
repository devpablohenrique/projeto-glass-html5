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
