![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-Repository-black?style=for-the-badge&logo=github)
![Status](https://img.shields.io/badge/status-Em%20andamento-yellow?style=for-the-badge)

# 🌐 Curso de HTML — Anotações e Exemplos Práticos

Este repositório reúne as páginas que fui criando enquanto aprendia HTML "na prática": cada arquivo `.html` é uma aula sobre um assunto específico (áudio, comentários, formulários, tabelas, links, etc), com o código comentado explicando o que cada tag faz e como usei ela.

A ideia aqui não é um projeto "bonito" pronto, e sim um **material de estudo** — por isso o comentário dentro do próprio código, escrito no momento em que eu tava aprendendo.

---

## 📚 Índice das Aulas

| # | Arquivo | Assunto |
|---|---------|---------|
| 1 | [`Audio.html`](#-1-audiohtml--aula-de-áudio) | Tag `audio` e `source` |
| 2 | [`Comentarios.html`](#-2-comentarioshtml--comentários-em-html) | Comentários `<!-- -->` |
| 3 | [`DivEHtmlSemantico.html`](#-3-divehtmlsemanticohtml--divs-e-html-semântico) | `div`, tags semânticas e CSS básico |
| 4 | [`ExemploAulaLink.html`](#-4-exemploaulalinkhtml--página-de-apoio-para-links) | Página auxiliar para testar links |
| 5 | [`Formularios.html`](#-5-formularioshtml--formulários) | `form`, `input`, `select`, `textarea` |
| 6 | [`Iframes.html`](#-6-iframeshtml--iframes) | Tag `iframe` |
| 7 | [`Imagens.html`](#-7-imagenshtml--imagens-e-gifs) | Tag `img`, gifs, image map |
| 8 | [`Links.html`](#-8-linkshtml--links-hyperlinks) | Tag `a`, `href`, `target` |
| 9 | [`Listas.html`](#-9-listashtml--listas-ordenadas-e-não-ordenadas) | `ul`, `ol`, `li` |
| 10 | [`Tabelas.html`](#-10-tabelashtml--tabelas) | `table`, `tr`, `th`, `td` |
| 11 | [`Video.html`](#-11-videohtml--vídeo) | Tag `video` e `source` |
| 12 | [`elementosCitar.html`](#-12-elementoscitarhtml--elementos-de-citação-e-texto) | `abbr`, `cite`, `q`, `blockquote`, `bdo` |
| 13 | [`index.html`](#-13-indexhtml--primeira-aula) | Primeiros contatos: `del`, `strike`, `sup`, `sub`, `mark` |

---

## 🔊 1. `Audio.html` — Aula de Áudio

Primeira aula sobre mídia. Aqui aprendi:

- A tag principal é a `<audio>`, e dentro dela colocamos a `<source>`, que é a tag **filha** responsável por indicar o arquivo e o tipo (`type="audio/mpeg"`).
- Para o player aparecer na tela (play, pausa, volume), é obrigatório colocar o atributo `controls` na tag `audio`.
- Dica de digitação: `&nbsp;` (com o `;` no final) cria um espaço "forçado" no HTML, já que espaços comuns são ignorados.

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1>Aula de Audio</h1>
    vamos usar audio agr dica <b>&nbsp</b> com ; faz um espaço <br>
    tag de audio é <b>audio</b> junto da <b>source</b> que seria a tag filho <br>
    dentro do audio tempos que colocar a tag <b>controls</b><br><br>

    <audio controls>
        <source src="audio/AudioDoido.mpeg" type="audio/mpeg">
    </audio>


    
</body>
</html>
```

---

## 💬 2. `Comentarios.html` — Comentários em HTML

Aula curtinha, mas essencial: comentário serve pra deixar anotações no código que **não aparecem** na página renderizada.

- Sintaxe: `<!--` para abrir e `-->` para fechar.
- Atalho no VS Code: `Ctrl + K` seguido de `C` comenta um bloco inteiro de uma vez.

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="estou vendo a aula de comentarios guys">
    <meta name="author" content="Carlos Sales">
    <meta name="keywords" content="Aprender">


    <title>Aula dobre Comentarios</title>
</head>
<body>
    <h1>aula de <b>Comentarios</b></h1>
    <!--isso é um comentario aq no html-->
    <p>paragrafos guys</p>
    <p>pra comentar em html vc usa  sinal maíor junto do ! e depois -- </p>
    <!--Assimm-->
    <!-- crtl k c pega um monte de coisa-->
    
</body>
</html>
```

---

## 🧱 3. `DivEHtmlSemantico.html` — Divs e HTML Semântico

Aqui saí do "tudo dentro de `p`" e comecei a organizar a página em blocos de verdade:

- `<div>` serve pra **dividir o site em blocos** genéricos (sem significado próprio).
- As tags **semânticas** (`header`, `nav`, `section`, `footer`) fazem a mesma coisa que a `div`, só que já dizem *o que* aquele bloco representa.
- Usei `class` pra estilizar cada bloco com CSS: `.topo` (header cinza), `.menu` (nav azul escuro com links flutuando lado a lado via `float: left`) e `.coluna1` (duas colunas de 50% cada, lado a lado).
- `* { box-sizing: border-box; }` garante que padding e borda não estourem a largura definida.

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>semantico</title>
    <style>
        *{ 
            box-sizing:  border-box;


        }
        body{
            margin: 0;
        }
        .topo{
            background-color: gray;
            padding: 30px;
            text-align: center;

        }
        .menu{
            background-color: darkblue;
            overflow: hidden;
            

        }
        .menu a{
            color: aliceblue;
            padding: 14px 16px;
            float: left;
            display: block;
            text-decoration:  none;
            

        }
        .coluna1{
            float: left;
            width: 50%;
            padding: 15px;

        }
        
        
    </style>
</head>
<body>
    <p>
       
        <!--usamos div para dividir o site em blocos-->
        <header class="topo">
              
            <h1>topo</h1>
            <p>aq o é o topo</p>
        </header>
        <nav class="menu">
            <a href="Comentarios.html">secao de comentarios</a> 
            <a href="Imagens.html"> imagens</a>
            <a href="Iframes.html"> iframes</a>
            <a href="Listas.html"></a>
        </nav>
        <section class="coluna1">
            <h2>Coluna</h2>
            <p>
                akshahhhdasdlasdhjahkldsadhjsa
            </p>


        </section>
         <section class="coluna1">
            <h2>Colunaa</h2>
            <p>
                akshahhhdasdlasdhjadsdasdasdasdasdadaskldsadhjsa
            </p>


        </section>
        <!--rodape-->
        <footer>



        </footer>
        




    </p>
    
</body>
</html>
```

---

## 🔗 4. `ExemploAulaLink.html` — Página de apoio para Links

Essa página não é uma aula em si — é o **destino** de um dos links criados na aula de `Links.html`, só pra provar que dá pra navegar entre arquivos do próprio projeto (link relativo) e não só pra sites externos.

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="author" content="Carlos Sales">
    <meta name="keywords" content="Exemplo">
    <meta name="description" content="Exemplo do seguimento">
    <title>Exemplo do link</title>
</head>
<body>
    <h1> exemplo que to usando pra acssar esse arquivo site do outro arquivo da aula sobre links </h1><br>
    <p><a href="Links.html">voltar para a aula</a></p>
</body>
</html>
```

---

## 📝 5. `Formularios.html` — Formulários

Aula mais completa até agora. Formulário é usado pra **coletar dados de entrada** (login, cadastro, etc). Resumo dos elementos usados:

- `<form>` é o container de tudo; pode receber `action` (pra onde os dados vão, geralmente um `.php`) e `method`.
- `<input>` é o campo mais versátil, e o `type` muda o comportamento:
  - `text` → campo comum de texto.
  - `password` → mascara o que é digitado.
  - `email` → valida automaticamente se o formato é de e-mail.
  - `radio` → várias opções, mas só **uma** pode ser escolhida (por isso todos compartilham o mesmo `name`).
  - `checkbox` → várias opções e pode marcar **quantas quiser**.
- `placeholder` é o texto de dica dentro do campo, antes de digitar.
- `label` (usando `for` ligado ao `id` do input) posiciona o texto explicativo ao lado do campo.
- `required` obriga o usuário a preencher aquele campo antes de enviar.
- Fora do `input`, temos o `<select>` com várias `<option>` dentro — um menu suspenso de escolha única.
- `<textarea>` é uma caixa de texto livre, e `rows`/`cols` controlam o tamanho dela.
- `submit` (`<input type="submit">`) já valida e envia o formulário; `<button>` é mais genérico e não faz isso sozinho.

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="author" content="Carlos Sales">
    <meta name="description" content="falando de formularios">
    <meta name="keywords" content="Aprender">
    <title>Aula de Formularios</title>
</head>
<body>
    <h1>Formulatios html</h1>
    <p>bora falar de formularios <br>
        sao dados de entrada login...... essas coisas <br>
        <a href="index.html">voltar pra principal</a> <br><br>

        vamos usar a tag <b>forms</b> e dentro dela nos temos
        o <b>imput</b> <br>
        ele tem varios coisas, o primeiro é o text
        <br>
        <b> placeholder </b> é pra falar pro usuario oq é pra fazer <br>

        <b>label</b> é pra deixar no canto esquerdo do retangulo
        <br>
        tbm temos o campo do tipo senha  no input vamos colocar o type <b>password</b> mascara oq ta sendo digitado <br> 
        tbm temos o tipo email type <b>email</b> detecta se oq digitou é email <br>
        e o <b>sumit/value</b> que faz a validação <br>
        no form da pra colocar <b>action</b> junto do <b>method</b>
        o arquivo geralmente é php <br>
        se colocar <b>required</b> nos input, a pessoa vai ser obrigada a colocar algo <br>
        o imput do tipo <b>radio</b> é aonde tem as bolinhas de varias esccolhas radio é apenas uma opcao de escolha <br>

        agr o <b>checkbox</b> ele vai ser de multiplas escolhas <br>
        lembrando, faz input e depois o label <br><br>
        
        saindo do input, vamos usar o <b>select</b> e dentro dele temos as <b>option</b> <br> <br>



        e temos o campo de <b>textarea</b> um campo de texto que a pessoa escreve <br>
        <b>rows</b>  e <b>cols</b> deixa maior a caixa de texto <br>
        o <b>button</b> é quase igual o sumbit mas ele é generico

        
        <br>



        <form  >
            <label for="campo_nome">Nome:</label>
            
            <input  id="campo_nome" type="text" placeholder="Digite seu nome aqui!" required >
            <br><br>
            <label for="campo_sobre">Sobrenome:</label>
            <input  id="campo_sobre" type="text" placeholder="Digite o Sobrenome!" required >
            <br><br>
            <label for="campo_senha">Senha:</label>

            <input  id="campo_senha" type="password" placeholder="Digite sua senha" required > <br><br>
            <label for="campo_email">Email:</label>

            <input  id="campo_email" type="email" placeholder="Digite um email" required > <br><br>



            <h2>Escolha teste</h2>
            <input type="radio" id="Cachorro" name="animal" value="Cachorro" > 
            <label for="Cachorro"> Cachoroos</label>
            <br><br>
            <input type="radio" id="cat" name="animal" value="gato" > 
            <label for="cat"> Gato</label>
            <br><br>
             <input type="radio" id="bird" name="animal" value="Passaro" > 
            <label for="bird"> Passaro</label>
            <br><br><br><br>

            <h2>Oque vc tem em casa?</h2>

        

            <input id="item1" type="checkbox" name="Item1" value="Tv">
            <label for="item1"> TV</label> <br><br>
            <input id="item2" type="checkbox" name="item2" value="Video Game">
            <label for="item2"> Video Game</label> <br><br>
            <input id="item3" type="checkbox" name="item3" value="Cama">
            <label for="item3"> Cama</label> <br><br> <br>



            <h2>Escolha uma Cor</h2>
            <select name="Cores">
                <option selected  disabled value="">Selecione uma cor</option>
                <option value="vermelho">Vermelho</option>
                <option value="Preto">Preto</option>
                <option value="Azul">Azul</option>
                <option value="Amarelo">Amarelo</option>
                <option value="Magenta">Magenta</option>





            </select> <br><br><br>

            <h2>Digite sua Mensagem</h2>
            <textarea  placeholder="Digite o texto"  rows="10"  cols="60" name="mensagem" id="1"></textarea> <br><br>


            <input type="submit" value="Enviar Formulario">
            <button>clique aq</button>











        </form>
    
    

    
    
    
    </p>
    
</body>
</html>
```

---

## 🖼️ 6. `Iframes.html` — Iframes

Iframe é uma forma de **exibir um site (ou outra página) dentro da própria página**, sem precisar sair dela.

- Tag principal `<iframe>`, com `src` apontando pro conteúdo que vai ser exibido.
- `width` e `height` controlam o tamanho da "janela".
- `title` é usado para acessibilidade.
- Se o `<iframe>` tiver um `name`, uma tag `<a>` pode usar `target="nome-do-iframe"` pra abrir o link **dentro** dele, em vez de navegar a página toda.
- Com CSS (`style="border:none;"`) dá pra tirar a borda padrão, fazendo parecer que é conteúdo nativo da página.
- Pra incorporar vídeo do YouTube: Compartilhar → Incorporar → copiar o `<iframe>` gerado e colar.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="author" content="Carlos Sales">
    <meta name="keywords" content="Aprender">
    <meta name=" description" content="indo alem">
    <title>Iframes</title>
</head>
<body>
    <h1>Vamo de iframe</h1>

    <p>
        <b>primeira aula </b><br>
        ao inves de ir em outro site, ele abre direto na mesma pagina <br>
        <a href="index.html" target="meu-iframe"> sobre o primeiro site</a> <br>
        <br>
        é uma maneira de mostrar um site html dentro de um site html <br>
        vamos usar a tag <b>iframe</b> depois <b>src</b> <br>
        e podemos especificar uma altura e largura usando o <b> width/ height </b> <br>
        e podemos colocar <b>title</b><br>
        no <b>src</b> podemos colocar sites e um monte de coisa e ela q linca tudo <br>
        se eu colocar usando css <b>style= border:none</b> vai ficar parecendo que é o mesmo site <br><br>
        <hr>

       <iframe   style="border:none;" src="Imagens.html"  width="600"    height="500" title="Meu iframe"></iframe> <br><br><br>
       <hr>

       <iframe   width="100%" style="border:none;"  src="index.html" name="meu-iframe" title="iframe de exemplo"></iframe>
       <br><br><br><br>
       para incorporarmos um video no yt é so eu clicar em compartilhar, encorporar e pego o iframe dele e copio e colo <br> <hr>

       <iframe width="560" height="315" src="https://www.youtube.com/embed/z7m9xryJtfQ?si=-g1Y7yXGhTe5dkIX" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


    </p>
    
</body>
</html>
```

---

## 🖼️ 7. `Imagens.html` — Imagens e Gifs

- A tag `<img>` mostra imagens, e é uma tag **sem fechamento**.
- `width` define o tamanho, `height` a altura (se colocar só um dos dois, o navegador mantém a proporção).
- `alt` é o texto alternativo — importante pra acessibilidade (leitores de tela) e aparece caso a imagem não carregue.
- Dá pra usar tanto uma **imagem externa** (link direto de outro site) quanto uma **imagem própria**, guardada numa pasta local (`img/`) do projeto.
- Envolver a `<img>` com uma tag `<a>` transforma a imagem inteira num link clicável.
- **Gif** funciona exatamente igual a uma imagem comum — é só o formato de arquivo que muda.
- Havia também um teste de **image map** (comentado no código) — uma forma de tornar áreas específicas de uma mesma imagem em links diferentes, usando `<map>` e `<area>` com coordenadas.
- Sites úteis anotados: **Pexels** (imagens/gifs grátis), **Flaticon** (ícones), **Photopea** (editor pra deixar imagens com fundo transparente) e o gerador de **image maps**.

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="author" content="Carlos Sales">
    <meta name="keywords" content="Aprender">
    <meta name="description" content="Vamos aprender a usar imagens no html">
    <title>  Aula de Imagens</title>
</head>
<body>
    <h1> <img src="img/heart.png" width="10">Vamos usar imagens agr eheh</h1>
    <p>partiu imagenss po <br>
        a Tag <b>img </b> que mexe com as imagens <br>
        e a tag seguida <b> width </b> faz o tamanho dela <br>
        e o <b> height </b> mede a altura  <br>
        seria algo como width = 300 e o height = 300... <br>
        o alt seria o atributo visual pra quem é cego <br>
        pexels é um site com imagens gratuitas <hr>
       <img src="https://imgs.search.brave.com/PesXYT5mYlCf8xuH0m5oSXk8htWC5Nna_FW2MDMe7mM/rs:fit:500:0:1:0/g:ce/aHR0cHM6Ly9paDEu/cmVkYnViYmxlLm5l/dC9pbWFnZS4xMDQ3/NzI0NDQ1LjY0OTkv/c3Qsc21hbGwsNTA3/eDUwNy1wYWQsNjAw/eDYwMCxmOGY4Zjgu/anBn" width="300" alt="gru apontando uma arma">
    </p> <hr>
    <p> vamos usar nossas proprias imagens <br>
        criei um pacote no vscode chamado img e coloquei uma la, agr é so usar a tag de imagem e colocar o nome dela <br>
        
        <a href="https://github.com/GoblinCaulG/Sites/tree/main/ClinicaPsicopedagoga"><img src="img/samurai.jpg" width="300"></a>
       <!-- Image Map Generated by http://www.image-map.net/ -->
<!--<img src="img/samurai.jpg" usemap="#image-map">

<map name="image-map">
    <area target="" alt="chapeu" title="chapeu" href="https://www.google.com/search?q=chapeu+samurai&amp;udm=2&amp;sxsrf=APpeQnvChQ1I0josMSGridQnF5GF_rwBSw%3A1788640696847" coords="1188,2069,2432,2864" shape="rect">
    <area target="" alt="Katana" title="Katana" href="https://www.google.com/search?q=katana+samurai&amp;udm=2&amp;sxsrf=APpeQnvTXDY0LKIhnm2VJIHzmIJAxdxLQw%3A1788640703765" coords="3354,4990,3074,1941" shape="rect">
    <area target="" alt="github" title="github" href="https://github.com/GoblinCaulG/Sites/tree/main/ClinicaPsicopedagoga" coords="1042,2930,2951,5028" shape="rect">
</map> --> <hr> <br>
        photopea é um site que eu consigo fazer imagens transparente <hr> <br>
    </p>
    <h2>Gifs</h2> <hr>
    <p>gif é a mesmissima coisa ok? <br>
        <img src="https://media2.giphy.com/media/v1.Y2lkPTZjMDliOTUydTczZHZ1NWR6cDh4bjR1b3Bmejc1Nmo1ZHdyc3FlNXd6eTUwcHA1ayZlcD12MV9naWZzX3NlYXJjaCZjdD1n/MOYUOOoIHOj9PKN1rE/200w.gif" > <br><br>
        <hr>
        flaticon é o site que usamos pra fazer icones
        tbm tenho o pexels ne <br>
        image map generator <br><br>
        <hr>
        <br>
        exemplo <br>
        <img src="img/heart.png" width="30" >
    
    </p>
</body>
</html>
```

---

## 🔗 8. `Links.html` — Links (Hyperlinks)

- Link e hyperlink são a mesma coisa; a tag usada é a `<a>`.
- O caminho vai dentro de `href`, e o texto que aparece clicável fica entre a abertura e o fechamento da tag.
- Por padrão o link abre na **mesma aba**; para abrir em uma **aba nova**, usa-se `target="_blank"`.
- Também dá pra linkar para outro arquivo **do próprio projeto** (link relativo, ex: `ExemploAulaLink.html`), e não só para sites externos.

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name = "author" content="Carlos Sales">
    <meta name="description" content="Vamos aprender a usar Links">
    <meta namte="keywords" content="Aprender">
    <title>Document</title>
</head>
<body>
    <h1>Aula de como vamos aprender a usar <b>Links</b> guys <br></h1>

    <p>Link ou imperlink a mesma coisa <br>
        usamos a TAG <b>a</b> para usarmos no link <br>
        <!--usamos a e depois colocamos o link nos "" e do lado o texto-->

        <hr><a href="https://github.com/GoblinCaulG/Sites/tree/main/ClinicaPsicopedagoga"> ir para meu github</a> <hr><br>
        agr pra poder ir numa outra aba usamos o target blank
        <hr>
        <a href="https://github.com/GoblinCaulG/Sites/tree/main/ClinicaPsicopedagoga" target="_blank">Abrindo nova guia</a><br><hr>
        <br> indo pra um um link dentro do projeto que eu to tipo, puxar um site do meu proprio projeto <br>
        <a href="ExemploAulaLink.html">aq vamos pra outro link</a> <hr><br>
    


    </p>

    
</body>
</html>
```

---

## 📋 9. `Listas.html` — Listas ordenadas e não ordenadas

- **Lista não ordenada** (sem numeração, com bolinhas): tag `<ul>`, e cada item dentro dela é um `<li>`.
- **Lista ordenada** (numerada): tag `<ol>`, também usando `<li>` pra cada item — a única diferença é a tag "container".

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="author" content="Carlos Sales">
    <meta name="keywords" content="Aprender">
    <meta name="description" content="Aprendendo Listas em html">

    <title>Listas em HTML</title>
</head>
<body>
    <h1>Vamo Aprender Listas -nao ordenada</h1>
    <p>para criarmos uma listas nao ordenadas, vamos usar a tag <b>ul</b> ela que cria as listas
    <br> dentro da ul nos temos a tag <b>li</b> que seria um item da lista <br>
    
    <hr>
    <ul>
        <li>arroz</li>
        <li>feijao</li>
        <li>macarrao</li>
        <li>uranio</li>



    </ul>
    
    
    
    
    </p>
    <h2>Listas Ordenadas</h2>
    <p>as lista ordenada vamos usar a tag <b>ol</b> <br>
        e continuamos usando o li 
        
        
    <hr>
    <ol>
        <li>sabao</li>
        <li>sabonete</li>
        <li>nao sei</li>


    </ol>
    
    
    
    </p>
    
</body>
</html>
```

---

## 📊 10. `Tabelas.html` — Tabelas

- Container principal: `<table>`.
- Cada linha é uma `<tr>`.
- Na **primeira linha**, as colunas usam `<th>` (título da coluna).
- Nas linhas seguintes, os dados usam `<td>`, sempre respeitando a ordem das colunas definida pelo `th`.
- `border` desenha as linhas de grade da tabela, `width` controla a largura, e `style` (como `text-align: center`) ajuda a deixar mais organizada.

```html
<!doctype html>
<html lang="pt-br">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta name = "author" content="Carlos Sales">
    <meta name="description" content="mexendo tabelas">
    <meta name="keywords" content="aprender">

    <title>Aprendendo tabelas em HTML</title>
  </head>
  <body>
    <h1>Aprendendo tabelas</h1><hr>
    <p>
        para criarmos tabela usamos a Tag <b>Table</b>
        <br><b>tr</b> tag que vc quer criar uma linha <br>
        dentro da linha nos temos a tag <b>th</b> que sao as colunas(titulo de uma coluna) <br>
        so usamos <b>th</b> na primeira linha <br>
        na proxima linha vamos usar a tag <b>td</b> <br>
        se no primeiro th ta nome no primeiro td vai ta relacionado ao nome
        <br>da pra usar width nela tbm e com o border que vai fazer linhas <br>
        <b>style</b> e o estilo que deixa bonito <hr> 
        <table width="100% " border="1" style="text-align: center;">
            <tr>
                <th>nome</th>
                <th>idade</th>
                <th>peso</th>

            </tr>
            <tr>
                <td>Carlos Sales</td>
                <td>19 anos</td>
                <td> 71 kg</td>
            </tr>
            <tr>
                <td>teste1</td>
                <td>200 anos</td>
                <td>545 kg</td>
            </tr>
            <tr>
                <td>blabla</td>
                <td>55 anos</td>
                <td>34 kg</td>
            </tr>
        </table>

        
    </p>



  </body>
</html>
```

---

## 🎬 11. `Video.html` — Vídeo

- A tag `<video>` funciona parecido com o `<audio>`, também usando `<source>` como filha.
- `poster` define uma imagem de capa exibida antes do vídeo começar a tocar.
- `autoplay` faz o vídeo tocar automaticamente assim que a página carrega.
- `controls` mostra os botões de play/pausa/volume.

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Video</title>
</head>
<body>
    <h1>Vamos falar de videos</h1>
    <p>a tag é <b>video</b> junto do source <br>
        a tag <b>poster</b> pegamos um caminho de uma imagem <br>
        <b>autoplay</b> toca no momento que entra no site
        <video   poster="img/Speed.jpg" width="100%" controls>
            <source src="Video/Teste.mp4" type="video/mp4">


        </video>
    
    
    
    
    </p>
    
</body>
</html>
```

---

## ✍️ 12. `elementosCitar.html` — Elementos de Citação e Texto

Aula sobre tags que dão **significado** a trechos de texto:

- `<abbr title="...">` marca uma abreviação; ao passar o mouse em cima, aparece o significado completo.
- `<address>` indica um endereço.
- `<cite>` é usada para o título de uma obra (livro, filme, etc).
- `<q>` faz uma citação **curta**, em linha com o resto do texto.
- `<blockquote>` destaca um **trecho maior**, separado do restante do parágrafo.
- `<bdo dir="rtl">` (ou `ltr`) inverte a direção do texto — usada pra forçar leitura da direita pra esquerda ou vice-versa.
- `<hr>` foi usada várias vezes só pra separar visualmente cada tópico da aula.

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="aula sobre citaçoes em html">
    <meta name="author" content="Carlos Sales">
    <meta name="keywords" content="Aprender">

    <title>Aulas de Citação</title>
</head>
<body>
    <h1>E <b>Boraaaa</b></h1>
    <p>estou aqq no html</p> <hr><br>
    <p><b>abbr</b> é abreviação aonde se vc passa o mouse encima e fala oq é</p>
    <p>estou no <abbr title="text markup language">html</abbr></p>
    <hr>



    <p>vamos usar o <b>address</b> que é o endereço</p>
    <p>Carlos
        <address>rua do sonhos quero dinheiro 7777</address>


    </p> <hr>
    <p>vamos usar a tag <b>cite</b> ela é um titulo 
        <br>
        o filme da minha vida chamado <cite>Carlos</cite> é incrivel
    </p><hr>
    <p>a tag <b>q</b> é usada pra fazer citação <br>
    exemplo: usando agora -- <q>eu quero dinheiroooooo</q>
    </p><hr>

    <p>o <b>blockquote</b> é algo destacado um trecho destacado <br>

        Partiu exemplooo: BALLALALAL E AGR <blockquote>eu to aq guys para destacar as coisas</blockquote>
    
    </p><hr><br>
    <p> a tag <b>bdo</b>inverte seu texto e vc tem que colocar auto ou ltr ou rtl<br>
    exemplo: e agr... <bdo dir="rtl"> estou aq subi no onibus</bdo>

    </p><hr>
    <p>Fim da aula de Hojeeee!! ate mais guys <br>
    
    </p> <hr>


    
</body>
</html>
```

---

## 🚀 13. `index.html` — Primeira Aula

Página inicial do repositório e primeiro contato com formatação de texto:

- `<del>` e `<strike>` fazem a mesma coisa visualmente (riscar o texto), mas `strike` é uma tag **antiga** (obsoleta), enquanto `del` é a forma moderna e correta de usar.
- `<sup>` sobrescreve o texto (número pequeno acima da linha) e `<sub>` faz o mesmo, só que abaixo da linha — comuns em fórmulas matemáticas/químicas.
- `<mark>` destaca um trecho de texto com um fundo colorido (tipo marca-texto).
- `<strong>` deixa o texto em negrito, mas com significado de **importância**, diferente do `<b>` que é só visual.

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name= "description" content="esse é meu primeiro site"> 
    <meta name= "keywords" content="superrrr"> 
    <meta name="author" content="Carlos Sales">


    <title>hmmmmmmmm!</title>
    
    
</head>
<body>
    <h1>A</h1>
    <p>nesta aula estou aq e descobri que eu tinha que mandar os cod de todas as aulas -_-</p>
    <b><del> estou </del>doiidoooo</b><b></b>
    <p><strike> aiai a strike é antiga coisa que a del é nova</strike></p>
    <p>vendo numeros 2 <sup>12121</sup>
    </p>
    <p>beijos juju</p>
    <p>o sub deixa em baixo 34 <sub>12121</sub> <sup>44</sup></p>
    <p>e bora testar o mark <mark>ehehehehhe</mark></p>
  
  
  
  
    <hr>
    <h2>E BORA BORA</h2>
    <p>trdhsjdkhasjdhasdkjhjsahd <b>jhsadhjsahdjahdjahdha</b>sdhjak</p>
    <p>sasamk  <strong> sahsahs</strong> asasa </p>
</body>
</html>                  
```

---

## 🧠 Conceitos Aplicados no Geral

- Estrutura básica de um documento HTML (`DOCTYPE`, `head`, `meta`, `body`)
- Mídia: `audio`, `video`, `img`, `iframe`
- Formulários e seus tipos de `input`
- Tabelas (`table`, `tr`, `th`, `td`)
- Listas ordenadas e não ordenadas
- Tags semânticas x `div` genérica
- Tags de texto/citação (`abbr`, `cite`, `q`, `blockquote`, `bdo`, `mark`, `sup`, `sub`)
- Links internos (relativos) e externos, com e sem `target`
- Comentários no código

---

## 👨‍💻 Autor

Carlos Sales
