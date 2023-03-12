
## __#1 Conhecendo o Poder do FlexBox__


Para saber mais: [Guia completo sobre flexbox][1]




`display: flex;`

> Aplicando o valor "flex" a propriedade "display" em um container, fará com  que todos os elementos fiquem um ao lado do outro nesse container.



`justify-content: space-between;`

> Aplicando o valor "space-between" a propriedade "justify-content", fará com  que todos os elementos tenha um espaço entre si (horizontal), sendo este espaço, de acordo como atual tamanho do container.


`align-items: center;`

> Esta propriedade específica o alinhamento dos itens dentro container flexbox. Abaixo estão os possivei valores para essa propridade;

![align-items](./readme-images/align-items.png)

`postion: center;`

> Esta propriedade específica a método de posicionamento para um elemento. Abaixo estão os possiveis valores para essa propridade;
- `static`
- `relative`
- `fixed`
- `absolute`
- `sticky`

> OBS: Elements are then positioned using the top, bottom, left, and right properties. However, these properties will not work unless the position property is set first. They also work differently depending on the position value.



### __@media__



A aplicação de regras com `@media` no CSS permite aplicar estilos a um elemento HTML com base nas caracteristicas do dispositivo ou tamanho da tewla em que o contéudo é exibido. Essa funcionalidade é conhecida como design responsivo ou apatável.

A sintaxe básica do `@media` é a seguinte:

```css
@media (condition){
    /* CSS rules */
}
```
A condição pode ser uma das seguintes 

- `width`: define a largura da viewport (areá vísivel do navegador) em pixels.
- `min-width`: define a largura mínima da viewport em pixels.
- `max-width`: define a largura máxima da viewport em pixels.
- `height`: define a altura da viewport em pixels.
- `min-height`: define a altura mínima da viewport em pixels.
- `max-height`: define a algutura máxima da viewport em pixels.
- `orientation`: define a orienta do dispositivo (retrato ou paisagem).
- `aspect-ratio`: define a relação de aspecto da viewport.
- `min-aspect-ratio`: define a relação de aspecto mínima da viewport.
- `max-aspect-ratio`: define a relação de aspecto máxima da viewport.

Por exemplo, para aplicar um estilo diferente a um elemento HTML quando a largura da viewport for menor que 768 pixels, pode-se usar a seguinte regra:

```css
@media (max-width: 768px) {
  /* regras CSS aqui */
}
```

No caso do projeto, o campos de pesquisa deve aparecer só a partir de uma
determinada largura da viewport, que no caso é 834px. Assim o esse campo irá aparecer apenas quando a largura máxima for maior ou igual a 834px.


```css
.cabecalho__pesquisar_item { 
    display: none;  /* Elemento não deve ser mostrado na tela*/
}


@media (min-width: 834px){ /* Verifica se a largura da tela é >= 834*/
    /* Largura da tela é >= 834*/
    .cabecalho__pesquisar_item{
        display: block; /* Sobrepoem a regra anterior e aplica novos valores a propriedade do elemento*/
    }
}
```
### __Reset CSS__

No projeto deste curso é utilizado o arquivo com nome reset.css. É comum encontrar este mesmo arquivo em muitos projetos por aí. Entretanto, você sabe exatamente por que que ele foi criado e qual sua influência no desenvolvimento de uma interface?

Quando você abre um mesmo arquivo HTML em diferentes navegadores, podendo ser Chrome, Firefox ou Edge, por exemplo, este mesmo arquivo pode aparecer de formas diferentes. Isso acontece porque cada um desses navegadores insere automaticamente uma série de valores divergentes de padding, margin e diversas estilizações do CSS.

Como este problema da falta de compatibilidade entre navegadores tem bastante importância para entender como organizar elementos em uma página, trago o artigo “[Reset CSS][2]" O que é, exemplos, como Criar e utilizar”, escrito pela instrutora Laís Cavalcanti, que explica em detalhes como o reset.css resolve o problema.


Vídeos da sessão vídeos:

