
## __#01 Conhecendo o Poder do FlexBox__


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




## __02# Rodapé responsivo__

[Flex Box Guia Completo][3]


No caso do radapé precisamos que o elementos fiquem em coluna, mas se espalhando apenas dentro do container do rodapé. Para minipularmos podemos usar o display flex, e mudar a direção, em vez de line, usamos colunm;


> "Define se os itens devem quebrar ou não a linha. Por padrão eles não quebram linha, isso faz com que os flex itens sejam compactados além do limite do conteúdo. Essa é geralmente uma propriedade que é quase sempre definida como flex-wrap: wrap; Pois assim quando um dos flex itens atinge o limite do conteúdo, o último item passa para a coluna debaixo e assim por diante."

```css
.rodape__container {
    display: flex;  /*Aplica o display flex*/
    flex-direction: column;  /*Muda a orientação para coluna*/
}

```
Agora precisamos quebrar essas colunas, igualmente, de acordo como tamanho da viewport. Para isso usamos o
`flex-wrap: wrap`



```css
.rodape__container {
    display: flex;  /*Aplica o display flex*/
    flex-direction: column;  /*Muda a orientação para coluna*/
    flex-wrap:  wrap;
}
```

O Flexbox pode ser utilizado alterando o valor do display de um container para flex, ou inline-flex. Vamos descobrir quais são suas diferenças e similaridades.

O que eles têm em comum?
Ambos valores de display permitem alinhar itens com propriedades do Flexbox.

O que eles não têm em comum?
O display: flex faz com que o container se expanda ocupando toda a largura do leiaute(repare na cor preta de background ocupando toda a largura disponível), assim, os outros containers com o mesmo valor de display ficam um embaixo do outro, na direção vertical.

Já o display: inline-flex, utiliza as mesmas características de exibição do display: inline. Exibindo os elementos em nível de linha, na horizontal, sem ocupar toda a largura do leiaute.

Confira abaixo, exemplo de código no editor de código online Codepen, apenas alterando os displays de seus containers para ver na prática suas diferenças:


![inline-flex](./readme-images/inlineflex.png)




### __gap__

> A priedade `gap` é utilizada para colocar espaçamento entre os items dentro de um container, de forma que ela nãoa aplica o mesmo espaçamento nas extremidades dos mesmos.


```css
.superior__secao__container {
    display: flex; /* Aplicar o flexbox no container*/
    align-items: center; /* Centralizar os elementos no meio do container*/
    white-space: nowrap; /* Aplicar quebra de linha apenas para os textos (espaços em branco)*/
    overflow: scroll; /* Adicionar barra de rolagem */
    gap: 15px; /*Aplicar espaçamento entre os items*/
    
```
> The gap property defines the size of the gap between the rows and between the columns in flexbox, grid or multi-column layout. It is a shorthand for the following properties:
- row-gap
- column-gap

### __Resumo__

- Aplicamos propriedades flex para:
- Alterar o eixo principal de elementos;
- Quebra de itens em linhas ou colunas;
- Aplicar espaçamento entre itens;
- Definimos as diferenças entre display flex e inline-flex.
 DISCUTIR NO FORUM


# Tags

```html
<aside></aside>
```
O elemento HTML <aside> representa uma seção de uma página que consiste de conteúdo que é tangencialmente relacionado ao conteúdo do seu entorno, que poderia ser considerado separado do conteúdo. Essas seções são, muitas vezes, representadas como barras laterais. Elas muitas vezes contem explicações laterais, como a definição de um glossário; conteúdo vagamente relacionado, como avisos; a biografia do autor; ou, em aplicações web, informações de perfil ou links de blogs relacionados.



[1]:https://css-tricks.com/snippets/css/a-guide-to-flexbox/ "Guia completo sobre flexbox"
[2]:https://www.alura.com.br/artigos/o-que-e-reset-css "Reset CSS"
[3]:https://origamid.com/projetos/flexbox-guia-completo/ "Flexbox Guia Completo"