```html
    <li class="videos__item">
        <iframe width="100%"  height="72%" src="https://www.youtube.com/embed/pA-EgOaF23I" title="YouTube video player" frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen></iframe>
        <div class="descricao-video">
            <img src="./img/videos/Ellipse 11.png" alt="Logo do canal Alura Cursos Online">
            <h3>Qual é o melhor hardware para programação com Mario Souto</h3>
            <p>236 mil visualizações - Há 8 dias</p>
        </div>
    </li>
    <li class="videos__item">
        <iframe width="100%"  height="72%" src="https://www.youtube.com/embed/OrnUhR41MYI"
            title="Voltando ao mercado após a maternidade: Ana Silvério" frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen></iframe>
        <div class="descricao-video">
            <img src="./img/videos/Ellipse 11.png" alt="Logo do canal Alura Cursos Online">
            <h3>Voltando ao mercado após a maternidade: Ana Silvério</h3>
            <p>618 visualizações - Há 1 mês</p>
        </div>
    </li>
    <li class="videos__item">
        <iframe width="100%"  height="72%" src="https://www.youtube.com/embed/YhnNOTde2I0"
            title="Mercado de Trabalho | Desmistificando Mobile - Episódio 5" frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen></iframe>
        <div class="descricao-video">
            <img src="./img/videos/Ellipse 11.png" alt="Logo do canal Alura Cursos Online">
            <h3>Mercado de Trabalho | Desmistificando Mobile...</h3>
            <p>1,1 mil visualizações - Há 1 mês</p>
        </div>
    </li>
    <li class="videos__item">
        <iframe width="100%"  height="72%" src="https://www.youtube.com/embed/y8FeZMv37WU" title="Conhecendo a linguagem Go | Hipsters.Talks"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen></iframe>
        <div class="descricao-video">
            <img src="./img/videos/Ellipse 11.png" alt="Logo do canal Alura Cursos Online">
            <h3>Conhecendo a linguagem Go | Hipsters.Talks</h3>
            <p>3 mil visualizações - Há 3 meses</p>
        </div>
    </li>
    <li class="videos__item">
        <iframe width="100%"  height="72%" src="https://www.youtube.com/embed/fmu1LQvZhms"
            title="Desmistificando mobile- Linguagens e Frameworks - Episódio 2" frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen></iframe>
        <div class="descricao-video">
            <img src="./img/videos/Ellipse 11.png" alt="Logo do canal Alura Cursos Online">
            <h3>Desmistificando mobile- Linguagens e Frameworks</h3>
            <p>1,5 mil visualizações - Há 2 meses</p>
        </div>
    </li>
    <li class="videos__item">
        <iframe width="100%"  height="72%" src="https://www.youtube.com/embed/jpuJ1qrluoU"
            title="Orientação a objetos com Roberta Arcoverde | #HipstersPontoTube" frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen></iframe>
        <div class="descricao-video">
            <img src="./img/videos/Ellipse 11.png" alt="Logo do canal Alura Cursos Online">
            <h3>Orientação a objetos com Roberta Arcoverde | #Hipster...</h3>
            <p>30 mil visualizações - Há 3 meses</p>
        </div>
    </li>
    <li class="videos__item">
        <iframe width="100%"  height="72%" src="https://www.youtube.com/embed/2HhPcadvjqU"
            title="Tire suas dúvidas sobre o bootcamp de Data Science." frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen></iframe>
        <div class="descricao-video">
            <img src="./img/videos/Ellipse 11.png" alt="Logo do canal Alura Cursos Online">
            <h3>Tire suas dúvidas sobre o bootcamp de Data Science...</h3>
            <p>1,6 mil visualizações - Transmitido há 6 meses</p>
        </div>
    </li>
    <li class="videos__item">
        <iframe width="100%"  height="72%" src="https://www.youtube.com/embed/h83e1aAM5xQ" title="
            4:06
            TOCANDO AGORA
            Linguagens e ferramentas usadas em Ciência de Dados | Universo Data Science - Episódio 3"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen></iframe>
        <div class="descricao-video">
            <img src="./img/videos/Ellipse 11.png" alt="Logo do canal Alura Cursos Online">
            <h3>Linguagens e ferramentas usadas em Ciência de Dados...</h3>
            <p>2,5 mil visualizações - Há 9 dias</p>
        </div>
    </li>
    <li class="videos__item">
        <iframe width="100%"  height="72%" src="https://www.youtube.com/embed/CnB3eLTrkn4"
            title="Reencontrando a paixão por programar: Beatriz Ramerindo" frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen></iframe>
        <div class="descricao-video">
            <img src="./img/videos/Ellipse 11.png" alt="Logo do canal Alura Cursos Online">
            <h3>Reencontrando a paixão por programar: Beatriz Ramerindo</h3>
            <p>1,2 mil visualizações - Há 1 mês</p>
        </div>
    </li>
    <li class="videos__item">
        <iframe width="100%"  height="72%" src="https://www.youtube.com/embed/vf9P_PycgRw"
            title="Híbridos: Flutter e React Native | Desmistificando Mobile - Episódio 4" frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen></iframe>
        <div class="descricao-video">
            <img src="./img/videos/Ellipse 11.png" alt="Logo do canal Alura Cursos Online">
            <h3>Híbridos: Flutter e React Native | Desmistificando...</h3>
            <p>1,6 mil visualizações - Há 1 mês</p>
        </div>
    </li>
    <li class="videos__item">
        <iframe width="100%"  height="72%" src="https://www.youtube.com/embed/Nts3P35mHzE"
            title="Data Science na prática- com Jéssika Ribeiro do Grupo Boticário | Universo Data Science - Episódio 4"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen></iframe>
        <div class="descricao-video">
            <img src="./img/videos/Ellipse 11.png" alt="Logo do canal Alura Cursos Online">
            <h3>Data Science na prática- com Jéssika Ribeiro do Grupo...</h3>
            <p>3,2 mil visualizações - Há 7 dias</p>
        </div>
    </li>
    <li class="videos__item">
        <iframe width="100%"  height="72%" src="https://www.youtube.com/embed/HBVCsBtsmzA" title="baNaNa | Memes do JavaScript - Episódio 2"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen></iframe>
        <div class="descricao-video">
            <img src="./img/videos/Ellipse 11.png" alt="Logo do canal Alura Cursos Online">
            <h3>baNaNa | Memes do JavaScript #2</h3>
            <p>1,2 mil visualizações - Há 5 dias</p>
        </div>
    </li>
    <li class="videos__item">
        <iframe width="100%"  height="72%" src="https://www.youtube.com/embed/SyEdlBSw11k"
            title="Aniversário da Casa do Código | 10 anos da sua editora de Tecnologia" frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen></iframe>
        <div class="descricao-video">
            <img src="./img/videos/Ellipse 11.png" alt="Logo do canal Alura Cursos Online">
            <h3>Aniversário da Casa do Código | 10 anos da sua editora de...</h3>
            <p>1,3 mil visualizações - Há 1 mês</p>
        </div>
    </li>
    <li class="videos__item">
        <iframe width="100%"  height="72%" src="https://www.youtube.com/embed/FKYBCl_I9zU"
            title="Jetpack Compose: Estados e animações | #AluraMais" frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen></iframe>
        <div class="descricao-video">
            <img src="./img/videos/Ellipse 11.png" alt="Logo do canal Alura Cursos Online">
            <h3>Jetpack Compose: Estados e animações</h3>
            <p>1,6 mil visualizações - Há 8 dias</p>
        </div>
    </li>
    <li class="videos__item">
        <iframe width="100%"  height="72%" src="https://www.youtube.com/embed/68EGCA67g_A"
            title="[Casa do Código] Lançamento do Livro Certificação Linux" frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen></iframe>
        <div class="descricao-video">
            <img src="./img/videos/Ellipse 11.png" alt="Logo do canal Alura Cursos Online">
            <h3>[Casa do Código] Lançamento do Livro Certificação Linux</h3>
            <p>1,2 mil visualizações - Há 1 mês</p>
        </div>
    </li>
    <li class="videos__item">
        <iframe width="100%"  height="72%" src="https://www.youtube.com/embed/VHxoyduIt18"
            title="Por que o JavaScript é assim? | Memes do JavaScript - Episódio 1" frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen></iframe>
        <div class="descricao-video">
            <img src="./img/videos/Ellipse 11.png" alt="Logo do canal Alura Cursos Online">
            <h3>Por que o JavaScript é assim? | Memes JavaScript #01</h3>
            <p>2,3 mil visualizações - Há 2 dias</p>
        </div>
    </li>
```


Notes:


# Tags

```html
<aside></aside>
```
O elemento HTML <aside> representa uma seção de uma página que consiste de conteúdo que é tangencialmente relacionado ao conteúdo do seu entorno, que poderia ser considerado separado do conteúdo. Essas seções são, muitas vezes, representadas como barras laterais. Elas muitas vezes contem explicações laterais, como a definição de um glossário; conteúdo vagamente relacionado, como avisos; a biografia do autor; ou, em aplicações web, informações de perfil ou links de blogs relacionados.



[1]:https://css-tricks.com/snippets/css/a-guide-to-flexbox/ "Guia completo sobre flexbox"
[2]:https://www.alura.com.br/artigos/o-que-e-reset-css "Reset CSS"

